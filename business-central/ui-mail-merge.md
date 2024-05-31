---
title: Använda Word-mallar för masskommunikation
description: Med Word-mallar kan du enkelt skapa dokument som är anpassade för specifika entiteter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
ms.service: dynamics-365-business-central
---

# <a name="use-word-templates-for-bulk-communication"></a>Använda Word-mallar för masskommunikation

Microsoft Word-mallar kan göra det enklare att kommunicera i skrivit eller e-post med enheter som kontakter, kunder och leverantörer. Du kan till exempel skapa:

* Broschyrer som varnar kunderna om en försäljningskampanj
* Brev till leverantörer om nya inköpsprinciper
* Inbjudningar för att locka kontakter till ett kommande evenemang

> [!NOTE]
> När du ställer in Word-mallar måste du använda en enhet med Microsoft Word 2019 eller nyare och Windows-operativsystemet installerat.

## <a name="set-up-the-source-of-data"></a>Ange datakälla

Använda entiteter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakälla för mallen och lägga till kopplings instruktioner i anpassa dokument för varje entitet. Sammankopplingsfälten hämtas från entiteten i [!INCLUDE[prod_short](includes/prod_short.md)]. När du använder en Word-mall på en entitet infogas data från sammankopplingsfälten i dokumentet.

På sidan **Word-mallar**, när du skapar en ny mall kommer en assisterad installationsguide att hjälpa dig genom följande steg:

1. Välj en eller flera enheter som ska användas som datakälla. Om du till exempel vill skapa en broschyr för en försäljningskampanj väljer du förmodligen entiteten Kund som källa.
2. Välj andra entiteter som extra datakällor. Mer information finns i [Lägga till transaktioner som är relaterade eller inte relaterade till källentiteten](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Ladda ned en tom mall. Du kan ställa in mallen i Word direkt, eller så kan du överföra den tomma mallen och avsluta guiden. När mallens funktion är klar använder du åtgärden **överför** på sidan **Word-mallar** för att ersätta den tomma mallen med den färdiga mallen. Mer information finns i [Skapa mallar i Word](#set-up-the-template-in-word).
4. Ladda upp mallen som du har förberett.
5. Ange en kod och ett namn som identifierar mallen.

När du hämtar en mall får du en zip-fil som innehåller två filer.

|Fil  |Beskrivning  |
|---------|---------|
|DataSource.xlsx     | Data källfilen innehåller de fält som du kan använda i mallen. Redigera inte datakällfilen. Du kan bara använda Word-mallen och de datakällfiler som du hämtar och du måste lagra filerna på samma plats.     |
|Word-mall     | En .docx-fil som ska användas som mall.        |

Om du vill veta mer om hur du ställer in en mall i Word går du till [Ställa in mallen i Word](#set-up-the-template-in-word).

## <a name="add-entries-that-are-related-or-unrelated-to-the-source-entity"></a>Lägg till poster som är relaterade eller orelaterade till källentiteten

Du kan också koppla data från andra entiteter. Om du vill lägga till andra entiteter som data källor använder du någon av följande åtgärder på sidan **Word-mallar** eller när du använder den guidade installationen:

|Åtgärd  |Beskrivning  |
|---------|---------|
|**Lägg till relaterad enhet**  | Använd data från enheter som är relaterade till källentiteten. För entiteten kund kan du till exempel också koppla data från entiteten kontakt. Entiteter är relaterade när ett fält på en enhet refererar till en annan. Ett fält i entiteten kund avser ett fält i entiteten kontakt, så de är kopplade till varandra. Det delade fältet är ofta en identifierare som t.ex. namn, kod eller ID.        |
|**Lägg till en icke-relaterad entitet**| Använd data från enheter som inte är relaterade till källentiteten. Du skapar till exempel en mall för entiteten kund. Du kan lägga till entiteten företagsinformation så att du kan ta med din kontaktinformation. En viktig fördel är att om du ändrar din kontakt information uppdateras den automatiskt i mallen. När du har lagt till en orelaterade entitet kan du lägga till entiteter som är kopplade till den.         |

För orelaterade poster kan du välja en specifik post. Eftersom du endast kan lägga till en entitet en gång, måste du ta bort entiteten och lägga till den igen med den nya posten för att kunna använda en annan post.

Du kan skapa en hierarki med entiteter, både relaterade och orelaterade. Relationen visas som en trädstruktur. Fältet **Entitetsrelation** visas även information om relationen. För orelaterade entiteter visar fältet den post som skapar relationen.

När du lägger till entiteter använder du **Fältprefix** för att ange ett prefix för fältnamnen. Senare, när du lägger till fält i mallen, hjälper prefixet att skilja mellan fält från källan och andra enheter.

### <a name="select-the-fields-to-include"></a>Markera de fält som ska inkluderas

För varje entitet kan du ange vilka fält som ska vara tillgängliga för mallen. Välj ett nummer i kolumnen **antal markerade fält** om du vill visa en lista över tillgängliga fält. På sidan **Val av fält** använd kryssrutan **Inkludera** för att ange fälten. För vissa enheter ingår fält som företag vanligtvis använder som standard. Du kan redigera listan, till exempel, för att ta bort standardfälten. Ändringarna gäller endast för den mall som du arbetar med.

> [!NOTE]
> Det totala antalet fält som du kan lägga till från alla entiteter är 250.

> [!NOTE]
> Du eller din Microsoft-partner kan lägga till anpassade fält i entiteter. När du gör det prefixar vi namnet på fälten med **CALC** och ger det fälttypen **beräknad**. Fälttypen kallas beräknad för att visa att fältet kan visa olika typer av värden, till exempel text, siffror, datum och så vidare.

## <a name="to-create-a-word-template-in-business-central"></a>Så här skapar du en Word-mall i Business Central

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Word-mallar** och väljer sedan relaterad länk.
2. Välj **Ny**, sedan **Skapa en mall** och följ sedan instruktionerna i guiden assisterad konfiguration. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Du kan också skapa en mall direkt från sidan för en entitet genom att välja åtgärd för att **tillämpa Word-mall** för att öppna guiden inställningsguiden och **ny mall**. När du gör det väljs datakälla för dig baserat på typen av entitet.

## <a name="set-up-the-template-in-word"></a>Konfigurera mall i Word

När du lägger upp mallen i Word på fliken **Utskick** kan du lägga till sammankopplingsinstruktioner genom att välja **Infoga sammankopplingsfält**. De kopplingsfält kommer från datakällfilen som du hämtade för entiteten. De fungerar som platshållare som berättar för Word var i dokumentet informationen om enheten ska placeras.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Lägga till kopplingsinstruktioner i Microsoft Word":::

## <a name="apply-a-template"></a>Tillämpa en mall

När Word-mallen är klar kan du på sidan **Word-mallar** välja **Använd** för att skapa dokumenten. När du använder en Word-mall på en entitet infogas data från sammankopplingsfälten i dokumentet. Du kan antingen skapa ett dokument som innehåller avsnitt för varje entitet, eller **dela** för att skapa ett nytt dokument för varje entitet.

Du kan använda åtgärden **Använd Word-mallar** för att tillämpa mallar på en eller flera av samma typ av enhet, till exempel en kund, direkt i sammanhanget för sidan för enheten. Till exempel sidorna **Kund** eller **Leverantör**.

## <a name="use-word-templates-with-email"></a>Använda Word-mallar med e-post

Du kan använda Word-mallar för att lägga till innehåll i e-postmeddelanden. När du skriver ett e-postmeddelande kan du välja instruktionen **Använd Word-mall** om du vill använda innehållet i en mall i meddelandet. Du måste ha skapat mallar för entiteten. Du kan använda en mall i taget och när du växlar mellan mallar ändras meddelandet så att det återspeglar innehållet i den valda mallen.

Dessutom kan du använda åtgärden **Lägg till fil från Word-mall** för att koppla innehållet i mallen till e-postmeddelandet som en fil. Filen kommer att använda det format som du har angett för mallens utdata.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Alternativ för att använda innehåll från en Word-mall i ett e-postmeddelande":::

## <a name="edit-a-word-template"></a>Redigera en Word-mall

Du kan göra följande ändringar i Word-mallarna:

* För att redigera brödtexten eller slå samman fält som ingår i mallen, använd åtgärden **Hämta**, gör dina ändringar och använd sedan **Överför** åtgärden
* Om du vill ändra data källorna använder du **redigera relaterade entiteter** åtgärden
* Om du vill ersätta Word-mallen med en ny mall använder du åtgärden **Överför**
* Ta bort mallen

## <a name="see-also"></a>Se även

[Hantera rapport- och dokumentlayouter](ui-manage-report-layouts.md)  
[Konfigurera e-post](admin-how-setup-email.md)  
