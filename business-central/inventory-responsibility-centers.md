---
title: 'Så här: Arbeta med ansvarsenheter'
description: Ansvarsenhet som administrativa centraler hjälper företag att skapa användarspecifika vyer över försäljnings- och inköpsdokument som är relaterade uteslutande till varje centrum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 5714, 5715
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 3aabc4f60d30d6a5eaef838fa1b8b03e58c2341d
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530007"
---
# <a name="work-with-responsibility-centers"></a>Arbeta med ansvarsenheter

Med ansvarsenheterna kan användarna hantera administrativa enheter. En ansvarsenhet kan vara ett kostnadsställe, en vinstenhet, en investeringsenhet eller en annan typ av administrativ enhet som har definierats av företaget. Exempel på ansvarsenheter är ett försäljningskontor, en inköpsavdelning för flera lagerställen och en fabriks planeringskontor. Med den här funktionen kan företagen till exempel ställa in användarspecifika vyer för försäljnings- och inköpsdokument som endast kan kopplas till en viss ansvarsenhet.  

Genom att använda funktionen för flera lagerställen och ansvarsenheter i kan företagen med utlokaliserad verksamhet sköta affärsverksamheten på ett mycket flexibelt men också optimalt sätt.

Om funktionen för flera lagerställen används kan företagen sköta lagerhanteringen för flera lagerställen i en enda databas. De två koncepten – lagerställena och lagerställeenheterna – är hörnstenar i den här underavdelningen. Den fysiska placeringen och artikelantalen hanteras på ett lagerställe. Konceptet är omfattande och kan därför inkludera lagerställen i form av anläggningar eller produktionsinrättningar, men också i form av distributionscenter, distributionslager, utställningslokaler och servicefordon. En lagerställeenhet definieras som en artikel på ett specifikt lagerställe och/eller som en variant. Företagen med flera lagerställen kan, om de använder lagerställeenheter, lägga till återanskaffningsinformation, adresser samt information om ekonomisk bokföring på lagerställenivå. Detta medför att de kan återanskaffa varianter av samma artikel för varje lagerställe och att de kan beställa artiklar för varje lagerställe utifrån återanskaffningsinformation som är specifik för lagerstället.  

## <a name="to-set-up-a-responsibility-center"></a>Så här skapar du en ansvarsenhet

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **ansvarsenheter** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Om du använder ansvarsenheter för att administrera ditt företag kan det vara praktiskt att ange en standardansvarsenhet för företaget.
4. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Företagsinformation** och väljer sedan relaterad länk.
5. I fältet **ansvarsenhet** anger du en ansvarsenhetskod.

Den här koden används på alla inköps- försäljnings- och servicedokument om användaren, kunden eller leverantören inte har någon standardansvarsenhet. På ett försäljnings-, inköps- eller servicedokument, kan du ange en annan ansvarsenhet än standard.

> [!NOTE]  
> När du anger en ansvarsenhetskod i ett dokument, påverkas adressen, dimensionerna och priserna i dokumentet.  

## <a name="to-assign-responsibility-centers-to-users"></a>Så här tilldelar du ansvarsenheter till användare

Du kan definiera användare så att endast de dokument som är relevanta inom deras arbetsområden hämtas som standard. Användare associeras vanligtvis med en ansvarsenhet och arbetar normalt sett endast med dokument som är knutna till särskilda moduler inom just den ansvarsenheten.  

Du anger dessa inställningar genom att tilldela ansvarsenheter till användare inom tre olika huvudområden: Inköp, Försäljning och Servicehantering.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Användarinställning** och väljer sedan relaterad länk.  
2. På sidan **Användarinställning** markerar du den användare som du vill tilldela en ansvarsenhet till. Om användaren inte finns med i listan anger du ett användar-ID i fältet **Användar-ID**.  
3. I fältet **Förs.ansvarsenhet filter** anger du den ansvarsenhet i vilken användaren ska tilldelas försäljningsrelaterade uppgifter.  
4. I fältet **Inköpsansvarsenhet filter** anger du den ansvarsenhet i vilken användaren ska tilldelas inköpsrelaterade uppgifter.  
5. I fältet **Serviceansvarsenhet filter** anger du den ansvarsenhet i vilken användaren ska tilldelas servicerelaterade uppgifter.  

> [!NOTE]  
> Användarna kan bara visa de bokförda dokument som har samband med användarens egen ansvarsenhet. De kan emellertid visa alla reskontratransaktioner och navigera till andra bokförda dokument från reskontratransaktionerna.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/set-up-responsibility-centers/)

## <a name="see-also"></a>Se även

[Ställa in lager](inventory-setup-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
