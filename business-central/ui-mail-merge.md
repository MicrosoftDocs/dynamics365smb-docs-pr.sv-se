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
ms.openlocfilehash: 84b6a9fa74cea99f8b939edcf0cd883e39eb6937
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445978"
---
# <a name="using-word-templates-for-bulk-communication"></a>Använda Word-mallar för masskommunikation
Microsoft Word-mallar kan göra det enklare att kommunicera med enheter som kunder och leverantörer. Du kan till exempel skapa broschyrer för att avisera kunder om en försäljningskampanj, brev för att informera leverantörer om nya inköpsprinciper eller inbjudningar till att locka kontakter till ett kommande evenemang.

> [!NOTE]
> Du kan bara använda Word-mallar på enheter med Microsoft Word 2019 och Windows operativsystem installerat.

Du kan använda entiteter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla för mallen och lägga till kopplings instruktioner i anpassa dokument för varje entitet. Sammankopplingsfälten hämtas från entiteten i [!INCLUDE[prod_short](includes/prod_short.md)]. När du använder en Word-mall på en entitet infogas data från sammankopplingsfälten i dokumentet.

På sidan **Word-mallar** kan du använda en assisterad installations handbok för att hämta en zip-fil som innehåller en DataSource.txt-och en Word-mallfil för en entitet. När du har skapat mallen och lagt till sammankopplingsinstruktioner använder du samma stödlinje för att överföra mallen. Du kan bara använda Word-mallen och de datakällfiler som du hämtar från [!INCLUDE[prod_short](includes/prod_short.md)] och du måste lagra filerna på samma plats.

> [!NOTE]
> När du väljer en entitet för vilken du vill skapa en mall visar listan alla entiteter i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan emellertid inte skapa mallar för alla entiteter. Om namnet på en entitet innehåller specialtecken, till exempel **/**, **.**, **_** eller **-** kan du inte skapa en mall för den. Namnet på entiteten visas i kolumnen **Objektrubrik**.

När du lägger upp mallen i Word på fliken **Utskick** kan du lägga till sammankopplingsinstruktioner genom att välja **Infoga sammankopplingsfält**.

> [!NOTE]
> Du kan inte använda sammankopplingsfält om fältnamnet innehåller 40 tecken eller mer. Du kan till exempel inte använda fältet Company__Information_Customs_Permit_Date eftersom det innehåller 40 tecken. 

När Word-mallen är klar kan du på sidan **Word-mallar** välja **Använd** för att skapa dokumenten. Du kan antingen skapa ett dokument som innehåller avsnitt för varje entitet, eller dela operationen för att skapa ett nytt dokument för varje entitet.

## <a name="to-create-a-word-template"></a>Skapa en Word-mall
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Word-mallar** och väljer sedan relaterad länk.
2. Följ instruktionerna i assisterad konfiguration. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Se även
[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
