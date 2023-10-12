---
title: Fördela kostnader till koncerninterna partner | Microsoft-dokument
description: Läs om hur momsinställningar för kunder och leverantörer styr om – och hur – moms beräknas.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocate-costs-to-intercompany-partners"></a>Fördela kostnader till koncerninterna partner
När du använder koncerninterna bokföringar för att överföra dokument mellan partnerföretag, kontrollerar de momsrelaterade inställningarna (främst rörelsebokföringsmallen för mots) som tilldelats kund- eller leverantörskonton (som är kopplade till den koncerninterna partnern) om, och hur, moms beräknas och registreras. Du kan också göra kostnadsfördelningar direkt från en inköpsorder till partnerföretag. Om du till exempel registrerar en inköpsfaktura från en extern leverantör och vill distribuera vissa eller samtliga kostnader till en eller flera koncerninterna partner.

Du kan fördela kostnader till en eller flera koncerninterna partner med hjälp av följande:

* **Koncerninterna allmänna journaler** – Dessa journaler är användbara när en tjänst köps in. När ett moderbolag till exempel anlitar en tjänst för att konfigurera datorsystem i två dotterbolag. Fakturan skickas till moderbolaget, men kostnaderna fördelas på de koncerninterna partnerna. Mer information finns i [Arbeta med koncerninterna dokument och journaler](intercompany-how-work-documents-journals.md).
* Inköpsorder och fakturor – Att använda inköpsdokument är användbart när inköpsfunktionerna för till exempel rörelsekostnader centraliseras i ett företag och sedan allokeras till de koncerninterna partnerna.

## <a name="to-allocate-costs-using-an-intercompany-general-journal"></a>Så här fördelar du kostnader med hjälp av en koncernintern redovisningsjournal
Gör så här om du vill ange en rad i en koncernintern redovisningsjournal. 

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Koncernintern redovisningsjournal** och väljer sedan relaterad länk.
2. Vid behov anger du det dokumentnummer som finns på fakturan från leverantören i fältet **Externt dokumentnr**.
3. I fältet **Dokumenttyp** väljer du **Faktura**.
4. I fältet **Kontotyp** väljer du **Leverantör**.
5. I fältet **Kontonr.** väljer du leverantören.
6. I fältet **Belopp** anger du ett negativt belopp som är lika med beloppet på fakturan.
7. I fältet **Balanskontotyp** väljer du **Redovisningskonto**.
8. I fältet **Balanskontonr.** väljer du det balanskonto som ska användas.
9. Om du vill fördela kostnader till koncerninterna partner gör du så här:
   1. Skapa en ny rad.
   2. Låt fältet **Dokumenttyp** vara – välj det alternativ som lämnar fältet tomt.
   3. I fältet **Dokumentnr.** anger du ett nummer som skiljer sig från numret i fältet **Externt dokumentnr.**. Kostnadsfördelningen betraktas som en annan transaktion.
   4. I fältet **Kontotyp** väljer du **Intern partner**.
   5. I fältet **Kontonr.** väljer du den koncerninterna partner som kostnaden ska allokeras till.
   6. I fältet **Balanskontotyp** väljer du **Redovisningskonto**.
   7. I fältet **Balannskontonr.** väljer du det redovisningskonto där det belopp du erhåller från den koncerninterna partnern ska bokföras.
   1. I fältet **Belopp** anger du beloppet fakturan som ska fördelas till den koncerninterna partnern.
   1. I fältet **Redovisningskontonr. för intern partner** väljer du det redovisningskonto där du vill bokföra beloppet för den koncerninterna partnern. 
   1. Fyll i återstående fält om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Upprepa dessa steg för varje koncernintern partner som ska dela kostnaden.
1. Om du vill bokföra dokumentet och fördela kostnaderna väljer du **Bokför**.  

## <a name="to-allocate-costs-using-a-purchase-document"></a>Så här fördelar du kostnader med hjälp av ett inköpsdokument
I följande procedur beskrivs hur du fördelar kostnader med hjälp av en inköpsfaktura. Stegen är desamma för inköpsorder.

> [!NOTE]
> För att slutföra dessa steg måste du anpassa sidan **Inköpsfaktura** genom att lägga till fälten **Intern partnerkod**, **Ref.typ för intern partner** samt **Intern partner**. Mer information finns i [Så här börjar du anpassa en sida genom den anpassningsbanderollen](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **inköpsorder** och väljer sedan relaterad länk.
2. I fältet **Typ** väljer du **Redovisningskonto**.
   
   Redovisningskonto är det enda alternativ som du kan använda för att fördela kostnader.  
1. I fältet **Nr.** fältet väljer du det redovisningskonto du vill bokföra till.
1. I fältet **Intern partnerkod** väljer du den koncerninterna partner som kostnaden ska fördelas till.
1. Under **Ref.typ för intern partner** väljer du det redovisningskonto som du vill använda för fördelningen.. Det här kontot kommer att koppla utgifterna till ett konto i den koncerninterna partnerns kontoplan.
1. I fältet **Kvantitet** anger du antalet enheter som ska debiteras den koncerninterna partnern.
1. I fältet **Direkt styckkostnad exkl. moms (eller inkl. moms)** anger du kostnaden per artikel som ska debiteras till den koncerninterna partnern.
1. Fyll i återstående fält om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Om du vill bokföra inköpsordern väljer du **Bokför**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners"></a>Så här skickar du fördelade kostnader till koncerninterna partner
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Transaktioner för int. utkorg** och väljer sedan relaterad länk.
2. Klicka på raderna som ska skickas och välj sedan åtgärden **Skicka till intern partner**. 
3. Om du vill fördela kostnaderna väljer du åtgärden **Slutför radåtgärder**.

## <a name="calculating-vat-for-cost-distributions"></a>Beräkna moms för kostnadsfördelningar
När du använder ett dokument för att fördela kostnader till koncerninterna partner finns det två momsinställningar att tänka på: 
* Inställningarna på redovisningskontot för utgifter:
   * Om de allmänna generella moms-rörelsebokföringsmallarna är inställda på redovisningskontot beror beräkningen på grupperna och produktgrupperna från dokumentraden.
   * Om de allmänna rörelse- eller moms-rörelsebokföringsmallarna inte anges på redovisningskontot, beror beräkningen på följande:
* Inställningarna för bokföringsmallen för den koncerninterna partnern
   * Om den koncerninterna partnern har tilldelats ett kundnummer som inte har någon generell rörelsebokföringsmall för rörelse eller moms.
   * Det finns inget kundnummer associerat med den koncerninterna partnern. Då är de generella rörelse- eller moms-rörelsebokföringsmallarna tomma och raden i momsbokföringsinställningarna används, vilket oftast är en grupp där 0 % moms har angetts.

> [!NOTE]
> Det är viktigt att validera både inställningen för koncerninterna partner och inställningen för redovisningskonto (för det kostnadskonto som används för kostnadsfördelningen) innan du fördelar kostnader till koncerninterna partner.

## <a name="see-also"></a>Se även
[Koncerninterna inställningar](intercompany-how-setup.md)  
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
