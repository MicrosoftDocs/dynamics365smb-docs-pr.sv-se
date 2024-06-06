---
title: Så här skapar du arbetsflöden från arbetsflödesmallar
description: Du kan spara tid när du skapar nya arbetsflöde för godkännande genom att skapa arbetsflöden från arbetsflödesmallar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-workflows-from-workflow-templates"></a>Skapa arbetsflöden från arbetsflödesmallar

På sidan **arbetsflöde** du skapar ett arbetsflöde genom att skapa en serie arbetsflödessteg på raderna. Varje steg består av en arbetsflödehändelse (När händelse), modifierad av händelsevillkor (På villkor), och ett arbetsflödesvar (Då svar) som modifieras av svarsalternativ. Fälten på arbetsflödesrader ger fasta listor över händelse- och svarsvärden som representerar scenarierna som [!INCLUDE [prod_short](includes/prod_short.md)] stödjer. Läs mer i [skapa arbetsflöden](across-how-to-create-workflows.md).

För att spara tid när du skapar arbetsflöden för godkännande tillhandahåller [!INCLUDE [prod_short](includes/prod_short.md)] arbetsflödesmallar. Mallarna finns på sidan **Arbetsflödesmallar**. Du kan använda mallarna som de är eller anpassa dem efter behov. Koderna för arbetsflödesmallar som skapas från Microsoft har prefixet **MS-**.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Om du ändrar en arbetsflödesmall men senare ångrar ändringen använder du åtgärden **Återställ Microsoft-mallar** för att återgå till den ursprungliga inställningen för arbetsflödet.

> [!CAUTION]
> Åtgärden **Återställ Microsoft-mallar** återställer alla Microsoft-arbetsflödesmallar. Du kan inte återställa en enskild mall.  

Ett annat sätt att snabbt skapa ett arbetsflöde är att importera det, till exempel om du har exporterat det från en annan instans av [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Så här skapar du ett arbetsflöde från en arbetsflödesmall

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.  
2. Välj åtgärden **Nytt arbetsflöde från mallen**. Sidan **arbetsflödesmallar**.  
3. Markera en arbetsflödesmall och välj sedan **OK**.  

   Sidan **Arbetsflöde** öppnas för ett nytt arbetsflöde som innehåller all information för den valda mallen. Värdet i fältet **Kod** utökas med till exempel ”-01" för att ange att det är det första arbetsflödet som skapas från arbetsflödesmallen.  
4. För att anpassa arbetsflödet redigerar du arbetsflödesstegen, eller lägger till nya steg. Läs mer i [skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se även

[Skapa arbetsflöden för godkännande](across-how-to-create-workflows.md)  
[Exportera och importera arbetsflöden för godkännande](across-how-to-export-and-import-workflows.md)  
[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)  
[Ta bort arbetsflöden för godkännande](across-how-to-delete-workflows.md)  
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Använda arbetsflöden för godkännande](across-use-workflows.md)  
[Arbetsflöde](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
