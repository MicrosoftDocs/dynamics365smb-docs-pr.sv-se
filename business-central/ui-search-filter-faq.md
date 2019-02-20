---
title: "Om sökning och filtrering i Business Central"
description: "Svar på vanliga frågor om att söka och filtrera."
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 10/01/2018
ms.author: mikebc
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: 099a2a800cb71e7a0b8dd02901928b43dfa199ca
ms.contentlocale: sv-se
ms.lasthandoff: 01/22/2019

---

# <a name="about-searching-and-filtering-in-included365finincludesd365finmdmd"></a>Om sökning och filtrering i [!INCLUDE[d365fin](includes/d365fin_md.md)]
Den här artikeln besvarar vanliga frågor som du kanske har om att söka och filtrera.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Finns det en skillnad mellan sökning och filtrering?
Ja.
- Sökning är enkel och omfattande: den matchar poster som innehåller söktexten i alla fält som visas på sidan och är skiftlägeskänslig.
- Filtrering är mycket flexibel och kan kopplas till speciella områden, inklusive de som inte visas på sidan: den visar poster med samma skiftlägeskänsliga matchningar, men kan justeras med kraftfulla söksymboler, variabler och formler. Mer information om hur du använder dessa funktioner finns i [sortering, sökning och filtrering i Listor](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Finns det en upplevelse för dig för att söka och filtrera?
Söka och filtrera har optimerats mycket för användare som vill ha interaktion utan mus för att arbeta effektivt med sina data. Det finns en mängd olika kortkommandon som kan användas i följd för att arbeta med hög hastighet. Mer information finns i [Kortkommandon](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Finns filterrutan i alla listor?
Filterrutan finns på sidor där listan är det primära innehållet på sidan, till exempel kalkylblad och listsidor inklusive listor som kan nås från navigeringsfältet. Filterrutan är ännu inte tillgänglig för inbäddade listor, till exempel försäljningsrader på försäljningsorder eller för listor med dynamiska kolumner (ofta kallade matrissidor). 

## <a name="how-can-i-save-my-filters"></a>Hur kan jag spara mina filter?

Dina filter och justeringar till fördefinierade filter sparas under hela sessionen (medan du fortfarande är inloggad), även om du lämnar den här sidan. Det går för närvarande inte att spara filter permanent. Till skillnad från filter sparas söktext inte när du lämnar en sida.

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Är det detsamma som Avancerat filter och Begränsa totaler i Microsoft Dynamics NAV?
[!INCLUDE[d365fin](includes/d365fin_md.md)] bygger på dessa populära funktioner och ger en moder och mycket användbar upplevelse för att söka efter och analysera data. Med fler kortkommandon och introduktion av sökning överträffar [!INCLUDE[d365fin](includes/d365fin_md.md)] funktionerna i Dynamics NAV.

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Kan jag söka och filtrera med tillhörande appar och Outlook-tillägg?
På olika visningsmål såsom mobila enheter eller i Outlook kan du söka i listor men det går inte att filtrera efter enskilda fält i de flesta fall.

## <a name="is-the-filter-pane-available-for-filtering-reports"></a>Finns filterrutan för att filtrera rapporter?
Nej. Dialogrutan för rapportfilter, vanligen kallad sidan för begäran, använder för närvarande en annan upplevelse som innehåller vissa, men inte alla, funktioner i filterrutan.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Kommer Microsoft att utöka filterrutans upplevelse?
På Microsoft lyssnar vi ständigt på feedback från våra olika användargrupper och handlar efter de bästa förslagen. Om du vill utöka filterrutan till fler formfaktorer, fler typer av listor och rapporter och har en bra idé om hur du förbättrar den, lägger du till en idé eller röstar på befintliga förslag på [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Kan jag göra något om meddelandet ”söka efter rader tar alltför lång tid”?

Det finns en tidsgräns för hur långt sökningen kan ta. Försök först att ändra sökvillkoren och söka igen. Om du använder [!INCLUDE[prodshort](includes/prodshort.md)] lokalt, kontakta systemadministratören, eftersom en administratör kan öka tidsfristen för sökningar.

Som lokal administratör ökar du tidsfristen på sökningar genom att ändra inställningen **Timeout för sökning** för [!INCLUDE[prodshort](includes/prodshort.md)]-servern. Mer information finns i [Konfigurera Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) i Business Central -utvecklare och IT-proffs.

## <a name="see-also"></a>Se även
[Komma igång](product-get-started.md)  
[Sortera, söka och filtrera i listor](ui-enter-criteria-filters.md)

