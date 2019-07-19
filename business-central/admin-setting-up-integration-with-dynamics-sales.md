---
title: Ställa in konton för integrering med Dynamics 365 for Sales | Microsoft Docs
description: Lär dig hur du konfigurerar användarkonton med program som utbyter data och som människor använder för att få tillgång till och synkronisera data i program.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0f59324e41695e35e09a2dd970492acb3a8dba58
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726888"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Ställa in konton för integrering med Dynamics 365 for Sales
Den här artikeln innehåller en översikt över hur du ställer in de konton som behövs för att integrera [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Ställa in Administratörsanvändarkontot i Försäljning
Du måste lägga till ditt administratörsanvändarkonto för [!INCLUDE[d365fin](includes/d365fin_md.md)] som en användare i [!INCLUDE[crm_md](includes/crm_md.md)] och sedan befordra användaren till administratör i [!INCLUDE[crm_md](includes/crm_md.md)]. Administratörsanvändarkontot måste också ha rollen systemanpassare och minst en annan användarroll som inte är administratör, till exempel försäljningschef, i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Konfigurera användarkontot för integrering
Du måste skapa ett dedikerat användarkonto i din Office 365-prenumeration som både [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] kan använda för att synkronisera data. Det här användarkontot måste kunna logga in på [!INCLUDE[crm_md](includes/crm_md.md)], vilket innebär att användaren måste ha en licens för [!INCLUDE[crm_md](includes/crm_md.md)] och minst en säkerhets rollsom har tilldelats den i [!INCLUDE[crm_md](includes/crm_md.md)] som beskrivs [här](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). För information om hur du skapar användare i [!INCLUDE[crm_md](includes/crm_md.md)], se [Hantera säkerhet, användare och team](http://go.microsoft.com/fwlink/?LinkID=616518). bNär anslutningen är upprättad kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] tilldelar du användarkontot de säkerhetsroller som behövs i [!INCLUDE[d365fin](includes/d365fin_md.md)] och det här kontot kan anges till [icke-interaktivt åtkomstläge](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account)[!INCLUDE[crm_md](includes/crm_md.md)]

![Assisterad installationsguide visar var du kan ange autentiseringsuppgifter för synkronisering](media/sync-user-setup.png "Sidan för assisterade konfiguration för visualisering visar var du ska skriva autentiseringsuppgifter för synkronisering")

> [!IMPORTANT]  
> Använd inte administratörskontot för [!INCLUDE[crm_md](includes/crm_md.md)] för synkronisering. Om du gör det bryts synkroniseringen.
> Dessutom, för att undvika konstant synkronisering synkroniseras inte ändringar av integreringsanvändarkontot. <!--What changes would this account make?--> När anslutningen har upprättats bör du ange åtkomstläget för användarkontot för integration i icke-interaktivt läge i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [skapa ett icke-interaktivt användarkonto](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Ställa in konton för säljare
Du måste skapa användarkonton i [!INCLUDE[crm_md](includes/crm_md.md)] för säljare från [!INCLUDE[d365fin](includes/d365fin_md.md)]. För att göra detta enklare erbjuder Microsoft 365 administratörscenter en Excel-mall som du kan använda. På sidan **aktiva användare** väljer du **Mer** och sedan **Importera flera användare**. Välj **Hämta en CSV-fil med endast rubriker** och ange sedan ange information om säljarna. För att se ett exempel väljer du **Hämta en CSV-fil med rubriker och exempelanvändarinformation**. När du har angett information om användarna är nästa steg i importprocessen att tilldela användarlicenser till Dynamics 365 Customer Engagement-planen.  

När du har importerat användarna och tilldelat dem licenser för Dynamics 365 Customer Engagement måste du tilldela användare till rollen **säljare** i [!INCLUDE[crm_md](includes/crm_md.md)].

![Koppla säljare till användare i Dynamics 365 for Sales](media/couple-salespeople.png "visualisering av kopplingen av säljare för användare i Dynamics 365 for Sales")

## <a name="minimum-permissions-for-user-accounts-in-includecrmmdincludescrmmdmd"></a>Lägsta behörigheten för användar konton i [!INCLUDE[crm_md](includes/crm_md.md)]
När du installerar integrationslösningen konfigureras behörigheter för användarkontot för integration i [!INCLUDE[crm_md](includes/crm_md.md)]. Om behörigheterna ändras kan du behöva återställa dem. Det kan du göra genom att installera om integreringslösningen eller återställa dem manuellt. I följande tabeller visas minimibehörigheterna för användar kontona i [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="integration-administrator"></a>Integrationsadministratör
I följande tabell visas de minsta behörigheterna på varje flik för varje säkerhetsroll som krävs för administratöranvändaren.

##### <a name="customization"></a>Anpassning
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Modelldriven app|Global|||Läs|
|Plugin-paket|Global|Läs|Läs|Läs|
|Plugin-typ|Global|Läs|Läs|Läs|
|Samband|Global|||Läs|
|SDK-meddelande|Global|Läs|Läs|Läs|
|SDK-meddelande bearbetningssteg|Global|Läs|Läs|Läs|
|SDK-meddelande bearbetningsbild|Global|Läs|Läs|Läs|
|System från|Global|||Skriv|

##### <a name="custom-entities"></a>Anpassade entiteter
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Statistik för Business Central-konto|Global|Läs|Läs|Läs|
|Anslutning för Business Central|Global|Skapa, läsa, skriva, ta bort|Skapa, läsa, skriva, ta bort|Skapa, läsa, skriva, ta bort|
|Efter konfiguration|Global|||Skriv|

#### <a name="integration-user"></a>Integrationsanvändare
I följande tabell visas de minsta behörigheterna på varje flik för varje säkerhetsroll som krävs för integrationsanvändaren.

##### <a name="core-records"></a>Kärnposter
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Konto|Global|Skapa, läsa, skriva, lägga till, lägga till i, tilldela|Skapa, läsa, skriva, lägga till, lägga till i, tilldela|Skapa, läsa, skriva, lägga till, lägga till i, tilldela|
|Åtgärdskort|Global||Läs|Läs|
|Anslutning|Global|Läs|Läs|Läs|
|Kontakt|Global|Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|
|Anmärkning|Global|||Skapa, läsa, skriva, ta bort lägga till, tilldela|
|Affärsmöjlighet|Global||Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|
|Post|Global|||Skapa, läsa, lägga till i|
|Användargränssnitt för entitet|Användare|Skapa, läsa, skriva|Skapa, läsa, skriva|Skapa, läsa, skriva|

##### <a name="sales"></a>FÖRS
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Fakturera|Global|Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|
|Order|Global|Skapa, skriva, lägga till i|Skapa, skriva, lägga till i|Läsa, skriva, lägga till, lägga till i, tilldela|
|Produkt|Global|Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|
|Egenskap|Global|Läs|Läs|Läs|
|Egenskapskoppling|Global|Läs|Läs|Läs|
|Egenskapsalternativ ange objekt|Global|Läs|Läs|Läs|
|Offert|Global|Läs|Läs|Läs|

##### <a name="service"></a>Service
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Ärende|Global|Läs|Läs|Läs|

##### <a name="business-management"></a>Verksamhetsstyrning
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Valuta|Global|Skapa, läsa, skriva|Skapa, läsa, skriva|Skapa, läsa, skriva|
|Organisation|Global|Läsa, skriva|Läsa, skriva|Läsa, skriva|
|Säkerhetsroll|Global|||Läs|
|Användare|Global|Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|Skapa, läsa, skriva, lägga till, lägga till i|
|Användarinställningar|Global|Skapa, läsa, skriva, ta bort, lägga till i|Skapa, läsa, skriva, ta bort, lägga till i|Skapa, läsa, skriva, ta bort, lägga till i|
|Agera för en annan användares räkning|Global|Ja|Ja|Ja|

##### <a name="customization"></a>Anpassning
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Fält|Global||Läs|Läs|
|Plugin-paket|Global|Läs|Läs|Läs|
|Plugin-typ|Global|Läs|Läs|Läs|
|SDK-meddelande|Global|Läs|Läs|Läs|
|SDK-meddelande bearbetningssteg|Global|Läs|Läs|Läs|
|Webbresurs|Global|Läs|Läs|Läs|

##### <a name="custom-entities"></a>Anpassade entiteter
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central kontostatistik|Global|Skapa, läsa, skriva, lägga till i|Skapa, läsa, skriva, lägga till i|Skapa, läsa, skriva, lägga till i|
|Dynamics 365 Business Central-anslutning|Global|Läs|Läs|Läs|

### <a name="product-availability-user"></a>Produktartikelanvändare
Du kan låta säljare visa lagernivåer för de artiklar som de säljer genom att bevilja dem de behörigheter som beskrivs i följande tabell.

##### <a name="custom-entities"></a>Anpassade entiteter
|Säkerhetsroll|Åtkomstnivå|Dynamics NAV 2018 och tidigare|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central kontostatistik|Global|Skapa, läsa, skriva, lägga till i|Skapa, läsa, skriva, lägga till i|Skapa, läsa, skriva, lägga till i|
|Dynamics 365 Business Central-anslutning|Global|Läs|Läs|Läs|

## <a name="see-also"></a>Se även  
[Integrera med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
