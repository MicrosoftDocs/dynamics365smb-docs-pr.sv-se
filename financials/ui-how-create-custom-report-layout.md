---
title: "Så här skapar du en anpassad rapport eller layout för | Microsoft Docs"
description: "Lär dig hur du kan designa hur rapporten ska se ut."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 79c1e5c1ea01077e2e5012ba07618760ccf2a4af
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-create-a-custom-report-or-document-layout"></a>Så här skapar du en anpassad rapport eller dokumentlayout
Som standard kommer en rapport ha inbyggd rapportlayout, antingen RDLC- eller Word-rapportlayout eller båda typerna. Du kan inte ändra inbyggda layouter. Du kan skapa egna anpassade layouter som du kan använda för att ändra utseendet på rapporten när den visas, skrivs ut eller sparas. Du kan skapa flera anpassade rapportlayouter för samma rapport, och sedan byta layout som används av en rapport efter behov.

**Obs!** I [!INCLUDE[d365fin](includes/d365fin_md.md)] omfattar termen "rapporter" även externa dokument som t.ex. fakturor och bekräftelser av inköpsorder som du skickar till kunder som PDF-filer.

Om du vill skapa en anpassad layout kan du antingen skapa en kopia av en befintlig anpassad layout eller lägga till en ny anpassad layout, som baseras i de flesta fall på en inbyggd layout. När du lägger till en ny anpassad layout kan du välja att lägga till en RDLC-rapportlayout, Word-rapportlayout eller både och. Den nya anpassade layouten baseras automatiskt på den inbyggda layouten för rapporten, om en är tillgänglig. Om det inte finns någon inbyggd layout för typen, skapas en ny tom layout som du måste ändra och utforma från noll. Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Så här skapar du en anpassad layout
1. I det övre högra hörnet väljer du ikonen **Söka efter sida eller rapport** ![Söka efter sida eller rapport](media/ui-search/search_small.png "Search for Page or Report icon"), går till **Val av rapportlayout** och väljer sedan relaterad länk.  
   I fönstret ** Report Layout Selection** visas alla rapporter som är tillgängliga i företaget som har angetts i fältet Företag högst upp i fönstret.
2. Ange fältet **Företag** till företaget som du vill skapa rapportlayouten i.
3. Markera raden för rapporten som du skapa layouten för och välj sedan **Anpassade layouter**.  
   i fönstret **Anpassade rapportlayouter** visas alla anpassade layouter som är tillgängliga för den valda rapporten.
4. Om du vill skapa en kopia av en befintlig anpassad layout, markera den befintliga anpassade layouten i listan och välj sedan **Kopiera**.  
   Kopian av den anpassade layouten visas i fönstret **Anpassade rapportlayouter** och har orden Kopia av i fältet Beskrivning.
5. Om du vill lägga till en ny anpassad layout som baseras på en inbyggd layout gör du följande:  
   1. Välj **Ny**. Fönstret **Infoga inbyggd layout för en rapport** visas. Fälten **ID** och **Namn** fylls i automatiskt.
   2. Om du vill lägga till en anpassad Word-rapportlayouttyp markerar du kryssrutan **Infoga Word-layout**.
   3. Om du vill lägga till en anpassad RDLC-rapportlayouttyp markerar du kryssrutan **Infoga RDLC-layout**.
   4. Välj **OK**.  
      De nya anpassade layouterna visas i fönstret **Anpassade rapportlayouter**. Om en ny layout baseras på en inbyggd layout får den orden **Kopia av en inbyggd layout** i fältet **Beskrivning**. Om det inte fanns en inbyggd layout för rapporten, får den nya layouten orden **Ny layout** i fältet **Beskrivning**, vilket anger att den anpassade layouten är tom.
6. Som standard är fältet **Företagsnamn** tomt, vilket betyder att den anpassade layouten är tillgänglig för rapporten i alla företag. För att du ska kunna göra den anpassade layouten tillgänglig väljer du **Redigera** och ställer sedan in fältet **Företagsnamn** till företaget som du vill ha.

## <a name="see-also"></a>Se även
[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Så här ändrar du vilken layout som används i en rapport för närvarande](ui-how-change-layout-currently-used-report.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

