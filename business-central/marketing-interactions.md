---
title: Hantera interaktioner med dina kontakter
description: 'Du kan hantera all slags kommunikation eller interaktioner mellan ditt företag och kontakterna, till exempel för brev, telefonsamtal, sammanträden och så vidare.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5082,'
ms.date: 04/01/2021
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Spela in interaktioner med kontakter

Registrering av interaktioner med affärskontakter består av följande uppgifter:

* Skapa interaktionsmallar  
* Så här skapar du interaktioner på kontakter och segment  
* Visa och hantera registrerade interaktioner  

## Konfigurera interaktionsmallar

Innan du kan registrera interaktioner måste du lägga upp interaktionsmallar. En interaktionsmall en modell som definierar en interaktions grundläggande egenskaper. När du registrerar en interaktion behöver du ange vilka interaktionsmallar den baseras på. Inställningar såsom vilket kommunikationssätt som användes, vem som initierade interaktionen och dess kostnad, överförs till interaktionen.

Du skapar en interaktionsmall på sidan **Interaktionsmallar**.

När du skapar en interaktionsmall kan du lägga till en bilaga. Du kan till exempel bifoga ett Microsoft Word-dokument som innehåller anteckningar från ett möte. Mer information om bifogade filer finns i [Bilagor för interaktioner](marketing-interaction-attachments.md). Upprepa stegen för varje interaktionsmall du vill skapa.  

## Skapa interaktioner

Det finns två sätt att registrera interaktioner:

* Du kan manuellt skapa interaktioner som är länkade till en enda kontakt eller till ett segment. Mer information finns i [Skapa interaktioner på kontakter och segment](marketing-how-create-interactions.md).  
* När du utför uppgifter i , till exempel skriver ut fakturor eller offerter, kan interaktioner registreras automatiskt. Mer information finns i [automatiskt registrera interaktioner med kontakter](marketing-auto-record-interactions.md).

## Visa och hantera registrerade interaktioner

Alla registrerade interaktioner och bifogade filer som inte har raderats kan visas på sidan **Interaktionslogg**. Du kan öppna sidan genom att:

* Med hjälp av ikonen **Sök efter sida eller rapport** för att söka i **Interaktionslogg**.
* Välj åtgärden **Interaktionslogg** på en kontakt eller ett segment.

  Sidan **Interaktion loggtrans.** innehåller de interaktioner du skapar manuellt samt de interaktioner som [!INCLUDE [prod_short](includes/prod_short.md)] registrerar automatiskt.

Använd sidan Interaktionsloggposter för att visa status för interaktioner och avbryta interaktioner.

Du kan ta bort interaktionsloggar som har avbrutits. För att ta bort transaktioner, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Ta bort avbrutna interaktionsloggtrans** och välj relaterad länk och fyll i information.

## Se även

[Hantera kontakter](marketing-contacts.md)  
[Hantera Försäljningsmöjligheter](marketing-manage-sales-opportunities.md)  
[Arbeta med Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
