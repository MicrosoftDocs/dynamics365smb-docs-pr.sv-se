---
title: Anslut till Dynamics 365 Sales | Microsoft Docs
description: Du kan integrera andra appar med Business Central via Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196645"
---
# <a name="connect-to-common-data-service"></a>Anslut till Common Data Service
I det här avsnittet beskrivs hur du upprättar en anslutning mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)]. Vanligtvis skapar företag anslutningen för att integrera och synkronisera data med en annan Dynamics 365-affärsapp, till exempel [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Innan du börjar
Det finns lite information du bör ha tillhanda innan du skapar anslutningen:  

* Webbadressen (URL) till den [!INCLUDE[d365fin](includes/cds_long_md.md)]-miljö du vill ansluta till. Om du använder den assisterade konfigurationsguiden **Inställningar för CDS-anslutning** för att skapa anslutningen kommer vi att upptäcka dina miljöer, men du kan också ange URL:en till en annan miljö i din klientorganisation.  
* Användarnamn och lösenord för ett användarkonto används endast för integrering. Detta kontot kallas "integreringsanvändar"-kontot. 
* Användarnamn och lösenord för ett konto som har administratörsbehörigheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] och [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Här beskrivs proceduren för onlineversionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Ställ in en anslutning till [!INCLUDE[d365fin](includes/cds_long_md.md)].  
För alla autentiseringstyper förutom Office 365-autentisering kan du ställa in anslutningen till [!INCLUDE[d365fin](includes/cds_long_md.md)] på sidan **Inställningar för CDS-anslutning**. För Office 365-autentisering rekommenderar vi att du använder den assisterade konfigurationsguiden **Inställningar för CDS-anslutning**. Guiden gör det enklare att konfigurera anslutningen och specificera avancerade funktioner, till exempel att koppla mellan transaktioner.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>Så här använder du den assisterade konfigurationsguiden Inställningar för CDS-anslutning 
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Assisterad konfiguration** och välj sedan relaterad länk.
2. Välj **Ställ in Inställningar för CDS-anslutning** för att starta guiden för assisterad konfiguration.
3. Fyll i fälten om det behövs.

> [!Note]
> Den assisterade konfigurationsguiden **Inställningar för CDS-anslutning** tilldelar automatiskt säkerhetsrollerna **Integreringsadministratör** och **Integreringsanvändare** till det användarkonto som används för integrering, samt anger åtkomstläget för till **icke-interaktivt**.

### <a name="to-create-or-maintain-the-connection-manually"></a>Om du vill skapa eller hantera anslutningen manuellt
I följande procedur beskrivs hur du konfigurerar anslutningen manuellt på sidan **Inställningar för CDS-anslutning**. Detta är sidan där du hanterar inställningar för integrering.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för CDS-anslutning** och välj sedan tillhörande länk.
2. Ange följande information om anslutningen från [!INCLUDE[d365fin](includes/d365fin_md.md)] till [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Fält|Beskrivning|
|-----|-----|
|**Miljö-URL**|Om du äger miljöerna i [!INCLUDE[d365fin](includes/cds_long_md.md)] kommer vi att upptäcka dem när du kör installationsguiden. Om du vill ansluta till en annan miljö i en annan klientorganisation, kan du ange administratörsbehörighet för miljön så att vi upptäcker dem. |
|**Användarnamn** och **lösenord**|Autentiseringsuppgifterna för användarkontot är avsedd för integrering. Mer information finns i [ställa in konton för att integrera med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Aktiv**|Starta använda integreringen Om du inte aktiverar anslutningen nu sparas anslutningsinställningarna, men användarna kan inte få åtkomst till data i [!INCLUDE[d365fin](includes/cds_long_md.md)] från [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan gå tillbaka till sidan och aktivera anslutningen senare.  |

3. I fältet **Ägarskapsmodlel** väljer du om du vill att en gruppenhet i [!INCLUDE[d365fin](includes/cds_long_md.md)] ska äga nya transaktioner, eller om en eller flera specifika användare ska göra det. Om du väljer **Person** måste du ange varje enskild användare. Om du väljer **Team** visas den förvalda affärsenheten "BCI Company" i fältet **Kopplad affärsenhet**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Kontrollera anslutningsinställningarna genom att välja **Anslutning** och sedan **Testa anslutning**.  

    > [!NOTE]  
    >  Om datakrypteringen inte har aktiverats i [!INCLUDE[d365fin](includes/d365fin_md.md)] kommer du att tillfrågas om du vill aktivera den. Välj **Ja** och ange den obligatoriska informationen om du vill aktivera datakryptering. Annars väljer du **Nej**. Du kan aktivera datakryptering senare. Mer information finns i [kryptering av data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) i Hjälp för utvecklare och IT-proffs.  

5. Om [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkroniseringen inte redan har ställts in får en fråga om du vill använda standardsynkroniseringskonfigurationen. Beroende på om du vill bokföra poster justerade i [!INCLUDE[d365fin](includes/cds_long_md.md)] och [!INCLUDE[d365fin](includes/d365fin_md.md)], välj **Ja** eller **Nej**.

> [!Note]
> Anslutning till [!INCLUDE[d365fin](includes/cds_long_md.md)] via sidan **Inställningar för CDS-anslutning** kan kräva att du tilldelar säkerhetsrollerna Integreringsadministratör och Integreringsanvändare till det konto som används för integrering i Dynamics 365 Sales. Mer information finns i [tilldela en säkerhetsroll till en användare](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>Koppla bort från [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för CDS-anslutning** och välj sedan tillhörande länk.
2. På sidan **Inställnignar för CDS-anslutning** stänger du av brytaren **Aktiverad**.  

## <a name="see-also"></a>Se även  
[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  
