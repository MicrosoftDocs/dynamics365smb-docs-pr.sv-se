---
title: Koppla Data med | Microsoft Docs
description: "Du kan göra dina Financials-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa ett automatiskt arbetsflöde."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 277dda7c954380138af1ecabc02d77121f35aac7
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] i ett automatiskt arbetsflöde
Du kan använda din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av ett arbetsflöde i Microsoft Flow.  

> [!NOTE]  
>   Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i Flow.
1. I webbläsaren, går du till [flow.microsoft.com](https://flow.microsoft.com/en-us/), och loggar in.
2. Välj **Mina flöden** från menyn längst upp på sidan.
3. I fönstret **Mina flöden** kan välja alternativet **Skapa från tom**.
4. I listan över tillgängliga utlösare markerar du ett av två [!INCLUDE[d365fin](includes/d365fin_md.md)]-utlösare som är tillgängliga: *När en post skapas*, eller *När en post ändras *.
5. Flow visar en anslutningssida som uppmanar dig till att ge den information som behövs för att ansluta till din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Du måste ange ett namn för anslutningen, OData-URL, användarnamn, lösenord och företagsnamn för att ansluta.

   För den *OData-URL*, kan du kopiera OData V4-URL för någon av webbtjänsterna som finns på sidan **webbtjänster** i [!INCLUDE[d365fin](includes/d365fin_md.md)], som t.ex. `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   För *företagsnamn*, använder du namnet som visas i fältet **namn** i fönstret **företagsinformation** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om din [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller flera företag, väljer du relevant företagsnamn i listan i fönstret **företag**. I båda fallen kontrollerar du att namnet som du anger i PowerApps-guiden motsvarar exakt den text som visas i [!INCLUDE[d365fin](includes/d365fin_md.md)], som t.ex. `My Company`.

   För användarnamn och lösenord, använder du de namn- och webbtjänstnycklar som har angetts för kontot i fönstret **användare** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ditt användarnamn är till exempel *ADMIN* och webbtjänståtkomstnyckeln som fungerar som ditt lösenord och *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*. Mer information finns i [Så här hanterar du användare och behörigheter](ui-how-users-permissions.md).
6. Välj knappen **skapa** längst ned på sidan om du vill fortsätta.

   Flow visar en lista över tabeller som finns på [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dessa listor eller slutpunkter motsvarar de webbtjänster som du har publicerat från ditt [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Du kan också skapa en ny webbtjänst-URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställ in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.
7. Välj de data som du vill ska användas för i Flow.

Nu har du lyckats ansluta till dina Dynamics 365-data och är redo att börja skapa ditt flöde. Mer information finns i [Flow-dokumentation](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Se även
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Så här hanterar du användare och behörigheter](ui-how-users-permissions.md)    
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  

