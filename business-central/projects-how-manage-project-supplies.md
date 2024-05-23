---
title: Hantera projektleveranser
description: Beskriver olika sätt hur du hanterar försörjning och inköp av material och tjänster för projekt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Hantera projektleveranser

Du bör hantera projektleveranser av artiklar, tjänster och utgifter som en integrerad och kritisk aspekt av alla projekt. Du kan använda lagerantal eller göra projektspecifika inköp med hjälp av inköpsorder eller inköpsfakturor. Ett serviceprojekt på en dator kräver till exempel en ny disk. Du skapar då en inköpsfaktura för att köpa en ny hårddisk registrerar projektet som använder det.

Om inköpsprocessen inte kräver att du registrerar den fysiska transaktionen separat, kan du behandla ett köp på sidan **Projektredovisningsjournal**. Mer information finns i [Så här bokför du en projektrelaterad utgift](projects-how-manage-project-supplies.md#to-post-a-project-related-expense).

## Köpa artiklar eller tjänster till ett projekt

Efterföljande procedur visar hur du använder en inköpsfaktura för att köpa produkter till ett projekt. Samma steg gäller när du använder en inköpsorder.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsfakturor** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll i fälten efter behov. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md).
3. I fältet **Projektnr.** I fälten **Projektaktivitetsnr.** väljer du informationen för det projekt som du vill köpa artiklar eller tjänster för. Använd anpassningsverktygen om ett fält inte syns. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

    Värdet som du väljer i fältet **Projektradtyp** definierar om en planeringsrad skapas när du bokför artikelförbrukningen. Om fältet innehåller **Fakturerbart** skapas projektplaneringsrader som är klara att faktureras till kunden. Mer information finns i [Fakturaprojekt](projects-how-invoice-jobs.md).
4. Välj åtgärden **Bokföra**.

## Visa värdet på inköp till ett projekt

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Projekt** och välj sedan relaterad länk.
2. Öppna ett relevant projektkort.

    På snabbfliken **Uppgifter** visar fältet **Utestående order** det totala utestående beloppet, i lokal valuta, för lagerartiklar och tjänster för inköpsdokument för projektaktivitetsraden.  

    Fältet **Inlevererat bel. ej faktrd** visar värdet för artiklarna som har levererats på inköpsdokument, men ännu inte har fakturerats.  
3. Välj något av fälten för att öppna sidan **Inköpsrader** där du kan granska information om relaterade inköpsdokumentrader, bland annat vilka artiklar eller tjänster som har inlevererats.

## Så här bokför du en projektrelaterad utgift

Om du ådrar dig extraordinära eller engångsutgifter för projekt kan du använda sidan **Projektredovisningsjournal** för att bokföra dem direkt till det relevanta projektkontot.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projektredovisningsjournaler** och väljer sedan relaterad länk.  
2. Skapa en ny rad och registrera information om utgiften, bland annat information i fälten **Projektnr.** och **Projektaktivitetsnr**.  
3. När journalen är slutförd väljer du åtgärden **Bokföra**.

## Se även

[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
