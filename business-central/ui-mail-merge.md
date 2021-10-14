---
title: Använda Word-mallar för masskommunikation | Microsoft Docs
description: Med Word-mallar kan du enkelt skapa dokument som är anpassade för specifika entiteter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: c624d718d27de607aed49a82a506f81eec57247c
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588913"
---
# <a name="using-word-templates-for-bulk-communication"></a>Använda Word-mallar för masskommunikation
Microsoft Word-mallar kan göra det enklare att kommunicera i skrivit eller e-post med enheter som kontakter, kunder och leverantörer. Du kan till exempel skapa broschyrer för att avisera kunder om en försäljningskampanj, brev för att informera leverantörer om nya inköpsprinciper eller inbjudningar till att locka kontakter till ett kommande evenemang.

> [!NOTE]
> Du kan bara använda Word-mallar på enheter med Microsoft Word 2019 och Windows operativsystem installerat.

Du kan använda entiteter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla för mallen och lägga till kopplings instruktioner i anpassa dokument för varje entitet. Sammankopplingsfälten hämtas från entiteten i [!INCLUDE[prod_short](includes/prod_short.md)]. När du använder en Word-mall på en entitet infogas data från sammankopplingsfälten i dokumentet.

På sidan **Word-mallar**, när du skapar en ny mall kan du använda en assisterad installations handbok för att hämta en zip-fil som innehåller en DataSource.xlsx- och en Word-mallfil för en entitet. Data källfilen innehåller de fält som du kan använda i mallen. Redigera inte datakällfilen. Du kan bara använda Word-mallen och de datakällfiler som du hämtar från [!INCLUDE[prod_short](includes/prod_short.md)] och du måste lagra filerna på samma plats.

När du har skapat mallen och lagt till sammankopplingsinstruktioner använder du samma stödlinje för att överföra mallen.

## <a name="setting-up-the-template-in-word"></a>Konfigurera mall i Word
När du lägger upp mallen i Word på fliken **Utskick** kan du lägga till sammankopplingsinstruktioner genom att välja **Infoga sammankopplingsfält**. De kopplingsfält som är tillgängliga kommer från datakällfilen som du hämtade för entiteten. De fungerar som platshållare som berättar för Word var i dokumentet informationen om enheten ska placeras. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Lägga till kopplingsinstruktioner i Microsoft Word":::

## <a name="adding-related-entities"></a>Lägga till relaterade entiteter
Förutom att lägga till data för källentiteten, d.v.s. den entitet som du skapar mallen för, kan du också koppla data från enheter som är relaterade till den. Om källan exempelvis är en kundentitet kan du också koppla data från fält på kund-/inköpare, eftersom båda entiteterna har ett gemensamt fält.

Relaterade enheter delar ett fält, som ofta är en identifierare som t.ex. namn, kod eller ID, med källentiteten. När du lägger upp en mall finns det enkla och avancerade alternativ för att välja relaterade entiteter:

* Enkel – Lägg till kända relationer som [!INCLUDE[prod_short](includes/prod_short.md)] gör tillgängliga som standard.
* Avancerad – Lägg till relationer som inte är standard, till exempel sådana som har lagts till med tillägg eller anpassningar. Detta kräver att du känner till fälten som enheterna delar.

När du lägger till en relaterad entitet måste du ange ett prefix för fältnamnet. När du lägger till fält i mallen kan prefixet göra det enklare att skilja mellan fälten från källentiteten och fält från relaterade entiteter.

## <a name="to-create-a-word-template-in-business-central"></a>Så här skapar du en Word-mall i Business Central
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Word-mallar** och väljer sedan relaterad länk.
2. Välj **Ny**, sedan **Skapa en mall** och följ sedan instruktionerna i guiden assisterad konfiguration. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Du kan också skapa en mall direkt från sidan för en entitet genom att välja åtgärd för att **tillämpa Word-mall** för att öppna guiden inställningsguiden och **ny mall**. När du gör det väljs datakälla för dig baserat på typen av entitet.

## <a name="applying-a-template"></a>Tillämpa en mall
När Word-mallen är klar kan du på sidan **Word-mallar** välja **Använd** för att skapa dokumenten. När du använder en Word-mall på en entitet infogas data från sammankopplingsfälten i dokumentet. Du kan antingen skapa ett dokument som innehåller avsnitt för varje entitet, eller **dela** för att skapa ett nytt dokument för varje entitet.

Du kan tillämpa mallar på en eller flera av samma typ av entiteter, till exempel en kontakt, direkt i kontexten för den sidan eller på sidan Word-mallar om du vill använda mallen på alla enheter av den aktuella typen.

## <a name="using-word-templates-with-email"></a>Använda Word-mallar med e-post
Du kan använda Word-mallar för att lägga till innehåll i e-postmeddelanden. När du skriver ett e-postmeddelande kan du välja instruktionen **Använd Word-mall** om du vill använda innehållet i en mall i meddelandet. Detta förutsätter att du har skapat en eller flera mallar för entiteten. Du kan använda en mall i taget och när du växlar mellan mallar ändras meddelandet så att det återspeglar innehållet i den valda mallen.

Dessutom kan du använda åtgärden **Lägg till fil från Word-mall** för att koppla innehållet i mallen till e-postmeddelandet som en fil. Filen kommer att använda det format som du har angett för mallens utdata.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Alternativ för att använda innehåll från en Word-mall i ett e-postmeddelande":::

## <a name="see-also"></a>Se även
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
