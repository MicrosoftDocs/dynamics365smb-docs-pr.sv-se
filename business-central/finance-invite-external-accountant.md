---
title: Lägga till en extern revisor till Business Central | Microsoft Docs
description: Lär dig hur du kan bjuda in din externa revisor till ditt Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: b6577c183e708b02699161a98197ad60ac1006fd
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "934356"
---
# <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]
Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till dina [!INCLUDE[d365fin](includes/d365fin_md.md)] så att de kan arbeta med dig med räkenskapsårets informationen.

När din revisorn har fått tillgång till din [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de använda rollcenter **revisorn** som ger enkel åtkomst till de mest relevanta sidor för att kunna arbeta.  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]

Vi har gjort det lätt för dig att bjuda in en extern revisor. Öppna bara sidan **Användare** och välj åtgärden **Bjuda in extern revisor** i menyfliksområdet. Ett e-postmeddelande är redo för dig, lägg bara till din revisors e-postadress för arbete och skicka inbjudan.  

![Bjud in din revisor](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Detta kräver att du har installerat SMTP-e-post. Du kan göra det själv eller fråga din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner. Dessutom måste du vara inloggad i [!INCLUDE[d365fin](includes/d365fin_md.md)] som en användaradministratör och inte som ansvarig chef eller andra användare. Slutligen kan ha du lämnat testföretaget så att du får en Azure Active Directory-administratör.  

> [!IMPORTANT]  
> Revisorns e-postadress måste vara en arbetsadress som baseras på ett Azure Active Directory. Om revisorn har en annan typ av e-post kan inte inbjudan skickas.  

### <a name="separate-license"></a>Separera licens
I bakgrunden läggs revisorn till i din Active Directory-innehavare. Administratören kan verifiera att revisorn har accepterat din inbjudan och tilldelas rätt licens. Stegen för att göra detta beror på vilken typ av konto som du använde när du registrerade dig för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det här avsnittet baseras på användning av ett Office 365-konto som använder Microsoft Azure Active Directory.  

Om du har aktiverat prenumerationen av [!INCLUDE[d365fin](includes/d365fin_md.md)] och är inte längre med utvärderingen företaget kan du har en Azure Active Directory för klientorganisation. Administratören eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner hanterar den här klientorganisationen i [Azure portal](https://portal.azure.com). Det är där nya användare läggs till och licenser används och tas bort. Mer information finns i [Microsoft Azure portalöversikten](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

En av licenstyperna för [!INCLUDE[d365fin](includes/d365fin_md.md)] är licens *externa revisorn*. Den här typen av licens är avsedd att användas av användare, till exempel externa revisorer. Detta innebär att du inte behöver köpa ett extra säte i den aktuella Active Directory eller använda en av dina befintliga [!INCLUDE[d365fin](includes/d365fin_md.md)]-konton på en extern revisor. Om din aktuella prenumeration i Office 365 omfattar 10 användare för exempelvis [!INCLUDE[d365fin](includes/d365fin_md.md)], och du använder 10 *fullständiga användare*-licenser kan din administratör bara lägga till en extern revisor som gästanvändare i Azure portalen och tilldela användaren licensen *extern revisor* utan extra kostnad. Du kan dock endast ha en användare med licensen *extern revisor*. Om du vill lägga till fler användare, måste du uppdatera prenumerationen på Office 365 i enlighet med detta.  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Konfigurera e-post manuellt eller med hjälp av assisterad konfiguration](admin-how-setup-email.md)  
[Revisorlösningar i Business Central ](finance-accounting.md)  
[Business Central for Accountants på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
