---
title: "Så här bokför du preliminära fakturor med ankomstregistrering"
description: "Med en ankomstregistrering kan du bokföra en preliminär inköpsfaktura, som du senare skriver över när du bokför fakturan som vanligt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6da6ed40c805645e1b41a64b7349c733ea7b950e
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="post-preliminary-invoices-by-using-inward-registration"></a>Så här bokför du preliminära fakturor med ankomstregistrering
Med en ankomstregistrering kan du bokföra en preliminär inköpsfaktura, som du senare skriver över när du bokför fakturan som vanligt. Mer information finns i Ankomstregistrering.  

## <a name="to-post-a-preliminary-invoice"></a>Så här bokför du en preliminär faktura  

1.  Välj ikonen ![Söka efter sida eller rapport](../../media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Inköpsfakturor** och välj sedan relaterad länk.  
2.  Välj en faktura eller skapa en ny faktura.  
3.  Välj åtgärd **Ankomstregistrering**.  
4.  Välj **Ny**, ange ett leverantörsfakturanummer i huvudet i fönstret **Ankomstregistrering** och fyll sedan i raderna på det sätt som beskrivs i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Moms produktbokföringsmall**|Ange en momsbokföringsmall. Den här koden används tillsammans med rörelsebokföringsmallen för moms för att hämta momssatsen och momsberäkningstypen.|  
    |**Produktbokföringsmall**|Ange en generell bokföringsmall.|  

5.  Om du vill bokföra preliminära fakturan väljer du åtgärden **Bokför**.  
6.  Välj **Ja** för att bekräfta att du vill bokföra ankomstregistreringen.  

Nu skapas en ankomstregistrering. Den representerar den preliminära fakturabokföringen tills du senare skriver över den med den slutgiltiga fakturabokföringen. Du kan visa den positiva transaktionen som skapas i fönstret **Ankomstreg.trans.**.  

Om du vill ångra ankomstregistreringen före den slutgiltiga fakturabokföringen måste du återföra ankomstregistreringen manuellt. Mer information finns i [Så här återför du preliminära fakturor med ankomstregistrering](how-to-reverse-preliminary-invoices-by-using-inward-registration.md)  

## <a name="see-also"></a>Se även  
 [Registrera inköp](../../purchasing-how-record-purchases.md)   
 [Så här återför du preliminära fakturor genom att använda ankomstregistrering](how-to-reverse-preliminary-invoices-by-using-inward-registration.md)   
 [Rapportera moms till skattemyndigheterna](../../finance-how-report-vat.md)   
 [Lokal funktionalitet för Sverige](sweden-local-functionality.md)

