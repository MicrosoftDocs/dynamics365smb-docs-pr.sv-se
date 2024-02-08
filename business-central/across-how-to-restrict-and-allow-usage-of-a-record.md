---
title: Så här begränsar och tillåter du användning av en post
description: 'Om du vill begränsa en post från att användas, kan du inkorporera två arbetsflödesvar i ett arbetsflöde som kontrollerar användningen av posten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Begränsa och tillåt användningen av en post

Om du vill begränsa en post från att användas i vissa aktiviteter, till exempel tills posten har godkänts, kan du inkorporera två arbetsflödessvar i ett arbetsflöde som kontrollerar användningen av posten. Ett arbetsflödessvar ska begränsa användningen av posten enligt definitionen i arbetsflödeshändelsen och villkoren. Ett annat arbetsflödessvar ska tillåta användning av posten enligt definitionen i arbetsflödeshändelsen och villkoren. Det finns två svar i standard versionen av [!INCLUDE[prod_short](includes/prod_short.md)] för det här ändamålet: **Lägg till postbegränsning** och **Ta bort postbegränsning**.

> [!NOTE]  
> Standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)] erbjuder stöd för att begränsa en post från att bokföras, från att exporteras som en utbetalning och från att skrivas ut som en check. För att stödja andra begränsningar måste en Microsoft-partner anpassa programkoden.  

> [!NOTE]  
> Arbetsflödesfunktionen för att begränsa och tillåta poster att användas är inte relaterad till funktionen att spärra artikel-, kund- och leverantörsposter från att bokföras.

Följande procedur beskriver hur du begränsar inköpsorder från att bokföras tills de har godkänts. Det nya arbetsflödet baseras på det befintliga mallen *Arbetsflöde för godkännande av inköpsfaktura*.  

## Skapa ett arbetsflödessteg som begränsar bokföring av icke godkända inköpsorder

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. På sidan **Arbetsflöden** väljer du åtgärden **Nytt arbetsflöde från mall**. Läs mer på [Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)
3. På sidan **Arbetsflödesmallar** väljer du mallen *Arbetsflöde för godkännande av inköpsfaktura*.  

   Lägg märke till att de första två arbetsflödesstegen är om du vill begränsa och sedan tillåta användning av inköpsfakturor. Ändra händelsevillkoret i det första steget i det nya arbetsflödet för att ange att det gäller inköpsorder.  
4. På snabbfliken **Arbetsflödessteg** väljer du fältet **På villkor** för första steget sedan för filtret **Dokumenttyp**, välj **Order**.  
5. Fortsätt med att redigera, ta bort eller lägga till andra arbetsflödessteg så att de återspeglar en affärsprocess som börjar med att begränsa så att icke godkända inköpsorder bokförs.  

## Se även

[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)  
[Arbetsflöde](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
