---
title: "Importera affärsdata äldre till Financials | Microsoft Docs"
description: Beskriver hur du kan importera egna data till Dynamics 365 for Financials.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migrate, initialize, implement
ms.date: 04/27/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 001dccf7935f38dd2f409e4fea31598a279472d4
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="importing-business-data-from-other-finance-systems"></a>Importera verksamhetsdata från andra finanssystem
När du registrerar dig på [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du välja att skapa ett tomt företag så att du kan överföra din egen information och testa det nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företaget. Beroende på finanslösningen som används i din verksamhet idag, kan du överföra information om kunder, leverantörer, lager och bankkonton.  

Från startsidan kan du starta en guide för assisterad installation som hjälper dig att överföra affärsdata från en Excel-fil eller från andra format. Typen av filer som du kan överföra, beror på tilläggen som är tillgängliga. Du kan till exempel migrera data från QuickBooks, eftersom [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett tillägg som ska hantera omvandlingen från QuickBooks. Om du vill migrera data från andra finanslösningar, måste du antingen kontrollera om det finns ett tillägg för den lösningen eller importera från Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderar mallar förkonton, kunder, leverantörer och lagerartiklar som du kan välja att koppla, när du importerar dina data.  

## <a name="importing-data-from-quickbooks-or-dynamics-gp"></a>Importera data från QuickBooks eller Dynamics GP
Om ditt arbete använder QuickBooks eller Dynamics GP i dag, kan du exportera den relevanta informationen till en fil. Därefter kan du öppna guiden för assisterad installation och överföra data.
Om till exempel din fil innehåller kunder och leverantörer, kan du välja att överföra endast kunddatan. Därefter kan du överföra resten av den senare.  

Guiden för assisterad installation omfattar ett alternativ för att ändra standardkonfigurationen för överföring, men vi rekommenderar att du bara gör den avancerade inställningen om du är van vid databastabeller. I de flesta företag kommer standardmappningen från QuickBooks till [!INCLUDE[d365fin](includes/d365fin_md.md)] överföra den information som du vill.  

## <a name="importing-data-from-configuration-packages"></a>Importera data från ett konfigurationspaket
[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett konfigurationpaket som du kan exportera till Excel och ange dina data där. Sedan kan du importera datan från Excel igen. Paketet består av 27 register, inklusive huvuddata som t.ex. kunder, leverantörer, artiklar och konton, andra grundläggande inställningstabeller, som till exempel leveransmetoder och transaktionstabeller som t.ex. rubrik och rader.  

> [!NOTE]  
>  Att arbeta med konfigurationpaket innebär avancerade funktioner och vi rekommenderar att du kontaktar din administratör. Mer information finns i [Importera data från äldre redovisningsprogrammet med ett konfigurationspaket](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)  
[Importera data från äldre redovisningsprogrammet med ett konfigurationspaket](across-import-data-configuration-packages.md).  
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)]med tillägg](ui-extensions.md)   
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
