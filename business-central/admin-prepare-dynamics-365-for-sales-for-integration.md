---
title: Integrering med Dynamics 365 Sales
description: Lär dig hur du hämtar Dynamics 365 Business Central redo att integreras med Dynamics 365 Sales.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 12/15/2023
ms.author: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Integrering med Dynamics 365 Sales

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Rollen säljare betraktas ofta som en de mest utåtriktade projekten i ett företag. Men kan det vara användbart för säljare att kunna se inuti verksamheten och se vad som händer på serverdelen. Genom att integrera [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] kan du ge säljarna en insikt. Integreringen låter användare visa information i [!INCLUDE[prod_short](includes/prod_short.md)] medan de arbetar i [!INCLUDE[crm_md](includes/crm_md.md)]. Till exempel när du förbereder en försäljningsoffert kan det vara bra att veta om det finns tillräckligt mycket lager för att uppfylla ordern. Mer information finns i [Använd Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> I detta ämne beskrivs hur du integrerar onlineversioner av [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)] med hjälp av [!INCLUDE[prod_short](includes/cds_long_md.md)]. Information om lokal konfiguration finns i [förbereda Dynamics 365 Sales för integrering lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## Integrera via Dataverse

Om du vill göra det enklare att ansluta och synkronisera data med andra Dynamics 365-program kan [!INCLUDE[prod_short](includes/prod_short.md)] också integrera med [!INCLUDE[prod_short](includes/cds_long_md.md)]. Du kan t.ex. ansluta till [!INCLUDE[crm_md](includes/crm_md.md)] eller appar som du själv har skapat. Om du integrerar för första gången måste du göra detta via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Mer information finns i [Integrera med Dataverse](admin-common-data-service.md).

Om du redan har integrerat [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)] kan du fortsätta att synkronisera data med hjälp av dina inställningar. Om du uppgraderar eller stänger av [!INCLUDE[crm_md](includes/crm_md.md)]-integreringen måste du emellertid ansluta dig via [!INCLUDE[prod_short](includes/cds_long_md.md)] för att aktivera den igen. Mer information finns i [Uppgradera en integrering med Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> När du återansluter via [!INCLUDE[prod_short](includes/cds_long_md.md)] används standardinställningarna för synkroniseringen, och eventuella konfigurationsinställningar skrivs över. Till exempel tillämpas standardmappningarna för tabeller.

## Integreringsinställningar som är specifika för en [!INCLUDE[crm_md](includes/crm_md.md)]-integrering

Integreringen med [!INCLUDE[prod_short](includes/prod_short.md)] sker via [!INCLUDE[prod_short](includes/cds_long_md.md)], och det finns många standardinställningar och tabeller som tillhandahålls. Utöver standardinställningarna finns det vissa som är specifika för [!INCLUDE[crm_md](includes/crm_md.md)]. Följande avsnitt visar dessa inställningar.

## Behörigheter och säkerhetsroller för användarkonton i Sales

När du installerar integreringslösningen konfigureras behörigheter för användarkontot för integrering. Om behörigheterna ändras kan du behöva återställa dem. Detta kan du göra genom att ominstallera integreringslösningen genom att välja **Omdistribuera integreringslösning** på sidan **Anslutningsinställningar för Dynamics 365**. Följande säkerhetsroller har distribuerats:

* Dynamics 365 Business Central-integreringsadministratör
* Dynamics 365 Business Central-integreringsanvändare
* Dynamics 365 Business Central-produktartikelanvändare

> [!NOTE]
> Om du vill använda åtgärden **Öppna i Business Central** i Sales måste du ha följande privilegier för följande tabeller:
>
> * Du måste ha läsbehörighet för tabellen Anslutning i Dynamics 365 Business Central (nav_connection).
> * Du måste ha läs-, skriv- och borttagningsbehörighet för tabellen Standardanslutning i Dynamics 365 Business Central (nav_defaultconnection).

### Anslutningsinställningar i installationsguiden

Du kan använda en assisterad konfigurationsguide för att snabbt ställa in anslutningen och ange avancerade funktioner, till exempel att koppla mellan transaktioner.

1. Välj **inställningar och tillägg**, och välj **assisterad konfiguration**.
2. Välj **Ställ in Dynamics 365 Sales-anslutning** för att starta guiden för assisterad konfiguration.
3. Fyll i fälten om det behövs.
4. Du kan också använda avancerade inställningar som förbättrar säkerheten och aktiverar fler funktioner. Avancerade inställningarna beskrivs i tabellen nedan.  

| Fält | Description |
|--|--|
| **Importera Dynamics 365 Sales-lösning** | Installera och konfigurera lösningen för integrering i [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Synkronisera artikeldisposition automatiskt**|Anger att projektkötransaktionen för artikeldisposition måste schemaläggas. Jobbkön körs var 30:e minut och uppdaterar tillgängligheten för de kopplade artiklarna.|
| **Aktivera integration av äldre försäljningsorder** | När en användare skapar försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] och expedierar order i [!INCLUDE[prod_short](includes/prod_short.md)] integrerar denna inställning processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).<br><br>**Obs!** Du kan inte använda det här alternativet om du använder alternativet **Dubbelriktad synkronisering av försäljningsorder**. De två inställningarna utesluter varandra. Mer information om det här alternativet finns i [Enkel och dubbelriktad synkronisering av försäljningsorder](#single-and-bi-directional-synchronization-of-sales-orders). |
|**Aktivera anslutning för Dynamics 365 Sales** | Aktivera anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **SDK-version för Dynamics 365** | Detta gäller endast om du integrerar med en lokal version av [!INCLUDE[crm_md](includes/crm_md.md)]. Det här är den SDK-version för Dynamics 365 (även kallat Xrm) för att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen måste vara kompatibel med SDK-versionen som används av [!INCLUDE[crm_md](includes/crm_md.md)] och motsvarande eller senare än den version som används av [!INCLUDE[crm_md](includes/crm_md.md)]. |
|**Dubbelriktad synkronisering av försäljningsorder**|Synkronisera försäljningsorder i båda riktningar. Mer information om det här alternativet finns i [Enkel och dubbelriktad synkronisering av försäljningsorder](#single-and-bi-directional-synchronization-of-sales-orders).<br><br>**Obs!** Du kan inte använda det här alternativet om du använder alternativet **Aktivera integration av äldre försäljningsorder**. De två inställningarna utesluter varandra.|

### Anslutningsinställningar på inställningssidan för Microsoft Dynamics 365-anslutningar

Ange följande information om anslutningen från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[prod_short](includes/prod_short.md)].

| Fält | Description |
|--|--|
|**Dynamics 365 Sales-URL**|URL:en för din instans av [!INCLUDE[crm_md](includes/crm_md.md)]. Med den här inställningen kan användare öppna de poster i [!INCLUDE[prod_short](includes/prod_short.md)] som motsvarar poster i [!INCLUDE[crm_md](includes/crm_md.md)]. Till exempel ett konto eller en produkt. [!INCLUDE[prod_short](includes/prod_short.md)]-poster är öppna i [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Synkronisera artikeldisposition automatiskt**|Anger att projektkötransaktionen för artikeldisposition måste schemaläggas. Jobbkön körs var 30:e minut och uppdaterar tillgängligheten för de kopplade artiklarna.|
|**SDK-version för Dynamics 365**|Om du integrerar med en lokal version av [!INCLUDE[crm_md](includes/crm_md.md)] är det denna SDK-versionen för Dynamics 365 (även kallad Xrm) som du använder för att ansluta [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]. Den version som du väljer måste vara kompatibel med SDK-versionen som används av [!INCLUDE[crm_md](includes/crm_md.md)]. Den här versionen motsvarar eller är senare än den version som används av [!INCLUDE[crm_md](includes/crm_md.md)].|

Förutom inställningarna ovan anger du följande inställningar för [!INCLUDE[crm_md](includes/crm_md.md)].

| Fält | Beskrivning |
|--|--|
| **Försäljningsorderintegrering är aktiverad** | Användaren ska kunna skicka försäljningsorder och aktiverade offerter i [!INCLUDE[crm_md](includes/crm_md.md)] och sedan granska och bearbeta dem i [!INCLUDE[prod_short](includes/prod_short.md)]. Denna inställning integrerar processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Skapa försäljningsorder automatiskt** | Skapa en försäljningsorder i [!INCLUDE[prod_short](includes/prod_short.md)] när en användare skapar och skickar en i [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Bearbeta försäljningsofferter automatiskt** | Bearbeta en försäljningsoffert i [!INCLUDE[prod_short](includes/prod_short.md)] när en användare skapar och aktiverar en i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Hantering av försäljningsoffertdata](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Dubbelriktad synkronisering av försäljningsorder**|Synkronisera försäljningsorder i båda riktningar. Mer information om det här alternativet finns i [Enkel och dubbelriktad synkronisering av försäljningsorder](#single-and-bi-directional-synchronization-of-sales-orders).|
<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->
### Enkel och dubbelriktad synkronisering av försäljningsorder

När du ställer in integreringen, antingen i installationsguiden eller på sidan Microsoft Dynamics 365-anslutningsinställning, finns det alternativ som styr i vilken riktning du synkroniserar försäljningsorder och hur du skickar dem.

Med alternativet **Dubbelriktad synkronisering av försäljningsorder** kan du synkronisera försäljningsorder från Sales till [!INCLUDE [prod_short](includes/prod_short.md)] och vice versa. Om en kund t.ex. ändrar sig angående den produkt eller kvantitet de beställt i [!INCLUDE[crm_md](includes/crm_md.md)] kan du utföra ändringen genom att arkivera försäljningsdokumentet och skapa ett nytt [!INCLUDE[prod_short](includes/prod_short.md)]. Detsamma gäller dokument i [!INCLUDE[prod_short](includes/prod_short.md)]. Om t. ex. priser, momsbelopp eller förväntade leveransdatum ändras, synkroniseras ändringarna till [!INCLUDE[crm_md](includes/crm_md.md)]. Dubbelriktad synkronisering hjälper säljarna hållas uppdaterade med de senaste ändringarna och statusen för försäljningsorder.

För dubbelriktad synkronisering gör du försäljningsorder tillgängliga för synkronisering när du ändrar deras status till **Skickad** i Sales. När du anger den statusen kan du inte längre ändra informationen på orderraderna. När du synkroniserar överförs ordern till [!INCLUDE [prod_short](includes/prod_short.md)] med statusen **Släppt**. Om det finns ett misstag kan du återställa ordern till **Öppen** (i [!INCLUDE [prod_short](includes/prod_short.md)]) eller **Aktiv** (i Sales) och lägg sedan till eller ta bort rader för att rätta till misstaget och skicka beställningen igen.

> [!TIP]
> När du aktiverar alternativet **Dubbelriktad synkronisering av försäljningsorder** skapar [!INCLUDE [prod_short](includes/prod_short.md)] en post på sidan **Arkiv för försäljningsorder** när du bokför eller ändrar information på en order. De arkiverade versionerna kan till exempel vara användbara för att utforska en orders historik.

Alternativet **Aktivera integrering av äldre försäljningsorder** synkroniseras endast från Sales till [!INCLUDE [prod_short](includes/prod_short.md)]. För det här alternativet använder du åtgärden **Skicka** i Sales för att göra order tillgängliga för synkronisering. När du gör det kan du inte längre ändra någon information på ordern. När du synkroniserar överförs ordern till [!INCLUDE [prod_short](includes/prod_short.md)] med statusen **Släppt**.

För att använda detta alternativ måste du ange autentiseringsuppgifter för en administratörs användarkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Hantera speciella försäljningsorderdata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!NOTE]
> Alternativen **Dubbelriktad synkronisering av försäljningsorder** och **Aktivera integration av äldre försäljningsorder** utesluter varandra. Du kan inte använda båda alternativen samtidigt.

För båda alternativen [!INCLUDE [prod_short](includes/prod_short.md)] visas alla försäljningsorder med statusen **Skickad** på sidan **Order – Microsoft Dynamics 365 Sales**.

### Standardinställd försäljningsenhetsmappningar för synkronisering

Enheter i [!INCLUDE[crm_md](includes/crm_md.md)], till exempel order, är integrerade med motsvarande tabelltyper i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel försäljningsorder. För att arbeta med [!INCLUDE[crm_md](includes/crm_md.md)]-data anger du länkar kallade "kopplingar" mellan tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[crm_md](includes/crm_md.md)].

I följande tabell visas standardmappningen mellan tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] som [!INCLUDE[prod_short](includes/prod_short.md)] tillhandahåller.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synkroniseringsriktning | Standardfilter |
|--|--|--|--|
| Enhet | Enhetsgrupp | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Artikel | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-kontaktfilter: **produkttyp** är **Sales-lager** |
| Resurs | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-kontaktfilter: **produkttyp** är **Tjänster** |
| Artikelenhet | CRM UOM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Resursenhet | CRM UOM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Enhetsgrupp | CRM Uomschedule | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Kund prisgrupp | Prislista | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Förs.pris | Produktprislista | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] kontaktfilter: **försäljningskod** är inte tom, **förs.typ** är **kundprisgrupp** |
| Affärsmöjlighet | Affärsmöjlighet | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Försäljningsfakturahuvud | Fakturera | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Försäljningsfakturarad | Fakturaprodukt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Rubrik för försäljningsorder | Försäljningsorder | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Om du vill synkronisera i båda riktningarna måste du aktivera reglaget **Dubbelriktad synkronisering av försäljningsorder** på sidan **Anslutningsinställningar för Dynamics 365**.| [!INCLUDE[prod_short](includes/prod_short.md)] Försäljningsrubrikfilter: **Dokumenttyp** är Order, **Status** är Utsläppt |
| Försäljningsordermeddelanden | Försäljningsordermeddelanden | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Mappningarna för tabellerna Artikelenhet, Resursenhet och Enhetsgrupp är endast tillgängliga om din administratör har aktiverat växeln **enhetsgruppmappning** på sidan **Microsoft Dynamics 365 anslutningsinställningar**. Mer information finns i [Synkronisera artiklar och resurser med produkter i andra måttenheter](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronize-items-and-resources-with-products-with-different-units-of-measure).

## Synkronisera artiklar och resurser med produkter i andra måttenheter

Företag producerar eller köper ofta artiklarna i en enhet och säljer dem sedan i en annan enhet. För att synkronisera objekt som använder flera måttenheter måste du aktivera växeln **Mappning av enhetsgrupp** på sidan **Microsoft Dynamics 365 anslutningsinställning**. 

När du aktiverar funktionen för uppdatera skapas en ny enhetsgrupptabell som tilldelas varje artikel och resurs i [!INCLUDE[prod_short](includes/prod_short.md)]. Tabellerna gör att du kan kartlägga tabellerna enhetsgrupp, artikelmåttenhet och resursmåttenhet i [!INCLUDE[prod_short](includes/prod_short.md)] till Dynamics 365 Sales enhetsgrupp i [!INCLUDE[crm_md](includes/crm_md.md)]. I följande bild visas mappningarna.

:::image type="content" source="media/unit group 1.png" alt-text="Register mappningar för enhetsgrupper":::

Du kan skapa flera måttenheter för varje enhetsgrupp och tilldela grupperna till produkter i [!INCLUDE[crm_md](includes/crm_md.md)]. Därefter kan du synkronisera produkterna med artiklar och resurser i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan manuellt koppla artikelenheter eller resursenheter med en enhetsgrupp. När du gör det och enhetsgruppen för artikeln eller resursen inte är kopplad till en enhetsgrupp i [!INCLUDE[crm_md](includes/crm_md.md)], till exempel eftersom enhets gruppen inte finns, [!INCLUDE[prod_short](includes/prod_short.md)] skapas enhetsgruppen automatiskt i [!INCLUDE[crm_md](includes/crm_md.md)].

### Mappa artiklar och resurser till produkter

När du aktiverar växeln **Mappning av enhetsgrupp** på sidan **Microsoft Dynamics 365 anslutningsinställning** sker följande:

* Nya mappningar skapas för artiklar och resurser.
* Befintliga mappningar tas bort. <!--which mappings?-->
* Vid en datauppgradering skapas enhetsgrupper för artiklar och resurser.

Om du vill använda de nya mappningarna måste du synkronisera enhetsgrupper, artikelenheter och måttenheter. Du måste också synkronisera om artiklar och resurser. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] tillåter inte att du ändrar en enhetsgrupp mot en produkt. Därför måste du dra av produkterna och koppla loss artiklarna och resurserna och sedan synkronisera genom att skapa nya produkter i [!INCLUDE[crm_md](includes/crm_md.md)]. 

Följande steg beskriver hur du börjar mappa enhetsgrupper:

1. Kontrollera att produkter i [!INCLUDE[crm_md](includes/crm_md.md)] inte är kopplade till artiklar eller resurser i [!INCLUDE[prod_short](includes/prod_short.md)]. Om de är det går du till sidorna för **Artiklar** och/eller **Resurser** och använder filteralternativen för att välja kopplade poster. Välj sedan åtgärden **Dynamics 365 Sales** och sedan **Ta bort koppling**. Denna åtgärd schemalägger ett bakgrundsprojekt för att koppla loss posterna. När projektet körs kan du kontrollera dess status med hjälp av åtgärden för **synkroniseringsloggen**. Mer information finns i [Koppla och synkronisera](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Eftersom nya produkter kommer att skapas i [!INCLUDE[crm_md](includes/crm_md.md)] med nya enhetsgrupper gör du något av följande för att undvika dubblettnamn:
    
  * Byt namn på produkterna och ställ sedan av dem i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Ställa av produkter (Försäljningsnav)](/dynamics365/sales-enterprise/retire-product). Om du vill massredigera dina produkter i Microsoft Excel loggar du in på Power Apps, väljer din miljö, går till tabellen **Produkt** och väljer sedan fliken **Data**. Rensa alla filter som tillämpas. I gruppen **Data**, välj åtgärden **Redigera data i Excel**. Lägg till ett prefix eller suffix för de tillkopplade produkterna och ställ sedan av dem.
    * Ställ av produkterna och ta bort dem. 

3. Utför följande steg för att synkronisera **enhetsgrupper**, **måttenheter**, **artiklar** och **resurser**:
    1. I [!INCLUDE[prod_short](includes/prod_short.md)], öppna sidan **Dynamics 365 Sales anslutningsinställningar**
    2. Använd åtgärden **kör fullständig synkronisering** för att öppna sidan **Dataverse Fullständig synk.granskning**.
    3. För mappningarna **ARTIKELENHET**, **RESURSENHET** och **ENHETSGRUPP** väljer du åtgärden **Rekommendera fullständig synkronisering**.
    4. Välj åtgärden **Synkronisera alla**.

    > [!NOTE]
    > För mappningar som ännu inte har synkroniserats helt synkroniseras dessa åtgärder helt och hållet. Ta bort mappningarna från sidan för att förhindra att mappningar synkroniseras. Detta innebär att de endast tas bort från den aktuella fullständiga synkroniseringen och att mappningarna inte tas bort.
    
5. Välj mappningen **ARTIKEL-PRODUKT** och sedan åtgärden **Starta om**. Omstart skapar nya produkter från artiklarna i [!INCLUDE[crm_md](includes/crm_md.md)] och tilldelar en ny enhetsgrupp som är specifik för artikeln.
6. Välj mappningen **RESURS-PRODUKT** och sedan åtgärden **Starta om**. Omstart skapar nya produkter från resurserna i [!INCLUDE[crm_md](includes/crm_md.md)] och tilldelar en ny enhetsgrupp som är specifik för resurser.

### Synkroniseringsregler

Följande tabell anger regler som kontrollerar synkroniseringen mellan [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)]. Dessa regler gäller utöver de regler som angetts för Dataverse, vilka också gäller. För mer information, se [Standardenhetsmappningar](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Ändrar data som genomfördes av användarkontot för integrering synkroniseras inte. Därför rekommenderar vi att du inte ändrar data när du använder kontot. Mer information finns i [Ställa in konton för att integrera med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Bord|Regel|
|-----|----|
|Enheter|Måttenheter synkroniseras med enhetsgrupper i [!INCLUDE[crm_md](includes/crm_md.md)]. Det kan finnas endast en måttenhet som definieras i enhetsgruppen.|
|Artiklar|När artiklar synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter skapar [!INCLUDE[prod_short](includes/prod_short.md)] automatiskt en prislista i [!INCLUDE[crm_md](includes/crm_md.md)]. För att undvika synkroniseringsfel bör du inte ändra denna prislista manuellt.|
|Resurser|Resurser som ska synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-produkter som har produktypen tjänster.|
|Kundprisgrupper|Kundprisgrupper synkroniseras med Sales-prislistor.|
|Förs.priser|Sales-priser som har försäljning skriver kundprisgrupp och har definierats försäljningskod synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-prislistrader|
|Affärsmöjligheter|Affärsmöjligheter som ska synkroniseras med [!INCLUDE[crm_md](includes/crm_md.md)]-affärsmöjligheter. Värdet för säljarkod definierar ägare till den kopplade tabellen i [!INCLUDE[crm_md](includes/crm_md.md)].|
|Bokförda försäljningsfakturor|Bokförda försäljningsfakturor som är synkroniserade med försäljningsfakturor. Innan du kan synkronisera en faktura är det bättre att synkronisera alla andra tabeller som kan delta i fakturan, från säljare till prislistor. Värdet för säljarkod i fakturarubriken definierar ägaren till den kopplade tabellen i Sales.|
|Försäljningsorder|När integrering av försäljningsorder har aktiverats synkroniseras försäljningsorder i [!INCLUDE[prod_short](includes/prod_short.md)] som har skapats från skickade försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] med försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] när de släpps. Innan du synkroniserar order bör du först synkronisera alla tabeller som ingår i ordern, till exempel säljare och prislistor. Fältet Säljarkod i orderrubriken definierar ägaren till den kopplade tabellen i [!INCLUDE[crm_md](includes/crm_md.md)].|

### Synkroniseringsprojekt för Sales-integrering

Projekten körs i följande ordning i syfte att undvika kopplingsberoenden mellan tabeller. Det finns ytterligare projekt tillgängliga från Dataverse. Mer information finns i [Använda projektköer för att schemalägga uppgifter](./admin-job-queues-schedule-tasks.md).

1. MÅTTENHET – Dynamics 365 Sales synkroniseringsprojekt  
2. RESURS-PRODUKTER – Dynamics 365 Sales synkroniseringsprojekt  
3. ARTKEL-PRODUKTER – Dynamics 365 Sales synkroniseringsprojekt  
4. ANPASSADPRISGRUPP – Dynamics 365 Sales-synkroniseringsprojekt.
5. FÖRSÄLJNPRIS – PROUDUKTPRIS – Dynamics 365 Sales synkroniseringsprojekt.
6. BOKFÖRD FÖRSÄLJNINGSFAKTURA-FAKT – Dynamics 365 Sales-synkroniseringsprojekt.

### Poster för standardsynkroniseringjobbkön

I följande tabell beskrivs standardsynkroniseringjobben för [!INCLUDE[crm_md](includes/crm_md.md)].  

|Projektkötransaktion|Beskrivning|Riktning|Registermappning för integrering|Standardfrekvens för synkronisering (minuter)|Standardväntetid för inaktivitet (minuter)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MÅTTENHET – Dynamics 365 Sales synkroniseringsprojekt|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper med [!INCLUDE[prod_short](includes/prod_short.md)]-måttenheter.|Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|MÅTTENHET|30|720<br> (12 tim)|
|RESURS-PRODUKTER – Dynamics 365 Sales synkroniseringsprojekt|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[prod_short](includes/prod_short.md)]-resurser.|Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|RESURS-PRODUKT|30|720<br> (12 tim)|
|ARTIKEL – PRODUKT – Dynamics 365 Sales synkroniseringsprojekt|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-produkter med [!INCLUDE[prod_short](includes/prod_short.md)]-artiklar.|Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUKT|30|1440<br> (24 tim)|
|ANPASSADPRISGRUPP – PRIS – Dynamics 365 Sales synkroniseringsprojekt|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] försäljningsprislistor med [!INCLUDE[prod_short](includes/prod_short.md)] kundprisgrupper.| |KUNDPRISGRUPPER – FÖRSÄLJNINGSPRISLISTOR|30|1440<br> (24 tim)|
|FÖRSÄLJNPRIS – PROUDUKTPRIS – Dynamics 365 Sales synkroniseringsprojekt|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)] produktpriser med [!INCLUDE[prod_short](includes/prod_short.md)] försäljningspriser.||PRODUKTPRIS-FÖRSÄLJNINGSPRIS|30|1440<br> (24 tim)|
|BOKFÖRD FÖRSÄLJNINGSFAKTURA-FAKT – Dynamics 365 Sales synkroniseringsprojekt|Synkroniserar [!INCLUDE[crm_md](includes/crm_md.md)]-fakturor med [!INCLUDE[prod_short](includes/prod_short.md)] bokförda försäljningsfakturor.|Från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]|FAKTUROR-BOKFÖRDA FÖRSÄLJNINGSFAKTUROR|30|1440<br> (24 tim)|
|Kundstatistik – Dynamics 365 Sales-synkronisering.|Uppdaterar [!INCLUDE[crm_md](includes/crm_md.md)]-konton med senaste [!INCLUDE[prod_short](includes/prod_short.md)] kundinformation. I [!INCLUDE[crm_md](includes/crm_md.md)] visas den här informationen i snabbformuläret **Business Central bankkontostatistik** som är kopplat till [!INCLUDE[prod_short](includes/prod_short.md)] kunder.<br /><br /> Informationen kan även uppdateras manuellt från varje kundpost. Mer information finns i [Koppla och synkronisera posterna manuellt](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Obs:** denna projektkötransaktion är endast relevant om [!INCLUDE[prod_short](includes/prod_short.md)] integreringslösning är installerad i [!INCLUDE[crm_md](includes/crm_md.md)]. |Ej tillämpbart|Ej tillämpbart|30|Ej tillämpbart| 

## Anslut till lokala versioner av Business Central 2019 utgivningscykel 1 och Microsoft Dynamics NAV 2018

Microsoft Power Platform-teamet har [meddelat](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) att man kommer att fasa ut autentiseringstypen Office365. Om du använder en version av [!INCLUDE[prod_short](includes/prod_short.md)] lokalt som är äldre än Business Central 2019 utgivningscykel 1 måste du använda OAuth-autentiseringstypen för att ansluta till [!INCLUDE[crm_md](includes/crm_md.md)] online. Instruktionerna i det här avsnittet beskriver hur du ansluter följande produktversioner:

* Business Central 2019 utgivningscykel 1
* Microsoft Dynamics NAV 2018

### Förutsättningar

* Du måste ha en Microsoft Azure-prenumeration. Ett provkonto kommer att fungera för programregistrering.
* [!INCLUDE[crm_md](includes/crm_md.md)] är konfigurerad för att använda någon av följande autentiseringstyper:

   * Office 365 (äldre)

     > [!IMPORTANT]
     > Från och med april 2022 kommer Office 365 (äldre) inte längre att stödjas. Mer information finns i [Viktiga ändringar (utfasningar) som kommer i Power Apps, Power Automate och kundengagemangsappar](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   * OAuth

### Anslut Business Central 2019 utgivningscykel 1 och Dynamics NAV 2018

1. Importera integreringslösningen Microsoft Dynamics 365 Business Central i din [!INCLUDE[crm_md](includes/crm_md.md)]-miljö. Integreringslösningen finns i mappen CrmCustomization på [!INCLUDE[prod_short](includes/prod_short.md)] eller Dynamics NAV 2018 installation DVD. Beroende på produktversionen importerar du något av följande lösningar:

   * För [!INCLUDE[prod_short](includes/prod_short.md)] innehåller mappen DynamicsNAVIntegrationSolution_v9 och DynamicsNAVIntegrationSolution_v91. lösningar. Vilken lösning du bör importera beror på vilken version av [!INCLUDE[crm_md](includes/crm_md.md)] du ansluter till. [!INCLUDE[crm_md](includes/crm_md.md)] online kräver integreringslösningen DynamicsNAVIntegrationSolution_v91.
   * För Dynamics NAV 2018, installera lösningen DynamicsNAVIntegrationSolution.

2. Skapa en icke-interaktiv integrationsanvändare i din [!INCLUDE[crm_md](includes/crm_md.md)]-miljö och tilldela användaren följande säkerhetsroller. Mer information finns i [skapa ett icke-interaktivt användarkonto](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central-integreringsadministratör
   * Dynamics 365 Business Central-integreringsanvändare

   > [!Important]
   > Den här användaren får inte ha säkerhetsrollen Systemadministratör. Du kan heller inte använda systemadministratörskontot som integrationsanvändare.

3. Skapa en programregistrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Azure-portalen. Mer information finns i [Registrera ett program i Microsoft Entra ID](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Vi rekommenderar att du registrerar appen i samma klientorganisation som din Dataverse-miljö så att du inte behöver ge appen åtkomst till miljön. Om du registrerar programmet i en annan miljö måste du logga in på Microsoft Entra ID med administratörskontot för din Dataverse-miljö och ge ditt tillstånd.
   >
   > Dessutom måste appen du registrerar inte ha någon hemlighet. Det går bara att ansluta en app med hemlighet till Dataverse i Business Central 2020 utgivningscykel 1 och senare.
  
4. Beroende på produktversionen importerar du något av följande steg:

    * I [!INCLUDE[prod_short](includes/prod_short.md)] söker du efter **Konfiguration av anslutning till Microsoft Dynamics 365** och väljer sedan relaterad länk. 
    * I Dynamics NAV 2018 söker du efter **Konfiguration av anslutning till Microsoft Dynamics 365 for Sales** och väljer sedan relaterad länk.

5. I fältet **Autentiseringstyp**, välj alternativet för OAuth. 
6. Välj den CRM SDK-version som matchar den lösningsversion som du importerade i steg 1.

   > [!NOTE]
   > Det här steget är bara relevant för [!INCLUDE[prod_short](includes/prod_short.md)].

7. Ange URL för din [!INCLUDE[crm_md](includes/crm_md.md)]-miljö och anger sedan användarnamn och lösenord för integrationsanvändaren. 

   * I [!INCLUDE[prod_short](includes/prod_short.md)] använd fältet **Serveradress**.
   * I Dynamics NAV 2018, använd fältet **Dynamics 365 Sales URL**.

8. I fältet **Anslutningssträng** anger du ID för programregistreringen. Detta fält har två token i vilka ID:t för ditt program ska anges.

   |Token           |Beskrivning  |
   |----------------|-------------|
   |**AppId**       |Ange program-ID.      |
   |**RedirectUri** |Ange program-ID, men Lägg till prefixet **app://**.         |

    **Exempel** Följande exempel visar en anslutningssträng.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Aktivera anslutningen.

> [!Note]
> Om du vill konfigurera en anslutning till en [!INCLUDE[crm_md](includes/crm_md.md)]-instans med en specifik autentiseringstyp fyller du i fälten i snabbfliken **Information om autentiseringstyp**. Mer information finns i [Autentisering med Microsoft Dataverse webbtjänster](/powerapps/developer/data-platform/authentication). Detta steg är inte nödvändigt när du ansluter en onlineversion av [!INCLUDE[prod_short](includes/prod_short.md)].

## Se även

[Ställa in konton för integrering med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Ställ in en anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synkroniserar Business Central och [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Förbereder Dynamics 365 Sales för integrering lokalt](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
