---
title: "Bearbeta affärsmöjligheter | Microsoft Docs"
description: "Beskriver bearbetning av försäljningsmöjligheter i Financials"
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 889ef028b34ddad52c978373a5dab4329d96c91f
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="processing-sales-opportunities"></a>Behandlar försäljningsmöjligheter
När du har skapat en affärsmöjlighet, finns det flera funktioner för att hantera affärsmöjligheten och flytta den igenom till färdigställande.

## <a name="view-opportunities"></a>Visa affärsmöjligheter.
De befintliga försäljningsmöjligheterna finns i fönstret **Affärsmöjlighetslista**. Det finns andra sätt att komma åt det här fönstret för att bearbeta affärsmöjligheter:

| Visa affärsmöjligheter för | Genom att |
| --- | --- |
| Alla säljare och kontakter |I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Affärsmöjlighetslista**, och välj sedan relaterad länk. |
| En viss säljare |I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **försäljningspersonal**, och välj sedan relaterad länk. Välj säljare, välj åtgärden **Affärsmöjligheter** och välj sedan åtgärden **Lista**. |
| En viss kontakt |I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kontakter**, och välj sedan relaterad länk. Välj kontakt från listan, välj åtgärden **Affärsmöjligheter**. |

Var och en av dessa uppgifter öppnar fönstret **Affärsmöjlighetslista**.

## <a name="close-opportunities"></a>Avsluta affärsmöjligheter
Du kan avsluta affärsmöjligheter när en förhandling är över. När du avslutar en affärsmöjlighet kan du ange om den har vunnits eller förlorats och anledningen till att avsluta den. Om du vill ange en orsak måste du lägga upp koder för avslutade affärsmöjligheter.

1. I fönstret **Affärsmöjlighetslista** väljer du affärsmöjlighet och väljer sedan åtgärden **Avsluta**. Fönstret **Avsluta affärsmöjlighet** öppnas.
2. Fyll i relevanta fält och välj sedan knappen **OK**.

   Fälten **Avslutskod affärsmöjlighet** och **Avslutsdatum** är obligatoriska fält och måste fyllas i innan du kan välja knappen **OK**.

   I fältet **Avslutskod affärsmöjlighet** kan du välja från en av de befintliga avslutskoder affärsmöjligheter eller lägga till en ny kod. Om du vill lägga till en ny kod väljer du **Välj från fullständig lista** i listrutan och väljer sedan **ny**. På den nya tomma raden fyller du i fälten **Kod**, **Typ** och **Beskrivning** och väljer sedan knappen **OK**.

## <a name="create-quotes-for-opportunities"></a>Skapa offerter för affärsmöjligheter
Du kan skapa försäljningsofferter för kontakter som inte är registrerade som kunder.

1. I fönstret **Affärsmöjlighetslista** väljer du affärsmöjlighet och väljer sedan åtgärden **Skapa försäljningsoffert**. Fönstret **Försäljningsoffert** visas.
2. Fyll i relevanta fält.

## <a name="create-sales-orders-for-opportunities"></a>Skapa försäljningsorder för affärsmöjligheter
Du kan skapa order från förs.offerter som du har skapat för affärsmöjligheter. Innan du kan skapa försäljningsorder till kontakterna måste du ska kontakten som en kund. Mer information finns i [Skapa en företagskontakt från kund, leverantör eller bankkonto från en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

1. Sök efter den affärsmöjligheten som du har skapat en försäljningsoffert för i fönstret **Affärsmöjlighetslista**.
2. Välj åtgärden **Skapa försäljningsoffert**. Fönstret **Förs.offert** öppnas och visar den förs.offert som du har tilldelat affärsmöjligheten.
3. Fyll i de extra fälten och välj sedan åtgärden **Skapa order**.

När du hanterar affärsmöjligheter kan du behöva skapa en offert för den kontakt som affärsmöjligheten är kopplad till.

## <a name="delete-opportunities"></a>Ta bort affärsmöjligheter
Du kan ta bort affärsmöjligheter när du till exempel har tagit hem en affär. Du kan bara ta bort avslutade affärsmöjligheter. Det finns två sätt att ta bort avslutade affärsmöjligheter. Du kan ta bort enskilda avslutade affärsmöjligheter från fönstret **Affärsmöjlighetslista** eller så kan du köra batch-jobbet **Ta bort avslutade affärsmöjligheter** för att ta bort flera affärsmöjligheter baserat på angivet kriterium.

Om du vill ta bort avslutade affärsmöjligheter från fönstret **Affärsmöjlighetslista** väljer du affärsmöjligheten och sedan åtgärden **Ta bort**.

Gör följande steg om du vill ta bort avslutade affärsmöjligheter med batch-jobbet **Ta bort avslutade affärsmöjligheter**:

1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Ta bort affärsmöjligheter**, och välj sedan relaterad länk.
2. I avsnittet **Affärsmöjlighet** ställer du in de filter som anger den avslutade affärsmöjligheten som ska tas bort.
3. Välj **OK**.

När du har tagit bort en affärsmöjlighet tas den bort från fönstret **Affärsmöjlighetslista**.

## <a name="move-an-opportunity-through-sales-cycle-stages"></a>Flytta en Affärsmöjlighet via försäljningscykeletapper
Om en affärsmöjlighet följer en försäljningscykel, kan du flytta den framåt eller bakåt via de olika etapperna, till exempel att flytta nästa eller föregående etapp och även hoppa över en etapp.

1. I fönstret **Affärsmöjlighetslista**, välj åtgärden **Uppdatera**. **Uppdatera affärsmöjlighet** visas.
2. Använd fältet **Åtgärdstyp** för att flytta affärsmöjligheten via försäljningscykeletapperna:
   * **Nästa** flyttar affärsmöjligheten en etapp.
   * **Hoppa över** flyttar affärsmöjligheten eftersänder en eller flera etapper i försäljningscykeln, som du anger i fältet **Presentation**. Du kan endast hoppa över etapper som har ställts in att tillåta fältet om du vill tillåta överhoppning.
   * **Föregående** flyttar affärsmöjligheten tillbaka en etapp.
   * **Hoppa** flyttar affärsmöjligheten tillbaka en eller flera etapper i försäljningscykeln, som du anger i fältet **Presentation**.
   * **Uppdatera** låter dig ändra information (t.ex. ändra utvärderingen av deras chanser att lyckas och uppskattade värden) utan att flytta till en annan etapp.
3. Fyll i de andra fälten efter behov och välj sedan knappen **OK**.

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Skapa och hantera kontakter](marketing-contacts.md)  
[Arbetar med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

