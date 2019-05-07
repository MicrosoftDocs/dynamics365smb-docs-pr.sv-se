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
ms.openlocfilehash: c318346c62b7776a550a77a2947173e33d5f17c0
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2019
ms.locfileid: "940380"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Ställa in konton för integrering med Dynamics 365 for Sales
Den här artikeln innehåller en översikt över hur du ställer in de konton som behövs för att integrera [!INCLUDE[crm_md](includes/crm_md.md)] med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Ställa in Administratörsanvändarkontot i Försäljning
Du måste lägga till ditt administratörsanvändarkonto för [!INCLUDE[d365fin](includes/d365fin_md.md)] som en användare i [!INCLUDE[crm_md](includes/crm_md.md)] och sedan befordra användaren till administratör i [!INCLUDE[crm_md](includes/crm_md.md)]. Administratörsanvändarkontot måste också ha rollen systemanpassare och minst en annan användarroll som inte är administratör, till exempel försäljningschef, i [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Konfigurera användarkontot för integrering
Du måste skapa ett dedikerat användarkonto i din Office 365-prenumeration som både [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)] kan använda för att synkronisera data. Det här användarkontot måste kunna logga in på [!INCLUDE[crm_md](includes/crm_md.md)], vilket innebär att användaren måste ha en licens för [!INCLUDE[crm_md](includes/crm_md.md)]. Det här kontot måste också vara ett icke-interaktivt konto i [!INCLUDE[crm_md](includes/crm_md.md)]. För information om hur du skapar användare i [!INCLUDE[crm_md](includes/crm_md.md)], se [Hantera säkerhet, användare och team](http://go.microsoft.com/fwlink/?LinkID=616518). När anslutningen har konfigurerats kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] att tilldela säkerhetsroller till användarkontot som krävs i [!INCLUDE[d365fin](includes/d365fin_md.md)].

![Assisterad installationsguide visar var du kan ange autentiseringsuppgifter för synkronisering](media/sync-user-setup.png "Sidan för assisterade konfiguration för visualisering visar var du ska skriva autentiseringsuppgifter för synkronisering")

> [!IMPORTANT]  
> Använd inte administratörskontot för [!INCLUDE[crm_md](includes/crm_md.md)] för synkronisering. Om du gör det bryts synkroniseringen.
> Dessutom, för att undvika konstant synkronisering synkroniseras inte ändringar av integreringsanvändarkontot. <!--What changes would this account make?--> När anslutningen har upprättats bör du ange åtkomstläget för användarkontot för integration i icke-interaktivt läge i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [skapa ett icke-interaktivt användarkonto](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Ställa in konton för säljare
Du måste skapa användarkonton i [!INCLUDE[crm_md](includes/crm_md.md)] för säljare från [!INCLUDE[d365fin](includes/d365fin_md.md)]. För att göra detta enklare erbjuder Microsoft 365 administratörscenter en Excel-mall som du kan använda. På sidan **aktiva användare** väljer du **Mer** och sedan **Importera flera användare**. Välj **Hämta en CSV-fil med endast rubriker** och ange sedan ange information om säljarna. För att se ett exempel väljer du **Hämta en CSV-fil med rubriker och exempelanvändarinformation**. När du har angett information om användarna är nästa steg i importprocessen att tilldela användarlicenser till Dynamics 365 Customer Engagement-planen.  

När du har importerat användarna och tilldelat dem licenser för Dynamics 365 Customer Engagement måste du tilldela användare till rollen **säljare** i [!INCLUDE[crm_md](includes/crm_md.md)].

![Koppla säljare till användare i Dynamics 365 for Sales](media/couple-salespeople.png "visualisering av kopplingen av säljare för användare i Dynamics 365 for Sales")

## <a name="see-also"></a>Se även  
[Integrera med Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
