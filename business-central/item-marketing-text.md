---
title: Lägg till marknadsföringstext för artiklar
description: Skriv marknadsföringstext för artiklar i Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# <a name="add-marketing-text-to-items"></a><a name="add-marketing-text-to-items"></a>Lägg till marknadsföringstext för artiklar

För alla objekt som är registrerade i Business Central kan du skriva *marknadsföringstext* om artikeln. Även om marknadsföringstexten är en sorts beskrivning är den annorlunda än fältet **Beskrivningar**. Fältet **Beskrivning** används vanligtvis som ett kortfattat visningsnamn för att snabbt identifiera produkten. Marknadsföringstexten är å andra sidan en mer omfattande och beskrivande text. Dess syfte är att lägga till marknadsförings- och reklam innehåll, även kallat *Kopiera*. Denna text kan sedan publiceras med artikeln om den är publicerad på en webbutik, till exempel Shopify.

Det finns två sätt att skapa marknadsföringstexten. Det enklaste sättet att komma igång är att använda en Copilot, som föreslår AI-genererad text åt dig. Det andra sättet är att börja från början. 

## <a name="create-ai-generated-marketing-text-preview-with-copilot"></a><a name="create-ai-generated-marketing-text-preview-with-copilot"></a><a name=copilot></a>Skapa AI-genererad marknadsföringstext (förhandsgranskning) med Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Med hjälp av Copilot får du snabbt ett textförslag som genereras automatiskt. Den AI-genererade texten är skräddarsydd för artikeln och ger en bra utgångspunkt. Texten bygger delvis på följande information:

- Attribut som har definierats för artikeln, t.ex. beskrivning, färg, dimensioner, material och så vidare.
- Valbara stilinställningar som t.ex. röst, format och längd.

Copilot är utformad för att spara tid och hjälpa dig att skriva kreativ och engagerande text som återspeglar ditt varumärke och som är konsekvent över hela produktlinjen. Börja med att generera ett förslag och ändra sedan den föreslagna texten efter behov.

> [!NOTE]
> I förhandsgranskningsversionen av Business Central är AI-genererad text endast på engelska.

### <a name="prerequisites"></a><a name="prerequisites"></a>Förutsättningar

- Du använder en [förhandsversion](ai-preview-getstarted.md) av Business Central som har aktiverats för Copilot. Att aktivera Copilot utförs av en administratör. Om du vill ha mer information går du till [Konfigurera marknadsföringstext för AI-baserad artikel med Copilot](enable-ai.md).
- Det språk som du använder i Business Central måste vara engelska. Alla tillgängliga engelska språk kommer att fungera, t.ex. engelska (USA), engelska (Storbritannien) eller engelska (Sydafrika).

   Om du vill ändra språk väljer du ikonen **Inställningar** i det övre högra hörnet ![Inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") > **Mina inställningar** > **Språk**. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md#language).
- Läs [vanliga frågor och svar om Copilot](ai-faq.md) om du vill veta mer om AI-genererade textförslag från Copilot och hur du bör använda dem.

### <a name="create-first-draft-with-copilot"></a><a name="create-first-draft-with-copilot"></a>Skapa första utkast med Copilot

1. Öppna den artikel som du vill ändra i Business Central. För att öppna en artikel, gör följande:

   1. I det övre högra hörnet, välj ![Glödlampa som öppnar funktionen Berätta 22.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikonen, ange **artiklar** och välj sedan relaterad länk för att visa en lista med tillgängliga artiklar.
   2. Om du vill öppna objektet dubbelklicka på det eller markera värdet i fältet **Nr.** kolumn.

   Om du vill ha information om hur du skapar en artikel går du till [registrera nya artiklar](inventory-how-register-new-items.md).

   [![Visar artikelkort med fönstret marknadsföringstext](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. Från artikelkortet finns det två sätt att komma igång med att skriva marknadsföringstext med Copilot:

   - Använd rutan **marknadsföringstext** i faktabox på sidans högra sida. Följ dessa steg:

     1. I rutan **Marknadsföringstext**, välj **Skapa med Copilot**.

        Den föreslagna texten visas i rutan.
     2. Om du vill använda ett annat förslag väljer du **Skapa med Copilot** igen. Om du inte är nöjd med förslaget väljer du **Ignorera** för att rensa rutan.

        Du kan göra detta steg över och över tills du får ett förslag om att det är en bra utgångspunkt. Tänk dock på att det aktuella förslaget skrivs över och inte visas igen. Om du vill använda det aktuella förslaget går du vidare till nästa steg. Du har fortfarande möjlighet att få fler förslag och till och med förbättra förslagen om du vill senare.
      3. Välj **Granska och spara förslaget** eller **Redigera** om du vill granska, redigera och spara texten.

         Det här steget tar dig till sidan **Skapa med Copilot**. Gå till nästa avsnitt.

         > [!NOTE]
         > Texten sparas inte förrän du tar det här steget.

   - Välj åtgärden **Marknadsföringstext** högst upp på sidan artikel kort och gå direkt till sidan **Skapa med Copilot**.

     Från sidan **Skapa med**, välj **Skapa med Copilot** för att hämta det första förslaget. Du kan sedan få fler förslag, försöka förbättra de förslag du får, redigera text med mera. Gå till [Granska, redigera och spara](#review-edit-and-save-text) för mer information.

   > [!TIP]
   > [Var kommer förslaget från?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### <a name="review-edit-and-save-text"></a><a name="review-edit-and-save-text"></a>Granska, redigera och spara text

När du har det första utkastet måste du granska det och göra ändringar i texten för att kunna publicera det. Det här arbetet görs från sidan **Skapa med Copilot**. Den aktuella texten visas i **Marknadsföringtext**. På sidan kan du få fler förslag, ändra inställningar för att påverka förslagen och manuellt göra ändringar och formatera texten.

[![Visar fönstret skapa med Copilot](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> Den AI-genererade texten från en Copilot är endast ett förslag och kan ha misstag. Det krävs mänsklig tillsyn och översyn så att det är korrekt och lämpligt. Granska all föreslagen text och redigera den efter behov innan du sparar och publicerar den för offentlig förbrukning.

Använd följande riktlinjer för att slutföra och spara marknadsföringstexten.

1. Ändra texten direkt i rutan **Marknadsföring**. Använd verktygsfältet längst ned i rutan för att formatera text, lägga till länkar med mera.
2. För att få ett nytt förslag, välj **Skapa utkast**.
3. Om du inte är nöjd med förslagen kan du förbättra textförslaget enligt dina önskemål.

   Välj **Fler inställningar**, ändra alternativen som visas under **Välj hur en Copilot skapar förslag** och välj sedan **Skapa utkast** för att få ett nytt förslag.

   För riktlinjer för att förbättra förslag, gå till [Förbättra och anpassa textförslag](#improve-and-tailor-text-suggestions).

4. Om du vill gå tillbaka till föregående förslag väljer du **Ångra**.
5. Kontrollera noga texten och är korrekt och välj sedan **OK** för att spara den.

### <a name="improve-and-tailor-text-suggestions"></a><a name="improve-and-tailor-text-suggestions"></a>Förbättra och anpassa textförslag

Det finns några steg som du kan utföra för att förbättra textförslagen och anpassa dem så att de passar ditt personliga eller företagets önskemål.

1. Använd alternativen högst upp på sidan **Skapa med Copilot** för att påverka resultatet av AI-genererad text: 

   |Alternativ|Beskrivning|
   |-|-|
   |Attribut att inkludera|Använd det här alternativet om du delvis vill basera förslagen på de attribut som tilldelats artikeln. Välj de attribut som bäst överensstämmer med de egenskaper som du vill marknadsföra. De mer relevanta attribut som du tar med desto bättre blir resultatet. Om du anser att du saknar några nyckelattribut lägger du till fler. För mer information om attribut, gå till [Arbeta med artikelattribut](inventory-how-work-item-attributes.md) |
   |Betona en kvalitet|Använd det här alternativet om du vill välja från en lista med fördefinierade kvaliteter som du vill framhäva i texten. Välj en kvalitet som bäst passar den typ av artikel du skriver om artikel. Kvaliteterna överensstämmer inte direkt med artikelns attribut, beskrivning eller kategori. Till exempel kan **kvalitet** vara ett bra val för både en cykel eller ett skrivbord medan **hastighet** skulle passa en cykel men inte ett skrivbord.|
   |Tonfall|Använd det här alternativet om du vill påverka vilken typ av ord, fraser och skiljetecken som används för att engagera målgruppen. Du kan välja mellan flera fördefinierade tonfall, allt från **Formell** (vilket resulterar i en mest affärsmässig ton) till **Skapa** (vilket resulterar i en mycket informell ton). |
   |Format och längd|Använd det här alternativet när du vill styra textens allmänna struktur, som består av tre delar, som täcks av fyra olika alternativ: <ul><li>**Slogan** – Ett slogan eller kort mening som identifierar föremålet eller varumärket.</li><li>**Stycke** – Ett enda stycke med flytande och utförlig text, bestående av flera fullständiga meningar.</li><li>**Slogan + stycke** – En slogan följt av ett stycke</li><li>**Korthet** – En inledande mening, som liknar en slogan, följt av en punktlista med viktiga punkter av intresse.</li></ul> |

2. Förbättra fältet **Beskrivning** på artikelkortet.

   Texten i fältet **Beskrivning** kommer att användas i befintligt skick på många ställen i den föreslagna texten, så det är viktigt att beskrivningen bäst beskriver hur du vill referera artikeln i marknadsföringstexten. 

3. Kontrollera att fältet **Artikelkategorikod** på artikelkortet är inställt på en lämplig kategori.

   Copilot kommer att söka efter ord och fraser som hör till kategorin och som arbetar med den föreslagna texten.

## <a name="create-marketing-text-from-scratch"></a><a name="create-marketing-text-from-scratch"></a>Skapa marknadsföringstext från grunden

1. Öppna den artikel som du vill ändra i Business Central enligt följande:

    1. I det övre högra hörnet, välj ![Glödlampa som öppnar funktionen Berätta 22.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikonen, ange **artiklar** och välj sedan relaterad länk för att visa en lista med tillgängliga artiklar.
    2. Om du vill öppna objektet dubbelklicka på det eller markera numret i **Nr.** .

2. Gör något av följande:

   - I rutan **Marknadsföringstext** i faktabox på sidans högra sida, välj **Redigera**.
   - Välj åtgärden **Marknadsföringstext**.
3. Ändra texten direkt i rutan **Marknadsföring**. Använd verktygsfältet längst ned i rutan för att formatera text, lägga till länkar med mera.
4. Välj **OK** när du är klar för att spara texten.

## <a name="see-also"></a><a name="see-also"></a>Se även

[Översikt över marknadsföringstext för AI-baserad artikel med Copilot](ai-overview.md)  
[Konfigurera marknadsföringstext för AI-baserad artikel med Copilot](enable-ai.md)  
[Marknadsföringstext för AI-baserad artikel med vanliga frågor om Copilot](ai-faq.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
