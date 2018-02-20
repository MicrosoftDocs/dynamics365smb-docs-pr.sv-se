---
title: "Importera dina äldre affärsdata i Finance and Operations, Business edition | Microsoft Docs"
description: "Du kan migrera data för exempelvis kunder, leverantörer och lager från Excel, QuickBooks eller Dynamics GP till Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QuickBooks, transfer, import, migrate, initialize, implement
ms.date: 09/25/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f1339468507efc474c709f35fa04d61ca7e5b9a2
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a>Importera verksamhetsdata från andra finanssystem
När du registrerar dig på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du välja att skapa ett tomt företag så att du kan överföra din egen information och testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget. Beroende på finanslösningen som används i din verksamhet idag, kan du överföra information om kunder, leverantörer, lager och bankkonton.  

Från startsidan kan du starta en guide för assisterad installation som hjälper dig att överföra affärsdata från en Excel-fil eller från andra format. Typen av filer som du kan överföra, beror på tilläggen som är tillgängliga. Du kan till exempel migrera data från QuickBooks, eftersom [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett tillägg som ska hantera omvandlingen från QuickBooks. Om du vill migrera data från andra finanslösningar, måste du antingen kontrollera om det finns ett tillägg för den lösningen eller importera från Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]  inkluderar mallar förkonton, kunder, leverantörer och lagerartiklar som du kan välja att koppla, när du importerar dina data.  

## <a name="importing-data-from-quickbooks-desktop-quickbooks-online-or-dynamics-gp"></a>Importera data från QuickBooks Desktop, QuickBooks Online eller Dynamics GP
Om ditt arbete använder QuickBooks eller Dynamics GP i dag, kan du exportera den relevanta informationen till en fil. Därefter kan du öppna guiden för assisterad installation och överföra data.
Om till exempel din fil innehåller kunder och leverantörer, kan du välja att överföra endast kunddatan. Därefter kan du överföra resten av den senare.  

Guiden för assisterad installation omfattar ett alternativ för att ändra standardkonfigurationen för överföring, men vi rekommenderar att du bara gör den avancerade inställningen om du är van vid databastabeller. I de flesta företag kommer standardmappningen från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)] överföra den information som du vill.  

Mer information finns i [QuickBooks Desktop datamigrering](ui-extensions-quickbooks-data-migration.md), [QuickBooks Online datamigrering](ui-extensions-quickbooks-online-data-migration.md), eller [Dynamics GP datamigrering](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="importing-data-from-configuration-packages"></a>Importera data från ett konfigurationspaket
[!INCLUDE[d365fin](includes/d365fin_md.md)]  innehåller ett konfigurationpaket som du kan exportera till Excel och ange dina data där. Sedan kan du importera datan från Excel igen. Paketet består av 27 register, inklusive huvuddata som t.ex. kunder, leverantörer, artiklar och konton, andra grundläggande inställningstabeller, som till exempel leveransmetoder och transaktionstabeller som t.ex. rubrik och rader.  

> [!NOTE]  
>   Att arbeta med konfigurationpaket innebär avancerade funktioner och vi rekommenderar att du kontaktar din administratör. Mer information finns i [Importera data från äldre redovisningsprogrammet med ett konfigurationspaket](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Importera data från äldre redovisningsprogrammet med ett konfigurationspaket](across-import-data-configuration-packages.md).  
[QuickBooks Desktop datamigrering](ui-extensions-quickbooks-data-migration.md)  
[QuickBooks Online datamigrering](ui-extensions-quickbooks-online-data-migration.md)  
[Dynamics GP Datamigrering](ui-extensions-dynamicsgp-data-migration.md)  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)   
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

