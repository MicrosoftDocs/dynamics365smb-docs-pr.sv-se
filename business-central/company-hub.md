---
title: Hantera arbete i flera företag med företagsnavet
description: Lär dig mer om företagsnavet i Dynamics 365 Business Central som du använder för att hantera ditt arbete över flera företag.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '1151, 1154, 1165, 1166'
ms.date: 04/01/2021
ms.author: edupont
---

# <a name="manage-work-across-multiple-companies-in-the-company-hub"></a><a name="manage-work-across-multiple-companies-in-the-company-hub"></a><a name="manage-work-across-multiple-companies-in-the-company-hub"></a>Hantera arbete i flera företag med företagsnavet

Vissa människor arbetar i flera företag i [!INCLUDE [prod_short](includes/prod_short.md)], medan andra också arbetar i mer än en organisation, till exempel externa revisorer, anställda och chefer hos företag med flera dotterbolag. För dessa användare och många andra, fungerar företagsnavet som en landningssida som ger en ekonomisk översikt över företag och miljöer. Det förser användarna med ett verktyg för att hantera arbete i olika miljöer som de arbetar inom, mellan företag, miljöer och regioner.  

Du kan komma åt företagsnavet genom att växla till rollen **Företagsnav** i Mina inställningar, eller genom att öppna sidan **Företagsnav** direkt. Du kan göra samma sak på båda ställena, men åtgärder placeras något annorlunda på menyerna.  

[![Visar företagsnavsidan som innehåller en lista över alla företag.](media/company-hub.png)](media/company-hub.png#lightbox)  

> [!NOTE]
> Du kan ansluta företagets nav till så många företag som behövs. Du kan emellertid bara ansluta företagsnavet till företag som finns i [!INCLUDE [prod_short](includes/prod_short.md)] online.

## <a name="company-hub-home-page"></a><a name="company-hub-home-page"></a><a name="company-hub-home-page"></a>Företagetsnavets hemsida

Om du använder rollen **Företagsnav** visas en lista på din hemsida över företag som du har tillgång till, bland annat information om KPI-data (nyckeltal) och länkar för att öppna respektive företag. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Välj åtgärden **Företagsnav** för att öppna företagsnavet, där du kan arbeta mer tätt med varje företag.  

> [!TIP]
> Om du vill komma åt ett visst företag i [!INCLUDE [prod_short](includes/prod_short.md)] väljer du namnet på företaget eller väljer menyobjektet **Gå till företag**. Du loggas in automatiskt på en ny flik i webbläsaren.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Åtgärder för ett företag som anges i företagsnavet.":::

Du kan lägga till nya företag, till exempel när du skaffar en ny kund eller när företaget lägger till ett nytt dotterbolag. Mer information finns i avsnittet [Lägga till företag i företagsnavet](company-hub-add-company.md).  

> [!TIP]
> För att du ska kunna uppdatera informationen i företagsnavet måste du ha tillgång till data i de företag som data kommer från.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## <a name="assigned-tasks"></a><a name="assigned-tasks"></a><a name="assigned-tasks"></a>Tilldelade uppgifter

I [!INCLUDE [prod_short](includes/prod_short.md)] kan du tilldela uppgifter till dig själv och andra och andra kan tilldela uppgifter till dig. Företagsnavet ger dig en översikt över tilldelade uppgifter för varje företag och du öppnar en lista med alla tilldelade uppgifter genom att välja **Mina användaruppgifter** på sidan **Start**.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### <a name="my-user-tasks"></a><a name="my-user-tasks"></a><a name="my-user-tasks"></a>Mina användaruppgifter

Listan **Mina användaruppgifter** hjälper dig att prioritera din arbetsdag genom att visa mer information om uppgifter som har tilldelats på alla företag.  

Du kan sortera efter förfallodatum, till exempel eller någon annan typ av data som hjälper dig att prioritera din dag. I listan visas alla uppgifter som har tilldelats dig som standard, men du kan ställa in filter för att endast visa uppgifter som är markerade med hög prioritet, till exempel.  

Om du vill välja en uppgift, väljer du den bara från listan över väntande användaruppgifter. I menyfliken öppnar länken **Gå till uppgiftsobjekt** sidan där du kan utföra arbetet.  

När du har slutfört en uppgift bara markerar du den som slutförd.  

Mer information om företag och miljöer finns i avsnittet om [Miljölänkar](company-hub-add-company.md#environment-links).  

## <a name="access-the-company-hub"></a><a name="access-the-company-hub"></a><a name="access-the-company-hub"></a>Komma åt företagsnavet

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

För att få tillgång till företagsnavet måste du ha åtkomst via antingen användargruppen *D365 FÖRETAGSNAV* eller genom behörighetsuppsättningen *D365 FÖRETAGSNAV*. Du måste också ha åtkomst till de företag som finns i företagsnavet, vilket innebär att du måste vara användare i dessa företag. Mer information finns i [Skapa användare enligt licenser](ui-how-users-permissions.md).  

> [!IMPORTANT]
> Företagsnavet är en lista över hela företaget, så alla användare som beviljats åtkomst till företagsnavet kan se alla företag i sin egen [!INCLUDE [prod_short](includes/prod_short.md)]-klientorganisation och alla KPI:er för de företag som de har tillgång till.

Om du inte hittar företagsnavet och du vet att du har beviljats åtkomst till det, kan du kontakta administratören om företagsnavet finns med på sidan **Tilläggshantering**. Mer information finns i [Anpassa Business Central med hjälp av tillägg](ui-extensions.md).  

## <a name="set-up-the-company-hub"></a><a name="set-up-the-company-hub"></a><a name="set-up-the-company-hub"></a>Ställa in företagsnavet

Om du vill börja använda företagsnavet måste du lägga till ett eller flera företag på instrumentpanelen. Mer information finns i avsnittet [Lägga till företag i företagsnavet](company-hub-add-company.md).  

Men om du vill lägga till ett företag måste du ha åtkomst till en eller flera instanser av [!INCLUDE [prod_short](includes/prod_short.md)] utöver det företag som du använder för företagsnavet.  

Om du till exempel är en revisor kan klienterna bjuda in dig till deras [!INCLUDE [prod_short](includes/prod_short.md)]. Mer information finns i [Bjud in din externa revisor till din Business Central](finance-accounting.md#inviteaccountant).  

Administratörer kan använda samma guide för assisterad konfiguration för att lägga till dig till deras [!INCLUDE [prod_short](includes/prod_short.md)], eller så kan de lägga till dig på det aktuella Azure AD-kontot i administratörscentret för Microsoft 365. Mer information finns i [Hantera användare och grupper](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Lägg till företag till företagsnavet](company-hub-add-company.md)  
[Revisorlösningar i Business Central](finance-accounting.md)  
[Företagsnavet för Business Central-tillägget](ui-extensions-company-hub.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
