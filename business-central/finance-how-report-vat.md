---
title: Skicka momsrapporter till skattemyndigheterna
description: Lär dig hur du förbereder en rapport över moms från försäljning under en period eller från försäljning och inköp och skickar rapporten till en skattemyndighet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, tax, report, EC sales list, statement'
ms.search.form: '321, 322, 323, 474, 475, 739, 740, 741, 742, 743, 744, 745, 746, 747, 748, 9401'
ms.date: 01/31/2022
ms.author: bholtorf
---

# <a name="report-vat-to-tax-authorities"></a>Rapportera moms till skattemyndigheterna

Det här avsnittet beskrivs rapporterna i [!INCLUDE[prod_short](includes/prod_short.md)] som du kan använda för att skicka information om moms (VAT) för försäljning och inköp till skattemyndigheten i din region. Beroende på vilket land/region det gäller kan rapporterna innehålla specifik information eller så kan det finnas ytterligare rapporter som du måste skicka. Kontrollera artiklarna för ditt land/region i avsnittet [Lokala funktioner](about-localization.md).  

Du kan använda följande inbyggda rapporter:

* Rapporten **EU-försäljningslista**  

    Europeiska unionens (EU) rapport med försäljningslista visar momsbeloppen (VAT) som du har samlat in för försäljning till momsregistrerade kunder i EU-länderna/regionerna.  
* Rapporten **Momsretur**  

    Rapporten Momsretur inkluderar moms för försäljning och inköp till kunder och från leverantörer i alla länder/regioner som använder moms.  

I båda fallen (som i andra momsrelaterade rapporter) beräknas moms utifrån tabellen Moms-bokföringsinställningar och de momsbokföringsmallar du har skapat. [!INCLUDE[prod_short](includes/prod_short.md)] visar momstransaktioner som alltid baseras på deras **momsdatum** som ett primärt rapporteringsdatum.  

> [!NOTE]
> Alla momsrelaterade rapporter körs nu med **momsdatumet** för att filtrera relevanta poster. Även om du ställer in **Användning av momsdatum** som **Använd inte funktionen för momsdatum** [!INCLUDE[prod_short](includes/prod_short.md)] kommer det att dölja alla instanser av **Momsdatum** i appen. **Momsdatumet** används dock fortfarande i alla rapporter och fylls i automatiskt med **bokföringsdatum**.

Om du vill se en fullständig historik över momstransaktioner för alla bokföringar som avser moms skapas en transaktion på sidan **momstransaktioner**. Dessa transaktioner används för att beräkna momsavräkningsbeloppet (betalningen eller återbetalningen) för en bestämd period. För att se momstransaktioner, välj ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **momstransaktioner** och väljer sedan relaterad länk.

> [!NOTE]
> Varje [!INCLUDE[prod_short](includes/prod_short.md)] miljö är avsedd att hantera lagstadgad rapportering i ett enda land/region. Den nederländska versionen av [!INCLUDE[prod_short](includes/prod_short.md)] hanterar momsrapportering i Nederländerna men inte i andra länder/regioner. På samma sätt hanterar USA-versionen av [!INCLUDE[prod_short](includes/prod_short.md)] 1099 rapportering i USA och saknar stöd för att åberopa momsrapportering i andra länder/regioner, såvida det inte har gjorts av ett tillägg som levererats av vårt partner ekosystem eller en kundspecifik kodändring.

## <a name="about-the-ec-sales-list-report"></a><a name="ecsaleslist"></a>Om rapporten med EU-försäljningslista

I Europeiska Unionen (EU) och i Storbritannien måste alla företag som säljer varor och tjänster till momsregistrerade kunder, bland annat kunder inom länder//regioner i Europeiska unionen (EU), lämna in en elektronisk version av rapporten i XML-format till sina tull- och skattemyndigheter. **EU-försäljningslisterapporten** fungerar bara för länder//regioner inom EU.

Rapporten innehåller en rad för varje typ av transaktion med kunden och visar det totala beloppet för alla typer av transaktioner. Det finns tre olika typer av transaktioner som kan tas med i rapporten:  

* B2B varor  
* B2B-tjänster  
* B2B triangulerade varor  

*B2B*-varor och -tjänster anger om du köpt en vara eller tjänst, och är kontrollerade av inställningen **EU-tjänst** i momsbokföringen. *B2B triangulerade varor* anger om du bedriver handel med en 3:e part och är kontrollerad av inställningen **EU trepartshandel** för försäljningsdokument, till exempel försäljningsorder, fakturor, kreditnotor och så vidare.  

När skattemyndigheten granskar rapporten, skickar de ett e-postmeddelande till kontaktpersonen för ditt företag. I [!INCLUDE[prod_short](includes/prod_short.md)] anges kontaktpersonen på sidan **företagsinformation**. Kontrollera att du väljer en kontaktperson i tabellen innan du skickar rapporten.  

### <a name="submit-an-ec-sales-list-report"></a>Skicka in en rapport med EU-försäljningslista

[!INCLUDE [finance-ecsaleslist](includes/finance-ecsaleslist.md)]

## <a name="about-the-vat-return-report"></a><a name="vatreturn"></a>Om rapporten Momsretur

Använd den här rapporten om du vill skicka in moms för försäljnings- och inköpsdokument, till exempel inköpsorder och försäljningsorder, fakturor och kreditnotor. Informationen i rapporten är uppställd på samma sätt som i deklarationen från skattemyndigheten.  

För momsreturen kan du ange transaktionerna som ska inkluderas:

* Skicka endast öppna transaktioner, eller öppna och stängda. Detta är till exempel användbart när du förbereder ditt slutliga årliga moms.
* Skicka bara transaktioner i de angivna perioderna, eller inkludera också transaktioner från tidigare perioder. Detta är användbart när du uppdaterar en momsretur som du har redan skickat, till exempel om en leverantör skickar en faktura för sent.    

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Ansluta till webbtjänsten för lokal skattemyndighet
[!INCLUDE[prod_short](includes/prod_short.md)] ger tjänstanslutningar som ansluter till skattemyndighetens webbplatser. Till exempel om du befinner dig i Storbritannien kan du aktivera serviceanslutningen **GovTalk** för att skicka rapporterna EU-försäljningslista och momsreturen elektroniskt. Om du vill skicka rapporten manuellt, till exempel genom att ange data på skattemyndighetens webbplats krävs inte detta.   

Om du vill rapportera moms till en skattemyndighet elektroniskt, måste du ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till den skattemyndighetens webbplats. Detta kräver att du upprättar ett konto med skattemyndigheten. Om du har ett konto kan du aktivera en service-anslutning som finns i [!INCLUDE[prod_short](includes/prod_short.md)].

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Serviceanslutningar** och väljer sedan lämplig länk.
2. Fyll i relevanta fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > Det är en bra idé att testa anslutningen. Detta gör du genom att markera kryssrutan **Testläge** och sedan förbereda och skicka in din momsrapport enligt anvisningarna i avsnittet [Förbereda och skicka in en momsrapport](#to-prepare-and-submit-a-vat-report). I testläget testar tjänsten om skattemyndigheten kan ta emot rapporten och rapportstatus talar om att testet lyckades. Det är viktigt att komma ihåg att det inte är en verklig inlämning. Om du vill skicka rapporten på riktigt måste du rensa kryssrutan **testläge** och upprepa överföringen.

## <a name="to-set-up-vat-reports-in-"></a>Så här ställer du in momsrapporter i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

### <a name="to-set-up-vat-return-periods"></a>Så här ställer du in momsreturperioder

Om företaget inte finns i Storbritannien kan du använda sidan **Momsreturperioder** för att ställa in planerade momsreturer. Om företaget finns i Storbritannien, se [Göra skatt digital i Storbritannien](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md).  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsreturperioder** och väljer sedan relaterad länk.  
2. På sidan **Momsreturperioder** fyller du i fälten för att ställa in den första perioden. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)].  
3. Upprepa steg 2 för de ytterligare perioder som du vill lägga till.  

Nu när det är dags att skicka in en momsrapport för en momsreturperiod väljer du perioden på sidan **Momsreturperioder** och väljer sedan åtgärden **Skapa momsretur**. På kortet **Momsretur** väljer du sedan åtgärden **Föreslå rader** enligt anvisningarna i steg 3 i följande procedur.  

## <a name="to-prepare-and-submit-a-vat-report"></a>Förbereda och skicka en momsrapport

1. Välj den ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **EU-försäljningslista** eller **momsretur** och väljer sedan relaterad länk.  
2. Välj **Ny** och fyll sedan i relevanta fält. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill generera innehållet i rapporten, väljer du åtgärden **Föreslå rader**.  

    > [!NOTE]  
    >  Du kan granska transaktionerna i rapportraderna innan du skickar rapporten med EU-försäljningslista. Välj raden och välj sedan åtgärden **Visa momstransaktioner**.  

4. När du validerar och förbereder rapporten för att skicka den, välj åtgärden **Frisläpp**.  

    > [!NOTE]  
    > [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerar att rapporten har ställts in korrekt. Om valideringen misslyckas visas felen i **Fel och varningar** så att du kan göra lämpliga ändringar. Vanligtvis om en inställning som saknas i [!INCLUDE[prod_short](includes/prod_short.md)], kan du klicka på meddelandet för att öppna sidan som innehåller informationen som du vill korrigera.  
5. Om du vill skicka rapporten, väljer du åtgärden **skicka**.  

När du skickar rapporten, övervakar [!INCLUDE[prod_short](includes/prod_short.md)] tjänsten och håller reda på dina meddelanden. Fältet **Status** indikerar var rapporten finns i processen. Till exempel när myndigheterna bearbetar rapporten, ändras rapportens status till **lyckades**. Om fel hittas i rapporten som du har skickat in till skattemyndigheten visar status för rapporten **misslyckad**. Du kan visa fel under **fel och varningar**, rätta till dem och sedan skicka rapporten igen. Om du vill visa en lista över alla EG-försäljningslisterapporter, går du till sidan **EG försäljningsrapporter**.  

### <a name="vat-return-statuses"></a>Momsreturstatus

Momsreturer kan ha olika status enligt beskrivningen i följande tabell.

| Status | Beskrivning |
|------------|-------------------------|
| Öppna | När du skapar en ny momsretur. Du kan köra åtgärden **Föreslå rader**. Om du behöver rätta till värdena kan du köra åtgärden **Föreslå rader** igen. Du kan inte skicka en momsretur med denna status. |
| Släppt | Status ändras när du använder åtgärden **Frisläppning**. [!INCLUDE[prod_short](includes/prod_short.md)] snabbfliken **fel och varningar**. Du kan inte göra ändringar eller använda åtgärden **Föreslå rader**. Om du vill göra ändringar måste du öppna momsreturen igen. |
| Avvisade | Om överföringen misslyckas (t.ex. om autentiseringen misslyckades) ändras statusen till **avvisad**. Du kan inte öppna en momsretur igen med denna status. |
| Skickade | Momsreturen skickas med åtgärden **Skicka** eller markeras som skickad med hjälp av funktionen **Markera som skickad**. |
| Godkänd | Momsreturen har denna status om rapporten har markerats som accepterad med hjälp av funktionen **Markera som accepterad**. Om rapporten **Momsretur** är markerad som **Accepterad** kan du köra åtgärden **Beräkna och bokför momsavräkning**. |

## <a name="viewing-communications-with-your-tax-authority"></a>Visa kommunikationen med skattemyndigheten.

I vissa länder//regioner skickar du meddelanden till skattemyndigheten när du skickar rapporter. Du kan visa första och det sista meddelandet som du skickat eller tagit emot genom att välja åtgärderna **hämta skickat meddelande** och **hämta svarsmeddelandet**.  

## <a name="submitting-vat-reports-manually"></a>Skicka momsrapporter manuellt
Om du använder en annan metod för att skicka rapporten, till exempel genom att exportera XML-data och överföra den till en skattemyndighetens webbplats, kan du välja **Välj som levererad** för att stänga perioden. När du markerar en momsrapport som släppt, går den inte längre att redigera. Om du måste ändra rapporten, när du har markerat den som släppt, måste du först öppna den på nytt.

## <a name="vat-settlement"></a>Momsavräkning
Med jämna mellanrum måste du betala nettomoms till skattemyndigheterna. När du måste avräkna momsen ofta kan du köra batch-jobbet **Beräkna/bokför momsavräkning** för att stänga de öppna momstransaktionerna och överföra inköps- och försäljningsbelopp till momsavräkningskontot.

När ett momsbelopp överförs till avräkningskontot krediteras kontot för ingående moms och kontot för utgående moms debiteras med beloppet från momsavräkningsperioden. Kontot för momsavräkning krediteras (eller, om beloppet för ingående moms är större, debiteras) med nettobeloppet. Du kan bokföra avräkningen direkt eller välja att först skriva ut en testrapport.  

> [!Note]
> När du använder batch-jobbet **Beräkna/bokför momsavräkning** om du inte anger en **Moms rörelsebokf.mall** och **Moms prod.bokf.mall** inkluderas transaktioner med alla rörelse- och produktbokföringsmallar.

## <a name="configuring-your-own-vat-reports"></a>Skapa egna momsrapporter.

Rapporten **EU-försäljningslista** är redo att använda från början. Du kan emellertid också skapa egna rapporter om du har en utvecklingslicens som du kan använda för att skapa kodmoduler. Kontakta en Microsoft Partner om du behöver hjälp.  

I följande tabell beskrivs de kodmoduler som måste skapas för rapporten.  

| Kodmodul | Vad du måste göra |
|----|-----|
|Föreslå rader| Hämta information från tabellen **Momstransaktioner** och visa dem i rader i momsrapporten.|
|Innehåll | Kontrollera formatet för rapporten. Till exempel om det är XML- eller JSON. Formaten som ska användas beror på kraven i din skattemyndighets webbtjänsten. |
|Överföring | Styra hur och när du skickar rapporten utifrån hänsyn till skattemyndigheterna. |
|Svarshanterare | Hantera returen från skattemyndigheten. Det kan till exempel skicka ett e-postmeddelande till företagets kontaktperson. |
|Annullera | Skicka en annullering av en momsrapport som har skickats tidigare till skattemyndigheterna. |  

> [!Note]
> När du skapar kodmoduler för rapporten måste du ta hänsyn till värdet i fältet **Momsrapportversion**. Det här fältet måste motsvara versionen av rapporten som är, eller var, krävd av skattemyndigheten. Du kan till exempel ange **2021** i kryssrutan för att ange att rapporten överensstämmer med de krav som gällde det året. Kontakta skattemyndigheterna för att få den senaste versionen.  

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Konfigurera beräknings- och bokföringsmetoder för moms](finance-setup-vat.md)  
[Arbeta med moms på försäljning och inköp](finance-work-with-vat.md)  
[Ställa in försäljning](sales-setup-sales.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
