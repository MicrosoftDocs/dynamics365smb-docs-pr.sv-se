---
title: Designinformation – ändra värderingsprinciper för artiklar
description: Så här tilldelar du en annan värderingsprincip till en artikel, även om du redan har använt artikeln i transaktioner.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing methods, costing, item cost
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 344aa53f965f832d8e7fb2abd3431a1853105c8c
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917532"
---
# <a name="design-details-change-the-costing-method-for-items"></a>Designinformation: ändra värderingsprinciper för artiklar

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du inte ändra en värderingsprincip för en artikel när du har inkluderat artikeln i en transaktion. När du till exempel har köpt eller sålt artikeln. Om en felaktig värderingsprincip har tilldelats till artikeln eller artiklarna kanske du inte upptäcker problemet förrän du gör din ekonomiska rapportering.

I det här avsnittet beskrivs hur du löser problemet. Den rekommenderade metoden är att ersätta artikeln med den felaktiga värderingsprincipen med en ny artikel och använda en monteringsorder för att överföra lagret från den gamla artikeln till det nya.

> [!NOTE]
> Med hjälp av monteringsorder kan kostnaderna fortfarande flöda även om det finns utestående inköpsfakturor eller leveranskostnader att bokföra. Dessutom kan du ångra konverteringen och få tillbaka antal ursprungliga artiklar om det behövs.

> [!TIP]
> Om du vill bekanta dig med den här metoden rekommenderar vi att du startar konverteringen med ett enstaka objekt eller en liten uppsättning objekt.

## <a name="about-costing-methods"></a>Om värderingsprinciper

Värderingsprinciper kontrollerar kostnadsberäkningar när varor köps, tas emot i lager och säljs. Värderingsprinciper påverkar tidpunkten för de belopp som registrerats för KSV och som påverkar bruttovinsten. Det är det här flödet som beräknar KSV. Kostnaden för sålda varor (KSV) och intäkter används för att bestämma bruttovinst enligt följande:

*bruttovinst* = *intäkt - COGS*

När du lägger upp lagerartiklar måste du tilldela en värderingsprincip. Metoden kan variera från affärsverksamhet till företag och från artikel till artikel så att det är viktigt att välja rätt namn. [!INCLUDE[d365fin](includes/d365fin_md.md)] stöder följande värderingsprinciper:

* Genomsnitt
* FIFO
* LIFO (Sist in, först ut)
* Standard
* Specifik

Mer information finns i [Designdetaljer: Värderingsprinciper](design-details-costing-methods.md).

## <a name="using-assembly-orders-to-change-costing-method-assignments"></a>Använda monteringsorder för att ändra tilldelningar av värderingsprincipen

I det här avsnittet beskrivs följande steg för att ändra värderingsprincipen som tilldelats en artikel:

1. Definiera standardvärderingsprincip.
2. Identifiera de artiklar som du vill ändra värderingsprincipen för och numrera om dem.
3. Skapa nya objekt med det gamla numreringsschema och kopiera huvuddata i en batch.
4. Manuellt kopiera relaterade huvuddata från det befintliga objektet till det nya.
5. Bestämma lagerkvantiteten som ska konverteras från den ursprungliga artikeln till den nya artikeln.
6. Överföra lagret till den nya artikeln.
7. Hantera lagerkvantiteter som har allokerats till behov.
8. Blockera det ursprungliga artikel från att användas.  

### <a name="define-a-default-costing-method"></a>Definiera standardvärderingsprincip

För att undvika framtida misstag kan du ange en värderingsprincip som är standard för nya artiklar. När någon skapar en ny artikel [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer den att föreslå standard värderingsprincipen. Du anger standardmetoden i fältet **Standardvärderingsprincip** på sidan **Lagerinställning**. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>Identifiera de artiklar som du vill ändra värderingsprincipen för och numrera om dem

Du kanske vill ge de nya objekten samma nummer som de som de ersätter. Det gör du genom att ändra numren på de befintliga objekten. Om det befintliga artikelnumret till exempel är "P1000" kan du ändra det till "X-P1000". Det här är en manuell ändring som du måste göra för varje artikel.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Skapa nya objekt med det gamla numreringsschema och kopiera huvuddata i en batch

Skapa nya objekt med aktuellt nummer schema. Med undantag av fältet **värderingsprincip** bör de nya artiklarna innehålla samma huvuddata som de befintliga artiklarna. Om du vill överföra huvuddata för artikeln och relaterade data från andra funktioner, använder du åtgärden **Kopiera artikel** på sidan **Artikelkort**. Mer information finns i [kopiera befintliga objekt om du vill skapa nya objekt](inventory-how-copy-items.md).

När du har skapat de nya artiklarna och överfört huvuddata tilldelar du rätt värderingsprincip.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Manuellt kopiera relaterade huvuddata från det ursprungliga objektet till det nya.

Om du vill göra de nya objekten fullt användbara måste du manuellt kopiera vissa huvuddata från andra områden enligt beskrivningen i följande tabell.

|Område  |Vad som ska kopieras  |Hur du kopierar det  |
|---------|---------|---------|
|Lager     |Lagerhållningsenheter (SKU)         |Kontrollera om en lagerställeenhet har angetts för den ursprungliga artikeln. Om du har angett planeringsparametrar för varje lagerställeenhetskort måste du manuellt skapa lagerställeenhet för den nya artikeln. Om parametrarna inte anges kan du använda batchjobb **Skapa lagerställeenhet** från sidan **Artikelkort** för att skapa data.        |
|     |Artikelersättningar         |Kontrollera om eventuella artikelersättningar har definierats för den ursprungliga artikeln. Om det finns överför du dessa data till det nya objektet. Om du vill visa ersättningsartiklar använder du åtgärden **ersättning** på sidan **artikelkort**.         |
|     |Analysrapporter         |Granska artikel analys-, försäljningsanalys- och inköpsanalysrapporter. För de artiklar som refererar till de ursprungliga artiklarna kan du antingen skapa en ny analysrapport med en referens till den nya artikeln (där den ursprungliga analysrapporten ska användas som historik) eller justera rapporterna så att de refererar till den nya artikeln.         |
|     |Standardjournaler         |Kontrollera om standardjournalerna refererar till den ursprungliga artikeln och överför dessa data till den nya artikeln vid behov. Informationen finns i standardjournalerna, som är tillgängliga i artikeljournalen.          |
|FÖRS     |Procentandelar, förskottsbetalning för försäljning         | Kontrollera om några procentandelar, förskottsbetalning för försäljning har definierats för den ursprungliga artikeln och överför dessa data till den nya artikeln. Om du vill visa förskottsbetalningsprocent väljer du **Artikelkort** väljer du **Försäljning** och **Procentandelar, förskottsbetalning**.        |
|Inköp     |Procentandelar, förskottsbetalning för inköp         |Kontrollera om några procentandelar, förskottsbetalning för inköp har definierats för den ursprungliga artikeln och överför dessa data till den nya artikeln. Om du vill visa förskottsbetalningsprocent väljer du **Artikelkort** väljer du **Inköps** och **Procentandelar, förskottsbetalning**.                 |
|Dist.lager     |Lagerplatsinnehåll         |Granska det lagerplatsinnehåll som har definierats för den ursprungliga artikeln. Om kolumner så som min. Antal max. Antal, standard och dedikerade har registrerats individuellt måste du skapa lagerplatsinnehåll manuellt för den nya artikeln. Om så inte är fallet krävs ingen åtgärd. [!INCLUDE[d365fin](includes/d365fin_md.md)] underhåller posterna när du registrerar distributionslagerdokument och journaler.|
|Projekt     |Projektpriser         |Kontrollera om projektpriser har definierats för den ursprungliga artikeln och överför dessa data till den nya artikeln. Informationen finns på sidan **Projektkort** i delen **Projektinformation – Projektdetaljer - antal priser** i **rutan Faktabox**.         |
|Service     |Serviceresurskvalifikation         |Kontrollera om serviceresurskvalifikation har definierats för den ursprungliga artikeln och överför dessa data till den nya artikeln. Om du vill visa resurs kvalifikationer använder du åtgärden **Resurskvalifikation** på sidan **Artikelkort**.          |
|     |Serviceartikelkomponenter         |Kontrollera om komponenter har definierats för den ursprungliga serviceartikeln och överför dessa data till den nya artikeln. Om du vill visa serviceartikel komponenter på **Artikelkort** använder åtgärden **Serviceartikel** för att öppna listan över relaterade service artiklar och sedan välja **Komponent**.          |
|Produktion     |Artikelstrukturer         |Kontrollera om det finns några produktionsstrukturer som innehåller den ursprungliga artikeln och ersätt det med den nya artikeln. Om du vill ersätta det ursprungliga artikel **Produktionsstruktur** väljer åtgärden **Byt ut artikel i prod.struktur**.         |
|Montering     |Monteringsstrukturer         |Kontrollera om några monteringsdelar innehåller originalobjektet och ersätt det manuellt med det nya artikeln.         |

> [!IMPORTANT]
> Om den nya värderingsprincipen är standard ska du ange ett värde i fältet **Standardkostnad** på **Artikelkort**. Du kan använda sidan **Standardkostnadsformulär** för att ange kostnadsandelarna på samma sätt. För mer information, se [Uppdateras standardkostnader](finance-how-to-update-standard-costs.md).

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>Bestämma lagerkvantiteten som ska konverteras från den ursprungliga artikeln till den nya artikeln

> [!NOTE]
> I det här steget beaktas inte antal som ingår i order som inte har levererats. Mer information finns i [Hantera lagerkvantiteter som har allokerats till behov](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Använd en inventeringsjournal för att producera en lista över antalet i lagret. Beroende på inställningen för distributionslagerplatsen använder du något av följande:

* Inventeringsjournaler
* Dist.lager. Inventeringsjournaler

I båda journalerna kan lagerkvantiteten för artikeln beräknas, inklusive lagerställe, variant, lagerplats och lagringsplats. Mer information finns i [Inventera, justera och gruppera om lager med hjälp av journaler](inventory-how-count-adjust-reclassify.md).

### <a name="transfer-the-inventory-to-the-new-item"></a>Överföra lagret till den nya artikeln

Skapa och bokför monteringsorder för att överföra kostnad och lagerkvantitet från den ursprungliga artikeln till den nya artikeln. Monteringsorder kan omvandla en artikel till en annan och bevara kostnaderna. På så sätt säkerställs att nettosummorna för lagerkontot och KSV inte påverkas (utom när den nya värderingsprincipen är standard, då kostnader kan fördelas på varians). Mer information finns i [Monteringshantering](assembly-assemble-items.md).

När du skapar monteringsorder använder du informationen från fältet inventeringsjournaler eller Dist. lager. Inventeringsjournal. I följande tabeller beskrivs informationen i rapporterna som ska anges i rubriken och på monteringsorderraderna.

#### <a name="header"></a>Rubrik

|Fält  |Värde att skriva  |
|---------|---------|
|Artikelnr     |Numret för den nya artikeln         |
|Antal     |Kvantiteten i inventeringsjournalen.<br> **OBS!** de kvantiteter som beräknas av inventeringsjournalerna innehåller inte de antal som finns på order som ännu inte har levererats.          |
|Variantkod     |Samma som i inventeringsjournalen.          |
|Lagerställekod     |Samma som i inventeringsjournalen.         |
|Enhetskod     |Samma som i inventeringsjournalen.         |
|Lagerplatskod     |Samma som i inventeringsjournalen.         |

#### <a name="lines"></a>Rader

|Fält  |Värde att skriva  |
|---------|---------|
|Typ     |Artikel         |
|Nr     |Numret för den ursprungliga artikeln         |
|Antal per     |1         |
|Variantkod     |Samma som i inventeringsjournalen.         |
|Lagerställekod     |Samma som i inventeringsjournalen.         |
|Enhetskod     |Samma som i inventeringsjournalen.         |

> [!NOTE]
> En monteringsorder kan endast hantera en lagerställeenhet för en artikel i taget. Du måste skapa en monteringsorder för varje kombination av lagerställeenheten som har ett antal i lagret.

> [!NOTE]
> För ett lagerställe måste du kanske skapa plockningar innan du kan bokföra monteringsorder. Kontrollera detta genom att granska inställningarna för plockning på sidan **lagerställekort**. Mer information finns i: [Så här skapar du artiklar och platser för dirigerad artikelinförsel och plockning](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Hantera lagerkvantiteter som har allokerats till behov

Vi rekommenderar att lagret för den ursprungliga artikeln flyttas tillbaka till noll när du överfört lagerkvantiteter. Det kan dock finnas utestående order, kalkylblad och journaler (se tabellen nedan) som fortfarande kräver en kvantitet av den ursprungliga artikeln. Antalet kan också spärras genom en reservation eller artikelspårning.

**Exempel** Det finns 1 000 stycken. i lager och 20 stycken. är reserverade för en försäljningsorder som ännu inte har levererats. I så fall kanske du bestämmer dig för att behålla de 20 stycken. i den gamla artikeln så att du kan uppfylla utestående order.

> [!NOTE]
> Det finns funktionsområden som kan påverka antalet som visas i tabellen nedan, så det kan vara svårt att hitta rätt belopp. För att kunna använda ovanstående exempel kan du välja att behålla 100 stycken. och överför de återstående 900 stycken. istället. Ett annat sätt att göra det är att hantera dokument och journaler så att endast de som hanteras blir kvar. Ännu en annan alternativ är att överföra hela kvantiteten till den nya artikeln och sedan överföra en del av den tillbaka till den ursprungliga artikeln med monteringsorder.

I följande tabell visas funktionsområden där det kan finnas utestående antal.

|Område  |Var du ska söka efter utestående kvantiteter  |
|---------|---------|
|FÖRS     |Försäljningsdokument, inklusive order, returorder, fakturor, offerter, avropsorder och kreditnotor         |
|Lager     |Artikeljournaler, reservationer, artikelspårning och standardkostnadsformulär         |
|Inköp     |Inköpsdokument, inklusive order, returorder, fakturor, offerter, avropsorder och kreditnotor         |
|Planering     |Inköpsförslag, planeringsförslag och orderplanering         |
|Dist.lager     |Överföringsorder, utleveranser, distributionslagerjournaler och lagerplockningar, artikelinförsel och transporter, interna plockningar och införsel och lagerplatsuppläggningsförslag         |
|Montering     |Monteringsdokument, inklusive order, returorder och avropsorder         |
|Projekt     |Projektplaneringsrader och projektjournalrader         |
|Service     |Servicedokument och servicekontrakt         |
|Produktion     |Produktionsorder (planerad, fast planerad och släppt)         |

### <a name="block-the-original-item-from-further-use"></a>Blockera det ursprungliga artikel från att användas

När lagret för den ursprungliga artikeln är noll, kan du spärra artikeln för att förhindra att den används i nya transaktioner. Om du vill spärra artikeln, på sidan **Artikelkort** aktivera växlingen **Blockrad**. Mer information finns i [Spärra artiklar från försäljning eller inköp](inventory-how-block-items.md).

## <a name="summary"></a>Översikt

Att ändra värderingsprincipen för artiklar som har använts i transaktioner är en bearbetning och inte en standard åtgärd i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan använda de steg som beskrivs i det här avsnittet som en mall för proceduren.

Det kan ta lång tid att utföra flera manuella åtgärder. Men att ta sig tid att slutföra det kommer att minimera inverkan av misstag i din redovisning.

Vi rekommenderar följande:

1. Bedöm hur genomförbart det är att utföra en eller flera, representativa artiklar genom hela förfarandet.
2. Du bör kontakta en erfaren partner som kan hjälpa dig med arbetet.

## <a name="see-also"></a>Se även

[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  
[Översikt](design-details-inventory-costing.md)
