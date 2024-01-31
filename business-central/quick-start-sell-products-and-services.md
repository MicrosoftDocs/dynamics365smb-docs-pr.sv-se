---
title: Snabbstart för försäljning (innehåller video)
description: Lär dig hur du fyller i de första kritiska fälten om produkter och kunder i Business Central så att du kan starta dina försäljningsprocesser.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Försäljning snabbstart

För att kunna sälja produkter och tjänster måste du först lägga upp objekt och kunder. När du är klar kan du börja registrera försäljningsorder och skicka ut fakturor.

## Ställ in objekt att sälja

Det här videoklippet visar hur du ställer in en artikel för försäljning [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### Skapa en ny artikel

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Mer information och andra åtgärder du kan utföra när du ställer in objekt finns i [registrera nya objekt](inventory-how-register-new-items.md).  

## Ställ in kunder

Det här videoklippet visar hur du lägger upp en ny kund i [!INCLUDE[prod_short](includes/prod_short.md)].  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### Skapa en ny kund

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Mer information och andra åtgärder du kan utföra när du ställer in kund finns i [registrera nya kunder](sales-how-register-new-customers.md).

## Skapa en försäljningsorder  

När du säljer något till en kund finns det två alternativ. Det första är att bara skapa en försäljningsfaktura. Om försäljningsprocesser är mer komplicerade, till exempel om du har situationer där du endast levererar delar av en orderkvantitet, använder du dock en försäljningsorder.

### Så här skapar du försäljningsorder  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 10.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsorder** och väljer sedan relaterad länk.
2. Skapa en ny post genom att välja **Ny**.
3. Ange namnet på en befintlig kund i fältet **Kund**.

    Andra fält på sidan **Försäljningsorder** fylls nu i med standardinformation om den valda kunden.  

4. På sidan **Förs.order** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.

6. I fältet **Nr.** anger du ett nummer för en lagerartikel eller tjänst.

7. Skriv det antal artiklar som ska säljas i fältet **Kvantitet**.

8. Ange ett värde i procent, om du vill bevilja kunden en rabatt på produkten i fältet **Radrabatt %**.

9. Gör en kommentar i fältet **Beskrivning** på en orderrad för att lägga till en kommentar om försäljningsorder som kunden kan se på den utskrivna offerten.

10. Upprepa moment 5 till 9 för varje artikel som du vill att sälja till kunden.

11. Att enbart leverera en del av orderkvantiteten , anger denna kvantitet i **Ant. att utleverera**. Värdet kopieras till **Ant. att fakturera**.

12. För att enbart fakturera en del av den levererade kvantiteten , anger du denna kvantitet i **Ant. att fakturera**. Antalet kan inte vara högre än värdet i fältet **Ant. att utleverera**.

13. När försäljningsorderraderna slutförda väljer du åtgärden **Bokföra och skicka**.

Mer information och andra åtgärder du kan utföra när du skapar kundförsäljningsorder finns i [sälja produkter med kundförsäljningsorder](sales-how-sell-products.md).  

## Skapa en försäljningsfaktura

När du skapar och bokför en försäljningsfaktura kan du inte bara skapa det fakturadokument som du skickar till kunden. Du kan också skapa tillhörande antal och värdetransaktioner i [!INCLUDE[prod_short](includes/prod_short.md)].

### Så här skapar och bokför du en försäljningsfaktura  

1. Välj den ![Glödlampa som öppnar funktionen Berätta 20.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **försäljningsfakturor** och väljer sedan relaterad länk.  

2. Skapa en ny post genom att välja **Ny**.

3. Ange namnet på en befintlig kund i fältet **Kund**.

4. På sidan **Inkommande dokument** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.

6. I fältet **Nr.** väljer du en post som ska bokföras enligt värdet i fältet **Typ**.

7. I fältet **Antal** anger du hur många enheter av produkt, kostnad eller transaktion som registreras på raden för kunden.  

8. Om du vill ge en rabatt kan du ange ett procenttal i fältet **radrabatt %**. Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.  

9. Upprepa moment 5 till 8 för varje produkt som du vill fakturera kunden för.  

10. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

11. När försäljningsfakturaraderna slutförda väljer du åtgärden **Bokföra och skicka**.  

Mer information och andra åtgärder du kan utföra när du skapar en kundförsäljningsfakturor i [Fakturaförsäljning](sales-how-invoice-sales.md).

## Se även

[Snabbstart för Business Central](quick-start-business-central.md)  
[Försäljningsöversikt](sales-manage-sales.md)  
[Sälja produkter med en kundförsäljningsreturorder](sales-how-sell-products.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)  
