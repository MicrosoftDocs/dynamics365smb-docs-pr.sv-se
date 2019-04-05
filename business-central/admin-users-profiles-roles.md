---
title: Hantera användare och roller | Microsoft Docs
description: Lär dig hantera användare och rollcenter i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/24/2018
ms.author: edupont
ms.openlocfilehash: 7ecd8a5ad2b321d4d1683047e70ede90c7ce229f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807890"
---
# <a name="understanding-users-profiles-and-role-centers"></a>Förstå användare, profiler och rollcenter

I [!INCLUDE[d365fin](includes/d365fin_md.md)] läggs användare till av en administratör som också ger användare tillgång till områden i [!INCLUDE[d365fin](includes/d365fin_md.md)] som de behöver i sitt arbete.  

Åtkomst till funktioner styrs genom *användargrupper* och *profiler*. Som administratör kan du tilldela och ändra profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)]-prenumeration och du kan lägga till och ta bort användare som en del av din användargrupp.  

## <a name="adding-users"></a>Lägga till användare

Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] online, måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center. Mer information finns i [Lägg till användare till Office 365 för företag](https://aka.ms/CreateOffice365Users)

Administratören kan sedan tilldela behörigheter till varje användare och användargrupper. Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).  

De mest kraftfulla behörigheter som en användare kan ha är behörighetsuppsättningen SUPER. Varje företag måste ha minst en användare med denna behörighet, men det är bäst att ge behörighet till alla användare som matchar arbetsbehoven i [!INCLUDE[prodshort](includes/prodshort.md)] och inte mer än så. Detta säkerställer att användare endast har tillgång till data som är relevanta för arbetet, t.ex.  

> [!TIP]
> Det är bäst att kontrollera att Office 365 administratören också har behörighetsuppsättningen SUPER [!INCLUDE[prodshort](includes/prodshort.md)]eftersom det underlättar många administrativa uppgifter, inklusive inställning av integrering med andra program.

### <a name="users-of-on-premises-deployments"></a>Användare av lokala distributioner

Vid lokal distribution av [!INCLUDE[d365fin](includes/d365fin_md.md)], kan administratören välja mellan olika autentiseringsmetoder för användare. När du sedan skapar en användare, tillhandahåller du olika information beroende på vilken autentiseringstyp du använder i den specifika [!INCLUDE[server](includes/server.md)]-instansen. Mer information finns på [autentisering och autentisering](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i avsnittet Administration av utvecklare och ITPro-innehåll för [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profiler

Personer i företaget som har tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)] är tilldelade en *profil* som ger åtkomst till ett *Rollcenter*.

Profiler är samlingar av [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som delar samma Rollcenter. Ett rollcenter är startpunkten och startsidan för [!INCLUDE[d365fin](includes/d365fin_md.md)] som ger dig snabb åtkomst till dina viktigaste uppgifter och visar olika kunskap och nyckeltal (KPI) om ändringarna.  

> [!NOTE]  
>  I den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan du inte lägga till, redigera eller ta bort profiler.  

### <a name="CreateProfile"></a>Skapa en profil

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Profillista** och välj sedan relaterad länk.  

2.  På sidan **Profillista** väljer du åtgärden **Ny** för att öppna sidan **Nytt profilkort**.  

3.  I fältet **Profil-ID**, ange ett namn som beskriver den påtänkta rollen för användaren.  

4.  I fältet **Beskrivning** anger du en beskrivning av profil-ID:t, t.ex. **Orderhandläggare**.  

5.  Ange fältet **Rollcenter-ID** till det rollcentret som du vill tilldela profilen.  

Proceduren som används för att ändra en befintlig profil är samma, förutom att du väljer en befintlig profil på sidan **Profillista** i stället för att välja åtgärden **Ny**.  


### <a name="copy-a-profile"></a>Kopiera en profil
Kopiera en profil kan spara tid, om du vill använda liknande inställningar på en profil, och du endast vill ändra några få inställningar.

1.  Öppna den profil som du vill kopiera och välj sedan åtgärden **Kopiera profil**.

2.  Skriv namnet på profilen som du vill kopiera i fältet **Nytt profil-ID**.

3.  Ange fältet **Ny profilomfattning** till något av följande:

    - **Systemet** så att den nya profilen är tillgänglig för alla innehavare av databaser som använder programmet.
    - **Klientorganisation** så att den nya profilen är tillgänglig bara för den aktuella klientorganisationens databas.
4. Välj knappen **OK** när du är klar.

### <a name="ExportImportProfile"></a>Exportera och importera profiler

Du kan exportera och importera profiler som XML-filer till och från en [!INCLUDE[d365fin](includes/d365fin_md.md)]-databas. Exportera och importera en profil låter dig spara tid när du konfigurerar användargränssnittet eftersom du kan återanvända en befintlig profilkonfiguration i stället för att konfigurera en profil från början. Om du har en profil som är konfigurerad i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-databas och du vill återanvända hela eller delar av samma profilkonfigurationer i en annan databas, kan du exportera profiler till en XML-fil. Du kan sedan importera XML-filen för profilen i den andra databasen.

-   Om du vill exportera en profil, kan du antingen välja åtgärden **Exportera profiler** från sidan **Profillista** eller **Profilkort** eller söka efter och öppna sidan **Exportera profiler**. Spara XML-filen till en plats på datorn eller i nätverket.

-   Om du vill importera en profil, kan du antingen välja åtgärden **Importera profil** från sidan **Profillista** eller söka efter och öppna sidan **Importera profiler**. 

    > [!NOTE]  
    >  Du kan inte importera en profil som redan finns i databasen, även om XML-filen har ett annat namn eller annat innehåll. Du måste ta bort den befintliga profilen innan du kan importera den nya profilen.


## <a name="configuration-and-personalization"></a>Konfiguration och anpassning
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

Användare anpassa användargränssnittet för sin egen version genom att anpassa användargränssnittet under sin egen användarinloggning. Den här anpassningen kan tas bort av administratören. Mer information finns i [Anpassa arbetsytan](ui-personalization-user.md).  

## <a name="see-also"></a>Se även  
[Hantera användare och behörigheter](ui-how-users-permissions.md)  
[Hantera anpassning som administratör](ui-personalization-manage.md)  
[Anpassa din arbetsyta](ui-personalization-user.md)  
