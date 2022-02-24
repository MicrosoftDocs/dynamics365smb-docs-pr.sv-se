---
title: Använda tillägget QuickBooks-migrering | Microsoft Docs
description: Beskriver hur du använder tillägget för att importera kunder, leverantörer, artiklar och konton från QuickBooks Desktop till Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 9b5129e4e9ddfe60d969e705d62e023716cde5b6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2311146"
---
# <a name="the-quickbooks-data-migration-extension"></a>Tillägget QuickBooks datamigrering
Detta tillägg gör det enkelt att migrera kunder, leverantörer, artiklar och konton från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om ditt företag använder QuickBooks i dag, kan du exportera nödvändig information och sedan öppna guiden för assisterad konfiguration för att överföra data till [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Mer information finns i [Importera företagsdata från ett annat finanssystem](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Data från QuickBooks Desktop
 
Du kan importera följande data från QuickBooks Online till Business Central:

- Kunder  
- Leverantör  
- Artiklar  
- Kontoplan  
- Transaktion för ingående saldo i redovisningen  
- Tillgängliga kvantiteter för lagerartiklar  
- Öppna dokument för kunder och leverantörer, till exempel fakturor, kreditnotor och betalningar  

Vi migrerar endast hela belopp på försäljnings- och inköpsdokument. Vi uppdaterar inte delvis betalda belopp. Exempelvis om en kund har betalat 300 av totalt 500 kronor på en försäljningsfaktura, migrerar vi hela 500. Om du har fått delbetalningar, måste du uppdatera dessa manuellt innan eller efter du migrerar data. Vi rekommenderar att installera utestående transaktioner innan du migrerar för att underlätta efteråt.

> [!NOTE]
> Vi migrerar inte inköpsorder eller försäljningsorder.

## <a name="before-you-start"></a>Innan du börjar
En viktig del av är att ange konton för att migrera transaktionerna till. Det är praktiskt att planera den här mappningen innan du migrerar data. Exempelvis konton där du bokför transaktioner för:

- Försäljning av artiklar eller tjänster till kunder.  
- Köp av varor eller tjänster från en leverantör.  
- Justeringar i redovisningen.  

Business Central kräver att redovisningskonton har tilldelade kontonummer. Kontrollera att nummer tilldelas till kontona i QuickBooks.
Transaktioner i QuickBooks måste ha skattebelopp, du ställer in ett skattekonto för din skattemyndighet i Business Central innan du kan bokföra transaktioner.

För att hämta data från QuickBooks desktop-programmet måste du hämta Microsofts verktyg för dataexportering.  Instruktioner för verktyget finns i datamigreringsguiden i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Verktyget ansluter dig till QuickBooks-programmet och exporterar tillämpliga data till en .zip-fil.  

> [!NOTE]
> För närvarande fungerar verktyget för dataexportering bara med QuickBooks 2017 och 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Hitta tillägget QuickBooks datamigrering
Tillägget QuickBooks datamigrering är installerat och klart som en integrerad del av guiden för assisterad konfiguration av datamigrering. Om du är redo att börja nu och har exporterat dina data från QuickBooks, välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Assisterad konfiguration** och välj sedan relaterad länk. Välj **Migrera affärsdata** och följ sedan anvisningarna i guiden.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Vad gör jag efter att jag har migrerat data?
När du har migrerat data har transaktionerna statusen ej bokförda, så att du kan granska dem och göra ändringar. Gå till sidan där du normalt hittar dem om du vill granska transaktionerna. Till exempel för att visa ej bokförda fakturor, går du till sidan försäljningsfakturor. Om du vill gå igenom journaler, går du till sidan betalningsjournaler.
Det finns några saker som du bör göra: om transaktionerna i QuickBooks hade pålägg eller rabattbelopp, måste du manuellt lägga till beloppen till de relaterade transaktionerna i Business Central innan du bokför dem.
Om du använder moms kan du behöva lägga till en rörelsebokföringsmall och en produktbokföringsmall till bokföringsinställningar så att du kan bokföra moms.
Kontrollera de ingående saldona för konton i redovisningen. QuickBooks sparar inte aktuellt saldo för alla konton, så du kan behöva åtgärda ingående saldon.

## <a name="see-also"></a>Se även
[Importera verksamhetsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
