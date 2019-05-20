---
title: Välja användargränssnittet för att visa eller dölja avancerade funktioner | Microsoft Docs
description: Lär dig vad användarupplevelsernivåerna Essential och Premium betyder för användargränssnitt, moduler och ditt företag.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 9110ee79e4d1788f41c8f1960f282cb490a3cc8a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251429"
---
# <a name="changing-which-features-are-displayed"></a>Ändra vilka funktioner som visas
[!INCLUDE[d365fin](includes/d365fin_md.md)] är utformad för att hjälpa dig att köra din verksamhet oavsett vilken verksamhet som du befinner dig i. I kärnan av [!INCLUDE[d365fin](includes/d365fin_md.md)] hittar du ekonomisk rapportering och försäljning-s och inköpsprocesser. Du lägger till upplevelser till detta i enlighet med dina företagsbehov genom att lägga till tillägg från AppSource eller genom att ändra upplevelseinställningen för ditt företag. Mer information finns i [Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] Använda tillägg](ui-extensions.md), eller [Välja en användarupplevelse för att visa eller dölja funktioner](ui-experiences.md#choosing-a-user-experience-to-show-or-hide-features).

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Om du väljer ett användargränssnitt för att visa eller dölja funktioner
Användarupplevelsen bestämmer hur mycket av kärnafunktionaliteten som finns när du och din kolleger använder [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan välja användarupplevelse för ditt företag på sidan **företagsinformation** i fältet **upplevelse**.

> [!NOTE]  
> Den här inställningen gäller för alla användare i företaget. Användarna kan anpassa sina egna upplevelser ännu mer genom att ändra sidans layout och innehåll. Mer information finns i [Anpassa arbetsyta och sidor](ui-personalization-user.md).  

Följande tabell listar de upplevelser som finns tillgängliga.

| Upplevelse | Inverkan på användargränssnitt |
| --- | --- |
| **Essential** |Visar alla åtgärder och fält för alla vanliga affärsfunktioner.|
| **Premium** |Visar alla åtgärder och fält för alla företagsfunktioner, till exempel produktion och service.|

> [!NOTE]  
> De lösningar som du kan välja mellan i [!INCLUDE[d365fin](includes/d365fin_md.md)] beror på din lösningslicens, även kallad en "plan". Information om planerna **Vital** och **Premium** finns i [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på marknadsföringswebbplatsen Microsoft Dynamics 365. Se även [[!INCLUDE[d365fin](includes/d365fin_md.md)] Licensieringsguide](https://go.microsoft.com/fwlink/?linkid=2068931) (kräver åtkomst till CustomerSource eller PartnerSource).

> [!IMPORTANT]  
> Alla vanliga användare i en lösning måste tilldelas samma plan Essential eller Premium, innan den miljön kan väljas för företaget. En användare kan inte därmed öppna Premium-funktioner om en eller flera användare kan endast åtkomst Essential-funktioner. Detta gäller inte för ej vanliga användare av typen gruppmedlem, intern administration, extern revisor och delegerad administratör, som var och en tilldelas ett annat schema än andra användare i lösningen.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivera Premium-funktioner när du har uppgraderat en Plan
Användare som är tilldelade till planer i Office 365 administratörscentret i samband med det allmänna arbetet som Business Central användare skapar. Mer information finns i [Lägg till användare till Office 365 för företag](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc)

Du kan definiera vilka funktioner och sidor inom miljön som de användare som ska ha tillgång genom att tilldela behörighetsgrupper. Mer information finns i [Hantera användare och behörigheter](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Uppdatera planändringar i användargrupper
När du har gjort en ändring i planer för användare i Office 365 administratörscentret, såsom tilldelat premiumplanen till flera användare, måste du visa ändringarna i [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Logga in som en administratör.
2. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användare** och välj sedan relaterad länk.
3. Alternativt kan du på sidan **Användare** välja åtgärden **Uppdatera all användargrupper**.

All ny information om användares planer och deras tilldelade användargrupper har nu uppdaterats enligt ändringarna i planen.

### <a name="to-select-the-premium-experience"></a>För att välja Premium-upplevelsen.
Du kan nu fortsätta med att välja den nya miljön.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Företagsinformation** och välj sedan relaterad länk.
2. På sidan **FöretagsInformation** på snabbfliken **användarupplevelse** väljer du fältet **upplevelse**.

## <a name="help-assumes-premium-experience"></a>Hjälp utgår från Premium-upplevelsen
Alla funktionsbeskrivningar i användardokumentationen för [!INCLUDE[d365fin](includes/d365fin_md.md)] antar **Premium**-upplevelsen, vilket innebär beskrivningarna som omfattar hela gränssnittselement. En textanteckning infogas i ett inledande hjälpavsnitt för funktionsområdena Tillverkning och Servicehantering om de kräver **Premium**-upplevelse.

## <a name="see-also"></a>Se även
[Skapa nya företag](about-new-company.md)  
[Hantera användare och behörigheter](ui-how-users-permissions.md)    
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Licensieringsguide](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
