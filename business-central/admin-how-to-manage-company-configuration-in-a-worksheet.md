---
title: Så här hanterar du företagskonfigurationen i ett kalkylark | Microsoft Docs
description: Konfigurationskalkylarket är centralplatsen där du kan planera, spåra och utföra ditt konfigurationsarbete. Du kan skapa ett kalkylark för varje företag som du arbetar med, eller skapa ett standardkonfigurationskalkylark som kan användas för att konfigurera flera identiska företag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 66b3f7fb4955d66202818a22aaa2a36235c77e9d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "913416"
---
# <a name="manage-company-configuration-in-a-worksheet"></a>Så här hanterar du företagskonfigurationen i ett kalkylark
Konfigurationskalkylarket är centralplatsen där du kan planera, spåra och utföra ditt konfigurationsarbete. Du kan skapa ett kalkylark för varje företag som du arbetar med, eller skapa ett standardkonfigurationskalkylark som kan användas för att konfigurera flera identiska företag.  

Det första steget för att skapa ett konfigurationspaket är att välja ett företag som du redan har upprättat och ändrat så att det passar många av dina behov. Detta företag fungerar som baslinje för ditt konfigurationsarbete med nya företag. I kalkylarket anger du vilka tabeller som ska kontrolleras och hanteras i konfigurationen. Eftersom de flesta tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)] har samband och beroenden med andra tabeller, bör du även inkludera de relaterade tabeller som behövs. Tillsammans ska dessa tabeller sedan fungera som struktur, som du kan skapa ett nytt företag kring. I följande steg får du hjälp att skapa paket och distribuera konfigurationen.  

Som hjälp i spårning och granskning av ditt arbete kan du använda faktaboxen **Konfig. pakettabell** för att visa information om poster. Använd den **konfiguration. Relaterade tabeller** faktabox för att övervaka tabellrelationer.  

I följande procedurer ser du hur du lägger till och anpassar tabellinformation för konfigurationen.  

## <a name="to-open-the-configuration-worksheet"></a>Så här öppnar du konfigurationskalkylarket  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] öppnar du företaget som är grunden för konfigurationen och öppnar sedan dess implementerings-rollcenter för RapidStart Services.  
2.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Konfigurationsformulär** och välj sedan relaterad länk.  

## <a name="to-add-a-table-to-the-worksheet"></a>Så här lägger du till en tabell i kalkylarket  
1.  På sidan **Konfig. kalkylark** väljer du åtgärden **Redigera lista**.  
2.  I fältet **Radtyp** på första raden väljer du **Tabell**.  
4.  I fältet **Tabell-ID** markerar du tabellen som du vill lägga till i konfigurationen.  
5.  I fältet **Sid-ID** anger du det sid-ID som är kopplat till tabellen. För standardtabeller fylls detta värde i automatiskt. För anpassade tabeller måste du ange ID.
6.  I fältet **Referens** anger du adressen (URL) till en dokumentationssida, exempelvis i hjälpen, med information om bästa praxis eller instruktioner för hur du ska skapa tabellen.  
7.  Lägg till relaterade tabeller genom att välja åtgärden **Hämta relaterade tabeller**.  

    > [!NOTE]  
    > Relaterade tabeller läggs inte till med åtgärden **Hämta relaterade tabeller** om något av följande gäller:
    > - Relationen är villkorlig.  
    > Exempel: Om du får relaterade tabeller för tabellen **Kund** kommer tabellen **Lagerställe** inte att läggas till eftersom den bara är villkorligt relaterad till tabellen **Kund**, nämligen om fältet **Lagerställekod** i tabellen **Kund** har fyllts i.  
    > - Den relaterade tabellen filtreras.  
    > Exempel: Ett fält i den relaterade tabellen har en WHERE-sats. Anledningen till detta är den komplicerade relationsinformationen som lagras i systemtabellen **Fält** som inte är helt tillgänglig för programmet.  
    > Du måste lägga till sådana typer av tabeller manuellt genom att följa steg 4 i den här proceduren.  

8.  Om du vill ändra den resulterande listan över tabeller väljer du en tabell som du vill ta bort och väljer sedan åtgärden **Ta bort**.  
9. Upprepa stegen för alla tabeller som du vill lägga till i konfigurationen.  
10. Om du vill ta bort dubbletter i tabellinformationen som kan uppstå genom åtgärden **Hämta relaterade tabeller** väljer du åtgärden **Radera dubblettrader**. Det tar bort dubblettabeller som har samma paketkod.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Så här kan du lägga till flera tabeller i konfigurationskalkylarket  
1. Välj åtgärden **Hämta tabeller**. Sidan för batch-jobb **Hämta konfig. tabell** öppnas.  
2. I snabbfliken **Alternativ** anger du de tabelltyper som du vill lägga till i konfigurationen enligt beskrivningen i följande tabell.

    |Alternativ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Inkludera enbart med data**|Markera kryssrutan om du vill att bara de tabeller som innehåller data ska ingå. Du kan t.ex. lägga till en tabell som redan definierar de vanligaste betalningsvillkoren som stöds i din lösning.|  
    |**Ta med motsvarande tabeller**|Markera kryssrutan om du vill ta med alla relaterade tabeller. I steg 3 i den här proceduren ser du hur du lägger till en underuppsättning av relaterade tabeller.|  
    |**Ta med måtttabeller**|Markera kryssrutan om du vill ta med alla relaterade måttabeller.|  
    |**Ta bara med licensierade tabeller**|Markera kryssrutan om du bara vill ta med tabeller som du har åtkomst till, med licensen som du använde när du skapade kalkylarket.|

3. På snabbfliken **Objekt** kan du ställa in filter för att ange vilka typer av tabeller du vill ta med eller utelämna.  
4. Välj **OK**. [!INCLUDE[d365fin](includes/d365fin_md.md)]tabeller läggs till i kalkylbladet. Varje transaktion i listan har en rad av typen **Tabell**.  
5. Om du vill ta bort dubbletter i tabellinformationen som kan uppstå genom åtgärden **Hämta tabeller** väljer du åtgärden **Radera dubblettrader**. Det tar bort dubblettabeller som har samma paketkod.  
6. Du kan lägga till tabeller i kalkylarket som är kopplat till en tabell som du har valt. Granska informationen i faktaboxen **Relaterade tabeller** om du vill se om det saknas tabeller. Om du vill lägga till relaterade tabeller för en viss tabell, väljer du tabellen i listan och väljer sedan åtgärden **Hämta relaterade tabeller**.  

    > [!NOTE]  
    > Relaterade tabeller läggs inte till med åtgärden **Hämta relaterade tabeller** om något av följande gäller:
    > - Relationen är villkorlig.  
    > Exempel: Om du får relaterade tabeller för tabellen **Kund** kommer tabellen **Lagerställe** inte att läggas till eftersom den bara är villkorligt relaterad till tabellen **Kund**, nämligen om fältet **Lagerställekod** i tabellen **Kund** har fyllts i.  
    > - Den relaterade tabellen filtreras.  
    > Exempel: Ett fält i den relaterade tabellen har en WHERE-sats. Anledningen till det är att den ingående relationsinformationen lagras i den virtuella tabellen **Fält** och är inte tillgänglig på sidor som konfigurationskalkylarket av prestandaanledningar.  
    > Du måste lägga till relaterade tabeller med sådana komplexa relationer manuellt genom att följa steg 4 i avsnittet [Så här lägger du till en tabell i kalkylarket](admin-how-to-manage-company-configuration-in-a-worksheet.md#to-add-a-table-to-the-worksheet).

7. Om du vill ta bort tabeller i den resulterande listan över tabeller, väljer du en tabell som du vill ta bort och väljer sedan åtgärden **Ta bort**.  

Använd nästa procedur för att ange vilka tabellfält du vill inkludera. När du har gjort denna specifikation kan du exportera tabellen till Excel och använda tabellstrukturen som mall för att samla in kunddata. Mer information finns också i [Så här förbereder du migrering av kunddata](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Så här kan du definiera en uppsättning fält och poster för en konfigurationtabell  
1. Markera en tabell i listan över konfigurationstabeller och välj sedan åtgärden **Redigera lista**.  
2. Välj en tabell för vilken du vill ange fältinformation och välj sedan åtgärden **Fält**.  
3. För att välja endast de fält som du vill inkludera, välj åtgärden **Rensa inkluderade**. Om du vill lägga till alla fält väljer du åtgärden **Ange inkluderade**.  
4. Om du vill ange att fältdatan inte ska valideras avmarkerar du kryssrutan **Validera fält** för fältet.  
5. Välj **OK**.  
6. För att filtrera en viss uppsättning poster som ska inkluderas i konfigurationskalkylarket väljer du åtgärden **Filter** och anger sedan lämpliga filtervärden.

Du kan skapa områden med funktioner och grupper av tabeller i kalkylarket så att liknande funktioner kan grupperas. Om du t.ex. ställer in kontoplanen för din konfiguration kan du välja att skapa en grupp bokföringstabeller. Områden används typiskt för att gruppera en uppsättning tabeller som motsvarar ett funktionellt område. Varje område kan innehålla grupper. En grupp kan användas för att gruppera tabeller som har en gemensam betydelse.  

Följande procedurer beskriver hur du lägger till områdes- och gruppbeteckningar när du har skapat den ursprungliga listan över tabeller. När du har lagt till dessa kategorier kan du fortsätta lägga till och ändra listan över tabeller.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Så här kan du kategorisera och gruppera funktioner i kalkylarket  
1. Infoga en ny rad i kalkylarket i början av ett område.  
2. Välj **Område** i fältet **Radtyp**. Ange ett **Namn** på området.  
3. Infoga en ny rad i kalkylarket i början av en tabellgrupp.  
4. Välj **Grupp** i fältet **Radtyp**. Ange ett **Namn** för området. Gruppnamnet dras in automatiskt.  
5. Om du vill flytta tabeller till lämplig kategori markerar du en tabell som ska flyttas och väljer sedan åtgärden **Flytta upp** eller **Flytta ner**. Du kan också ta bort en kalkylarksrad och infoga tabellen igen på önskad plats.  

Vissa [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabeller är standard och datan i dessa kommer troligtvis inte att ändras från implementering till implementering. För att förbättra din kundfokus kan du ta bort dessa tabeller från kalkylarket när du har inkluderat dem i konfigurationspaket. När de väl har lagts till fortsätter tabellerna vara en del av konfigurationspaket.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Så här tar du bort en standardtabell i kalkylarket  
När du har lagt till alla nödvändiga tabeller i ett konfigurationspaket kan du bestämma vilka tabeller inte ska kräva kunduppmärksamhet.  
1.  Välj tabellerna och ta bort dem genom att välja åtgärden **Ta bort**.  

    > [!NOTE]  
    >  Tabellerna finns kvar i paketet även om de tas bort från kalkylarket.  

## <a name="to-review-and-customize-existing-database-data"></a>Så här granskar och anpassar du befintliga databasdata
När du skapar ett konfigurationspaket för en lösning kan du visa och anpassa tillgängliga databasdata så att dessa stämmer överens med dina kundbehov. Databastabellen måste vara kopplad till en sida.  

## <a name="to-customize-data-in-the-database"></a>Så här kan du anpassa data i databasen  

1.  På sidan **Konfigurationskalkylark**, identifiera tabellerna med data som du vill visa eller anpassa.  

    > [!NOTE]  
    >  Se till att varje tabell tilldelats ett sid-ID. Som standarden [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabell fylls detta värdet i automatiskt. För anpassade tabeller måste du ange ID.  

2.  Välj åtgärden **Databasdata**.  

     Sidan [!INCLUDE[d365fin](includes/d365fin_md.md)] för sidan öppnas.  

3.  Granska den tillgängliga informationen. Ändra den efter behov genom att ta bort transaktioner som inte är relevanta eller lägga till nya.

## <a name="see-also"></a>Se även  
[Ställa in företagskonfiguration](admin-set-up-company-configuration.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)
