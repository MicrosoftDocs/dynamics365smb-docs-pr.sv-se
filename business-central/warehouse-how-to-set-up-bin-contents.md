---
title: "Så här skapar du lagerplatsinnehåll | Microsoft Docs"
description: "När du har skapat lagerplatserna kan du skapa deras innehåll. Du kan ange de artiklar som du vill lagra på en viss lagerplats och ange regler som styr hur lagerplatsen ska fyllas med en viss artikel."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2182b34721a3272ce784986de200cc87f51c2c37
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-bin-contents"></a>Skapa lagerplatsinnehåll
När du har skapat lagerplatserna kan du skapa deras innehåll. Du kan ange de artiklar som du vill lagra på en viss lagerplats och ange regler som styr hur lagerplatsen ska fyllas med en viss artikel. Du kan göra detta manuellt i fönstret **lagerplatsinnehåll** eller automatiskt med fönstret **skapa lagerplatsinnehåll i kalkylarket**.

## <a name="to-create-bin-content-manually"></a>Så här skapar du lagerplatsinnehåll manuellt  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Lagerställen** och välj sedan relaterad länk.  
2.  Markera platsen där du vill skapa lagerplatsinnehållet och väljer åtgärden **Lagerplatser**.  
3.  Markera lagerplatsen där du vill skapa lagerplatsinnehållet och väljer åtgärden **Innehåll**.  
4.  För varje artikel som du vill lagra på lagerplatsen fyller du i en rad i fönstret **Lagerplatsinnehåll** med tillämplig information. Vissa av fälten har redan fyllts i med information om lagerplatsen.  
5.  Fyll först i fältet **Artikelnr** och sedan, om du använder dirigerad artikelinförsel och plockning, fyller du i andra fält som **Enhetskod**, **Max. ant.** och **Min. ant.**.  

Välj **Fast** fältet, om det behövs. Om lagerplatsen ska användas som standardlagerplats för artikeln markerar du fältet **Standardlagerplats**.  

Om du använder dirigerad artikelinförsel och plockning, och har angett rätt dimensionsinformation på artikelkortet om varje artikels enheter, kontrolleras det högsta antalet som du har angett i fönstret **Lagerplatsinnehåll** mot lagerplatsens fysiska lagringskapacitet. Sedan används lägsta och högsta antal när lagerplatspåfyllning beräknas och artikelinförsel föreslås.  

Om du markerar fältet **Fast** kopplar du artikeln till lagerplatsen. Det betyder att [!INCLUDE[d365fin](includes/d365fin_md.md)] försöker placera den här artikeln på lagerplatsen om det finns utrymme för den, och den post som kopplar artikeln till lagerplatsen sparas även om antalet på lagerplatsen är noll. Andra artiklar kan placeras på lagerplatsen, även om en viss artikel har kopplats till lagerplatsen. Andra objekt kan placeras på lagerplatsen, även om en viss artikel har kopplats till lagerplatsen.  

> [!NOTE]  
>  Du kan skapa flera lagerplatsinnehåll samtidigt i fönstret **Lagerplatsinnehålluppl kalkylark**.  

## <a name="to-create-bin-content-with-a-worksheet"></a>Så här skapar du lagerplatsinnehåll i kalkylarket:  
När du har skapat lagerplatserna kan du skapa det lagerplatsinnehåll som du vill ha på varje lagerplats i lagerplatsuppläggningskalkylarket.

1.  Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten") ange **Lagerplatsinnehålluppl kalkylark**, och välj sedan relaterad länk.  
2.  I fältet **Namn** i kalkylarkshuvudet väljer du kalkylarket för det lagerställe där du vill skapa lagerplatsinnehåll.  
3.  I fältet **Lagerplatskod** väljer du den lagerplatskod som du vill definiera lagerplatsinnehåll för.   

    Om lagerstället är inställt på dirigerad artikelinförsel och plockning fylls fälten som rör just den lagerplatsen i automatiskt, exempelvis **Lagerplatstyp**, **Dist.lager klasskod** och **Lagerplatsordning**. Detta är information som du måste ta hänsyn till när du definierar lagerplatsinnehållet.  
4.  Välj den artikel som du vill tilldela lagerplatsen och fyll i de fält som avser lagerplatsinnehållet. Om du använder dirigerad artikelinförsel och plockning, och vill använda funktionen **Beräkna lagerplatsåteranskaffning**, fyller du i **Max. ant.** och **Min. ant.**.  

    Om du vill att den här lagerplatsen ska väljas automatiskt för artikeln, även om lagerplatskvantiteten är **0** och alla övriga artikelinförselvillkor är lika, markerar du fältet **Fast**.  
5.  Upprepa steg tre till fyra för varje artikel som du vill tilldela till en lagerplats.  
6.  Välj åtgärden **Skriv ut** för att förhandsgranska och skriva ut det lagerplatsinnehåll som du har angett i kalkylarket. Fortsätt att revidera lagerplatsinnehållet tills du är nöjd.  
7.  När du är klar kan du välja åtgärden **skapa lagerplatsinnehåll**.  

I det här kalkylarket kan du arbeta med flera lagerplatsinnehållsrader för flera lagerplatser och på så sätt få en bra översikt över vad du placerar på olika lagerplatser i en viss zon, gång eller ställning.  

## <a name="see-also"></a>Se även
[Beräkna lagerplatsåteranskaffning](warehouse-how-to-calculate-bin-replenishment.md)    
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

