---
title: "Använda tillägget QuickBooks-migrering | Microsoft Docs"
description: "Beskriver hur du använder tillägget för att migrera kunder, leverantörer, artiklar och konton från QuickBooks Online till Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fe87a108d132ff25f0c93a51df58bb88fb12f421
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---

# <a name="the-quickbooks-online-data-migration-extension-for-dynamics-365-for-financials"></a>Tillägget QuickBooks Online datamigrering för Dynamics 365 for Financials
Tillägget ingår i assisterade guiden **datamigrering** som hjälper dig att migrera viktiga affärsdata från QuickBooks Online till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Detta är exempelvis användbart när företaget växer och du har bestämt dig för att uppgradera ditt program för hantering av företag genom att börja använda [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="what-data-can-i-import-from-quickbooks-online"></a>Vilka data kan jag importera från QuickBooks Online?
Du kan importera följande data från QuickBooks Online till [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Kunder
* Leverantör
* Artiklar
* Kontoplan 
* Transaktion för ingående saldo i redovisningen
* Tillgängliga kvantiteter för lagerartiklar
* Öppna dokument för kunder och leverantörer, till exempel fakturor, kreditnotor och betalningar

Vi migrerar endast hela belopp på försäljnings- och inköpsdokument. Vi uppdaterar inte delvis betalda belopp. Exempelvis om en kund har betalat 300 av totalt 500 kronor på en försäljningsfaktura, migrerar vi hela 500. Om du har fått delbetalningar, måste du uppdatera dessa manuellt innan eller efter du migrerar data. Vi rekommenderar att installera utestående transaktioner innan du migrerar för att underlätta efteråt.

> [!NOTE]  
>   Vi migrerar inte inköpsorder eller försäljningsorder.

## <a name="before-you-start"></a>Innan du börjar
En viktig del av är att ange konton för att migrera transaktionerna till. Det är praktiskt att planera den här mappningen innan du migrerar data. Exempelvis konton där du bokför transaktioner för:  
  
* Försäljning av artiklar eller tjänster till kunder.
* Köp av varor eller tjänster från en leverantör.  
* Justeringar i redovisningen.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kräver att redovisningskonton har tilldelade kontonummer. Kontrollera att nummer tilldelas till kontona i QuickBooks Online.

Transaktioner i QuickBooks Online måste ha skattebelopp, du ställer in ett skattekonto för din skattemyndighet i [!INCLUDE[d365fin](includes/d365fin_md.md)] innan du kan bokföra transaktioner.

## <a name="how-do-i-start-using-the-extension"></a>Hur börjar jag använda tillägget?
Komma igång enkelt. Allt du behöver göra är att köra den assisterade guiden **datamigrering**. Så här gör du:

1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Assisterad konfiguration** och välj sedan **Migrera affärsdata**.
2. Följ instruktionerna i varje steg i guiden assisterad konfiguration.

## <a name="what-do-i-do-after-i-migrate-data"></a>Vad gör jag efter att jag har migrerat data?
När du har migrerat data har transaktionerna statusen **ej bokförda**, så att du kan granska dem och göra ändringar. Gå till sidan där du normalt hittar dem om du vill granska transaktionerna. Till exempel för att visa ej bokförda fakturor, går du till sidan **försäljningsfakturor**. Om du vill gå igenom journaler, går du till sidan **betalningsjournaler**.   

Det finns några saker som du bör göra:

* Om transaktionerna i QuickBooks Online har markerade eller rabatterade belopp måste du manuellt lägga till beloppen till de relaterade transaktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)]innan du bokför dem.
* Om du använder moms kan du behöva lägga till en rörelsebokföringsmall och en produktbokföringsmall till bokföringsinställningar så att du kan bokföra moms.
* Kontrollera de ingående saldona för konton i redovisningen. QuickBooks Online sparar inte aktuellt saldo för alla konton, så du kan behöva åtgärda ingående saldon.

## <a name="see-also"></a>Se även
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  

