---
title: Välja användargränssnittet för att visa eller dölja avancerade funktioner | Microsoft Docs
description: Lär dig vad användarupplevelsernivåerna Essential och Premium betyder för användargränssnitt, moduler och ditt företag.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 354791b9a1bafb07bc1e16530dc1d07c16d1e49d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747624"
---
# <a name="change-which-features-are-displayed"></a>Ändra vilka funktioner som visas
[!INCLUDE[prod_short](includes/prod_short.md)] är utformat för att hjälpa dig att driva företaget oavsett storlek och komplexitet. I produktens kärna finns viktiga funktioner, till exempel ekonomisk rapportering, försäljning, inköp och lagerhantering. När affärs komplexiteten ökar kan du t.ex. aktivera funktioner för produktion och tjänsthantering.

Du kan ange produktens komplexitets nivå och därmed vilka funktioner företagets användare får till gång till, genom att ändra inställningen **Upplevelse** på sidan **Företagsinformation**. Observera att upplevelseinställningen också kan ändras genom att lägga till vissa tillägg från AppSource. Mer information finns i [Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md).

Följande tabell listar de upplevelser som finns tillgängliga.

| Upplevelse | Inverkan på användargränssnitt |
| --- | --- |
| **Essential** |Visar alla åtgärder och fält för alla vanliga affärsfunktioner.|
| **Premium** |Visar alla åtgärder och fält för alla företagsfunktioner, till exempel produktion och service.|

De upplevelser som kan väljas i [!INCLUDE[prod_short](includes/prod_short.md)] reflekterar lösningslicenserna, som kallas planer, som har definierats för produkten. Information Essential- och Premium-planerna finns i [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) på marknadsföringswebbplatsen Microsoft Dynamics 365. Se även [[!INCLUDE[prod_short](includes/prod_short.md)] Licensieringsguide](https://go.microsoft.com/fwlink/?linkid=2068931) (kräver åtkomst till CustomerSource eller PartnerSource).

> [!IMPORTANT]  
> Alla vanliga användare i en lösning måste tilldelas samma plan Essential eller Premium, innan den miljön kan väljas för företaget. En användare kan inte därmed öppna Premium-funktioner om en eller flera användare kan endast åtkomst Essential-funktioner. Detta gäller inte för ej vanliga användare av typen gruppmedlem, intern administration, extern revisor och delegerad administratör, som var och en tilldelas ett annat schema än andra användare i lösningen.<br /><br /> Endast användare av typen Evaluation eller Premium kan ändra värdet i fältet **Upplevelse** från Essential till Premium.

Innan du definierar ett företags upplevelseinställning definierar du användarnas åtkomst till vissa funktioner och sidor genom att tilldela behörighetsuppsättningar. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

Inställningen **Upplevelse** gäller för alla användare i ett företag, men varje användare kan anpassa sin egen upplevelse ytterligare genom att ändra sidlayouter och innehåll. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Aktivera Premium-funktioner när du har uppgraderat en Plan
Användare som är tilldelade till planer i Microsoft 365 administratörscentret i samband med det allmänna arbetet som Business Central användare skapar. Mer information finns i [Lägga till användare och tilldela licenser samtidigt](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### <a name="to-update-plan-changes-in-users-groups"></a>Uppdatera planändringar i användargrupper
När du har gjort en ändring i planer för användare i Microsoft 365 administratörscentret, såsom tilldelat premiumplanen till flera användare, måste du visa ändringarna i [!INCLUDE[prod_short](includes/prod_short.md)].

1. Logga in som en administratör.
2. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användare** och välj sedan relaterad länk.
3. På sidan **Användare** väljer du åtgärden **Uppdatera all användargrupper**.

All ny information om användarna planer och deras tilldelade användargrupper har nu uppdaterats enligt ändringarna i planen.

### <a name="to-select-the-premium-experience"></a>För att välja Premium-upplevelsen.
Du kan nu fortsätta med att välja den nya miljön.
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Företagsinformation** och välj sedan relaterad länk.
2. På sidan **FöretagsInformation** på snabbfliken **användarupplevelse** väljer du fältet **upplevelse**.

## <a name="help-assumes-premium-experience"></a>Hjälp utgår från Premium-upplevelsen
Alla funktionsbeskrivningar i användardokumentationen för [!INCLUDE[prod_short](includes/prod_short.md)] antar **Premium**-upplevelsen, vilket innebär beskrivningarna som omfattar hela gränssnittselement.

## <a name="see-also"></a>Se även
[Anpassa din arbetsyta](ui-personalization-user.md)  
[Anpassa Business Central](ui-customizing-overview.md)  
[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Skapa nya företag](about-new-company.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Licensieringsguide](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]