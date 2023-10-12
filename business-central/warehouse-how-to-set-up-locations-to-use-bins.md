---
title: 'Så här: Lägger du upp lagerställen för att använda lagerplatser'
description: Lagerställen representerar den grundläggande lagerstrukturen och används för att lägga förslag om artiklarnas specifika placering av artiklar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# Registrera lagerställen för att använda lagerställen

Lagerplatser representerar den grundläggande lagerstrukturen och kan föreslå var artiklar ska placeras. När du har skapat dina lagerplatser definierar du deras innehåll, eller låter dem fungera som flytande lagerplatser utan specifikt innehåll.

Om du vill använda lagerplatsfunktionen på ett lagerställe går du till sidan **Lagerplats obligatorisk** på kortet **Lagerställe** När du har aktiverat växlingen är fälten **Lagerställeskod** och **Zonkod** tillgängliga för följande dokument:

* Dist.lager inleveranshuvud
* Dist.lager inleveransrad
* Dist.lager artikelinförselrader
* Dist.lager utleverans huvud
* Distributionslagerutleveransrader
* Dist.lager artikelinförselrader

Sedan designar du artikelflödet på lagerstället, genom att ange inställningar för lagerställeskoder i fältet som representerar de olika flödena.  

> [!NOTE]  
> Du måste skapa lagerplatskoder innan du kan ange dem för lagerstället. Mer information finns i [Skapa lagerställen](warehouse-how-to-create-individual-bins.md).  

## Så här lägger du upp ett lagerställe för att använda lagerställen

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2. Välj lagerstället där du vill använda lagerställen.  
3. Välj åtgärden **Redigera**.  
4. Markera fältet **Lagerplats ska finnas** på kryssrutan **Dist.lager**.  
5. Om du inte använder dirigerad artikelinförsel och plockning för ett lagerställe, i fältet **Standard lagerplatsval** väljer du den metod du vill att [!INCLUDE [prod_short](includes/prod_short.md)] ska använda för att tilldela en standardlagerplats till en artikel.  
6. Öppna kortet för den plats som du vill ställa in lagerställen för.
7. På snabbfliken **Lagerplatser** väljer du de lagerställen som du vill använda som standard för inleveranser, utleveranser samt inkommande, utgående och öppna produktionslagerställen.  

    De lagerställeskoder som du fyller i här visas automatiskt i huvudena och på raderna för olika distributionslagerdokument. Standardlagerställena definierar alla start- och slutplaceringar av artiklar i distributionslagret.  
8. Om du använder dirigerad artikelinförsel och plockning väljer du en lagerplats för distributionslagerjusteringarna. Lagerplatskoden i fältet **Justering lagerplatskod** anger den virtuella lagerplats för att registrera avvikelser i lager:

    * När du följer de skillnader som registrerats i distributionslagerartikeljournalen
    * Avvikelser som beräknas när du registrerar en utförd inventering  
9. Valfritt: På snabbfliken **Lagerplatsprinciper** fyller du i nödvändiga fält. De viktigaste fälten är **Lagerplats kapacitetsprincip**, **Tillåt brytenhet** och **Artikelinförsel mallkod**.  
10. På snabbfliken **Dist.lager** fyller du i fälten **utgående lagerhanteringstid**, **inkommande lagerhanteringstid** och **Baskalenderkod**. Om du vill ha mer information, gå till [Konfigurera baskalendrar](across-how-to-assign-base-calendars.md).

## Fylla i förbrukningslagerstället

Diagrammet visar hur **Lagerställeskod** på produktionsorderkomponentraderna fylls enligt platsinställningen.

:::image type="content" source="media/binflow.png" alt-text="Fältet Lagerställeskod på produktionsorderkomponentraderna.":::

## Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
