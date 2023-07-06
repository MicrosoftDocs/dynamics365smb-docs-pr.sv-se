---
title: Importerar många artikelbilder från en ZIP-fil
description: 'Bara ge bildfilerna namn som motsvarar dina artikelnummer, komprimera dem till en zip-fil och använd sedan sidan Importera artikelbilder för att importera flera artikelbilder.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'product, image'
ms.search.form: '30, 461'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="import-multiple-item-pictures"></a><a name="import-multiple-item-pictures"></a><a name="import-multiple-item-pictures"></a>Importera flera artikelbilder
Du kan importera flera artikelbilder samtidigt. Bara ge bildfilerna namn som motsvarar dina artikelnummer, komprimera dem till en zip-fil och använd sedan sidan Importera artikelbilder för att hantera vilka artikelbilder som ska importeras.

Alla vanliga filformat stöds.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>Namnge bildfiler med artikelnamnen och förbered ZIP-filen
1. På platsen där artikelbilderna sparas ska du namnge varje filnamn i enlighet med numret på den relaterade artikeln. Som exempel:

    |Artikelnr|Filnamn|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Samla alla filer i ZIP-filen. Till exempel i Windows Explorer, markerar du filerna och väljer **skicka till**, **komprimerad mapp**.     

## <a name="to-import-item-pictures"></a><a name="to-import-item-pictures"></a><a name="to-import-item-pictures"></a>För att importera artikelbilder
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **lagerinställning** och väljer sedan relaterad länk.
2. Välj åtgärden **Importera artikelbilder**.
3. I fältet **Välj en ZIP-fil** markerar du relevant ZIP-mapp och väljer sedan knappen **öppna**.

    En rad för varje artikel och bild skapas på sidan **Importera artikelbilder**.

    > [!NOTE]
    > För artikelkort som redan har en bild markeras kryssrutan **bilden finns redan**. Om du inte vill att några befintliga bilder ska bytas ut avmarkerar du kryssrutan **ersätta bilder**. Om du vill ta bort de enskilda befintliga bilderna som ska ersättas tar du bort de aktuella raderna.

3. Välj åtgärden **Importera bilder**.

Fältet **importstatus** uppdateras för att visa om bildimporten har hoppas över eller slutförts.       

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Skapa nummerserier](ui-create-number-series.md)  
[Lager](inventory-manage-inventory.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
