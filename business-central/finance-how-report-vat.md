---
title: Skicka momsrapporter till skattemyndigheten | Microsoft Docs
description: Lär dig hur du förbereder en rapport över moms från försäljning under en period eller från försäljning och inköp och skickar rapporten till en skattemyndighet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c4536dca720be5d52bc860c9acce8d7f903314ff
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "919081"
---
# <a name="how-to-report-vat-to-a-tax-authority"></a>Så här: rapportera moms till skattemyndigheterna
Det här avsnittet beskrivs rapporterna i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du kan använda för att skicka information om moms (VAT) för försäljning och inköp till skattemyndigheten i din region.

Du kan använda följande rapporter:

* **EU förs.lista** Europeiska gemenskapens (EG) rapport med försäljningslista visar momsbeloppen (VAT) som du har samlat in för försäljning till momsregistrerade kunder i EU-länderna.  
* Rapporten **momsretur** inkluderar moms för försäljning och inköp till kunder i alla länder som använder moms.

Om du vill se en fullständig historik över momstransaktioner för alla bokföringar som avser moms skapas en transaktion på sidan **momstransaktioner**. Dessa transaktioner används för att beräkna momsavräkningsbeloppet (betalningen eller återbetalningen) för en bestämd period. För att visa momstransaktioner, välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **momstransaktioner** och välj sedan relaterad länk.

## <a name="about-the-ec-sales-list-report"></a>Om rapporten med EU-försäljningslista
I Storbritannien måste alla företag som säljer varor och tjänster till momsregistrerade kunder, bland annat kunder i inom Europeiska unionen (EU) lämna in en elektronisk version av rapporten i XML-format via webbplatserna Her Majesty's Revenue och Customs. EG-försäljningslisterapporten fungerar bara för länder inom EU.

Rapporten innehåller en rad för varje typ av transaktion med kunden och visar det totala beloppet för alla typer av transaktioner. Det finns tre olika typer av transaktioner som kan tas med i rapporten:  

* B2B varor  
* B2B-tjänster  
* B2B triangulerade varor  

B2B varor och tjänster som anger om du köpt en vara eller tjänst, och är kontrollerade av inställningen **EU-tjänst** i momsbokföringen. B2B triangulerade varor anger om du bedriver handel med en 3:e part och är kontrollerad av inställningen **EU trepartshandel** för försäljningsdokument, till exempel försäljningsorder, fakturor, kreditnotor och så vidare.  

När skattemyndigheten granskar rapporten, skickar de ett e-postmeddelande till kontaktpersonen för ditt företag. I [!INCLUDE[d365fin](includes/d365fin_md.md)] anges kontaktpersonen på sidan **företagsinformation**. Kontrollera att du väljer en kontaktperson i tabellen innan du skickar rapporten.

## <a name="about-the-vat-return-report"></a>Om rapporten momsretur
Använd den här rapporten om du vill skicka in moms för försäljnings- och inköpsdokument, till exempel inköpsorder och försäljningsorder, fakturor och kreditnotor. Informationen i rapporten är uppställd på samma sätt som i deklarationen från skattemyndigheten.  

Moms beräknas utifrån tabellen Moms bokföringsinställningar och de momsbokföringsmallar du har skapat.

För momsreturen kan du ange transaktionerna som ska inkluderas:

* Skicka endast öppna transaktioner, eller öppna och stängda. Detta är till exempel användbart när du förbereder ditt slutliga årliga moms.
* Skicka bara transaktioner i de angivna perioderna, eller inkludera också transaktioner från tidigare perioder. Detta är användbart när du uppdaterar en momsretur som du har redan skickat, till exempel om en leverantör skickar en faktura för sent.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Ansluta till webbtjänsten för lokal skattemyndighet
[!INCLUDE[d365fin](includes/d365fin_md.md)] ger tjänstanslutningar som ansluter till skattemyndighetens webbplatser. Till exempel om du befinner dig i Storbritannien kan du aktivera serviceanslutningen **GovTalk** för att skicka rapporterna EU-försäljningslista och momsreturen elektroniskt. Om du vill skicka rapporten manuellt, till exempel genom att ange data på skattemyndighetens webbplats krävs inte detta.   

Om du vill rapportera moms till en skattemyndighet elektroniskt, måste du ansluta [!INCLUDE[d365fin](includes/d365fin_md.md)] till den skattemyndighetens webbplats. Detta kräver att du upprättar ett konto med skattemyndigheten. Om du har ett konto kan du aktivera en service-anslutning som finns i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Anslutningar till tjänst** och välj sedan lämplig länk.
2. Fyll i relevanta fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >   Det är en bra idé att testa anslutningen. Genom att välja **testläge** och sedan skapa och skicka en momsrapport som beskrivs i avsnittet _att förbereda och skicka en momsrapport_. I testläget testar tjänsten om skattemyndigheten kan ta emot rapporten och rapportstatus talar om att testet lyckades. Det är viktigt att komma ihåg att det inte är en verklig inlämning. Om du vill skicka rapporten på riktigt måste du rensa kryssrutan **testläge** och upprepa överföringen.

## <a name="to-set-up-vat-reports-in-included365finincludesd365finmdmd"></a>Så här ställer du in momsrapporter i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurera momsrapport** och välj sedan relaterad länk.  
2. Om du vill låta användarna ändra och skicka om rapporten, väljer du kryssrutan **ändra skickade rapporter**.  
3. Välj nummerserien som ska användas för varje rapport.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Förbereda och skicka en momsrapport
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **EU-försäljningslista** eller **Momsretur** och välj sedan relaterad länk.  
2. Välj **Ny** och fyll sedan i relevanta fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill generera innehållet i rapporten, väljer du åtgärden **Föreslå rader**.  

    > [!NOTE]  
    >   Du kan granska transaktionerna i rapportraderna innan du skickar rapporten med EU-försäljningslista. Välj raden och välj sedan åtgärden **Visa momstransaktioner**.  
4. När du validerar och förbereder rapporten för att skicka den, välj åtgärden **Frisläpp**.  

    > [!NOTE]  
    >   [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerar att rapporten har ställts in korrekt. Om valideringen misslyckas visas felen i **Fel och varningar** så att du kan göra lämpliga ändringar. Vanligtvis om en inställning som saknas i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du klicka på meddelandet för att öppna sidan som innehåller informationen som du vill korrigera.  
5. Om du vill skicka rapporten, väljer du åtgärden **skicka**.  

När du skickar rapporten, övervakar [!INCLUDE[d365fin](includes/d365fin_md.md)] tjänsten och håller reda på dina meddelanden. Fältet **Status** indikerar var rapporten finns i processen. Till exempel när myndigheterna bearbetar rapporten, ändras rapportens status till **lyckades**. Om fel hittas i rapporten som du har skickat in till skattemyndigheten visar status för rapporten **misslyckad**. Du kan visa fel under **fel och varningar**, rätta till dem och sedan skicka rapporten igen. Om du vill visa en lista över alla EG-försäljningslisterapporter, går du till sidan **EG försäljningsrapporter**.  

## <a name="viewing-communications-with-your-tax-authority"></a>Visa kommunikationen med skattemyndigheten.
I vissa länder skickar du meddelanden till skattemyndigheten när du skickar rapporter. Du kan visa första och det sista meddelandet som du skickat eller tagit emot genom att välja åtgärderna **hämta skickat meddelande** och **hämta svarsmeddelandet**.  

## <a name="submitting-vat-reports-manually"></a>Skicka momsrapporter manuellt
Om du använder en annan metod för att skicka rapporten, till exempel genom att exportera XML-data och överföra den till en skattemyndighetens webbplats, kan du välja **Välj som levererad** för att stänga perioden. När du markerar en momsrapport som släppt, går den inte längre att redigera. Om du måste ändra rapporten, när du har markerat den som släppt, måste du först öppna den på nytt.

## <a name="vat-settlement"></a>Momsavräkning
Med jämna mellanrum måste du betala nettomoms till skattemyndigheterna. När du måste avräkna momsen ofta kan du köra batch-jobbet **Beräkna/bokför momsavräkning** för att stänga de öppna momstransaktionerna och  överföra inköps- och försäljningsbelopp till momsavräkningskontot.

När ett momsbelopp överförs till avräkningskontot krediteras kontot för ingående moms och kontot för utgående moms debiteras med beloppet från momsavräkningsperioden. Kontot för momsavräkning krediteras (eller, om beloppet för ingående moms är större, debiteras) med nettobeloppet. Du kan bokföra avräkningen direkt eller välja att först skriva ut en testrapport.  

> [!Note]
> När du använder batch-jobbet **Beräkna/bokför momsavräkning** om du inte anger en **Moms rörelsebokf.mall** och **Moms prod.bokf.mall** inkluderas transaktioner med alla rörelse- och produktbokföringsmallar.

## <a name="configuring-your-own-vat-reports"></a>Skapa egna momsrapporter.
Du kan använda den EG-försäljningslisterapport men du kan också skapa egna rapporter. Detta innebär att du skapar några kodmoduler. Kontakta en Microsoft Partner om du behöver hjälp med.  

I följande tabell beskrivs de kodmoduler som måste skapas för rapporten.

| Kodmodul | Vad du måste göra |
|----|-----|
|Föreslå rader| Hämta information från tabellen momstransaktioner och visa dem i rader i momsrapporten.|
|Innehåll | Kontrollera formatet för rapporten. Till exempel om det är XML- eller JSON. Formaten som ska användas beror på kraven i din skattemyndighets webbtjänsten. |
|Överföring | Styra hur och när du skickar rapporten utifrån hänsyn till skattemyndigheterna. |
|Svarshanterare | Hantera returen från skattemyndigheten. Det kan till exempel skicka ett e-postmeddelande till företagets kontaktperson. |
|Annullera | Skicka en annullering av en momsrapport som har skickats tidigare till skattemyndigheterna. |  

> [!Note]
> När du skapar kodmoduler för rapporten måste du ta hänsyn till värdet i fältet **momsrapportversion**. Det här fältet måste motsvara versionen av rapporten som är, eller var, krävd av skattemyndigheten. Du kan till exempel ange **2017** i kryssrutan för att ange att rapporten överensstämmer med de krav som gällde det året. Kontakta skattemyndigheterna för att få den senaste versionen.
 
## <a name="see-also"></a>Se även
[Förbereda för beräknings- och bokföringsmetoder för moms](finance-setup-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)  
