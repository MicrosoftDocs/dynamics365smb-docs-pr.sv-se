---
title: Skapa en försäljningsfaktura för att fakturera ett projekt | Microsoft Docs
description: Beskriver hur du kan fakturera kunder för projektutgifter allt eftersom projektet fortskrider.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 368b0b1edf1105045a365d8d5ac523c88955ad8a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758748"
---
# <a name="invoice-jobs"></a>Fakturera projekt
Under projektet kan projektkostnade från resursförbrukning, material och projektrelaterade inköp uppstå. Dessa transaktioner bokförs i projektjournalen. Det är viktigt att alla kostnader registreras i projektjournalen innan kunden faktureras.

> [!NOTE]
> Du kan också köpa externa resurser som inte är kopplade till ett projekt om du t. ex. vill fakturera en leverantör för levererat arbete. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).

Du kan fakturera hela projektet från sidan **Projektaktivitetsrader** eller fakturera endast valda fakturerbara rader på sidan **Planeringsrader**. Faktureringen kan göras när projektet har slutförts eller allt eftersom projektet fortlöper enligt ett faktureringsschema.

> [!NOTE]  
> Om du väljer **Fakturerbart** i fältet **Projektradtyp** på inköpsdokumentet för projektrelaterade inköp, skapas projektplaneringsrader som är klara att faktureras till kunden. Mer information finns i [Hantera projektleveranser](projects-how-manage-project-supplies.md).

## <a name="to-create-multiple-job-sales-invoices"></a>Så här skapar du flera försäljningsfakturor för projekt
Du kan skapa en faktura för ett projekt för en eller flera projektaktiviteter för en kund, antingen när det arbete som ska faktureras har slutförts eller när datumet för fakturering, som är baserat på ett faktureringsschema, har infallit.

Efterföljande procedur visar hur du kan använda ett batch-jobb för att fakturera flera projekt.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Skapa försäljningsfaktura för jobb** och välj sedan tillhörande länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Ange filter om du vill begränsa de projekt som ska bearbetas av batch-jobbet.
4. Klicka på **OK** för att skapa fakturorna.  

Du kan granska och bokföra skapade fakturor i fönstret **Försäljningsfakturor**.

> [!NOTE]
> Du kan även fakturera en kund genom att välja jobbet och sedan åtgärden **Skapa försäljningsfaktura för projekt**. 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a>Så här skapar och publicerar du en försäljningsfaktura för projekt från projektplaneringsrader
Du kan skapa en faktura från projektplaneringsrader och då ange antal av artikeln, resursen eller redovisningskontot som du vill fakturera.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt** och välj sedan tillhörande länk.
2. Öppna ett relevant projekt.
3. Markera ett projekt där fältet **Typ av projektaktivitet** innehåller **Bokföring** och klicka sedan på åtgärden **Projektplaneringsrader**.  
4. Gå till fältet **Antal att överföra till faktura** på en projektplaneringsrad och ange antal av artikeln, resursen, typen av redovisningskonto som du vill fakturera.  
5. Välj åtgärden **Skapa försäljningsfaktura**.
6. På sidan **Projekt – Skapa förs.faktura** anger du bokföringsdatum och om du vill skapa en ny faktura eller koppla denna faktura till en befintlig.
7. Välj **OK**.  
8. På sidan **Projektplaneringsrader** väljer du åtgärden **Försäljningsfakturor/kreditnotor**.

    Sidan **Försäljningsfaktura** öppnas och visar antalet som du har överfört till fakturan.
9. Gör ytterligare ändringar och välj sedan åtgärden **Bokför**.

> [!NOTE]  
>   Ovanstående process är liknande för att skapa, granska och publicera en projektrelaterad försäljningskreditnota.

## <a name="to-calculate-and-post-job-completion-entries"></a>Beräkna och bokföra slutförda projekt
När du har slutfört alla aktiviteter i ett projekt, bland annat bokföringen och faktureringen av förbrukning, måste du uppdatera projektet så att projektet får **Statusen** **Slutförd**. Sedan måste du återföra alla PIA som har bokförs i redovisningen.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Projekt** och välj sedan tillhörande länk.  
2. Välj ett öppet projekt och välj sedan åtgärden **Redigera**.
3. Markera **Slutförd** i fältet **Status** .
4. Följ hjälpstegen steg för att beräkna och bokföra PIA. Följ alternativt steg 5 och 6 för att göra det manuellt.  
5. Välj åtgärden **Beräkna PIA**.
6. På sidan **Projekt – Beräkna PIA** fyller du i fälten efter behov.  

     De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.  
7. Välj åtgärden **Projekt – Bokför PIA i redovisning**.
8. På sidan **Projekt – Bokför PIA i redovisning** fyller du i fälten efter behov.  

     De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.

## <a name="see-also"></a>Se även
[Hantera projekt](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)         
[Försäljning](sales-manage-sales.md)      
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]