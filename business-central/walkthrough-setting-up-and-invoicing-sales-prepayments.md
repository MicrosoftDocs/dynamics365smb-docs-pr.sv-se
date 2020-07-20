---
title: 'Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning | Microsoft Docs'
description: Förskottsbetalningar är betalningar som faktureras och bokförs för en försäljnings- eller inköpsorder före slutfaktureringen. Du kan kräva en deposition innan du tillverkar artiklar mot order eller så kan du kräva betalning innan du levererar artiklar till en kund. Använd funktionen i för förskottsbetalning i Business Central för att fakturera och inkassera depositioner från kunder eller betala depositioner till leverantörer. På så sätt kan du se till att alla betalningar bokförs mot en faktura.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2020
ms.author: sgroespe
ms.openlocfilehash: 29ab09f12a31339810bd01af72ee488bfa879dc4
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529369"
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Genomgång: Lägga upp och fakturera förskottsbetaln., försäljning

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]  

Förskottsbetalningar är betalningar som faktureras och bokförs för en försäljnings- eller inköpsorder före slutfaktureringen. Du kan kräva en deposition innan du tillverkar artiklar mot order eller så kan du kräva betalning innan du levererar artiklar till en kund. Använd funktionen i för förskottsbetalning i [!INCLUDE[d365fin](includes/d365fin_md.md)] för att fakturera och inkassera depositioner från kunder eller betala depositioner till leverantörer. På så sätt kan du se till att alla betalningar bokförs mot en faktura.  

 Förskottsbetalningskrav kan definieras för en kund eller leverantör för alla artiklar eller valda artiklar. När du har gjort de nödvändiga inställningarna kan du generera förskottsfakturor från försäljnings- och inköpsorder för det beräknade förskottsbeloppet. Du ändra standardbeloppen på fakturan om det behövs. Du kan till exempel skicka ytterligare förskottsfakturor om ytterligare artiklar läggs till i ordern.  

## <a name="about-this-walkthrough"></a>Om den här genomgången  
 Den här genomgången kommer att innehålla följande scenarion:  

-   Lägga upp förskottsbetalningar  
-   Skapa en order som kräver förskottsbetalning  
-   Skapa en förskottsfaktura  
-   Korrigera förskottsbetalningskrav för en order  
-   Använda förskottsbetalningar för en order  
-   Fakturera slutbeloppet på en order med en förskottsbetalning  

### <a name="roles"></a>Roller  
 Den här genomgången innehåller aktiviteter för följande roller:  

-   Redovisningschef (Phyllis)  
-   Orderhandläggare (Susan)  
-   Kundreskontraadministratör (Arnie)  

## <a name="story"></a>Situation  
 Phyllis är redovisningschef. Hon fattar beslut om vilka kunder som måste betala en deposition innan artiklar tillverkas eller levereras. Phyllis lägger upp [!INCLUDE[d365fin](includes/d365fin_md.md)] för att beräkna förskottsbetalningar automatiskt.  

 Susan är försäljningsorderhandläggare. När en kund ringer in en order registrerar hon ordern i systemet medan kunden är i telefon. På så sätt kan hon verifiera priser och betalningsvillkor med kunden omedelbart, och hon kan göra justeringar i ordern medan hon förhandlar med kunden.  

 Arnie arbetar på kundreskontraavdelningen där han bokför fakturor och betalningar.  

 I det här scenariot lägger Phyllis upp förskottsbetalningskrav för kunden Service AB, baserat på deras kredithistorik, och ger Susan instruktioner för hur hon ska hantera deras order.  

 När kunden ringer förhandlar Susan med kunden tills de når ett avtal. Hon kan sedan välja att beräkna förskottsbetalningen på flera olika sätt.  

 När Susan har skickat förskottsfakturan beställer kunden ytterligare en artikel. Susan uppdaterar order och skapar en förskottsfaktura.  

 Arnie registrerar kundens betalning och bokför den mot fakturorna och skickar sedan den sista fakturan.  

## <a name="setting-up-prepayments"></a>Lägga upp förskottsbetalningar  
 Phyllis konfigurerar systemet för hantering av förskottsbetalningar från kunder.  

-   Phyllis väljer att ha samma nummerserie för förskottsbetalningar som för fakturering av försäljning.  
-   Phyllis konfigurerar programmet så att det kontrollerar om förskottsbetalningar krävs innan slutgiltig fakturering görs av en order.  
-   Phyllis lägger upp standardvärden för hur stor del av fakturan som ska förskottsbetalas för särskilda artiklar och kunder.  

I följande procedurer beskrivs hur Phyllis uppgifter ska utföras:  

#### <a name="to-set-up-number-series-for-prepayments"></a>Så här lägger du upp nummerserier för förskottsbetalningar  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsinställningar** och välj sedan relaterad länk.  
2.  På sidan **Försäljningsinställningar** expanderar du snabbfliken **Numrering**.  
3.  Kontrollera att nummerserien för bokförda förskottsfakturor i fältet **Försk.fakt.nr.serie (bokförd)** är samma som för bokförda försäljningsfakturor (**Fakturanr-serie (bokförd)**) och att nummerserien för bokförda förskottskreditnotor (**Försk.kredit.nr.serie (bokförd)**) är samma som för bokförda kreditnotor (**Kreditnotenr-serie (bokförd)**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Så här spärrar du utleveranser för obetalda förskottsbetalningar  
1.  På sidan **Försäljningsinställningar**, på snabbfliken **Allmänt**, markerar du kryssrutan **Kontrollera förskottsbet. vid bokföring**.

    Nu kan du inte utleverera eller fakturera en order med ett obetalt förskottsbetalningsbelopp.  

Phyllis kräver att kunden 20000 ska faktureras 30 % i förskott för alla order. Därför anger hon ett procentuellt standardvärde för förskottsbetalning.  

Phyllis kräver att alla kunder ska faktureras 20 % i förskott för artikel 1100. Kunden 20000 har dålig betalningshistorik. Därför kan kräver hon 40 % i förskottsbetalning från kund 20000 för artikel 1100. I följande exempel visas hur du lägger upp procentuella standardvärden för förskottsbetalningar.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Så här tilldelar du kunder och artiklar procentuella standardvärden för förskottsbetalningar  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kunder** och välj sedan relaterad länk.  
2.  Öppna kortet för kund 20000 (Selangorian).
3.  I fältet **Förskottsbetalning %** anger du **30**.  
4.  Välj **OK** för att stänga kundkortet.  
5.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artiklar** och välj sedan tillhörande länk.  
6.  Öppna kort för kund 1100.
7.  Välj åtgärden **procentandelar, förskottsbetalning**.  
8.  Fyll i de två raderna på sidan **Procentandelar, förskottsbetalning för försäljning** enligt nedan:  

    |**Förs.typ**|**Förs.kod**|**Artikelnr**|**Förskottsbetalning %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Kund**|**20000**|**1100**|**40**|  
    |**Alla kunder**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  Beroende på ditt land/din region måste du också ange en skattegruppskod på snabbfliken **Fakturering** för artiklarna 1000 och 1100.  

9. Stäng alla sidor.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Så här kan du skriva in ett konto för utgående förskottsbetalningar i bokföringsinställningarna  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokföringsinställningar** och välj sedan relaterad länk.  
2.  Markera raden där fältet **Gen. rörelsebokföringsmall** anges till **EXPORTERA** och fältet **Produktbokföringsmall** anges till **DETALJ** och välj sedan åtgärden **Redigera**.  
3.  På sidan **Bokföringsinställningskort** i fältet **Förskottsbet.konto, försäljning** anger du det relevanta kontot.  
4.  Välj **OK**.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Skapa en order som kräver förskottsbetalning  
 I följande scenario skapar Susan, orderhandläggaren, en order medan hon pratar med en kund. Artiklarna som kunden beställer kräver förskottsbetalning och kunden har betalat för sent förut. Därför Susan har blivit instruerad att kräva ett fast belopp på 2 000 som förskottsbetalning för ordern.  

Kunden ber att kunna få betala 35 %, vilket Susan går med på. Därför ändrar hon ordern.  

Susan skapar en förskottsfaktura och skickar den till kunden.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Så här skapar du en försäljningsorder med förskottsbetalning  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsorder** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  I fältet **Förs.kundnr.** välj **20000**.  
5.  Acceptera varningen för förfallet saldo som visas.  
6.  Fyll i två försäljningsrader med följande information.  

    |**Typ**|**Nr**|**Antal**|  
    |--------------|-------------|------------------|  
    |**Artikel**|**1000**|**1**|  
    |**Artikel**|**1100**|**1**|

    Förskottsfälten på försäljningsraden är dolda som standard så du måste visa dem.  

7. Kontrollera att fältet **Förskottsbetalning %** på raden med artikel **1000** innehåller värdet **30**. Standardvärdet hämtades från försäljningshuvudet som kopierades från kundkortet.  

    Fältet **Förskottsbetalning %** på raden med artikel **1100** innehåller värdet **40**. Det är den procentsats som du angav på sidan **Procentandelar, förskottsbetalning för försäljning** för artikel **1100** och kund **20000**.  

    Mer information finns i [Ange Förskottsbetalningar](finance-set-up-prepayments.md).  
8. Välj åtgärden **Statistik**.  
9. På snabbfliken **Förskottsbetalning** innehåller fältet **Radbelopp, förskottsbetalning exkl. moms** värdet **1 560**. Om du skapar en förskottsbetalning för ordern nu, är det detta belopp som visas på fakturan.  

    I det här scenariot har Susan blivit instruerad att föreslå en fullständig förskottsbetalning på 2 000 för ordern.  

    > [!IMPORTANT]  
    >  Beroende på ditt land/din region kan följande steg eventuellt inte utföras.  
10. Ändra värdet i fältet **Radbelopp, förskottsbetalning exkl. moms** till **2 000** och stäng sedan sidan.  
11. Kontrollera fältet **Förskottsbetalning %** på försäljningsraderna så ser du att det har ändrats till **40,81625**.  

    Omräkningen inkluderar alla rader med en procentuell förskottsbetalning som är större än 0.  

    Nu frågar kunden om den procentuella förskottsbetalningen kan ändras till 35 %. Susans chef godkänner ändringen.  

12. På sidan **Förs.order** i fältet **Förskottsbetalning %** anger du **35**.  
13. Välj **ja** för varningen som visas. En debitering på 35 % används som procentuell förskottsbetalning för hela ordern.  
14. Bekräfta att raderna har uppdaterats.  

## <a name="creating-a-prepayment-invoice"></a>Skapa en förskottsfaktura  
När Susan har angett korrekta värden för förskottsbetalning av ordern skapar hon förskottsfakturan och skickar den till kunden.  

#### <a name="to-create-a-prepayment-invoice"></a>Så här skapar du en förskottsfaktura  

1.  På sidan **Försäljningsorder** väljer du åtgärden **Bokför förskottsfaktura**.  

> [!NOTE]  
>  Susan skulle välja **Bokför och skriv ut faktura på förskottsbet.** och skicka fakturan per post till kunden.  

## <a name="creating-an-additional-prepayment-invoice"></a>Skapa ytterligare en förskottsfaktura  
Följande dag ringer kunden upp Susan och ändrar ordern. Kunden vill ha två stycken av artikel 1100. Susan öppnar ordern igen och uppdaterar den och skapar sedan ytterligare en förskottsfaktura för ordern och skickar den till kunden.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Så här skapar du ytterligare en förskottsfaktura  

1.  På sidan **Försäljningsorder** väljer du åtgärden **Öppna igen**.  
2.  På raden för artikel **1100** anger du **2** i fältet **Kvantitet**.  

    Bläddra för att visa förskottsfälten. Fältet **Förskottsbetalning exkl. Moms** innehåller nu **630** och **Fakturabelopp, förskottsbetalning exkl. moms** innehåller **315**. Detta visar att det finns ytterligare förskottsbelopp som ännu inte har fakturerats ännu.  
3.  Om du vill bokföra en faktura för det ytterligare förskottsbeloppet väljer du åtgärden **Bokför förskottsfaktura**.  

## <a name="applying-the-prepayments"></a>Använda förskottsbetalningar  
Kunden betalar förskottsfakturan och Arnie, som arbetar på bokföringsavdelningen, registrerar betalningen och bokför den mot förskottsfakturan.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Så här bokför du betalningar mot förskottsfakturor  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inbetalningsjournaler** och välj sedan tillhörande länk.  
2.  Fyll i journalraden med följande information.  

    |Fältnamn|Skriv in|  
    |----------------|-----------|  
    |**Dokumenttyp**|**Betalning**|  
    |**Kontotyp**|**Kund**|  
    |**Kontonr**|**20000**|  
3. Välj åtgärden **Koppla transaktioner**.  
4.  På sidan **Koppla kundtransaktioner** väljer du den första förskottsfakturan och väljer åtgärden **Ange Koppla till ID**.  
5.  Upprepa det föregående steget för den andra förskottsbetalningen.  
6.  Välj knappen **OK**.  

    Beloppsfältet har nu fyllts i med summan av de två förskottsfakturorna.  

7.  Bokför journalen.  

## <a name="invoicing-the-remaining-amount"></a>Fakturera återstående belopp  
Nu har Arnie blivit informerad om att artiklarna på ordern har levererats och att ordern är klar för fakturering. Arnie skapar fakturan för ordern.  

#### <a name="to-invoice-the-remaining-amount"></a>Så här fakturerar du återstående belopp  
1. Öppna försäljningsordern.  
2. Välj åtgärden **Leverera och fakturera** och sedan knappen **OK**.  

> [!NOTE]  
>  Normalt har leveransavdelningen redan bokfört utleveransen.  

Arnie kan visa historiken för att kontrollera att försäljningfakturan har skapats som avsett.  

1. Välj ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda försäljningsfakturor** och välj sedan relaterad länk.  

## <a name="next-steps"></a>Gå vidare  
Den här genomgången har gått igenom hur du konfigurerar [!INCLUDE[d365fin](includes/d365fin_md.md)] att hantera förskottsbetalningar. Du har lärt dig hur man lägger upp standardvärden för procentuell förskottsbetalning för kunder och artiklar, och du har också använt olika metoder för att beräkna förskottsbetalningar för en order. Du har provat att tilldela en order ett fullständigt förskottsbelopp och du har låtit beräkna förskottsbeloppet som en procentuell del av hela ordern.  

Du har också bokfört en förskottsfaktura, skapat en andra förskottsfaktura när ordern har ändrats och bokfört slutfakturan för det återstående beloppet.  

Förskottsfunktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)] gör det enkelt att lägga upp och använda förskottsregler för kunder och artiklar och det gör att du kan bokföra varje betalning mot en faktura.  

## <a name="see-also"></a>Se även  
[Fakturera förskottsbetalningar](finance-invoice-prepayments.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)
