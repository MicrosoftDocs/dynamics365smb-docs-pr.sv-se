---
title: Lägg till marknadsföringstext för artiklar
description: Skriv marknadsföringstext för artiklar i Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/06/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# Lägg till marknadsföringstext för artiklar

För alla objekt som är registrerade i Business Central kan du skriva *marknadsföringstext* om artikeln. Även om marknadsföringstexten är en sorts beskrivning är den annorlunda än fältet **Beskrivningar**. Fältet **Beskrivning** används vanligtvis som ett kortfattat visningsnamn för att snabbt identifiera produkten. Marknadsföringstexten är å andra sidan en mer omfattande och beskrivande text. Dess syfte är att lägga till marknadsförings- och reklam innehåll, även kallat *Kopiera*. Denna text kan sedan publiceras med artikeln om den publiceras på en webbutik, som Shopify, eller klistras in i e-postmeddelanden eller annan kommunikation med dina kunder.

Det finns två sätt att skapa marknadsföringstexten. Det enklaste sättet att komma igång är att använda en Copilot, som föreslår AI-genererad text åt dig. Det andra sättet är att börja från början. 

## <a name=copilot></a>Hämta marknadsföringstextförslag med Copilot

Med hjälp av Copilot får du snabbt ett textförslag som genereras automatiskt. Den AI-genererade texten är skräddarsydd för artikeln och ger en bra utgångspunkt. Texten bygger delvis på följande information:

- Attribut som har definierats för artikeln&mdash;t.ex. beskrivning, färg, dimensioner, material och så vidare. [Mer information attribut](inventory-how-work-item-attributes.md).
- Förbättra **beskrivning**.
- Artikelkategori. [Läs mer om att kategorisera objekt](inventory-how-categorize-items.md).
- Valbara stilinställningar som t.ex. röst, format och längd.

Copilot är utformad för att spara tid och hjälpa dig att skriva kreativ och engagerande text som återspeglar ditt varumärke och som är konsekvent över hela produktlinjen. Börja med att generera ett förslag och ändra sedan den föreslagna texten efter behov.

### Förutsättningar

- Funktionen för marknadsföringstextförslag är aktiverad och aktiverad i din miljö. Den uppgiften är vanligtvis av en administratör. Om du vill ha mer information går du till [Konfigurera Copilot och AI-funktioner](enable-ai.md).
- Du använder ett av de språk som för närvarande stöds av marknadsföringstextförslagen.

  [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Om du vill ändra språk väljer du ikonen **Inställningar** i det övre högra hörnet ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") > **Mina inställningar** > **Språk**. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md#language).
- Gå igenom [vanliga frågor för marknadsföringstextförslag](faqs-marketing-text.md) för att lära dig hur AI tillämpas.

### Skapa första utkast med Copilot

Utför följande steg för att lägga till marknadsföringstext till en befintlig artikel. För att lära dig hur du skapar ett nytt objekt, gå till [registrera nya artiklar](inventory-how-register-new-items.md).

1. Öppna den artikel som du vill ändra i Business Central ändra genom att slutföra följande steg:

   - I det övre högra hörnet, välj ![Glödlampa som öppnar funktionen Berätta 22.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikonen, ange **artiklar** och välj sedan relaterad länk för att visa en lista med tillgängliga artiklar.

   - Dubbelklicka på det eller markera värdet i fältet **Nr.** kolumn .

1. Från artikelkortet finns det två sätt att komma igång med att skriva marknadsföringstext med Copilot: från faktaboxen **Marknadsföringstext** eller med åtgärden **Marknadsföringstext**. Dessa metoder anges i följande bild på ett artikelkort.  

   [![Visar artikelkort med fönstret marknadsföringstext](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

   Så här skapar du ett första utkast för en artikel:

   - I rutan **Marknadsföringstext** i faktabox på sidans högra sida, välj **Utkast med Copilot**. 

     Copilot börjar ta fram utkastet till marknadsföringstexten.

   - Längst upp på sidan väljer du the **Marknadsföringstext**, sedan **Utkast med Copilot** i fönstret **Redigera marknadsföringstext**.  Fönstret **Utkast till marknadsföringstext med Copilot** visas med en lista över alla tillgängliga attribut för artikeln.
1. Välj de attribut som du vill ha Copilot-basförslag på och välj sedan **Generera**. Du kan ändra de markerade attributen och andra alternativ senare. Copilot börjar ta fram utkastet till marknadsföringstexten. 

   ![Visar fönstret för redigering av marknadsföringstext](media/marketing-text-copilot-attributes.svg)

1. När Copilot har slutfört utkastet visas texten i Copilot-redigeringsfönstret för dig att granska och redigera.

   [![Visar fönstret skapa med Copilot](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Du kan sedan nu få fler förslag, försöka förbättra de förslag du får, redigera text med mera. Gå till [Granska, redigera och spara](#review-edit-and-save-text) för mer information.

### Granska, redigera och spara text

När du har det första utkastet måste du granska det och göra ändringar i texten för att kunna publicera det. Detta arbete görs från Copilot-redigeraren, som som låter dig hämta fler förslag, ändra inställningar för att påverka förslagen och manuellt göra ändringar och formatera texten.

> [!IMPORTANT]
> Den AI-genererade texten från en Copilot är endast ett förslag och kan ha misstag. Det krävs mänsklig tillsyn och översyn så att det är korrekt och lämpligt. Granska all föreslagen text och redigera den efter behov innan du sparar och publicerar den för offentlig förbrukning.

Använd följande riktlinjer för att slutföra och spara marknadsföringstexten.

1. Ändra texten direkt i rtextutan. Använd verktygsfältet längst ned i rutan för att formatera text, lägga till länkar med mera.
2. För att få ett nytt förslag, välj **Generera om**.
3. Om du inte är nöjd med förslagen kan du förbättra textförslagen med hjälp av inställningsalternativen **Ton**, **Format** och **Betoning**.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   För riktlinjer för att förbättra förslag, gå till [Förbättra och anpassa textförslag](#improve-and-tailor-text-suggestions).

4. Om du vill gå fram och tillbaka genom förslagen använder du föregående och nästa länk högst upp på sidan (*x* **av** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Kontrollera noga texten och är korrekt:

   - Om du vill spara texten väljer du **Behåll den**. 
   - Om du inte vill spara väljer du knappen för att ignorera (papperskorgen) ![Visar papperskorgsikonen för att ta bort alla Copilot-förslag för bankkontoavstämning](media/copilot-delete-trash-can.png).

### Förbättra och anpassa textförslag

Det finns några steg som du kan utföra för att förbättra textförslagen och anpassa dem så att de passar ditt personliga eller företagets önskemål.

1. Ändra de artikelattribut som används av Copilot.

   Copilot-förslag baseras delvis på förslagen på de attribut som tilldelats artikeln. Om du vill visa tillgängliga attribut och aktuella inställningar väljer du ikonen ![Redigera visar redigeringsikonen i Copilot-fönstret för att ändra attribut](media/edit-pencil.png) i det övre vänstra hörnet. På sidan **Artikelattribut**, välj de attribut som bäst överensstämmer med de egenskaper du vill främja. De mer relevanta attribut som du tar med desto bättre blir resultatet. Om du anser att du saknar några nyckelattribut lägger du till fler. För mer information om attribut, gå till [Arbeta med artikelattribut](inventory-how-work-item-attributes.md)
1. Ändra inställningarna för alternativen **Ton**, **Format** och **Betoning**.

   |Alternativ|Beskrivning|
   |-|-|
   |Tonfall |Använd det här alternativet om du vill påverka vilken typ av ord, fraser och skiljetecken som används för att engagera målgruppen. Du kan välja mellan flera fördefinierade tonfall, allt från **Formell** (vilket resulterar i en mest affärsmässig ton) till **Skapa** (vilket resulterar i en mycket informell ton). |
   |Format och längd|Använd det här alternativet när du vill styra textens allmänna struktur, som består av tre delar, som täcks av fyra olika alternativ: <ul><li>**Slogan** – Ett slogan eller kort mening som identifierar föremålet eller varumärket.</li><li>**Stycke** – Ett enda stycke med flytande och utförlig text, bestående av flera fullständiga meningar.</li><li>**Slogan + stycke** – En slogan följt av ett stycke</li><li>**Korthet** – En inledande mening, som liknar en slogan, följt av en punktlista med viktiga punkter av intresse.</li></ul> |
   |Betoning|Använd det här alternativet om du vill välja från en lista med fördefinierade kvaliteter som du vill framhäva i texten. Välj en kvalitet som bäst passar den typ av artikel du skriver om artikel. Kvaliteterna överensstämmer inte direkt med artikelns attribut, beskrivning eller kategori. Till exempel kan **kvalitet** vara ett bra val för både en cykel eller ett skrivbord medan **hastighet** skulle passa en cykel men inte ett skrivbord.|

1. Förbättra fältet **Beskrivning** på artikelkortet.

   Texten i fältet **Beskrivning** kommer att användas i befintligt skick på många ställen i den föreslagna texten, så det är viktigt att beskrivningen bäst beskriver hur du vill referera artikeln i marknadsföringstexten. 

1. Kontrollera att fältet **Artikelkategorikod** på artikelkortet är inställt på en lämplig kategori.

   Copilot kommer att söka efter ord och fraser som hör till kategorin och som arbetar med den föreslagna texten.

### Arbeta med flera språk 

Text genereras alltid på det språk som definieras av dina [inställningar](ui-change-basic-settings.md#language). Om din organisation driver och matar in data i Business Central med ett annat språk, eller om Business Central är anslutet till din onlinebutik, till exempel med Shopify, kan detta leda till att innehåll publiceras som inte matchar liknande marknadsföringsinnehåll.

## Skapa text från grunden

1. Öppna den artikel som du vill ändra i Business Central enligt följande:

    1. I det övre högra hörnet, välj ![Glödlampa som öppnar funktionen Berätta 22.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikonen, ange **artiklar** och välj sedan relaterad länk för att visa en lista med tillgängliga artiklar.
    2. Om du vill öppna objektet dubbelklicka på det eller markera numret i fältet **Nr.** .

2. Gör något av följande:

   - I rutan **Marknadsföringstext** i faktabox på sidans högra sida, välj **Redigera**.
   - Välj åtgärden **Marknadsföringstext**.
3. Ändra texten direkt i rutan **Marknadsföring**. Använd verktygsfältet längst ned i rutan för att formatera text, lägga till länkar med mera.
4. Välj **OK** när du är klar för att spara texten.

## Se även

[Översikt över förslag på marknadsföringstext](ai-overview.md)  
[Felsöka Copilot- och AI-funktioner](ai-copilot-troubleshooting.md)  
[Frågor och svar om marknadsföringstext för artikel](faqs-marketing-text.md)  
[Konfigurera Copilot- och AI-funktioner](enable-ai.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
