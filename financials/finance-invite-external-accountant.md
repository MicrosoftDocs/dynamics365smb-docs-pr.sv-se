---
title: "Lägga till en extern revisor till Financials | Microsoft Docs"
description: "Lär dig hur du kan bjuda in dina externa revisorn till din Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 06/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1b9f88f02b198ae8da0f3359a3ce7799b9535739
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="invite-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]
Om du använder en extern revisor för att hantera böcker och redovisning kan du bjuda in dem till dina [!INCLUDE[d365fin](includes/d365fin_md.md)] så att de kan arbeta med dig med räkenskapsårets informationen.

När din revisorn har fått tillgång till din [!INCLUDE[d365fin](includes/d365fin_md.md)], kan de använda rollcenter **revisorn** som ger enkel åtkomst till de mest relevanta fönster för att kunna arbeta.  

> [!NOTE]  
>  Den här funktionen kräver att din upplevelse är inställd på **Paket**. Mer information finns i [anpassa din finansiella upplevelse](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Bjud in din externa revisorn till [!INCLUDE[d365fin](includes/d365fin_md.md)]
I den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)], krävs det att en administratör läggs till i din Active Directory-innehavare för att kunna bjuda in en extern revisor. Stegen för att göra detta beror på vilken typ av konto som du använde när du registrerade dig för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det här avsnittet baseras på användning av ett Office 365-konto som använder Microsoft Azure Active Directory.  

> [!TIP]  
>  Vi rekommenderar att du kontaktar din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner för att få hjälp.  

Om du har aktiverat prenumerationen av [!INCLUDE[d365fin](includes/d365fin_md.md)] och är inte längre med utvärderingen företaget kan du har en Azure Active Directory för klientorganisation. Administratören eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner hanterar den här klientorganisationen i [Azure portal](https://portal.azure.com). Det är där nya användare läggs till och licenser används och tas bort. Mer information finns på [Microsoft Azure portal översikt ](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

### <a name="separate-license"></a>Separera licens
En av licenstyperna för [!INCLUDE[d365fin](includes/d365fin_md.md)] är licens *externa revisorn*. Den här typen av licens är avsedd att användas av användare, till exempel externa revisorer. Detta innebär att du inte behöver köpa ett extra säte i den aktuella Active Directory eller använda en av dina befintliga [!INCLUDE[d365fin](includes/d365fin_md.md)]-konton på en extern revisor. Om din aktuella prenumeration i Office 365 omfattar 10 användare för exempelvis [!INCLUDE[d365fin](includes/d365fin_md.md)], och du använder 10 *fullständiga användare*-licenser kan din administratör bara lägga till en extern revisor som gästanvändare i Azure portalen och tilldela användaren licensen *externa revisorn* utan extra kostnad. Du kan dock endast ha en användare med licensen *extern revisor*. Om du vill lägga till fler användare, måste du uppdatera prenumerationen på Office 365 i enlighet med detta.  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Revisorupplevelse i Dynamics 365 for Financials](finance-accounting.md)  
[Financials for Accountants på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

