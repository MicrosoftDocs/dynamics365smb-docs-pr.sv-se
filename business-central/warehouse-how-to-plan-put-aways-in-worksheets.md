---
title: Planera artikelinförsel i kalkylarket | Microsoft Docs
description: Du kan använda artikelinförselkalkylarket om lagerstället kräver både artikelinförsel- och inleveransbearbetning, och du vill planera artikelinförselinstruktioner för flera inleveranser, i stället för att låta personalen följa de instruktioner som har skapats i programmet för separata bokförda inleveranser.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e0674c0c308cd83de8a6977e05445c22009f513c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "807044"
---
# <a name="plan-put-aways-in-worksheets"></a>Planera artikelinförsel i kalkylark
Du kan använda artikelinförselkalkylarket om lagerstället kräver både artikelinförsel- och inleveransbearbetning, och du vill planera artikelinförselinstruktioner för flera inleveranser, i stället för att låta personalen följa de instruktioner som har skapats i programmet för separata bokförda inleveranser.  

Om du vill lägga upp distributionslagret så att inleveransrader visas i artikelinförselkalkylarket så snart de har bokförts, markerar du fältet **Använd artikelinförselkalkylark** på snabbfliken **Dist.lager** på lagerställekortet. Mer information finns i [Ställa in Lagerstyrning](warehouse-setup-warehouse.md).  

Om du inte markerar fältet skapas automatiskt artikelinförselinstruktioner för inleveranser när de har bokförts.  

> [!NOTE]  
>  Oavsett statusen på fältet **Använd artikelinförselkalkylark** på lagerställekortet kan du alltid hämta instruktionsrader för artikelinförsel, d.v.s. bokförda inleveransrader, till artikelinförselkalkylarket genom att göra så här:  
>   
>  1.  På sidan **Dist.lager artikelinförsel** trycker du på Ctrl+D för att ta bort hela artikelinförselinstruktionen, eller markerar de rader som du vill behandla i kalkylarket och tar bort dem.  
> 2.  Fortsätt med det i så många artikelinförslar som du vill, tills du har tagit bort de rader om du vill arbeta med i kalkylarket. Välj nu **Artikelinförselkalkylark** och fortsätt planeringen.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>Så här planerar du instruktioner i artikelinförselkalkylarket  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artikelinförselförslag** och välj sedan relaterad länk.  
2.  Välj åtgärden **Hämta dist.lager dokument**. Sidan **Artikelinförselval** öppnas.  

    Alla bokförda inleveranser och registrerade interna artikelinförslar som har vidarebefordrats till artikelinförselfunktionen visas, däribland de som artikelinförselinstruktioner redan har skapats för. Dokument med artikelinförselrader som är klara och registrerade visas inte i den här listan.  

3. Välj de dokument som du vill arbeta med i förslaget. Du kan arbeta med rader från flera dokument samtidigt.  

    > [!NOTE]  
    >  Om du försöker välja ett inleverans- eller intern artikelinförseldokument, som du redan har skapat instruktioner för, för alla rader i dokumentet, får du information om att det inte finns någonting att hantera.  

4. Fyll i fältet **Sorteringsmetod** för att sortera raderna som du vill ha dem.  

    > [!NOTE]  
    >  Det sätt som raderna sorteras på i kalkylarket återspeglas inte automatiskt i artikelinförselinstruktionen, men samma sorteringsmöjligheter finns, tillsammans med lagerplatssortering. Den radsortering som du planerar i kalkylarket är därför enkel att återskapa när du skapar artikelinförselinstruktioner, eller genom att sortera artikelinförselinstruktionerna.  

5.  Fyll i fältet **Ant. att hantera**. Välj åtgärden **Fyll i auto. ant. att hantera** eller fyll i fälten manuellt.  
6.  Redigera raderna manuellt vid behov. Du kan ta bort rader om exempelvis vissa artiklar måste föras in på en lagerplats som ligger långt bort från övriga artiklars lagerplatser.  

    > [!NOTE]  
    >  De rader som tas bort tas endast bort från det här förslaget, inte från urvalslistan för artikelinförslar.  

7.  Välj åtgärden **Skapa artikelinförsel**. Sidan **Skapa dokument** öppnas, där kan du lägga till ytterligare information i artikelinförseln som du skapar, enligt följande:  

    -   Du kan fördela artikelinförseln till en särskild anställd.  
    -   Du kan sortera instruktionsraderna för artikelinförsel som du gjorde i kalkylarket eller genom att använda funktionen Lagerplatsordning. När du sorterar enligt lagerplatsordningen visas hämtningsraderna först eftersom de flesta inleveranslagerplatser har lagerplatsordning 0, och placeringsraderna visas sist, med de lagerplatser som har lägst lagerplatsordning högst upp i listan. Om du har strukturerat distributionslagret så att lagerplatser med liknande lagerplatsordning ligger bredvid varandra slipper personalen gå så mycket om du sorterar raderna på det här sättet.  
    -   Du kan välja att inte visa de övergångsrader som skapas när en större enhet bryts ned till mindre enheter, genom att markera fältet **Sätt brytenhetsfilter**. Mer information finns i [Aktivera Automatisk volymnedbrytning med dirigerad artikelinförsel och plockning](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    -   Du kan välja att inte låta fältet **Ant. att hantera** fyllas i automatiskt för artikelinförselinstruktionerna.  
    -   Du kan välja att skriva ut dokumentet omedelbart.  

8.  Välj knappen **OK** så skapas artikelinförseln enligt dina önskemål.  

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
