---
title: "Så här skapar du nummerserier | Microsoft Docs"
description: "Lära dig hur du anger nummerserier, som tilldelar unika ID-koder till konton och dokument i Dynamics 365 for Financials."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7cc119c5879400adf63e468259a2c3a275b71cca
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-number-series"></a>Så här skapar du nummerserier
För varje företag som du lägger upp måste du tilldela unika ID-koder till exempelvis redovisningskonton, kund- och leverantörskonton, fakturor och dokument. Numrering är viktigt inte enbart för identifiering. Ett adekvat numreringssystem gör också företaget mer hanterbart och enkelt att analysera, och kan minska antalet fel som uppstår vid datainmatning.

> [!NOTE]  
>   Vi rekommenderar att du använder samma nummerserie som du ser i fönstret **Nr-serielista** i demonstrationsföretaget CRONUS. Koder som *P-INV+* kanske inte passar direkt, men [!INCLUDE[d365fin](includes/d365fin_md.md)] har flera standardinställningar som hör ihop med dessa nummerseriekoder.

Du skapar ett numreringssystem genom att skapa en eller flera koder för varje typ av huvuddata eller dokument. Du kan till exempel skapa en kod för numrering av kunder, en annan för numrering av försäljningsfakturor och en annan för numrering av dokument i redovisningsjournaler. När du har skapat en kod måste du skapa minst en nummerserierad. Nummerserieraden innehåller information som första och sista nummer i serien och startdatum. Du kan registrera flera nummerserierader per nummerseriekod, med olika startdatum på varje rad. Nummerserierna används löpande, med början på respektive startdatum.

Du ställer normalt in nummerserier till att automatiskt infoga nästa nummer på nya kort eller dokument som du skapar. Men kan du också skapa en nummerserie för att manuellt ange det nya numret. Du anger detta med **Manuell numrering.** .

Om du vill använda mer än en nummerseriekod för en typ av huvuddata, till exempel om du vill använda olika nummerserier för olika kategorier med artiklar, kan du använda nummerseriesamband.

## <a name="to-create-a-new-number-series"></a>Så här skapar du nummerserier
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Nr-serier** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Tips**: för att ange ett nummer på nytt kort eller dokument manuellt måste du avmarkera den **standard nr.** Markera kryssrutan och markera **Manuell numrering.** .

Nu när du skapar ett nytt kort eller dokument som har konfigurerats till att använda den aktuella nummerserien, kan du manuellt fylla i fältet **nr.** med något värde.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Om du vill konfigurera var en nummerserie används
I följande procedur beskrivs hur du ställer in nummerserier för området Försäljning. Stegen är liknande för andra områden.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Försäljning & kundreskontra** och välj sedan relaterad länk.
2. I fönstret **försäljning** klickar du på snabbfliken **nr-serier** och väljer önskade nummerserier för varje försäljningskort och dokument.

Det markerade numret kommer nu att användas för att fylla i fältet **nr.** på kortet eller dokumentet i fråga enligt de inställningar du har gjort på nummerserieraden.

## <a name="to-create-relationships-between-number-series"></a>Så här skapar du samband mellan nummerserier
Om du har definierat mer än en nummerseriekod för samma typ av allmän information eller transaktioner kan du skapa samband mellan koderna. Den här funktionen gör det enklare för dig att välja bland koderna när du använder ett nummer.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Nr-serier** och välj sedan relaterad länk.
2. Markera raden med de nummerserier som du vill skapa relationer för och välj sedan **Relationer**.
3. I fältet **Seriekod** anger du koden för nummerserien som du vill koppla till serien du valde i steg 2.
4. Lägg till en rad för varje kod som du vill koppla till den valda nummerserien.
5. Stäng fönstret.

När du hädanefter definierar något för vilket ett nummer krävs kan du använda sambanden som har skapats för att välja bland de kopplade nummerserierna.

## <a name="see-also"></a>Se även
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

