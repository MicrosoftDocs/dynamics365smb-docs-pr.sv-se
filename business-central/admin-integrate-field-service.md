---
title: Integrera med Microsoft Dynamics 365 Field Service
description: Integration av Business Central Field Service.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# Integrera med Microsoft Dynamics 365 Field Service

Serviceorganisationer behöver ett komplett program där ekonomi, lager och inköp är tätt kopplade till tjänsteleverans. De genererar finansiella data med varje transaktion. Varje arbetsorder representerar kostnad och intäkt och varje resurs genererar vinst och förlust. Kundinteraktioner lägger till transaktioner i redovisningen. Integrationen mellan [!INCLUDE [prod_short](includes/prod_short.md)] och [!INCLUDE [field-service-short](includes/field-service-short.md)] effektiviserar hela processen för att hantera serviceåtgärder och säkerställer ett smidigt informationsflöde mellan de två systemen.  

Du kan enkelt skapa och hantera arbetsorder i [!INCLUDE [field-service-short](includes/field-service-short.md)], spåra förloppet för serviceuppgifter, tilldela resurser och samla in förbrukningsinformation. När du slutför en arbetsorder i [!INCLUDE [field-service-short](includes/field-service-short.md)] möjliggör integreringen en smidig överföring av data till [!INCLUDE [prod_short](includes/prod_short.md)] för vidare bearbetning.  

Integrationen underlättar också fakturering och uppfyllande av arbetsorder i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan generera korrekta fakturor baserat på serviceaktiviteter och den förbrukning som registrerats i [!INCLUDE [field-service-short](includes/field-service-short.md)].  

Genom att integrera [!INCLUDE [prod_short](includes/prod_short.md)] med [!INCLUDE [field-service-short](includes/field-service-short.md)] behöver du inte ange data manuellt eller duplicera ansträngningar. Integrationen ger också en heltäckande bild av serviceverksamheten och ekonomin, vilket möjliggör bättre beslutsfattande och operativ effektivitet.

## Förutsättningar

Eftersom [!INCLUDE [field-service-short](includes/field-service-short.md)] bygger på Dynamics 365 Sales måste du [konfigurera en anslutning till Dataverse](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) och [aktivera integrering med Dynamics 365 Sales](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

### Behörigheter och säkerhetsroller för användarkonton

När du installerar integreringslösningen konfigureras behörigheter för användarkontot för integrering. Om behörigheterna ändras kan du behöva återställa dem. Detta kan du göra genom att ominstallera integreringslösningen från sidan **Anslutningsinställningar för Dynamics 365** genom att välja **Omdistribuera integreringslösning**. I följande avsnitt visas de behörigheter och säkerhetsroller som lösningen distribuerar för varje app.

#### FÖRS

* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-integreringsadministratör
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)] integreringsanvändare
* Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]-produktartikelanvändare

#### Business Central

Användare som bokför projektjournaler måste ha följande behörighetsuppsättning:

* Integration med Dynamics 365 Sales

#### Fältservice

Om du vill använda integrerade data måste användarna ha följande säkerhetsroll:

* Integration av Business Central Field Service

Användare måste till exempel ha den här rollen att koppla arbetsorder till [!INCLUDE [prod_short](includes/prod_short.md)] för bearbetning.

> [!NOTE]
> Se till att användarna tilldelas standardsäkerhetsrollerna och standardprofilerna i [!INCLUDE [field-service-short](includes/field-service-short.md)].  
>
> Mer information om kolumnsäkerhetsprofiler i finns [!INCLUDE [field-service-short](includes/field-service-short.md)] i [ Field Service säkerhetsroller](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles).
>
> Administratörer måste lägga till en av lämpliga kolumnsäkerhetsprofiler för användare i Power Platform. Mer information finns i [Lägga till team eller användare i en kolumnsäkerhetsprofil för att styra åtkomsten](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Om du vill använda åtgärden **Öppna i Business Central** i Sales måste du ha följande privilegier för följande tabeller:
>
> * Du måste ha **läsbehörighet** för tabellen **Anslutning i Dynamics 365 Business Central** (nav_connection).
> * Du måste ha **läs**-, **skriv**- och **borttagnings**-behörighet för tabellen **Standardanslutning i Dynamics 365 Business Central** (nav_defaultconnection).

### Andra inställningar i Field Service

På sidan **Field Service-inställningar**, gör följande ändringar:

* På fliken **Inköp** avmarkerar du fältet **Användning av produkter slut i lager**. Annars kan du få en varning om att produkten är slut i lager när du väljer en produkt som är slut i lager i [!INCLUDE [field-service-short](includes/field-service-short.md)], men som finns i lager [!INCLUDE [prod_short](includes/prod_short.md)].
* På fliken **Arbetsorder/bokning** stänger du av växlingsknapparna **Beräkna pris** och **Beräkna kostnad**. I fältet **Skapa arbetsorderfaktura** klickar du på **Aldrig**.

> [!NOTE]
> Om du ställer in en anslutning till [!INCLUDE [field-service-short](includes/field-service-short.md)] tas kopplingen mellan resurser och produkter bort. Om du vill göra [!INCLUDE [prod_short](includes/prod_short.md)] artiklar tillgängliga i [!INCLUDE [field-service-short](includes/field-service-short.md)], uppdaterar du fältet **Field Service produkttyp** för att matcha fältet **Typ** för artiklarna i [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Skapa en produkt eller tjänst](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## Ställ in integrering i Business Central

När du har en anslutning till Dataverse och försäljning kan du ställa in integreringen till [!INCLUDE [field-service-short](includes/field-service-short.md)]. På sidan **Assisterad konfiguration** i [!INCLUDE [prod_short](includes/prod_short.md)] väljer du **Konfigurera integrering till Dynamics 365 Field Service** för att köra guiden för assisterad konfiguration. I det här avsnittet beskrivs nyckelinställningarna i guiden.

Om du vill låta personer bokföra förbrukning av artiklar och tjänster i [!INCLUDE [field-service-short](includes/field-service-short.md)] arbetsorder anger du vilken **Projektjournalmall** och **Projektjournal** som ska användas för att bokföra förbrukning av produkter och tjänster.

Eftersom tjänster uttrycks i varaktighet i [!INCLUDE [field-service-short](includes/field-service-short.md)] anger du vilken **måttenheten timmar** som ska användas för att konvertera varaktigheter till antal i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan också ange när arbetsorderprodukter och servicerader synkroniseras till [!INCLUDE [prod_short](includes/prod_short.md)]. De kan till exempel synkroniseras när arbetsorderrader används eller när någon slutför en arbetsorder. Välj lämpligt alternativ i fältet **Synkronisera produkter/tjänster för arbetsorder**.

När produkter och tjänster för arbetsordern har synkroniserats med projektjournaler i [!INCLUDE [prod_short](includes/prod_short.md)] kan du välja om du vill bokföra projektjournalerna manuellt. Välj lämpligt alternativ i fältet **Bokför projektjournalrader automatiskt**:

* När en arbetsorder är slutförd.
* När arbetsorderprodukter eller tjänster används.

När du är klar med installationen kör du en fullständig synkronisering från sidan **Dynamics 365 Field Service integreringsinställningar**. Den här åtgärden synkroniserar tabellmappningar för till exempel:

* Projektuppgifter för projekt med uppsättningen **Använd förbrukningslänk**. Den här synkroniseringen gör [!INCLUDE [prod_short](includes/prod_short.md)] projekt tillgängliga för urval i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* Resurser som inte är blockerade, som inte har **Använd tidrapport** markerat och som har **Timmar** angivna som enhet på sidan **Integreringsinställningar för Dynamics 365 Field Service**.
* Serviceartiklar (kräver att du använder Premium-upplevelsen i [!INCLUDE [prod_short](includes/prod_short.md)]).

## Standardinställd Field Service enhetsmappning för synkronisering

Grunden för att synkronisera data är att mappa tabeller och fält i [!INCLUDE [prod_short](includes/prod_short.md)] med tabeller och kolumner i Dataverse så att dessa kan utbyta data. Mappning sker via integreringsregister. Mer information om tabellmappningar finns i [Mappa tabeller och fält som ska synkroniseras](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

Integrering med [!INCLUDE [field-service-short](includes/field-service-short.md)] introducerar följande standardmappningar av integreringsregister:

* **PJLINE-WORDERPRODUCT** – Mappar arbetsorderprodukter i [!INCLUDE [field-service-short](includes/field-service-short.md)] till projektjournalrader i [!INCLUDE [prod_short](includes/prod_short.md)].
* **PJLINE-WORDERSERVICE** – Mappar arbetsordertjänster i [!INCLUDE [field-service-short](includes/field-service-short.md)] till projektjournalrader i [!INCLUDE [prod_short](includes/prod_short.md)].
* **PROJECTTASK** – Mappar projekt och projektuppgifter i [!INCLUDE [prod_short](includes/prod_short.md)] till produkter i externa projekt i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **RESOURCE-BOOKABLERSC** – Mappar resurser i [!INCLUDE [prod_short](includes/prod_short.md)] till bokningsbara resurser i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **SVCITEM-CUSTASSET** – (endast Premium-upplevelsen) Mappar serviceartiklar i [!INCLUDE [prod_short](includes/prod_short.md)] till kundtillgångar i [!INCLUDE [field-service-short](includes/field-service-short.md)].

## Använda data i båda programmen

I följande avsnitt beskrivs de funktioner där du kan använda data från [!INCLUDE [prod_short](includes/prod_short.md)] och [!INCLUDE [field-service-short](includes/field-service-short.md)].

### Fältservice

Du kan skapa [skapa arbetsorder](/dynamics365/field-service/create-work-order) med hjälp av **Tjänstkontot** och **Faktureringskontot** från [!INCLUDE [prod_short](includes/prod_short.md)]. På arbetsorder måste du välja **Business Central-projektaktivitet** i fältet **Externt projekt**. Om du väljer ett projekt kan du synkronisera arbetsorderprodukter och -tjänster med lämplig projektuppgift i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan lägga till lagerartiklar och ej lagerförda artiklar som **Arbetsorderprodukter** på arbetsorder och hämta lagersaldo samt kostnader och priser från [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Skapa en arbetsorder från arbetsorderformuläret och postlistan](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

Du kan lägga till artiklar av typen service som **Arbetsordertjänster** och hämta kostnader och priser från [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns på [fliken Produkter och tjänster](/dynamics365/field-service/work-order-experience#products-and-services-tab).

> [!NOTE]
> När status för en produkt eller tjänst på en arbetsorder ändras från **Uppskattad** till **Använd** i [!INCLUDE [field-service-short](includes/field-service-short.md)], synkroniseras de med projektjournalraderna i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan boka en resurs och relatera till **Bokningar** till arbetsordertjänster med hjälp av en **Bokningsbar resurs** från [!INCLUDE [prod_short](includes/prod_short.md)].

### Business Central

Beroende på dina inställningar på sidan **Konfigurera Field Service-integration**, när arbetsorder inkluderar produkter och tjänster, överförs förbrukningsinformation och bokförs med hjälp av en **Projektjournal** i [!INCLUDE [prod_short](includes/prod_short.md)].

Värdena **Kvantitet att fakturera** och **Varaktighet att fakturera** kopieras till fältet **Kvantitet att fakturera till faktura**. Baserat på dessa värden kan du skapa och bokföra försäljningsfakturor i [!INCLUDE [prod_short](includes/prod_short.md)] för att fakturera kunden. När fakturan har bokförts eller förbrukningen har bearbetats i [!INCLUDE [prod_short](includes/prod_short.md)] visas det fakturerade antalet och det förbrukade antalet på fliken [!INCLUDE [prod_short](includes/prod_short.md)] på sidorna **Arbetsorderprodukt** och **Arbetsordertjänst**.  

Använd sidan **Projektplaneringsrader** om du vill spåra bokföring och fakturering av förbrukning på arbetsorder. Från sidan **Projektplaneringsrader** kan du skapa och bokföra försäljningsfakturor i [!INCLUDE [prod_short](includes/prod_short.md)]. Därefter kan du synkronisera dem med [!INCLUDE [field-service-short](includes/field-service-short.md)] och hålla reda på fakturornas status.

> [!NOTE]
> Arbetsordertjänster med en bokning som använder en bokningsbar resurs som är kopplad till en [!INCLUDE [prod_short](includes/prod_short.md)]-resurs synkroniseras till två projektjournalrader: en rad av typen **Budget** för den kopplade resursen och en annan rad av typen **Fakturerbar** för artikeln som ska på service.
>
> Produkten som väljs i arbetsordertjänsten måste vara kopplad till en artikel av typen **Service** i [!INCLUDE [prod_short](includes/prod_short.md)]. Dessutom måste basenheten för artikeln anges till den **måttenhet för timmar** som har valts på sidan **Konfiguration av Dynamics 365 Field Service-integration**.
>
> Du kan skapa en faktura för en artikel av typen **Service** från den fakturerbara projektplaneringsraden och använda projektplaneringsraden för budget för att registrera kostnader med resursen.

## Se även

[Integrera med Microsoft Dataverse via datasynkronisering](admin-common-data-service.md)  
[Mappa register och fält som ska synkroniseras](admin-how-to-modify-table-mappings-for-synchronization.md)