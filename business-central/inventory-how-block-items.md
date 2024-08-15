---
title: Så här spärrar du artiklar eller artikelvarianter från försäljning eller inköp
description: Du kan spärra artiklar och artikelvarianter från att registreras på rader i försäljnings- eller inköpsdokument eller från att bokföras i en transaktion.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 05/16/2024
ms.service: dynamics-365-business-central
---

# Spärra artiklar eller artikelvarianter från försäljning eller inköp

Du kan spärra artiklar och artikelvarianter så att dessa inte kan registreras på rader i försäljnings- eller inköpsdokument, och du kan även spärra dem från att publiceras i transaktioner. Detta kan till exempel vara användbart när en artikel har en känd defekt. Om någon väljer en spärrad artikel eller variant i ett försäljnings- eller inköpsdokument kommer ett meddelande att informera vederbörande om att artikeln är spärrad.

I följande tabell beskrivs vad som händer när artiklar eller varianter spärras.  

|Alternativ|Description|  
|--------------------|------------|  
|**Spärrad för försäljning**|Du kan inte välja artikeln eller varianten i ett försäljningsdokument eller en artikeljournal för försäljning.|  
|**Spärrad för inköp**|Du kan inte välja artikeln eller varianten i ett inköpsdokument, en artikeljournal för inköp eller i planeringsprocesser för inköp.|  
|**Spärrad**|Du kan inte inkludera artikeln eller varianten när du bokför transaktioner.|  

> [!NOTE]
> Spärrade artiklar kan returneras. Detta innebär att inga av inställningarna ovan gäller för returorder och kreditnotor.

När du använder åtgärden **Kopiera från dokument** för att skapa nya dokument som bygger på befintliga dokument får du ett meddelande om någon artikel eller variant på källdokumentraderna är spärrad. De spärrade dokumentraderna tas inte med i det nya dokumentet och ett meddelande visar en översikt över alla dokumentrader som har spärrats i källdokumentet.

## Så här spärrar du en artikel  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.  
2. Beroende på vad du vill göra väljer du artikel och markerar sedan en eller flera av följande kryssrutor:
    * **Spärrad**
    * **Spärrad för försäljning**
    * **Spärrad för inköp**  

## Så här spärrar du en artikelvariant  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk.  
2. Välj den artikel som har en variant som du vill spärra, välj **Varianter** och markera sedan en eller flera av följande kryssrutor:  
    * **Spärrad**
    * **Spärrad för försäljning**
    * **Spärrad för inköp**

## Se även  

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]