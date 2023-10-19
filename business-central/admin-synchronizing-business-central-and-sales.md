---
title: Synkronisering och dataintegrering | Microsoft Docs
description: 'Synkroniseringen kopierar data mellan Microsoft Dataverse-register och Business Central-poster, och håller datan i båda systemen uppdaterade.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'Dataverse, integration, sync, synchronize, mapping'
---

# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Synkroniserar data i Business Central med Microsoft Dataverse

När du integrerar [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)] kan du bestämma om du vill synkronisera data i valda fält i [!INCLUDE[prod_short](includes/prod_short.md)] (till exempel kunder, kontakter och säljare) med motsvarande rader i [!INCLUDE[prod_short](includes/cds_long_md.md)] (till exempel konton, kontaktpersoner och användare). Beroende på radtyp kan du synkronisera data från [!INCLUDE[prod_short](includes/cds_long_md.md)] till [!INCLUDE[prod_short](includes/prod_short.md)] och vice versa. Mer information finns i [Integrera med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

Synkronisering använder följande element:

* Registermappningar för integrering
* Fältmappningar för integrering
* Synkroniseringsregler
* Kopplade poster

När synkroniseringen har konfigurerats kan du koppla [!INCLUDE[prod_short](includes/prod_short.md)]-poster till [!INCLUDE[prod_short](includes/cds_long_md.md)]-rader i syfte att synkronisera deras data. Du kan starta en synkronisering manuellt eller enligt ett schema. I tabellen nedan finns en översikt över olika sätt att synkronisera.  

|  Typ  |  Metod  |  Gå till  |  
|--------|----------|-------|  
|Manuell synkronisering|Synkronisera med utgångspunkt från rad-till-rad.<br /><br /> Du kan synkronisera enskilda poster i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel en kund, med en motsvarande [!INCLUDE[prod_short](includes/cds_long_md.md)]-rad, till exempel ett konto. Detta är vanligtvis hur användarna kommer att arbeta med [!INCLUDE[prod_short](includes/cds_long_md.md)] data i [!INCLUDE[prod_short](includes/prod_short.md)].|[Koppla och synkronisera poster manuellt](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Synkronisera utifrån registermappningen.<br /><br /> Du kan synkronisera alla poster i ett [!INCLUDE[prod_short](includes/prod_short.md)]-register med ett [!INCLUDE[prod_short](includes/cds_long_md.md)]-register.|[Synkronisera individuella registermappningar](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Synkronisera alla ändrade poster för alla registermappningar.<br /><br /> Du kan synkronisera alla poster som har ändrats i [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller sedan den senaste synkroniseringen.|[Synkronisera alla ändrade poster](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Fullständig synkronisering av all data för alla registermappningar.<br /><br /> Du kan synkronisera all data i [!INCLUDE[prod_short](includes/prod_short.md)]- och [!INCLUDE[prod_short](includes/cds_long_md.md)]-register som mappas, och skapa nya poster eller rader i mållösningen för ej kopplade poster i ursprungslösningen.<br /><br /> Fullständig synkronisering synkroniserar alla data och ignorerar kopplingen. Vanligtvis gör du en fullständig synkronisering när du ställer in integrering och endast en av lösningarna innehåller data. En fullständig synkronisering kan också vara lämplig i demonstrationsmiljöer.|[Kör en fullständig synkronisering](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Schemalagd synkronisering|Synkronisera alla ändringar i data för alla registermappningar.<br /><br /> Du kan synkronisera [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] på schemalagda intervall, genom att ställa in projekt i projektkön.|[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

> [!NOTE]
> Synkroniseringen mellan [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)] baseras på den tidsplanerade körningen av projektkötransaktioner och garanterar inte konsekventa realtidsdata mellan två tjänster. För konsekventa realtidsdata bör du utforska de [virtuella Business Central-tabellerna](/dynamics365/business-central/dev-itpro/powerplatform/powerplat-overview) eller API:erna för Business Central.   

## <a name="standard-table-mapping-for-synchronization"></a>Standardtabellmappning för synkronisering

Register i [!INCLUDE[prod_short](includes/cds_long_md.md)], till exempel konton, är integrerade med motsvarande registertyper i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel kunder. För att arbeta med [!INCLUDE[prod_short](includes/cds_long_md.md)]-data anger du länkar kallade "kopplingar" mellan tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)].

I följande tabell visas standardmappningen mellan register i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Du kan återställa konfigurationsändringar som har gjorts i integrationstabellen och fältmappningarna till standardinställningarna genom att välja mappningarna och sedan välja **Använd standardinställning för synkronisering**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Synkroniseringsriktning | Standardfilter |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Säljare/Inköpare | Användare | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] kontaktfilter: **Status** är **Nej**, **Licensierad användare** är **Ja**, integreringsanvändarläge är **Nej** |
| Kund | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] kontofilter: **Relationstyp** är **Kund** och **Status** är **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)] filter: **Spärrad** är tom (kunden är inte spärrad). |
| Leverantör | Konto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] kontofilter: **Relationstyp** är **Leverantör** och **Status** är **Aktiv**. [!INCLUDE[prod_short](includes/prod_short.md)] filter: **Spärrad** är tom (leverantör är inte spärrad). |
| Kontakt | Kontakt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-kontaktfilter: **Typen** är **Person** och kontakten har tilldelats till ett företag. [!INCLUDE[prod_short](includes/cds_long_md.md)]-kontaktfilter: Kontakten har tilldelats till ett företag och överordnad kundtyp är **Kund**. |
| Valuta | Transaktionsvaluta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |

> [!NOTE]
> **Dataverse**-åtgärderna kommer inte att vara tillgängliga på sidor, till exempel kundkortsidan, för poster som inte respekterar tabellfiltret för mappningen av integrationstabellen.

### <a name="tip-for-admins-viewing-table-mappings"></a>Tips för administratörer: Visa tabellmappningar

Du kan visa mappningen mellan register i [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)] på sidan **Tabellmappningar för integrering**, där du även kan tillämpa filter. Du definierar mappningen mellan fälten i [!INCLUDE[prod_short](includes/prod_short.md)]-register och kolumnerna i [!INCLUDE[prod_short](includes/cds_long_md.md)]-register på sidan **Mappning av integreringsfält**, där du kan lägga till ytterligare mappningslogik. Det kan exempelvis vara praktiskt om du behöver felsöka synkronisering.

## <a name="use-virtual-tables-to-get-more-data"></a>Använda virtuella tabeller för att hämta mer data

När du konfigurerar integreringen kan du använda virtuella tabeller för att göra mer data tillgängliga i [!INCLUDE[prod_short](includes/cds_long_md.md)], utan hjälp från en utvecklare.

En virtuell tabell är en anpassad tabell som har kolumner och rader som innehåller data från en extern datakälla, till exempel [!INCLUDE [prod_short](includes/prod_short.md)]. Kolumnerna och raderna i en virtuell tabell ser ut som en vanlig tabell, men datan lagras inte i en fysisk tabell i [!INCLUDE[prod_short](includes/cds_long_md.md)]-databasen. Istället hämtas data vid körning.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] innehåller objekt som även kallas virtuella tabeller. Dessa tabellobjekt är inte relaterade till de virtuella tabeller som du använder med [!INCLUDE[prod_short](includes/cds_long_md.md)].

Mer information om virtuella tabeller finns i följande artiklar:

* [Skapa och redigera virtuella tabeller som innehåller data från en extern datakälla](/power-apps/maker/data-platform/create-edit-virtual-entities) (Power Apps-dokumentationen)
* [Virtuell Business Central-tabell för Microsoft Dataverse-administratörsreferens](/business-central/dev-itpro/powerplatform/powerplat-admin-reference)  ([!INCLUDE [prod_short](includes/prod_short.md)]-dokumentation)

Om du vill använda virtuella tabeller måste du installera programmet **Virtuell Business Central-enhet** från [AppSource](https://appsource.microsoft.com/en-US/product/dynamics-365/microsoftdynsmb.businesscentral_virtualentity). 

När du har installerat programmet kan du aktivera virtuella tabeller från någon av följande sidor i [!INCLUDE [prod_short](includes/prod_short.md)]:

* När du kör den assisterade konfigurationsguiden **Konfigurera Dataverse-anslutning** kan du använda sidan **Dataverse-tillgängliga virtuella tabeller** om du vill välja flera virtuella tabeller. Därefter är tabellerna tillgängliga i [!INCLUDE[prod_short](includes/cds_long_md.md)] och PowerApps Maker Portal. 
* Från sidorna **Konfiguration för Dataverse-anslutning**, **Virtuella tabeller** och **Tillgängliga virtuella tabeller**.  
* Från Power App Maker Portal.

## <a name="synchronize-data-from-multiple-companies-or-environments"></a>Synkronisera data från flera företag eller miljöer

Du kan synkronisera data från flera [!INCLUDE [prod_short](includes/prod_short.md)]-företag eller miljöer med en [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljö. I synkroniseringsscenarier för flera företag finns det flera saker att tänka på.

### <a name="set-company-ids"></a>Ange företags-ID:n

När du synkroniserar poster anger vi ett företags-ID för entiteten [!INCLUDE[prod_short](includes/cds_long_md.md)] för att klargöra vilket [!INCLUDE [prod_short](includes/prod_short.md)]-företag som posterna kommer från. Integreringstabellmappningar har filterfält för integreringstabeller som tar hänsyn till företags-ID:t. Om du vill inkludera en tabellmappning i en konfiguration med flera företag markerar du kryssrutan **Synkronisering aktiverad för flera företag** på sidan **Mappning för integreringstabell**. Inställningen optimerar hur integreringstabellfilterfält filtrerar företags-ID:n i en konfiguration med flera företag.

Om du väljer kryssrutan **Synkronisering aktiverad för flera företag** för integrationstabellmappningar som synkroniserar dokument, till exempel order, offerter och affärsmöjligheter, kommer integreringen endast att beakta entiteter med företags-ID tillhörande aktuellt [!INCLUDE [prod_short](includes/prod_short.md)]-företag. Om du till exempel vill synkronisera dokument mellan Business Central och Sales måste användare i Försäljning ange företags-ID:t i dokumenten. Annars synkroniseras inte dokumenten.  

Om du markerar kryssrutan **Synkronisering aktiverad för flera företag** avlägsnas filtret på företags-ID:t för alla andra integreringstabellmappningar. Synkroniseringen tar hänsyn till relaterade entiteter, oavsett deras företags-ID.

### <a name="specify-the-synchronization-direction"></a>Ange synkroniseringsriktningen

Om du aktiverar stöd för flera företag för en integreringstabellmappning rekommenderar vi att du anger mappningens riktning till **FromIntegration**. Om du anger riktningen till **Till integration** eller **Dubbelriktad** är det en bra idé att använda **Tabellfilter** och **Integrationstabellfilter** för att styra vilka entiteter som ska synkroniseras med vilket företag. Det är också en bra idé att använda matchningsbaserad koppling för att undvika att skapa dubblettposter. Om du vill ha mer information om matchningsbaserad koppling [Anpassa matchningsbaserad koppling](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#customize-the-match-based-coupling).

### <a name="use-unique-numbers"></a>Använd unika nummer

Om din nummerserie inte garanterar att primärnyckelvärdena är unika för varje företag rekommenderar vi att du använder prefix. Om du vill börja använda prefix skapar du en transformeringsregel för integreringsfältmappningen. Mer information om omvandlingsregler finns i [Hantera skillnader i fältvärden](admin-how-to-modify-table-mappings-for-synchronization.md#handle-differences-in-field-values).

## <a name="see-also"></a>Se även

[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)   
[Schemalägg en synkronisering](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
