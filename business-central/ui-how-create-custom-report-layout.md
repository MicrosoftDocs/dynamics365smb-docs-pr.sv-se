---
title: Så här skapar och ändrar du en anpassad layout för rapport eller dokument | Microsoft Docs
description: Lär dig hur du kan skapa egna anpassade layouter för att personligt anpassa utseendet på rapporten när den visas, skrivs ut eller sparas.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: f7d907393f765538512a547c8eaa6a3f8963de79
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311050"
---
# <a name="create-and-modify-a-custom-report-or-document-layout"></a>Så här skapar och ändrar du en anpassad rapport eller dokumentlayout
Som standard kommer en rapport ha inbyggd rapportlayout, antingen RDLC- eller Word-rapportlayout eller båda typerna. Du kan inte ändra inbyggda layouter. Du kan skapa egna anpassade layouter som du kan använda för att ändra utseendet på rapporten när den visas, skrivs ut eller sparas. Du kan skapa flera anpassade rapportlayouter för samma rapport, och sedan byta layout som används av en rapport efter behov.

> [!NOTE]  
>   I [!INCLUDE[d365fin](includes/d365fin_md.md)], omfattar termen "rapporter" även externa dokument som t.ex. fakturor och bekräftelser av inköpsorder som du skickar till kunder som PDF-filer.

Om du vill skapa en anpassad layout kan du antingen skapa en kopia av en befintlig anpassad layout eller lägga till en ny anpassad layout, som baseras i de flesta fall på en inbyggd layout. När du lägger till en ny anpassad layout kan du välja att lägga till en RDLC-rapportlayout, Word-rapportlayout eller både och. Den nya anpassade layouten baseras automatiskt på den inbyggda layouten för rapporten, om en är tillgänglig. Om det inte finns någon inbyggd layout för typen, skapas en ny tom layout som du måste ändra och utforma från noll. Mer information om RDLC- och Word-rapportlayouter, inbyggda och anpassade layouter och mer finns i [Hantera rapportlayouter](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Så här skapar du en anpassad layout
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Val av rapportlayout** och välj sedan relaterad länk.

    På sidan **Val av rapportlayout** visas alla rapporter som är tillgängliga i företaget som har angetts i fältet **Företagsnamn** högst upp på sidan.
2. Ange fältet **Företag** till företaget som du vill skapa rapportlayouten i.
3. Markera raden för rapporten som du skapa layouten för och välj sedan **Anpassa layouter**.  

   På sidan **Anpassa rapportlayouter** visas alla anpassade layouter som är tillgängliga för den valda rapporten.
4. Om du vill skapa en kopia av en befintlig anpassad layout, markera den befintliga anpassade layouten i listan och välj sedan **Kopiera**.  

   Kopian av den anpassade layouten visas på sidan **Anpassa rapportlayouter** och har orden *Kopia av* i fältet **Beskrivning**.
5. Om du vill lägga till en ny anpassad layout som baseras på en inbyggd layout gör du följande:  
   1. Välj åtgärden **Ny**. På sidan **Infoga inbyggd layout för en rapport** visas. Fälten **ID** och **Namn** fylls i automatiskt.
   2. Om du vill lägga till en anpassad Word-rapportlayouttyp markerar du kryssrutan **Infoga Word-layout**.
   3. Om du vill lägga till en anpassad RDLC-rapportlayouttyp markerar du kryssrutan **Infoga RDLC-layout**.
   4. Välj **OK**.  

    De nya anpassade layouterna visas på sidan **Anpassa rapportlayouter**. Om en ny layout baseras på en inbyggd layout får den orden **Kopia av en inbyggd layout** i fältet **Beskrivning**. Om det inte fanns en inbyggd layout för rapporten, får den nya layouten orden **Ny layout** i fältet **Beskrivning**, vilket anger att den anpassade layouten är tom.
6. Som standard är fältet **Företagsnamn** tomt, vilket betyder att den anpassade layouten är tillgänglig för rapporten i alla företag. För att du ska kunna göra den anpassade layouten tillgänglig väljer du **Redigera** och ställer sedan in fältet **Företagsnamn** till företaget som du vill ha.

Den anpassade layouten har skapats. Du kan nu ändra den anpassade layouten efter behov.

## <a name="ModifyCustomLayout"></a>Ändra en anpassad layout
Om du vill ändra en rapportlayout måste du först exportera rapportlayouten som en fil till en plats på din dator eller nätverk, och sedan öppna det exporterade dokumentet och göra ändringarna. När du är klar med ändringarna importerar du rapportlayouten.

### <a name="to-modify-a-custom-layout"></a>Ändra en anpassad layout
1.  Du kan exportera en anpassad layout från sidan **anpassade rapportlayouter**. Om sidan inte redan är öppen, sök efter och öppna **Val av rapportlayout**, välj rapporten med layouten som du vill ändra och välj sedan åtgärden **Anpassade layouter**.  
2.  På sidan **anpassade rapportlayouter** väljer du den layout som du vill ändra, anger **exportera layout**, och välj **spara** eller **Spara som** för att spara rapportlayouten till en plats på datorn eller i nätverket.  

3.  Öppna rapportlayoutdokumentet som du sparade och gör ändringar.

      Om du ändrar layouten i Word, öppna layoutdokumentet i Word. Redigera information, finns i avsnittet [att göra ändringar i rapportlayout](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      RDLC rapportlayouter är mer avancerade än Word rapportlayouter. Mer information om att ändra en RDLC-rapportlayout finns i [Designa RDLC rapportlayout](/dynamics-nav/Designing-RDLC-Report-Layouts).

      Glöm inte att spara ändringar när du är klar.

4.  Gå tillbaka till sidan **anpassade rapportlayouter**, välj rapportlayouten som du har exporterats och ändrats, och välj sedan åtgärden **Importera layout**.  

5. I dialogrutan **Importera** väljer du **Välj** för att hitta och välja dokumentet och väljer sedan **Öppna**.

##  <a name="MakeChangesToLayout"></a> Så här gör du ändringar i en Word-rapportlayout  
Du kan göra allmänna formaterings- och layoutändringar, t.ex ändra textteckensnittet, lägga till och ändra en tabell eller ta bort ett datafält, genom att använda de grundläggande redigeringsfunktionerna i Word.

Om du designar en Word-rapportlayout från noll eller lägger till nya datafält, starta då genom att lägga till en tabell som innehåller rader och kolumner som kommer att innehålla datafälten.

> [!TIP]  
>  Visa tabellstödlinjerna så att du kan se gränserna mellan tabellceller. Kom ihåg att dölja stödlinjerna när du har redigerat klart. För att visa eller dölja tabellstödlinjer, välj tabellen och välj under **Visa stödlinjer** på fliken **Tabell** under **Layout**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Inbäddade teckensnitt i Word-ayouter för konsistens

För att säkerställa att rapporterna alltid visas och skrivs ut med planerade teckensnitt, oavsett om en användare öppnar eller skriver ut rapporter, kan du bädda in teckensnitt i Word-dokumentet. Men tänk på att inbäddade teckensnitt kan öka storleken på de Word-filerna väsentligt. Mer information om inbäddade teckensnitt i Word finns i [inbäddade teckensnitt i Word, PowerPoint eller Excel](https://support.office.com/en-us/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Ta bort rubrik- och datafält i Word-layouter  
 Rubrik- och datafält för en rapport finns i innehållskontroller i Word. Efterföljande diagram illustrerar en innehållskontroll när den har valts i Word-dokumentet.  

 ![Innehållskontroll för fält i Word-rapportlayout](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 Namnet på rubriken eller datafältet visas i innehållskontrollen. I exemplet är fältnamnet CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Så här tar du bort en rubrik eller ett datafält  

1.  Högerklicka på fältet som du vill ta bort och välj **Ta bort innehållskontroll**.  

     Innehållskontrollen tas bort, men fältnamnet förblir som text.  

2.  Ta bort den återstående texten efter behov.  

### <a name="adding-data-fields"></a>Lägga till datafält
Lägga till datafält från en -rapportdatauppsättning är mer avancerat och kräver viss kunskap om rapportdatauppsättningen. Information om att lägga till fält för data, etiketter, data och bilder finns i [Lägga till fält till en Word-rapportlayout](ui-how-add-fields-word-report-layout.md).  

###


## <a name="see-also"></a>Se även
[Hantera rapportlayouter](ui-manage-report-layouts.md)  
[Ändra aktuell rapportlayout](ui-how-change-layout-currently-used-report.md)  
[Så här importerar och exporterar du en anpassad rapport eller dokumentlayout](ui-how-import-and-export-report-layout.md)  
[Arbeta med rapporter och batch-jobb och XMLports](ui-work-report.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
