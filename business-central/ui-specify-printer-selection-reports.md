---
title: Ange en standardskrivare
description: Lär dig om olika sätt att konfigurera skrivare som ska användas som standard för utskriftsjobb.
author: jswymer
ms.topic: how-to
ms.reviewer: na
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="specify-a-default-printer"></a><a name="default"></a>Ange en standardskrivare

När du har skapat en skrivare i Business Central kan du ange vilken skrivare som ska användas som standard. Det finns ett par sätt att ange skrivare som ska användas som standard för rapporter och andra utskriftsjobb. En standardskrivare är användbar om du arbetar med olika rapporter som kräver olika skrivare på grund av sin placering i företaget eller deras utskriftskapacitet.

> [!IMPORTANT]
> De enda skrivare som du kan ange som standard är **Microsoft skriv ut till PDF** och molnskrivare som redan har ställts in för användning i Business Central, som e-postskrivare och skrivare för Universell utskrift. Molnskrivare konfigureras vanligtvis av en administratör. Mer information finns i [Skrivarinställningar och hantering](admin-printer-setup-overview.md).   

## <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Ange en skrivare som standardskrivare för alla utskriftsjobb

På sidan **Skrivarhantering** kan du ställa in en skrivare som standardskrivare för alla utskriftsjobb. Du kan ange skrivaren som standard för dig eller för alla användare.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utskriftshantering** och väljer sedan relaterad länk.

    > [!TIP]
    > Du kan också öppna sidan **Utskriftshantering** från sidan **Skrivarval** genom att välja **Utskriftshantering**.  
2. På sidan **Utskriftshantering** välj en skrivare från listan, välj **Hantera**, välj sedan **Ange som standardskrivare** eller **Använd som standardskrivare för alla användare**.

> [!NOTE]
> Om du anger en standardskrivare från **Skrivarhantering** läggs en post till i **skrivarvalet**.

## <a name="set-a-default-printer-for-specific-reports"></a>Ange standardskrivaren för specifika rapporter

På sidan **Skrivarval** kan du ange skrivaren som en rapport ska använda som standard. Standard skrivare är inställda på användarkontots grunder. Du kan ange en standardskrivare för bara dig själv, en annan användare eller alla användare.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Utskriftsval** och väljer sedan relaterad länk. Du kan också välja en skrivare på sidan **Skrivarhantering** och sedan välja åtgärden **Skrivarval**.
2. Välj åtgärden **Ny** om du vill lägga till ett Skrivarhantering för en specifik rapport.
3. Fyll i fälten om det behövs.

Den angivna rapporten är nu konfigurerad för att skriva ut på den valda skrivaren som standard.

> [!NOTE]
> När du skriver ut rapporten i fråga kan du välja en annan med hjälp av fältet **Skriv ut** på sidan för rapportbegäran.

> [!NOTE]
> Om du inte anger en rapport för en viss skrivare på sidan **Skrivarhantering** kommer den att skrivas ut till företagets standardskrivare enligt definitionen på sidan **Skrivarhantering**.

Du eller administratören kan också använda sidan **Skrivarhantering** för att definiera andra utskriftsvariationer för användare och rapporter. I följande tabell beskrivs kombinationen av värdena för att ange olika utskriftsinställningar för en rapport.

|Till                                                 |Ange följande värden                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Skriv ut en rapport till en viss skrivare för alla användare |Ange värden i fälten **Rapport-ID** och **Skrivarnamn** och lämna fältet **Användar-ID** tomt.|
|Skriv ut alla rapporter till en viss skrivare för en specifik användare|Ange värden i fälten **Användar-ID** och **Skrivarnamn** och lämna fältet **Rapport-ID** tomt. Denna post gör samma sak som åtgärden **Ange som standardskrivare** på sidan **Utskriftshantering**.|
|Ange standardskrivaren för alla rapporter för alla användare|Ange ett värde i fälten **Skrivarnamn** och lämna fälten **Användar-ID** och **Rapport-ID** tomma. Denna post gör samma sak som åtgärden **Ange som standardskrivare för alla användare** på sidan **Utskriftshantering**.|
|Skriv ut en viss rapport till användarens standardskrivare|Ange ett värde i fältet **Rapport-ID** och lämna fälten **Skrivarnamn** och **Användar-ID** tomma.|
|Skriv ut en specifik rapport till en viss skrivare för en viss användare|Ange värden i samtliga tre fält.|

> [!NOTE]
> Mer specifika skrivarval har företräde framför mer allmänna skrivarval. Ett skrivarval som exempelvis har värden i fälten **Användar-ID**, **Rapport-ID** och **Skrivarnamn** har företräde framför ett skrivarval som innehåller tomma poster i fälten **Användar-ID** och **Rapport-ID**.

## <a name="choosing-the-printer-when-running-a-report"></a>Välja skrivare när en rapport körs

I stället för att använda standardskrivaren när du kör en rapport kan du åsidosätta inställningen från begärandesidan. Välj helt enkelt den skrivare som du vill använda för denna rapportgenerering i listrutan **Skrivare**.

## <a name="sizing-print-jobs"></a>Ändra storlek på utskriftsjobb

Molnutskrift är utformat för dokument av rimligt storlek. De flesta molntjänster, inklusive PrintNode och HP ePrint, har en gräns på 10 MB per jobb. Om du behöver skriva ut större rapporter måste du kanske dela upp dem i flera utskrifter.

## <a name="see-also"></a>Se även

[Skrivarhantering](admin-printer-setup-overview.md)  
[Konfigurera skrivare för Universell utskrift](admin-printer-setup-universal-print.md)  
[Konfigurera e-postutskrift](admin-printer-setup-email.md)  
[Skriva ut en rapport](ui-work-report.md#PrintReport)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kör batchjobb](ui-how-run-batch-jobs.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
