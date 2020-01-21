---
title: Anslut till Dynamics 365 Sales | Microsoft Docs
description: Du kan integrera med Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 73607d238e31cc42680fae008cfdf0ee143d08f3
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910742"
---
# <a name="set-up-a-connection-to-dynamics-365-sales"></a>Konfigurera en anslutning till Dynamics 365 Sales
I det här avsnittet beskrivs hur du upprättar en anslutning mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[crm_md](includes/crm_md.md)].
<br><br>  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Innan du börjar
Innan du skapar anslutningen finns det lite information du bör ha tillhanda:  

* En URL för din [!INCLUDE[crm_md](includes/crm_md.md)]-app. Ett snabbt sätt att hämta URL:en är att öppna [!INCLUDE[crm_md](includes/crm_md.md)], kopiera URL-adressen och klistra in den i fältet **Dynamics 365 Sales-URL** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] korrigerar layouten.  
* Användarnamn och lösenord för ett användarkonto används endast för integrering.  
* Användarnamn och lösenord för det konto som har administratörsbehörigheter.  

> [!Note]
> Här beskrivs proceduren för onlineversionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrm_mdincludescrm_mdmd"></a>Ställ in, testa och aktivera en anslutning till [!INCLUDE[crm_md](includes/crm_md.md)]  
För alla autentiseringstyper förutom Office 365-autentisering kan du ställa in anslutningen till Dynamics 365 Sales på sidan **Microsoft Dynamics 365 Sales anslutningsinställningar**. För Office 365-autentisering kan du också använda assisterad inställningsguide för **Ställ in Dynamics 365 Sales-anslutning** som hjälper dig att hitta informationen som krävs.

### <a name="to-use-an-assisted-setup-guide"></a>Så här använder du guiden för assisterad konfiguration:
Guiden för assisterad konfiguration **Ställ in Dynamics 365 Sales-anslutning** kan hjälpa dig att skapa anslutningen och ange om du vill aktivera avancerade funktioner, till exempel koppla mellan poster.

1. Välj **inställningar och tillägg**, och välj **assisterad konfiguration**.
2. Välj **Ställ in Dynamics 365 Sales-anslutning** för att starta guiden för assisterad konfiguration.
3. Fyll i fälten om det behövs.
4. Om det finns avancerade inställningar som kan förbättra säkerheten och aktivera [!INCLUDE[crm_md](includes/crm_md.md)] ytterligare funktioner, till exempel behandling av försäljningsorder och visa lagernivåer. Avancerade inställningarna beskrivs i tabellen nedan.  

|Fält|Beskrivning|
|-----|-----|
|**Importera Dynamics 365 Sales-lösning**|Aktivera det här alternativet om du vill installera och konfigurera lösningen för integration i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [om Business Central integrationslösning](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Publicera webbtjänsten för artikeldisposition**|Aktivera människor som använder [!INCLUDE[crm_md](includes/crm_md.md)] för att visa disponibla artiklar (produkter) i lagret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Detta kräver att [!INCLUDE[d365fin](includes/d365fin_md.md)] användarkontot har en åtkomstnyckel för webbtjänsterna. Tilldela nyckeln är en tvåstegsprocess. För användarkontot i [!INCLUDE[d365fin](includes/d365fin_md.md)] måste du välja åtgärden **ändra webbtjänstnyckeln**. I guiden för assisterad konfiguration Dynamics 365 Sales-anslutning anger du Dynamics 365 Business Central OData webbtjänst-URL och ger [!INCLUDE[d365fin](includes/d365fin_md.md)] användarens autentiseringsuppgifter för att komma åt tjänsten. Mer information finns i [OData webbtjänst](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Dynamics 365 Business Central OData webbtjänst-URL**|Om du aktiverar webbtjänsten för artikeldisposition anges URL för OData webbadressen för dig.|
|**Dynamics 365 Business Central Användarnamn för OData-webbtjänsten**|Namnet på det [!INCLUDE[d365fin](includes/d365fin_md.md)] användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition i [!INCLUDE[d365fin](includes/d365fin_md.md)] via webbtjänsten för OData.|
|**Dynamics 365 Business Central Åtkomstnyckel för OData-webbtjänsten**|Åtkomstnyckeln för det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition från [!INCLUDE[d365fin](includes/d365fin_md.md)] via webbtjänsten för OData. Nyckeln tilldelas användaren i fältet **Dynamics 365 Business Central Användarnamn för OData-webbtjänsten**. Om du vill hämta nyckeln väljer du knappen **sök efter värdet** bredvid användarnamnet, väljer användaren, väljer **hantera** och sedan **redigera**. På användarkortet väljer du **åtgärder**, **autentisering** och väljer sedan **ändra webbtjänstnyckeln**.|
|**Aktivera försäljningsorderintegrering**|När en användare skapar försäljningsorder i [!INCLUDE[crm_md](includes/crm_md.md)] och uppfyller order i [!INCLUDE[d365fin](includes/d365fin_md.md)] integreras processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Detta innebär att du anger autentiseringsuppgifter för en administratörs användarkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i avsnittet [Hantera speciella försäljningsorderdata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Aktivera Dynamics 365 for Sales anslutning**|Aktivera anslutning till [!INCLUDE[crm_md](includes/crm_md.md)].|
|**SDK-version för Dynamics 365**|Detta gäller endast om du integrerar med en lokal version av [!INCLUDE[crm_md](includes/crm_md.md)]. Det här är den SDK-version för Dynamics 365 (även kallat Xrm) för att ansluta [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]. Versionen måste vara kompatibel med SDK-versionen som används av [!INCLUDE[crm_md](includes/crm_md.md)] och motsvarande eller senare än den version som används av [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Den assisterade inställningsguiden **Ställ in Dynamics 365 Sales-anslutning** tilldelar automatiskt säkerhetsrollerna **Integrationsadministratör** och **Integrationsanvändare** till användarkonton som används för integration.

### <a name="to-create-or-maintain-the-connection-manually"></a>Om du vill skapa eller hantera anslutningen manuellt
I följande procedur beskrivs hur du fyller i fälten på sidan **Microsoft Dynamics 365 Sales anslutningsinställningar** manuellt. Detta är sidan där du hanterar inställningar för integrering.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Microsoft Dynamics 365 anslutningsinställningar** och välj sedan relaterad länk.
2. Ange följande information om anslutningen från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)].

|Fält|Beskrivning|
|-----|-----|
|**Dynamics 365 Sales-URL**|URL:en för din instans av [!INCLUDE[crm_md](includes/crm_md.md)]. Om du vill hämta URL-adressen, öppna [!INCLUDE[crm_md](includes/crm_md.md)], kopiera URL från adressfältet i din webbläsare och klistra sedan in URL-adressen i fältet. [!INCLUDE[d365fin](includes/d365fin_md.md)] ser till att formatet är korrekt.|
|**Användarnamn** och **lösenord**|Autentiseringsuppgifterna för användarkontot är avsedd för integrering. Mer information finns i [Ställa in konton för att integrera med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Aktiv**|Starta använda integrationen Om du inte aktiverar anslutningen nu sparas anslutningsinställningarna, men användarna kan inte få åtkomst till data i [!INCLUDE[crm_md](includes/crm_md.md)] från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan gå tillbaka till sidan och aktivera anslutningen senare.  |
|**SDK-version för Dynamics 365**|Om du integrerar med en lokal version av [!INCLUDE[crm_md](includes/crm_md.md)] är det denna SDK-versionen för Dynamics 365 (även kallad Xrm) som du använder för att ansluta [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)]. Den version som du väljer måste vara kompatibel med SDK-versionen som används av [!INCLUDE[crm_md](includes/crm_md.md)]. Den här versionen motsvarar eller är senare än den version som används av [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Om du ansluter en lokal version av [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[crm_md](includes/crm_md.md)] kan du konfigurera en anslutning till en [!INCLUDE[crm_md](includes/crm_md.md)]-instans med en specifik autentiseringsmetod. Fyll i fälten på snabbfliken **information om autentiseringstyp**. Mer information finns i [använd anslutningssträngar i XRM verktygsuppsättning för att ansluta till Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Detta steg är inte nödvändigt när du ansluter en onlineversion av [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Ange följande information om anslutningen från [!INCLUDE[crm_md](includes/crm_md.md)] till [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Fält|Beskrivning|
|-----|-----|
|**Dynamics 365 Business Central Webbklient-URL**|URL:en för din instans av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det låter användare i [!INCLUDE[crm_md](includes/crm_md.md)] öppna motsvarande poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] från poster i [!INCLUDE[crm_md](includes/crm_md.md)], till exempel ett konto eller en produkt. -posterna öppnas i . [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster är öppna i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ange detta fält till url-adressen för den [!INCLUDE[d365fin](includes/d365fin_md.md)]-instans att använda.<br /><br /> Om du vill återställa fältet till standard-URL för [!INCLUDE[d365fin](includes/d365fin_md.md)], på Åtgärd-fliken, välj **Återställ webbklient-URL**.<br /><br /> Detta fält gäller endast om integrationslösningen för [!INCLUDE[d365fin](includes/d365fin_md.md)] har installerats i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Webbtjänsten Artikeldisposition har aktiverats**|Aktivera människor som använder [!INCLUDE[crm_md](includes/crm_md.md)] för att visa disponibla artiklar (produkter) i lagret i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om detta aktiveras måste du också ange ett namn och en snabbtangent för [!INCLUDE[crm_md](includes/crm_md.md)] för att fråga OData-webbtjänsten om disponibla artiklar (produkter). Mer information finns i [OData webbtjänst](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**Dynamics 365 Business Central OData webbtjänst-URL**|Om du aktiverar webbtjänsten för artikeldisposition anges URL för OData webbadressen för dig.|
|**Dynamics 365 Business Central Användarnamn för OData-webbtjänsten**|Namnet på det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition i [!INCLUDE[d365fin](includes/d365fin_md.md)] via webbtjänsten för OData.|
|**Dynamics 365 Business Central Åtkomstnyckel för OData-webbtjänsten**|Åtkomstnyckeln för det användarkonto som [!INCLUDE[crm_md](includes/crm_md.md)] använder för att hämta information om artikeldisposition från [!INCLUDE[d365fin](includes/d365fin_md.md)] via webbtjänsten för OData. Nyckeln tilldelas användaren i fältet **Dynamics 365 Business Central Användarnamn för OData-webbtjänsten**. Om du vill hämta nyckeln väljer du knappen **sök efter värdet** bredvid användarnamnet, väljer användaren, väljer **hantera** och sedan **redigera**. På användarkortet väljer du **åtgärder**, **autentisering** och väljer sedan **ändra webbtjänstnyckeln**.|

4. Ange följande inställningar för [!INCLUDE[crm_md](includes/crm_md.md)].

|Fält|Beskrivning|
|-----|-----|
|**Försäljningsorderintegration är aktiverad**|Användaren ska kunna skicka försäljningsorder och aktiverade offerter i [!INCLUDE[crm_md](includes/crm_md.md)] och sedan granska och bearbeta dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det här integrerar den här processen i [!INCLUDE[crm_md](includes/crm_md.md)]. Mer information finns i [Aktivera integrering av bearbetning av försäljningsorder](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).|
|**Skapa försäljningsorder automatiskt**|Skapa en försäljningsorder i [!INCLUDE[d365fin](includes/d365fin_md.md)] när en användare skapar och skickar en i [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Bearbeta försäljningsofferter automatiskt**|Bearbeta en försäljningsoffert i [!INCLUDE[d365fin](includes/d365fin_md.md)] när en användare skapar och aktiverar en i [!INCLUDE[crm_md](includes/crm_md.md)].|

5. Ange följande avancerade inställningar.

|Fält|Beskrivning|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)]-användare måste mappa till Dynamics 365 Sales-användare**|Ange om [!INCLUDE[d365fin](includes/d365fin_md.md)] konton måste ha matchande användarkonto i [!INCLUDE[crm_md](includes/crm_md.md)]. **Office 365 E-postadress för autentisering** av [!INCLUDE[d365fin](includes/d365fin_md.md)]-användaren måste vara samma som **Primär e-postadress** för [!INCLUDE[crm_md](includes/crm_md.md)]-användaren.<br /><br /> Om du anger värdet till **Ja** kommer [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som inte har något matchande [!INCLUDE[crm_md](includes/crm_md.md)]-användarkonto inte ha [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrationskapaciteter i användargränssnittet. Åtkomst till [!INCLUDE[crm_md](includes/crm_md.md)]-data direkt från [!INCLUDE[d365fin](includes/d365fin_md.md)] utförs på [!INCLUDE[crm_md](includes/crm_md.md)]-användarkontots vägnar.<br /><br /> Om du anger värdet till **Nej** kommer alla [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare ha [!INCLUDE[crm_md](includes/crm_md.md)]--integrationskapaciteter i användargränssnittet. Åtkomst till [!INCLUDE[crm_md](includes/crm_md.md)]-data gör på [!INCLUDE[crm_md](includes/crm_md.md)]-anslutningens (integration) vägnar.|
|**Nuvarande Business Central-användare mappas till en Dynamics 365 Sales-användare**|Anger om kontot har mappats till ett konto i [!INCLUDE[crm_md](includes/crm_md.md)]|

6. Kontrollera anslutningsinställningarna genom att välja **Testa anslutning**.  

    > [!NOTE]  
    >  Om datakrypteringen inte har aktiverats i [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer du att tillfrågas om du vill aktivera den. Välj **Ja** och ange den obligatoriska informationen om du vill aktivera datakryptering. Annars väljer du **Nej**. Du kan aktivera datakryptering senare. Mer information finns i [kryptering av data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i Hjälp för utvecklare och IT-proffs.  

7. Om [!INCLUDE[crm_md](includes/crm_md.md)]-synkroniseringen inte redan har ställts in får en fråga om du vill använda standardsynkroniseringskonfigurationen. Beroende på om du vill bokföra poster justerade i [!INCLUDE[crm_md](includes/crm_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)], välj **Ja** eller **Nej**.

> [!Note]
> Ansluta till Dynamics 365 Sales med sidan **Microsoft Dynamics 365 Sales-anslutningsinställning** kan kräva att du tilldelar säkerhetsrollerna Integrationsadministratör och Integrationsanvändare till användarkonton om används för integration. Mer information finns i [tilldela en säkerhetsroll till en användare](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).


> [!Note]
> Ansluta till Dynamics 365 Sales med **Microsoft Dynamics 365 Sales anslutningsinställningar** kan kräva att du [tilldelar säkerhetsrollerna **Integrationsadministratör** och **Integrationsanvändare**](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user) till användarkonton om används för integration.


### <a name="to-disconnect-from-includecrm_mdincludescrm_mdmd"></a>Koppla bort från [!INCLUDE[crm_md](includes/crm_md.md)]  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Microsoft Dynamics 365 Sales anslutningsinställningar** och välj sedan relaterad länk.
2. På sidan **Microsoft Dynamics 365 Sales anslutningsinställningar**, avmarkera kryssrutan **aktiverad**.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension?


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [https://go.microsoft.com/fwlink/?LinkID=616519](https://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](https://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.-->

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [Set Up a Microsoft Dynamics 365 Sales Connection]() -->

<!--
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Se även  
[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  
