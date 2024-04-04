---
title: Skapa en försäljningsfaktura för att fakturera ett projekt
description: Beskriver hur du kan fakturera kunder för projektutgifter allt eftersom projektet fortskrider och kostnader ackumuleras.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: project invoice
ms.search.form: '1002, 1007,'
ms.date: 06/22/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Fakturera projekt

Under projektet kan projektkostnade från resursförbrukning, material och projektrelaterade inköp uppstå. Dessa transaktioner bokförs i projektjournalen. Det är viktigt att alla kostnader registreras i projektjournalen innan kunden faktureras.

> [!NOTE]
> Du kan också köpa externa resurser som inte är kopplade till ett projekt om du t. ex. vill fakturera en leverantör för levererat arbete. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).

Du kan fakturera hela projektet från sidan **Projektaktivitetsrader** eller fakturera endast valda fakturerbara rader på sidan **Planeringsrader**. Faktureringen kan göras när projektet har slutförts eller allt eftersom projektet fortlöper enligt ett faktureringsschema.

> [!NOTE]  
> Om du väljer **Fakturerbart** i fältet **Projektradtyp** på inköpsdokumentet för projektrelaterade inköp, skapas projektplaneringsrader som är klara att faktureras till kunden. Mer information finns i [Hantera projektleveranser](projects-how-manage-project-supplies.md).

Du kan också fakturera ett företag som inte är slutkunden. Ibland partiet som ett projekt är inte densamma som den part som betalar räkningen. På sidan **Projekt** kan du ange kunden som kommer att dra nytta av projektet i **Sälja till** och parten som ska faktureras i **Fakturera till**. 

## Så här skapar du flera försäljningsfakturor för projekt

Du kan skapa en faktura för ett projekt för en eller flera projektaktiviteter för en kund, antingen när det arbete som ska faktureras har slutförts eller när datumet för fakturering, som är baserat på ett faktureringsschema, har infallit.

Efterföljande procedur visar hur du kan använda ett batch-jobb för att fakturera flera projekt.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt – Skapa förs.faktura** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Ange filter om du vill begränsa de projekt som ska bearbetas av batch-jobbet.
4. Klicka på **OK** för att skapa fakturorna.  

Du kan granska och bokföra skapade fakturor i fönstret **Försäljningsfakturor**.

> [!NOTE]
> Du kan även fakturera en kund genom att välja jobbet och sedan åtgärden **Skapa försäljningsfaktura för projekt**. 

## Så här skapar och publicerar du en försäljningsfaktura för projekt från projektplaneringsrader

Du kan skapa en faktura från projektplaneringsrader och då ange antal av artikeln, resursen eller redovisningskontot som du vill fakturera.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.
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

## Se även

[Hantera projekt](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
