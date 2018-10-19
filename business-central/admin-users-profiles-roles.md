---
title: "Hantera användare och roller | Microsoft Docs"
description: "Lär dig hantera användare och rollcenter i Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Förstå användare, profiler och rollcenter

I [!INCLUDE[d365fin](includes/d365fin_md.md)] läggs användare till av en administratör som också ger användare tillgång till områden i [!INCLUDE[d365fin](includes/d365fin_md.md)] som de behöver i sitt arbete.  

Åtkomst till funktioner styrs genom *användargrupper* och *profiler*. Som administratör kan du tilldela och ändra profiler i [!INCLUDE[d365fin](includes/d365fin_md.md)]-prenumeration och du kan lägga till och ta bort användare som en del av din användargrupp.  

## <a name="adding-users"></a>Lägga till användare

Om du vill lägga till användare i [!INCLUDE[d365fin](includes/d365fin_md.md)] online, måste företagets Office 365-administratör först skapa användare i Office 365 Admin Center. Mer information finns i [Lägg till användare till Office 365 för företag](https://aka.ms/CreateOffice365Users)

Administratören kan sedan tilldela behörigheter till varje användare och användargrupper. Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).  

### <a name="users-of-on-premises-deployments"></a>Användare av lokala distributioner

Vid lokal distribution av [!INCLUDE[d365fin](includes/d365fin_md.md)], kan administratören välja mellan olika autentiseringsmetoder för användare. När du sedan skapar en användare, tillhandahåller du olika information beroende på vilken autentiseringstyp du använder i den specifika [!INCLUDE[server](includes/server.md)]-instansen. Mer information finns på [autentisering och autentisering](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i avsnittet Administration av utvecklare och ITPro-innehåll för [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profiler

Personer i företaget som har tillgång till [!INCLUDE[d365fin](includes/d365fin_md.md)] är tilldelade en *profil* som ger åtkomst till ett *Rollcenter*.

Profiler är samlingar av [!INCLUDE[d365fin](includes/d365fin_md.md)]-användare som delar samma Rollcenter. Ett rollcenter är startpunkten och startsidan för [!INCLUDE[d365fin](includes/d365fin_md.md)] som ger dig snabb åtkomst till dina viktigaste uppgifter och visar olika kunskap och nyckeltal (KPI) om ändringarna.  

> [!NOTE]  
>  I den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan du inte lägga till, redigera eller ta bort profiler.  

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

