---
title: Översikt över uppgifter för hantering av försäljning
description: 'Läs allt om hur du använder Business Central-tjänster för att hantera försäljningsaktiviteter med kunder med försäljningsfakturor order, offerter med mera.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'trade, sell'
ms.search.form: '253,'
ms.date: 01/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# FÖRS

Du kan skapa en försäljningsfaktura eller försäljningsorder för att registrera en överenskommelse med en kund om att sälja vissa produkter till vissa leverans- och betalningsvillkor.

Du måste använda försäljningsorder om din försäljningsprocess kräver att du t. ex. kan leverera delar av en orderkvantitet eftersom hela kvantiteten inte är tillgängliga på en gång. Om du säljer artiklar genom att leverera direkt från din leverantör till kunden, som en direktleverans, måste du även använda försäljningsorder. I alla andra aspekter fungerar försäljningsorder på samma sätt som försäljningsfakturor. Med försäljningsorder kan du också använda funktionen orderlöfte för att kommunicera vissa leveransdatum till dina kunder.  

Du kan förhandla med kunden genom att först skapa förs.offerter, som du kan omvandla till en försäljningsfaktura eller försäljningsorder när du instämmer om försäljningen. När kunden har bekräftat avtalet skickar du en orderbekräftelse för att registrera dina åtagande att leverera produkterna enligt överenskommelse.

Det är enkelt att korrigera eller annullera en bokförd försäljningsfaktura, innan kunden betalar den. Till exempel om du vill rätta till ett skrivfel eller om du kunden göra en ändring tidigt i orderprocessen. Om den bokförda försäljningsfakturan betalas, måste du skapa en försäljningskreditnota och försäljningsreturorder för att återföra försäljningen.

Effektiva metoder för försäljning och marknadsföring handlar om hur du fattar rätt beslut vid rätt tidpunkt. Marknadsföringsfunktionen i [!INCLUDE[prod_short](includes/prod_short.md)] ger en exakt överblick över din kontaktinformation när du behöver den, så att du kan arbeta effektivt med potentiella kunder och öka kundtillfredsställelsen. Läs mer på [Kundhantering](marketing-relationship-management.md).

Om du använder Microsoft Dynamics 365 Sales för Customer Engagement kan du ta del av sömlös integration i processen från kundämne till betalning med [!INCLUDE [prod_short](includes/prod_short.md)] för underliggande verksamhet. Till exempel för att behandla order, hantera lager och sköta din ekonomi. Läs mer på [Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md).

I affärsmiljöer där kunden måste betala för produkter i förväg måste du vänta på kvittot på betalning innan du levererar produkterna. I de flesta fall behandlar du inkommande betalningar några veckor efter leverans, genom att koppla betalningarna till dess relaterade obetalda bokförda försäljningsfakturor. Läs mer på [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

Försäljningsdokument kan skickas som PDF-filer kopplade till e-postmeddelande. Brödtexten för e-post innehåller ett utdrag av försäljningsdokumentet, till exempel produkter, totalt belopp och en länk till webbplatsen för PayPal. Läs mer på [Skicka dokument via e-post](ui-how-send-documents-email.md).

För alla försäljningsprocesser kan du integrera ett arbetsflöde för godkännande. Ett arbetsflöde för godkännande kan till exempel kräva att en chef godkänner stora försäljningar till vissa kunder. Läs mer i [Använd arbetsflöden](across-use-workflows.md).

Följande avsnitt beskriver en serie uppgifter, med länkar till de artiklar där de beskrivs.

## Kom igång med försäljningsfunktioner

Innan du säljer måste du ange hur du vill hantera företagets försäljningsprocesser.

|Till...| Gå till |
|---|---|
| Skapa ett kundkort för varje kund som du säljer till.|[Registrera nya kunder](sales-how-register-new-customers.md) |
| Ange hur du bedriver försäljning, till exempel priser och rabatter, kundpris- och rabattgrupper, säljare, leveransmetoder och handläggare. | [Konfigurera försäljning](sales-setup-sales.md) |

## Försäljningsanalys

I det här avsnittet beskrivs analysverktyg som du kan använda för att få insikter om dina försäljningsdata.

| Till... | Gå till |
| --- | --- |
| Läs mer om funktionerna för att analysera försäljningsdata. | [Översikt över försäljningsanalys](sales-analytics-overview.md) |
| Utför ad hoc-analys av försäljningsdata direkt på listsidor och frågor. | [Skapa försäljningsanalysrapporter](bi-how-create-analysis-views-reports.md) |
| Utforska inbyggda rapporter för försäljning | [Inbyggda försäljningsrapporter](sales-reports.md) |

## Offert för order till försäljningsfaktura

I följande tabell beskrivs hur du använder enkla försäljningsprocesser.

|Till...| Gå till |
|---|---|
| Skapa en försäljningsoffert där du erbjuder produkter med förhandlingsbara villkor, innan du omvandlar offerten till en försäljningsfaktura. |[Skapa försäljningsofferter](sales-how-make-offers.md) |
| Bearbeta en försäljningsorder (kanske med en delleverans eller med en direktleverans.) |[Sälja produkter](sales-how-sell-products.md) |
| Skapa en försäljningsfaktura för att registrera en överenskommelse med en kund om att sälja produkter till vissa leverans- och betalningsvillkor. |[Fakturera försäljning](sales-how-invoice-sales.md) |
|Förstå vad som händer när du bokför försäljningsdokument.|[Bokföra försäljning](ui-post-sales.md)|

Om du behöver mer komplicerade försäljningsprocesser visas i följande tabell artiklar som förklarar vad du kan göra med [!INCLUDE[prod_short](includes/prod_short.md)].

|Till...| Gå till |
|---|---|
| Uppfylla en försäljningsorder med flera delleveranser. | [Bearbeta delleveranser](sales-how-send-partial-shipments.md) |
| Lägga upp standardförsäljnings- eller inköpsrader som du kan snabbt infoga i dokument, till exempel för återkommande påfyllningsorder.|[Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md)|  
|Hantera kundens engagemang att köpa stora kvantiteter som levereras i flera leveranser med tiden.|[Arbeta med försäljningsavropsorder](sales-how-to-create-blanket-sales-orders.md)|
|Fakturera kunder en gång för flera utleveranser genom att kombinera leveranser på en faktura.|[Kombinera leveranser på en enda faktura](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Du kan sälja monteringsartiklar som inte är tillgängliga genom att skapa en länkad monteringsorder. Monteringsordern kan leverera hela eller delar av kvantiteten på försäljningsordern.|[Sälja artiklar som monterats mot kundorder](assembly-how-to-sell-items-assembled-to-order.md)|

## Plocka och utleverera du artiklar

I följande tabell beskrivs hur du plockar artiklar till en försäljningsorder och levererar dem till kunden.

| Till | Gå till |
| --- | --- |
|Förbered för att plocka artiklar för utleverans.|[Skriva ut plocklistan](sales-how-print-picking-list.md)|
| Länka en försäljningsorder till en inköpsorder för att sälja ett direktutleveransobjekt som ska levereras direkt från din leverantör till kunden. |[Skapa direktleveranser](sales-how-drop-shipment.md) |
|Har en katalogartikel levererad från en leverantör till distributionslagret så att du kan leverera den till kunden.|[Skapa specialorder](sales-how-to-create-special-orders.md)|
|Informera dina kunder om orderleveransdatum genom att beräkna antingen kapabel att lova-datum eller dispositionsdatum.|[Beräkna orderlöftesdatum](sales-how-to-calculate-order-promising-dates.md)|
| Läs om hur du spårar ett paket från en bokförd utleverans. | [Spåra paket](sales-how-track-packages.md) |

## Annullerade beställningar, återbetalningar och returer

I följande tabell beskrivs hur du hanterar annullerade order, återbetalningar och returer av varor.

| Till | Gå till |
| --- | --- |
| Utför en åtgärd på en obetald bokförd försäljningsfaktura som automatiskt skapar en kreditnota och antingen annullerar försäljningsfakturan eller skapar den på nytt, så att du kan göra korrigeringar. |[Korrigera eller makulera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md) |
| Skapa en försäljningskreditnota för att återföra en särskild bokförd försäljningsfaktura för att visa produkter som kunden returnerar och återbetalningsbelopp. |[Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md) |

## Andra processer inom försäljning

I följande tabell beskrivs hur du hanterar andra inköpsprocesser.

| Till | Gå till |
| --- | --- |
|Lösa problem när det finns två eller flera poster för samma kund.|[Slå samman dubblettposter](sales-how-merge-duplicate-records.md)|

## Se även

[Konfigurera försäljning](sales-setup-sales.md)  
[Registrera nya kunder](sales-how-register-new-customers.md)  
[Översikt försäljningsanalys](sales-analytics-overview.md)   
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allmänna affärsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
