---
title: Ställa in konton för integrering med Microsoft Dataverse | Microsoft Docs
description: Lär dig hur du konfigurerar användarkonton med program som utbyter data och som människor använder för att få tillgång till och synkronisera data i program.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 01/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Konfigurera användarkonton för att integrera med Microsoft Dataverse via datasynkronisering

Den här artikeln innehåller en översikt över hur du ställer in de konton som behövs för att integrera [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

## Ställa in administratörsanvändarkontot

Om du vill konfigurera anslutningen mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[prod_short](includes/cds_long_md.md)], måste du logga in på [!INCLUDE[prod_short](includes/prod_short.md)] med ett användarkonto som är tilldelat till [!INCLUDE[prod_short](includes/prod_short.md)] Essential- eller [!INCLUDE[prod_short](includes/prod_short.md)] Premium-licens. Vi använder det här kontot en gång för att installera och konfigurera vissa nödvändiga komponenter.

> [!IMPORTANT]
> Under installationen ombeds du ange autentiseringsuppgifter för [!INCLUDE[prod_short](includes/cds_long_md.md)] miljön. Ange autentiseringsuppgifterna för ett konto som är en licensierad användare och tilldelat till **Systemadministratör** i [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljön och en global administratör på den klientorganisation som miljön tillhör. Det här kontot behöver ingen licens för [!INCLUDE[prod_short](includes/prod_short.md)], eftersom det endast används för att ställa in uppgifter i [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljö.
>
> När anslutningskonfigurationen är klar kan du ta bort denna [!INCLUDE[prod_short](includes/cds_long_md.md)]-användare. Integreringen fortsätter att använda användarkontot som har skapats automatiskt särskilt för integrering.

## Behörigheter och säkerhetsroller för användarkonton i [!INCLUDE[prod_short](includes/cds_long_md.md)]

Basintegreringslösningen skapar följande roll i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] för integreringen:

* **Business Central Dataverse-integrering** – Tillåter dig att hantera anslutningen mellan [!INCLUDE [prod_short](includes/prod_short.md)] och [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Vanligtvis tilldelas detta bara till det automatiskt skapade användarkontot för synkronisering.

> [!NOTE]
> Endast appanvändaren som kör integrationen ska ha rollen **Business Central Dataverse-integrering** . Programanvändaren behöver inte ha [!INCLUDE [prod_short](includes/prod_short.md)]- eller [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-licenser.

När du installerar basintegreringslösningen konfigurerar den behörigheter för integrationsanvändarkontot. Om behörigheterna ändras manuellt kan du återställa dem. Välj **Omdistribuera integreringslösning** på sidan **Dataverse anslutningsinställning** för att ominstallera basintegreringslösningen. I det här steget distribueras säkerhetsrollen för integrering av Business Central.

<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

### Minimum Permissions for automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user
The following table displays the minimum permissions on each tab for each security role that is required for the automatically created [!INCLUDE[prod_short](includes/prod_short.md)] Integration application user.

##### Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## Se även

[Integrera med Microsoft Dataverse](admin-common-data-service.md)  
[Integrering med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
