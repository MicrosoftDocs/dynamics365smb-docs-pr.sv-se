---
title: Skapa ett leverantörskort för att registrera en ny leverantör
description: I det här avsnittet lär du dig hur du skapar ett leverantörskort för registrering av en ny leverantör eller leverantör och hur du sparar leverantörskort som en mall.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 2d4943415af6f5cd91ac35c68a9d8433e024b6be
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445382"
---
# <a name="register-new-vendors"></a>Registrera nya leverantörer

Leverantörer erbjuder produkter som du säljer. Varje leverantör som du har köpt av måste registreras som ett leverantörskort.

Innan du kan registrera nya leverantörer, måste du lägga upp olika inköpskoder som du kan välja mellan, när du fyller i leverantörskort. När alla obligatoriska huvuddata skapats kan du konfigurera leverantören ytterligare, till exempel genom att prioritera leverantören i betalningssyfte och upprätta en lista över artiklar som leverantören och andra leverantörer kan tillhandahålla. En annan grupp av inställningsuppgifter för leverantörer är att lägga in dina avtal om inköpspris, rabatter och betalning. Mer information finns i [Konfigurera inköp](purchasing-setup-purchasing.md).

Leverantörskort innehåller den information som behövs för att köpa produkter från leverantören. Mer information finns i [Så här registrerar du inköp](purchasing-how-record-purchases.md) och [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).

> [!NOTE]  
> Om leverantörsmallar finns för olika leverantörstyper, visas en sida när du skapar ett nytt leverantörskort där du kan välja en lämplig mall. Om endast en leverantörsmall finns, då använder nya leverantörskort alltid den mallen.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Lägga till nya leverantörer

För att registrera en ny leverantör måste du fylla i ett leverantörskort. Du kan upprätta mallar för olika leverantörsprofiler eller lägga till leverantör utan mallar. Du kan också skapa en leverantör från en kontakt. Mer information finns i [Att skapa en kund, leverantör, anställd eller bankkonto från en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

> [!NOTE]  
> Om leverantörsmallar finns för olika leverantörstyper, visas en sida när du skapar ett nytt leverantörskort där du kan välja en lämplig mall. Om endast en leverantörsmall finns, då använder nya leverantörskort alltid den mallen.  

### <a name="to-create-a-new-vendor-card"></a>Skapa ett nytt leverantörskort.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.  
2. På sidan **Leverantörer** väljer du **Ny**.

    Om fler än en leverantörsmall finns, öppnas en sida där du kan välja leverantörsmall. I detta fall, följ nästa två steg.
    1. Välj den mall som du vill använda för den nya leverantörskortet på sidan **Välj en mall för en ny leverantör**.
    2. Välj **OK**. Ett nytt leverantörskort öppnas med några ifyllda fält med information från mallen.
3. Fortsätt att fylla i eller ändra fält på leverantörskortet vid behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > Om du inte vet vilken faktureringsadress som ska användas för respektive faktura från en leverantör fyller du inte i fältet **Leverantörsnr.**. Välj i stället betalningsleverantörens nummer när du har skapat en inköpsoffert, order eller ett inköpshuvud.

Leverantören är nu registrerad, och leverantörskortet är klart att användas i inköpsdokument.

Om du vill använda detta leverantörskort som en mall när du skapar nya leverantörskort, så fortsätt med att spara den som en leverantörsmall. Mer information finns i avsnittet [Så här sparar du leverantörskortet som en mall](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-vendor-cards"></a>Ta bort leverantörskort

Om du har bokfört en transaktion för en leverantör kan du inte ta bort kortet eftersom transaktionerna kan behövas för revision. Om du vill ta bort leverantörskort med transaktioner, kontaktar du Microsoft partner för att göra det via kod.

## <a name="to-save-the-vendor-card-as-a-template"></a>Om du vill spara leverantörskortet som en mall

1. På sidan **Leverantörskort** väljer du åtgärden **Spara som mall**. Sidan **leverantörsmall** öppnas uppvisar leverantörskortet som mall.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**. Sidan **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för leverantören.
4. Ändra eller ange dimensionskoder som ska kopplas till nya leverantörskort som skapas med hjälp av mallen.
5. Välj **OK** när du har slutfört den nya leverantörsmallen.  
   Leverantörsmallen läggs till listan över leverantörsmallar, så att du kan använda det för att skapa nya leverantörskort.

## <a name="see-also"></a>Se även

[Slå samman dubblettposter](sales-how-merge-duplicate-records.md)  
[Skapa nummerserier](ui-create-number-series.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]