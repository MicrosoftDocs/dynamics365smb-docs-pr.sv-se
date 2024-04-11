---
title: Mappa e-dokument mot inköpsorderrader med Copilot
description: Lär dig mer om hur du använder Copilot för att mappa e-dokument till inköpsorderrader.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 02/23/2024
ms.custom: bap-template
---

# <a name="map-e-documents-to-purchase-order-lines-with-copilot-preview"></a>Mappa e-dokument mot inköpsorderrader med Copilot (förhandsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

När anskaffningsprocesser blir mer digitala spelar e-dokumentfunktionen i Business Central en nyckelroll för att automatisera mottagning och bearbetning av leverantörsfakturor. Copilot kan hjälpa till i denna process genom att förbättra mappningen och matchningen av leverantörsfakturor till inköpsorder. Detta minskar tidskrävande uppgifter som normalt skulle omfatta omfattande sökning, uppslag och datainmatning. Fördelen förstärks av det faktum att leverantörsfakturor ofta inte överensstämmer exakt med inköpsorder, vilket innebär att Copilot är bättre positionerad att identifiera de motsvarande inköpsorder. Förbättrade matchningsfunktioner gynnar särskilt små och medelstora organisationer som behöver effektiv dokumentspårning för inköpsorderrader. Copilot är den AI-drivna assistenten för arbete som ökar kreativiteten och förbättrar produktiviteten för Business Central-användare.

> [!IMPORTANT]
> - Det här är en funktion för produktionsklar förhandsgranskning för produktionsmiljöer och miljöer i begränsat läge i alla länder, med undantag för Kanada.
> - Produktionsklara förhandsvisningar är föremål för kompletterande användarvillkor. Mer information: [Kompletterande användningsvillkor för förhandsversionen av Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)
> - AI-genererat innehåll kan vara felaktigt.

I den första versionen av appen **e-dokument** introducerade vi grundläggande scenarier för e-dokument för hela försäljningsprocessen. Det finns emellertid ett behov av förbättringar och automatisering vid hanteringen av mottagna dokument, särskilt i samband med inköpsprocesser. Copilot förfinar hur du hanterar e-dokument i inköpsprocessen, särskilt när det gäller inköpsorder. Med ramverket för e-dokument kan du ange vilken typ av inköpsdokument som ska skapas för varje leverantör när du tar emot e-fakturor från dem. Tidigare var det enda alternativet att skapa en inköpsfaktura, antingen som ett dokument eller en redovisningsjournal.

Du kan nu uppdatera en befintlig inköpsorder i Business Central med den information som tas emot i e-fakturan.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->


## <a name="identify-purchase-orders"></a>Identifiera inköpsorder

Först kan du identifiera de inköpsorder som du kan matcha automatiskt.

## <a name="map-lines"></a>Definitionsrader

Copilot hjälper dig att automatiskt matcha e-fakturarader med inköpsorderrader och erbjuder extra matchningsinformation för att förbättra matchningarna.

När de har matchats och mappats uppdaterar Business Central den matchade inköpsordern med relevant inleveransinformation för att säkerställa att rätt antal tas emot på orderraderna.

## <a name="see-also"></a>Se även

[Översikt över e-dokument](finance-edocuments-overview.md)  
[Använda e-dokument vid försäljning och inköp](finance-how-use-edocuments.md)  
[Felsöka Copilot- och AI-funktioner](ai-copilot-troubleshooting.md)  
[Ansvarig AI vanliga frågor för bankavstämningshjälp](faqs-bank-reconciliation.md)  
