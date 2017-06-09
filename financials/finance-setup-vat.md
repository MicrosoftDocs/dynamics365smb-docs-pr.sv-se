---
title: "Om att ställa in moms | Microsoft Docs"
description: "Se till att du korrekt beräknar, bokför och rapporterar om moms för försäljning och inköp."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value added tax
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bf06b41a87e24af9e7657dd0585d7d13e3cad1b2
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---

# <a name="setting-up-included365finlongincludesd365finlongmdmd-to-calculate-and-post-value-added-tax"></a>Ställa in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] för att beräkna och bokföra moms
Konsumenter och företag betalar moms när de köper varor eller tjänster. Momsbeloppet att betala kan variera beroende på flera faktorer. I [!INCLUDE[d365fin](includes/d365fin_md.md)] ställer du in moms för att ange de satser som ska användas för beräkning av momsbelopp baserat på följande: 

* Vem du säljer till  
* Vem du köper från  
* Vad du säljer  
* Vad du köper  
  
Du kan ställa in momsberäkningar manuellt, men det kan vara svårt och tidsödande. Om du vill göra det enklare, finns det en assisterade konfigurationsguid med namnet **momsinställning** som hjälper dig med stegen. Vi rekommenderar att du använder den assisterade konfigurationsguiden för att ställa in momsen.

**Observera**: Du kan endast använda guiden om du har skapat ett Mitt företag och inte har bokfört transaktioner som inkluderar moms. Annars skulle vara mycket emkelt att använda olika momssatser av misstag, och göra felaktiga momsrapporter.  
  
Om du vill ställa in momsberäkningar själv eller bara vill ha information om varje steg innehåller i det här avsnittet beskrivningar av varje steg. Dessa omfattar hur du:  
  
* Ställer in rörelsebokföringsmallar för moms för att definiera momssatser för marknader som du gör affärer med. Du tilldelar dessa till kunder och leverantörer.  
* Ställ in produktbokföringsmallar för moms för att definiera momssatser för de produkter och tjänster som du köper eller säljer.  
  
   **Observera**: Koncepten bakom rörelsebokföringsmallen för moms och produkt liknar generella bokföringsmallar. Mer information finns i [Inställning av bokföringsmall](finance-posting-groups.md).
* Kombinera rörelsebokföringsmallar för moms och produkt för att skapa momsinställningar som beräknar momsbelopp för försäljning och inköp.  
* Tilldela produktbokföringsmallar för moms till de redovisningskonton som du använder för försäljning och inköp, och artiklar och resurser.  

   **Observera**: Om du vill ställa in moms för resurser, måste du aktivera användarupplevelsen **Programsvit** för ditt företag. Mer information finns i [anpassa din upplevelse av Dynamics 365 for Financials](ui-experiences.md).
* Använd omvänd moms för handel mellan länder/regioner inom EU.  
* Förstå momsavrundning för dokument.  
* Ställ in klausuler som förklarar hur icke-standardmässiga momssatser används
* Kontrollera momsregistreringsnummer

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Använd den assisterade konfigurationsguiden för att ställa in momsen (rekommenderat).
Vi rekommenderar att du använder den assisterade konfigurationsguiden för att ställa in momsen i [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

Så här startar du den assisterade konfigurationsguiden:
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Assisterad konfiguration**, och välj sedan relaterad länk.  
2. Välj **momsinställning**.

## <a name="set-up-vat-business-posting-groups"></a>Skapa rörelsebokföringsmallar för moms.
Rörelsebokföringsmallar för moms representerar de marknader där du gör affärer med kunder och leverantörer och definierar hur moms beräknas och bokförs på varje marknad. Exempel på momsrörelsebokföringsmallar är **Inhemsk** och **Europeiska unionen (EU)**.  

Använd koder som är lätta att komma ihåg och som beskriver rörelsebokföringsmallen som t.ex. **EU**, **Icke-EU** eller **Inhemsk**. Koden måste vara unik. Du kan ställa in så många koder som du vill, men du kan inte använda samma kod mer än en gång i en tabell.
  
Om du vill konfigurera rörelsebokföringsmall för moms, gör du följande steg:

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Moms rörelsebokföringsmall**, och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.

Du kan skapa standardrörelsebokföringsmallar för moms genom att koppla rörelsebokföringsmallar för moms till generella rörelsebokföringsmallar. [!INCLUDE[d365fin](includes/d365fin_md.md)] tilldelar automatiskt rörelsebokföringsmallen för moms när du tilldelar rörelsebokföringsmallen till ett kund-, leverantörs- eller redovisningskonto. 

## <a name="set-up-vat-product-posting-groups"></a>Skapa produktbokföringsmallar för moms
Produktbokföringsmallar för moms representerar objekten och resurser och som köper och säljer, och bestämmer hur du beräknar och bokför typen av artikel som köps in eller säljs.
Det är praktiskt att använda koder som är lätta att komma ihåg och som beskriver satsen som **ej moms** eller **noll**, **moms10** eller **reducerad** 10 % moms och **moms25** eller **standard** för 25 %.

Om du vill konfigurera rörelsebokföringsmall för moms, gör du följande steg:

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Produktbokföringsmallar för moms**, och välj sedan relaterad länk.  
2. Fyll i fälten om det behövs.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinera momsbokföringsmallar i momsbokföringsinställningar
[!INCLUDE[d365fin](includes/d365fin_md.md)] beräknar momsbeloppen på försäljning och inköp utifrån momsbokföringsinställningar som är kombinationer av rörelsebokföringsmallar för moms och produktbokföringsmallar för moms. För varje kombination kan du fylla i momsprocent,  momsberäkningstyp och redovisningskonton för bokföring av moms som relaterar till försäljning, inköp och omvänd moms. Du kan också ange om momsbelopp ska omberäknas när en kassarabatt används eller tas emot.  

Du kan registrera så många kombinationer som du vill. Om du vill gruppera kombinationer av momsbokföringsinställningar med liknande attribut kan du ange ett **Moms-ID** för varje grupp och tilldela ID:t till gruppmedlemmarna.

Om du vill kombinera momsbokföringsinställningar gör du följande:

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bokföringsinställningar för moms**, och välj sedan relaterad länk.
2. Fyll i fälten om det behövs.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Tilldela momsbokföringsmallar som standard till flera enheter
Om du vill använda samma momsbokföringsmallar för flera poster kan du skapa [!INCLUDE[d365fin](includes/d365fin_md.md)] för att göra detta som standard. Detta kan göras på ett par sätt:

* Du kan tilldela rörelsebokföringsmallar för moms till generella rörelsebokföringsmallar eller kund- och leverantörsmallar 
* Du kan tilldela produktbokföringsmallar för moms från generella produktbokföringsmallar  

Rörelsebokföringsmallen eller produktbokföringsmallen för moms tilldelas när du väljer en rörelse- eller produktbokföringsmall för en kund, leverantör, artikel eller resurs.

## <a name="assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Tilldela momsbokföringsmallar till enskilda konton, kunder, leverantörer, artiklar och resurser
I följande avsnitt beskrivs hur du tilldelar momsbokföringsmallar till enskilda enheter.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Så här tilldelar du momsbokföringsmallar till individuella redovisningskonton 
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kontoplan**, och välj sedan relaterad länk.  
2. Öppna kortet **redovisningskontokortet** för det kontot.
3. På snabbfliken **bokföring** i fältet **Typ av bokföring** väljer du antingen **försäljning** eller **inköp **.  
5. Välj momsbokföringsmallar för försäljnings- eller inköpskontot.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>För att tilldela rörelsebokföringsmallar för moms till kunder och leverantörer  
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Kund** eller **Leverantör** och väljer sedan relaterad länk.  
2. På kortet **Kund** eller **Leverantör** expanderar du snabbfliken **Fakturering**.  
3. Välj rörelsebokföringsmallar för moms.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>För att tilldela produktbokföringsmallar till individuella artiklar och resurser  
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), anger du **Artikel** eller **Resurs** och väljer sedan relaterad länk.  
2. Gör något av följande:
* På kortet **artikel**, expandera snabbfliken **pris och bokföring** och välj **visa fler** för att visa .  
* På kortet **Resurs** expanderar du snabbfliken **Fakturering**.  
3. Välj produktbokföringsmallen med moms.

## <a name="set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Ställ in klausuler som förklarar hur icke-standardmässiga momssatser används
Du konfigurerar en momsklausul som beskriver information om vilken typ av moms som tillämpas. Informationen kan krävas av Myndighetsregleringar. När du registrerar en momsklausul och associera den med en momsbokföringsinställning, visas momsklausulen på alla utskrivna försäljningsdokument som använder momsbokföringsinställningsmallen. 

Om det behövs kan du också ange hur man konverterar momsklausuler till andra språk. När du sedan skapar och skriver ut ett försäljningsdokument som innehåller ett moms-ID, kommer dokumentet att ta med den översatta momsklausulen. Den språkkod som anges på kundkortet bestämmer språket.
  
### <a name="to-set-up-vat-clauses"></a>Så här konfigurerar du momsklausuler
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Momsklausuler**, och välj sedan relaterad länk.  
2. På sidan **momsklusuler** skapar du en ny rad.  
3. I fältet **Kod** anger du en identifierare för klausulen. Du använder den här koden för att tilldela klausulen till momsbokföringsmallar.  
4. I fältet **beskrivning** anger du den text som ska visas i dokument som kan inkludera moms. I fältet **Beskrivning 2** anger du ytterligare text om det behövs. Texten visas på nya rader.  
5. Tillval: Om du vill tilldela momsklausulen till en momsbokföringsinställning direkt väljer du **inställningar**, och väljer sedan klausulen. Om du vill vänta kan du tilldela klausulen vid ett senare tillfälle på sidan Momsbokföringsinställningar.  
6. Valfritt: Att ange hur man översätter momsklausulen, välj åtgärden **översättningar**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Så här tilldelar du en momsklausul till en momsbokföringsinställning
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bokföringsinställningar för moms**, och välj sedan relaterad länk.  
2. I kolumnen **momsklausul** väljer du klausul för varje momsbokföringsinställning som den gäller för.  

### <a name="to-specify-translations-for-vat-clauses"></a>Att ange översättningar för momsklausuler
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Momsklausuler**, och välj sedan relaterad länk.  
2. Välj åtgärden **Översättningar**.  
3. I fältet **språkkod** välj det språk du översätta till.  
4. I fältet **Beskrivning** och **Beskrivning 2** anger du översättning av beskrivningarna. Denna text visas i det översatta momsrapportdokument.  
  
## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Skapa en momsbokföringsinställning för hantering av importmoms
Du använder funktionen för importmoms när du bokför ett dokument där hela beloppet är moms. Du använder detta om du får en faktura med moms för importerade varor från skattemyndigheterna.  
  
Så här anger du koder för importmoms:  
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Produktbokföringsmallar för moms**, och välj sedan relaterad länk.  
2. På sidan Moms produktbokföringsmallar anger du en ny produktbokföringsmall för importmoms.  
3. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Bokföringsinställningar för moms**, och välj sedan relaterad länk.  
4. På sidan Moms bokföringsinställningar skapar du en ny rad eller använder valfri befintlig rörelsebokföringsmall för moms i kombination med den nya produktbokföringsmallen för moms för importmoms.  
5. I fältet **Momsberäkningstyp**väljer du **enbart moms **.  
6. Ange det redovisningskonto som ska användas för att bokföra importmoms i fältet **Ingående moms**. Alla andra konton är valfria.  
  
## <a name="verify-vat-registration-numbers"></a>Kontrollera momsregistreringsnummer
Det är viktigt att momsregistreringsnummer för kunder, leverantörer och kontakter är giltiga. Till exempel ändrar företag sin skatteskuldstatus och i vissa länder kan skattemyndigheterna be dig lämna rapporter som t.ex. EG-försäljningslisterapport som anger de momsregistreringsnummer som du använder när du gör affärer.  
  
Europeiska kommissionen har en tjänst för VIES momsnummervalidering på sin webbplats som är offentlig och kostnadsfri. Men det är fortfarande det extra steget att gå till webbplatsen. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan spara dig det steget och låter dig använda VIES-tjänsten för verifiering och spåra momsregistreringsnummer för kunder, leverantörer och kontakter direkt från kund-, leverantörs- och kontaktkort. Tjänsten i [!INCLUDE[d365fin](includes/d365fin_md.md)] heter EU momsreg. Nr. Valideringstjänst. Den är tillgänglig på sidan **Anslutningar till tjänst**, och du kan börja genom att markera en kryssruta. Registrering behövs inte och tjänsten är gratis.

När du använder vår tjänst registrerar vi en historik över momsregistreringsnummer och kontroller för varje kund, leverantör eller kontakt i **momsregistreringslogga**, så att du enkelt kan spåra dem. Loggen är unik för varje kund. Loggen är användbar för att verifierat att det aktuella momsregistreringsnumret är korrekt. När du verifierar ett momsregistreringsnummer kommer kolumnen **begär ID** i loggen att visa att du har vidtagit åtgärder. 

Du kan se momsregistreringsloggen på kund-, leverantör- eller kontaktkorten på snabbfliken **fakturering** genom att välja sökknappen i **Momsregistreringsnr.** .  

Tjänsten kan också spara tid när du skapar en kund eller leverantör. Om du känner till kundens momsregistreringsnummer kan du ange det i fältet **Momsregistreringsnr.** för kunden eller leverantören, och vi fyller i kundens namn åt dig. Vissa länder har dessutom företagsadresser i ett strukturerat format. I dessa länder fyller vi även i addressen.  

**Anteckningar**: det finns ett par saker att komma ihåg om tjänsten VIES momsnummervalidering:

* Den här tjänsten använder http-protokoll, vilket betyder att data som har överförts via tjänsten inte har krypteras.
* Det kan uppstå avbrott för den här tjänsten som inte Microsoft ansvarar för. Tjänsten är en del av ett omfattande EU-nätverk av nationella register för moms.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Använda omvänd moms för handel mellan länder/regioner inom EU
En del företag måste använda omvänd moms när de handlar med andra företag. Regeln gäller för inköp från länder/regioner inom EU och försäljning till länder/regioner inom EU.

**Obs!**: Denna regel gäller vid handel med företag som är registrerade som momspliktiga i ett annat land eller en annan region inom EU. Om du handlar direkt med konsumenter i andra länder/regioner inom EU bör du kontakta skattemyndigheterna för att få information om gällande momsregler.  

**Tips**: du kan verifiera att ett företag som är registrerat som momspliktigt i ett annat EU-land genom att använda tjänsten validering av EU-momsregistreringsnummer. Tjänsten är tillgänglig utan kostnad i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i delen _Kontrollera momsregistreringsnummer_ i det här avsnittet.

### <a name="sales-to-eu-countries-or-regions"></a>Försäljning till länder eller regioner inom EU
Ingen moms beräknas på försäljning till momspliktiga företag i andra länder/regioner inom EU. Du måste rapportera värdet för försäljningar till länder/regioner inom EU separat i momsrapporten.
För att korrekt beräkna moms på försäljning till länder/regioner inom EU bör du:  
  
* Lägg upp en rad för försäljning med samma information för inköp. Om du redan har lagt upp rader i fönstret Moms bokföringsinställning för inköp från andra länder/regioner inom EU kan du även använda dessa rader för försäljning.  
* Tilldela rörelsebokföringsmallar för moms i fältet **Moms rörelsebokföringsmall** på snabbfliken **Fakturering** på leverantörskortet för varje EU-leverantör. Du bör också ange kundens momsregistreringsnummer i fältet **Momsregistreringsnr.** på snabbfliken **Utlandshandel**.  

När du bokför en försäljning till en kund i ett annat land eller en annan region inom EU beräknas momsbeloppet och en momstransaktion skapas med informationen om omvänd moms och nettobeloppet (det belopp som används för att beräkna momsbeloppet). Inga poster bokförs på momskontona i redovisningen.

## <a name="understanding-vat-rounding-for-documents"></a>Förstå momsavrundning för dokument
Belopp i dokument som ännu inte har bokförts avrundas och visas på ett sätt som motsvarar den slutliga avrundningen av belopp som faktiskt bokförs. Moms beräknas för ett färdigt dokument, vilket innebär att moms som beräknas i dokumentet baseras på summan av alla rader med samma moms-id i dokumentet.

## <a name="see-also"></a>Se även  
[Ställa in orealiserad mervärdesskatt](finance-setup-unrealized-vat.md)
