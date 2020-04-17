---
title: Så här arbetar du med ansvarsenheter | Microsoft Docs
description: Med ansvarsenheterna kan användarna hantera administrativa enheter. En ansvarsenhet kan vara ett kostnadsställe, en vinstenhet, en investeringsenhet eller en annan typ av administrativ enhet som har definierats av företaget.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9aea2f4af1e7b8095d6768de94ae6b3c46479f80
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181802"
---
# <a name="work-with-responsibility-centers"></a>Arbeta med ansvarsenheter
Med ansvarsenheterna kan användarna hantera administrativa enheter. En ansvarsenhet kan vara ett kostnadsställe, en vinstenhet, en investeringsenhet eller en annan typ av administrativ enhet som har definierats av företaget. Exempel på ansvarsenheter är ett försäljningskontor, en inköpsavdelning för flera lagerställen och en fabriks planeringskontor. Med den här funktionen kan företagen till exempel ställa in användarspecifika vyer för försäljnings- och inköpsdokument som endast kan kopplas till en viss ansvarsenhet.  

Genom att använda funktionen för flera lagerställen och ansvarsenheter i kan företagen med utlokaliserad verksamhet sköta affärsverksamheten på ett mycket flexibelt men också optimalt sätt.

Om funktionen för flera lagerställen används kan företagen sköta lagerhanteringen för flera lagerställen i en enda databas. De två koncepten - lagerställena och lagerställeenheterna - är hörnstenar i den här underavdelningen. Den fysiska placeringen och artikelantalen hanteras på ett lagerställe. Konceptet är omfattande och kan därför inkludera lagerställen i form av anläggningar eller produktionsinrättningar, men också i form av distributionscenter, distributionslager, utställningslokaler och servicefordon. En lagerställeenhet definieras som en artikel på ett specifikt lagerställe och/eller som en variant. Företagen med flera lagerställen kan, om de använder lagerställeenheter, lägga till återanskaffningsinformation, adresser samt information om ekonomisk bokföring på lagerställenivå. Detta medför att de kan återanskaffa varianter av samma artikel för varje lagerställe och att de kan beställa artiklar för varje lagerställe utifrån återanskaffningsinformation som är specifik för lagerstället.  

Ansvarsenheterna ger funktionen för flera lagerställen en ännu större omfattning eftersom användarna då kan hantera administrativa enheter. En ansvarsenhet kan vara ett kostnadsställe, en vinstenhet, en investeringsenhet eller en annan typ av administrativ enhet som har definierats av företaget. Exempel på ansvarsenheter är ett försäljningskontor, en inköpsavdelning för flera lagerställen och en fabriks planeringskontor. Med den här funktionen kan företagen till exempel ställa in användarspecifika vyer för försäljnings- och inköpsdokument som endast kan kopplas till en viss ansvarsenhet.

## <a name="to-set-up-a-responsibility-center"></a>Så här skapar du en ansvarsenhet  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **ansvarsenhet** och välj sedan relaterad länk.  
2.  Välj åtgärden **Ny**.  
3.  Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Om du använder ansvarsenheter för att administrera ditt företag kan det vara praktiskt att ange en standardansvarsenhet för företaget.
4. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Företagsinformation** och välj sedan relaterad länk.
5. I fältet **ansvarsenhet** anger du en ansvarsenhetskod.

Den här koden används på alla inköps- försäljnings- och servicedokument om användaren, kunden eller leverantören inte har någon standardansvarsenhet. På ett försäljnings-, inköps- eller servicedokument, kan du ange en annan ansvarsenhet än standard.

> [!NOTE]  
>  När du anger en ansvarsenhetskod i ett dokument, påverkas adressen, dimensionerna och priserna i dokumentet.  

## <a name="to-assign-responsibility-centers-to-users"></a>Så här tilldelar du ansvarsenheter till användare  
Du kan definiera användare så att endast de dokument som är relevanta inom deras arbetsområden hämtas som standard. Användare associeras vanligtvis med en ansvarsenhet och arbetar normalt sett endast med dokument som är knutna till särskilda moduler inom just den ansvarsenheten.  

Du anger dessa inställningar genom att tilldela ansvarsenheter till användare inom tre olika huvudområden: Inköp, Försäljning och Servicehantering.  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Användarinställningar** och välj sedan relaterad länk.  
2.  På sidan **Användarinställning** markerar du den användare som du vill tilldela en ansvarsenhet till. Om användaren inte finns med i listan anger du ett användar-ID i fältet **Användar-ID**.  
3.  I fältet **Förs.ansvarsenhet filter** anger du den ansvarsenhet i vilken användaren ska tilldelas försäljningsrelaterade uppgifter.  
4.  I fältet **Inköpsansvarsenhet filter** anger du den ansvarsenhet i vilken användaren ska tilldelas inköpsrelaterade uppgifter.  
5.  I fältet **Serviceansvarsenhet filter** anger du den ansvarsenhet i vilken användaren ska tilldelas servicerelaterade uppgifter.  

> [!NOTE]  
>  Användaren kan fortfarande visa alla bokförda dokument och transaktioner och inte bara de som är kopplade till hans eller hennes ansvarsenhet.

## <a name="see-also"></a>Se även  
[Ställa in lager](inventory-setup-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)
[lager](inventory-manage-inventory.md)[lagerstyrning](warehouse-manage-warehouse.md)  
[Lagerstyrning](warehouse-manage-warehouse.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
