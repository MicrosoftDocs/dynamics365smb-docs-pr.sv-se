---
title: Bearbeta affärsmöjligheter i försäljningscykler | Microsoft Docs
description: Visa, stänga eller ta bort affärsmöjligheter och du kan skapa offerter och försäljningsorder för affärsmöjligheter och flytta en affärsmöjlighet genom försäljningscykelns olika faser.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: f58ea5c536ce8f1da0782cbebe6d1ef028bee137
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383931"
---
# <a name="process-sales-opportunities"></a>Behandla försäljningsmöjligheter
När du har skapat en affärsmöjlighet, finns det flera funktioner för att hantera affärsmöjligheten och flytta den igenom till färdigställande.

## <a name="to-view-opportunities"></a>Visa affärsmöjligheter.
De befintliga försäljningsmöjligheterna finns på sidan **Affärsmöjlighetslista**. Det finns andra sätt att komma åt denna sida för att bearbeta affärsmöjligheter:

| Visa affärsmöjligheter för | Då |
| --- | --- |
| Alla säljare och kontakter |Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Affärsmöjlighetslista** och välj sedan relaterad länk. |
| En viss säljare |Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Säljare** och välj sedan relaterad länk. Välj säljare, välj åtgärden **Affärsmöjligheter** och välj sedan åtgärden **Lista**. |
| En viss kontakt |Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Kontakter** och välj sedan relaterad länk. Välj kontakt från listan, välj åtgärden **Affärsmöjligheter**. |

Var och en av dessa uppgifter öppnar sidan **Affärsmöjlighetslista**.

## <a name="to-close-opportunities"></a>Avsluta affärsmöjligheter
Du kan avsluta affärsmöjligheter när en förhandling är över. När du avslutar en affärsmöjlighet kan du ange om den har vunnits eller förlorats och anledningen till att avsluta den. Om du vill ange en orsak måste du lägga upp koder för avslutade affärsmöjligheter.

1. På sidan **Affärsmöjlighetslista** väljer du affärsmöjlighet och väljer sedan åtgärden **Avsluta**. Sidan **Avsluta affärsmöjlighet** öppnas.
2. Fyll i relevanta fält och välj sedan knappen **OK**.

   Fälten **Avslutskod affärsmöjlighet** och **Avslutsdatum** är obligatoriska fält och måste fyllas i innan du kan välja knappen **OK**.

   I fältet **Avslutskod affärsmöjlighet** kan du välja från en av de befintliga avslutskoder affärsmöjligheter eller lägga till en ny kod. Om du vill lägga till en ny kod väljer du **Välj från fullständig lista** i listrutan och väljer sedan **ny**. På den nya tomma raden fyller du i fälten **Kod**, **Typ** och **Beskrivning** och väljer sedan knappen **OK**.

## <a name="to-create-quotes-for-opportunities"></a>Skapa offerter för affärsmöjligheter
Du kan skapa försäljningsofferter för kontakter som inte är registrerade som kunder.

1. På sidan **Affärsmöjlighetslista** väljer du affärsmöjlighet och väljer sedan åtgärden **Skapa försäljningsoffert**. Sidan **Försäljningsoffert** visas.
2. Fyll i relevanta fält.

## <a name="to-create-sales-orders-for-opportunities"></a>Skapa försäljningsorder för affärsmöjligheter
Du kan skapa order från förs.offerter som du har skapat för affärsmöjligheter. Innan du kan skapa försäljningsorder till kontakterna måste du ska kontakten som en kund. Mer information finns i [Skapa kontakter](marketing-create-contact-companies.md).

1. Sök efter den affärsmöjligheten som du har skapat en försäljningsoffert för på sidan **Affärsmöjlighetslista**.
2. Välj åtgärden **Skapa försäljningsoffert**. Sidan **Förs.offert** öppnas och visar den förs.offert som du har tilldelat affärsmöjligheten.
3. Fyll i de extra fälten och välj sedan åtgärden **Skapa order**.

När du hanterar affärsmöjligheter kan du behöva skapa en offert för den kontakt som affärsmöjligheten är kopplad till.

## <a name="to-delete-opportunities"></a>Ta bort affärsmöjligheter
Du kan ta bort affärsmöjligheter när du till exempel har tagit hem en affär. Du kan bara ta bort avslutade affärsmöjligheter. Det finns två sätt att ta bort avslutade affärsmöjligheter. Du kan ta bort enskilda avslutade affärsmöjligheter från sidan **Affärsmöjlighetslista** eller så kan du köra batch-jobbet **Ta bort avslutade affärsmöjligheter** för att ta bort flera affärsmöjligheter baserat på angivet kriterium.

Om du vill ta bort avslutade affärsmöjligheter från sidan **Affärsmöjlighetslista** väljer du affärsmöjligheten och sedan åtgärden **Ta bort**.

Gör följande steg om du vill ta bort avslutade affärsmöjligheter med batch-jobbet **Ta bort avslutade affärsmöjligheter**:

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Ta bort affärsmöjligheter** och välj sedan relaterad länk.
2. I avsnittet **Affärsmöjlighet** ställer du in de filter som anger den avslutade affärsmöjligheten som ska tas bort.
3. Välj **OK**.

När du har tagit bort en affärsmöjlighet tas den bort från sidan **Affärsmöjlighetslista**.

## <a name="to-move-an-opportunity-through-sales-cycle-stages"></a>Flytta en Affärsmöjlighet via försäljningscykeletapper
Om en affärsmöjlighet följer en försäljningscykel, kan du flytta den framåt eller bakåt via de olika etapperna, till exempel att flytta nästa eller föregående etapp och även hoppa över en etapp.

1. På sidan **Affärsmöjlighetslista**, välj åtgärden **Uppdatera**. **Uppdatera affärsmöjlighet** visas.
2. Använd fältet **Åtgärdstyp** för att flytta affärsmöjligheten via försäljningscykeletapperna:
   * **Nästa** flyttar affärsmöjligheten en etapp.
   * **Hoppa över** flyttar affärsmöjligheten eftersänder en eller flera etapper i försäljningscykeln, som du anger i fältet **Presentation**. Du kan endast hoppa över etapper som har ställts in att tillåta fältet om du vill tillåta överhoppning.
   * **Föregående** flyttar affärsmöjligheten tillbaka en etapp.
   * **Hoppa** flyttar affärsmöjligheten tillbaka en eller flera etapper i försäljningscykeln, som du anger i fältet **Presentation**.
   * **Uppdatera** låter dig ändra information (t. ex. ändra utvärderingen av deras chanser att lyckas och uppskattade värden) utan att flytta till en annan etapp.
3. Fyll i de andra fälten efter behov och välj sedan knappen **OK**.

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Skapa och hantera kontakter](marketing-contacts.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]