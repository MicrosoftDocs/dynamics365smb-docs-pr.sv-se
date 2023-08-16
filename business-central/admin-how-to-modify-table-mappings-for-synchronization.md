---
title: Mappa register och fält som ska synkroniseras
description: Läs om hur du kartlägger tabeller och fält för synkronisering av data mellan Business Central och Microsoft Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
---
# Mappa register och fält som ska synkroniseras

Grunden för att synkronisera data är att mappa tabeller och fält i [!INCLUDE[prod_short](includes/prod_short.md)] med tabeller och kolumner i [!INCLUDE[prod_short](includes/cds_long_md.md)] så att dessa kan utbyta data. Mappning sker via integreringsregister.

## Integreringsregister för mappning

Ett integreringsregister är ett register i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen som representerar ett register, exempelvis ett konto, i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Integreringsregistren innehåller fält som motsvarar kolumner i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-registret. Integreringsregistret Konto ansluter exempelvis till registret Konton i [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. För varje register i [!INCLUDE[cds_short_md](includes/cds_short_md.md)] som du vill synkronisera med data i [!INCLUDE[prod_short](includes/prod_short.md)] måste det finnas en mappning för integreringsregister.

När du skapar anslutningen mellan programmen ställer [!INCLUDE[prod_short](includes/prod_short.md)] in vissa standardmappningar. Om du vill kan du ändra registermappningarna. Mer information finns i [Standardinställd registermappning för synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Om du har ändrat standardmappningarna och vill återställa ändringarna går du till sidan **Mappningar för integreringsregister** och väljer **Använd standardinställningar för synkronisering**.

> [!Note]
> Om du använder en lokal version av [!INCLUDE[prod_short](includes/prod_short.md)] lagras mappningarna för integreringsregister i register 5335 Mappningar för integreringsregister, där du kan visa och redigera mappningarna. Komplexa mappningar och synkroniseringsregler definieras i codeunit 5341.

> [!TIP]
> När en kopplad post ändras synkroniserar [!INCLUDE [prod_short](includes/prod_short.md)] data automatiskt med Dataverse. I de flesta fall är automatisk synkronisering mycket praktiskt. Frekventa ändringar av stora mängder kopplade poster i en tabell kan emellertid sakta ner datasynkroniseringen.
>
> För att undvika långsam prestanda kan du aktivera eller inaktivera händelsebaserade datasynkroniseringar för alla tabeller på sidan **Registermappningar för integrering**. Som standard aktiveras händelsebaserat synkronisering så att befintliga integrationer inte påverkas. Administratören kan aktivera eller inaktivera den för specifika tabeller.

### Ytterligare mappningar

Betalningsvillkor, leveranssätt och speditörer kan ändras och det kan vara viktigt att kunna justera dem. Om du aktiverar **funktionsuppdateringen: mappa till alternativuppsättningar i Dataverse utan kod** på sidan [funktionshantering](https://businesscentral.dynamics.com/?page=2610) kan du lägga till mappningar för integrationstabeller för betalningsvillkor (BETALNINGSVILLKOR), Utleveransvillkor (LEVERANSSÄTT) och speditörer (SPEDITÖR). Med hjälp av den här mappningen kan du se till att alla principer är desamma för dessa inställningar i [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

### Synkroniseringsregler

En mappning av integreringsregister innehåller också regler som styr hur synkroniseringsjobb för integrering synkroniserar poster i ett [!INCLUDE[prod_short](includes/prod_short.md)]-register och ett register i [!INCLUDE[prod_short](includes/cds_long_md.md)]. För exempel på regler för en integration med Försäljning, gå till [Synkroniseringsregler](#synchronization-rules).

### Strategier för att lösa konflikter automatiskt

Datakonflikter kan lätt uppstå när affärsprogram utbyter data kontinuerligt. Någon kan t. ex. ta bort eller ändra en rad i ett av programmen, eller i båda. Om du vill minska antalet konflikter som ska lösas manuellt, kan du ange lösningsstrategier så löser [!INCLUDE[prod_short](includes/prod_short.md)] konflikter automatiskt enligt reglerna i strategierna.

Registermappningar för integrering innehåller regler som styr hur synkroniseringsjobb synkroniserar poster. På sidan **Registermappningar för integrering** i kolumnerna **Lös borttagningskonflikter** och **Lös uppdateringskonflikter** kan du ange hur [!INCLUDE[prod_short](includes/prod_short.md)] ska lösa konflikter som uppstår på grund av att poster togs bort i tabeller i det ena eller andra affärsprogrammet, eller uppdaterades i båda. 

I kolumnen **Lös borttagningskonflikter** kan du välja att [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt återställer borttagna poster, tar bort kopplingen mellan posterna eller inte gör någonting. Om du inte gör någonting måste du lösa konflikter manuellt. 

I kolumnen **Lös uppdateringskonflikter** kan du välja att [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt skickar datauppdateringar till integreringstabellen när data skickas till [!INCLUDE[prod_short](includes/cds_long_md.md)], eller att datauppdateringar ska hämtas från integreringstabellen när data hämtas från [!INCLUDE[prod_short](includes/cds_long_md.md)], eller att ingenting ska göras. Om du inte gör någonting måste du lösa konflikter manuellt.

När du har angett strategin kan du, på sidan **Fel vid synkronisering av kopplade data**, välja åtgärden **Försök alla igen** för att lösa konflikter automatiskt.

## Mappa integreringsfält

Att mappa register är bara det första steget. Du måste också mappa fälten i registren. Mappning av integreringsfält länkar fält i [!INCLUDE[prod_short](includes/prod_short.md)]-register med motsvarande kolumner i [!INCLUDE[prod_short](includes/cds_long_md.md)] och avgör om data ska synkroniseras i respektive register. Den standardregistermappning som [!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller innehåller fältmappningar, men du kan ändra dessa om du vill. Mer information finns i [Visa registermappningar](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings).

> [!Note]
> Om du använder en lokal version av [!INCLUDE[prod_short](includes/prod_short.md)] definieras mappningar av integreringsfält i register 5336 Mappning av integreringsfält.

Du kan mappa fälten manuellt, eller så kan du automatisera den genom att mappa flera fält på samma gång baserat på villkor som matchar deras värden. Mer information finns i [så här tar du flera poster baserat på fältvärdematchning](admin-how-to-couple-and-synchronize-records-manually.md).

### Hantera skillnader i fältvärden

Ibland är värdena i de fält som du vill mappa olika. I [!INCLUDE[crm_md](includes/crm_md.md)] är exempelvis språkkoden för USA "U.S.", men i [!INCLUDE[prod_short](includes/prod_short.md)] är den "US." Detta innebär att du måste omvandla värdet när du synkroniserar data. Detta sker genom omvandlingsregler som du definierar för fälten. Du definierar omvandlingsregler på sidan **Registermappningar för integrering** genom att välja **Mappning** och sedan **Fält**. Fördefinierade regler tillhandahålls, men du kan också skapa egna. Mer information finns i [Omvandlingsregler](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### Hantera alternativvärden som saknas

[!INCLUDE[prod_short](includes/cds_long_md.md)] innehåller kolumner för alternativuppsättningar som tillhandahåller värden som du kan mappa till [!INCLUDE[prod_short](includes/prod_short.md)]-fält av typen **Alternativ** för automatisk synkronisering. Under synkroniseringen ignoreras icke-mappade alternativ, saknade alternativ läggs till i relaterad [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen och läggs till i systemtabellen **CDS-alternativmappning** för att hanteras manuellt senare. Du kan t. ex. lägga till saknade alternativ i någon av produkterna och sedan uppdatera mappningen. Mer information finns i [Hantera saknade alternativvärden](admin-cds-missing-option-values.md).

## Koppla poster

Kopplingen länkar rader i [!INCLUDE[prod_short](includes/cds_long_md.md)] med poster i [!INCLUDE[prod_short](includes/prod_short.md)]. Till exempel är konton i [!INCLUDE[prod_short](includes/cds_long_md.md)] vanligtvis kopplade till kunder i [!INCLUDE[prod_short](includes/prod_short.md)]. Kopplingsposter ger följande fördelar:

* Det möjliggör synkroniseringen.
* Användare kan öppna poster eller rader i en företagsapp från den andra. Detta kräver att programmen redan har integrerats.

Kopplingar kan ställas in automatiskt genom att använda synkroniseringsjobb, eller manuellt genom att redigera posten i [!INCLUDE[prod_short](includes/prod_short.md)]. Mer information finns i [Synkronisera data i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) och [Koppla och synkronisera poster manuellt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## Filtrera poster och rader  

Om du inte vill synkronisera alla rader för ett specifikt register i [!INCLUDE[prod_short](includes/cds_long_md.md)] eller ett register i [!INCLUDE[prod_short](includes/prod_short.md)] kan du ställa in filter för att begränsa datan som synkroniseras. Du ställer in filtren på sidan **Registermappningar för integrering**.  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Registermappning för integrationen** och välj sedan relaterad länk.
2. För att filtrera [!INCLUDE[prod_short](includes/prod_short.md)]-poster anger du fältet **Tabellfilter**.  
3. För att filtrera [!INCLUDE[prod_short](includes/cds_long_md.md)]-rader ställer du in fältet **Filter för integreringsregister**.  

## Skapa nya poster  

Som standard är det bara de poster i [!INCLUDE[prod_short](includes/prod_short.md)] och rader i [!INCLUDE[prod_short](includes/cds_long_md.md)] som är kopplade som synkroniseras med integreringssynkroniseringsjobben. Du kan ställa in registermappningar så att nya poster eller rader skapas i målet (till exempel [!INCLUDE[prod_short](includes/prod_short.md)]) för varje rad i källan (till exempel [!INCLUDE[prod_short](includes/cds_long_md.md)]) som inte redan är kopplad.  

Till exempel använder synkroniseringsjobbet SÄLJARE – Dynamics 365 Sales registermappningen SÄLJARE. Synkroniseringsjobbet kopierar information från användare i [!INCLUDE[prod_short](includes/cds_long_md.md)] till säljare i [!INCLUDE[prod_short](includes/prod_short.md)]. Om du skapar registermappningen för att skapa nya poster kommer, för varje användare i [!INCLUDE[prod_short](includes/cds_long_md.md)] som inte redan är kopplad till en säljare i [!INCLUDE[prod_short](includes/prod_short.md)], en ny säljarrad att skapas i [!INCLUDE[prod_short](includes/prod_short.md)].  

### Så här skapar du nya poster under synkroniseringen  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Registermappning för integrationen** och välj sedan relaterad länk.
2. Rensa fältet i registermappningposten i fältet **Synka endast kopplade poster**.  

## Använda konfigurationsmallar på registermappningar

Du kan tilldela konfigurationsmallar till registermappningar som ska användas för nya poster eller rader som skapas i [!INCLUDE[prod_short](includes/prod_short.md)] eller [!INCLUDE[prod_short](includes/cds_long_md.md)]. För varje registermappning kan du ange en konfigurationsmall som ska användas för nya [!INCLUDE[prod_short](includes/prod_short.md)]-poster och en annan mall för att använda nya [!INCLUDE[prod_short](includes/cds_long_md.md)]-rader.  

Om du installerar standardsynkroniseringsinstallationen kommer för det mesta två konfigurationsmallar att skapas automatiskt och användas på registermappningen för [!INCLUDE[prod_short](includes/prod_short.md)]-kunder och [!INCLUDE[crm_md](includes/crm_md.md)]-konton: **CDSCUST** och **CDSACCOUNT**.  

* **CDSCUST** skapar och synkroniserar nya kunder i [!INCLUDE[prod_short](includes/prod_short.md)] baserat på konton i [!INCLUDE[crm_md](includes/crm_md.md)].  

     Skapa den här mallen genom att kopiera en befintlig konfigurationsmall för kunder. **CDSCUST** skapas endast om det finns en befintlig konfigurationsmall och fältet **Valutakod** i mallen är tomt. Om ett fält i konfigurationsmallen innehåller ett värde, används värdet istället för värdet i den mappade kolumnen för [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontot. Om exempelvis kolumnen **Land/region** i ett konto i [!INCLUDE[prod_short](includes/cds_long_md.md)] innehåller *USA* och fältet **Land/region** i konfigurationsmallen är **GB**, används **GB** som **Land/region** för kunden i [!INCLUDE[prod_short](includes/prod_short.md)].  

* **CDSACCOUNT** skapar och synkroniserar nya konton i [!INCLUDE[prod_short](includes/cds_long_md.md)] baserat på ett konto i [!INCLUDE[prod_short](includes/prod_short.md)].  

### Ange konfigurationsmallar på en registermappning  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Registermappning för integrationen** och välj sedan relaterad länk.
2. I registermappningposten i listan anger du fältet **Mallkod för tabellkonfig.** till konfigurationsmallen som ska användas för nya poster i [!INCLUDE[prod_short](includes/prod_short.md)].  
3. Ange fältet **Mallkod för int.tabellkonfig.** till konfigurationsmallen som ska användas för nya poster i [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Se även  

[Om integrering Dynamics 365 Business Central med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )  
[Synkroniserar Business Central och [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]