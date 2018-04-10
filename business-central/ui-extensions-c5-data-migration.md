---
title: "Använda tillägget C5 Data-migrering | Microsoft Docs"
description: "Använda det här tillägget för att flytta över kunder, leverantörer, artiklar och redovisningskonton från Microsoft Dynamics C5 2012 till Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 7fe6393ad43dbad032512b2d6d45cc8ee0392236
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a>Tillägget C5 för datamigrering för Business Central
Det här tillägget gör det enkelt att flytta över kunder, leverantörer, artiklar och dina redovisningskonton från Microsoft Dynamics C5 2012 till [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan också migrera historiska transaktioner för redovisningskonton.

> [!Note]
> Företag i [!INCLUDE[d365fin](includes/d365fin_md.md)] får inte innehålla några data. Dessutom, när du har startat en flyttning ska du inte skapa kunder, leverantörer, artiklar eller konton förrän migreringen har slutförts.

##<a name="what-data-is-migrated"></a>Vilka data överförs?
Följande data överförs för respektive enhet:

**Kunder**
* Plats
* Land
* Kunddimensioner (avdelning, center, ändamål)
* Utleveransmetod
* Säljare
* Betalningsvillkor
* Betalningssätt
* Kundprisgrupp
* Fakturarabatt för kund

Om du flyttar konton, flyttas även följande uppgifter:

* Kundbokföringsinställning
* Redovisningsjournaler
* Öppna kundreskontratransaktioner (kundreskontratransaktioner)

**Leverantör**
* Plats
* Land
* Leverantörsdimensioner (avdelning, center, ändamål)
* Fakturarabatt
* Utleveransmetod
* Inköpare
* Betalningsvillkor
* Betalningssätt
* Fakturarabatter för leverantör

Om du flyttar konton, flyttas även följande uppgifter:

* Leverantörsbokföringsinställningar
* Redovisningsjournaler
* Öppna transaktioner (leverantörsreskonstratransaktioner)

**Artiklar**
* Plats
* Land
* Artikeldimensioner (avdelning, center, ändamål)
* Försäljningsradrabatter
* Kundrabattgrupper
* Artikelrabattgrupper
* Försäljningspris
* Tullnummer
* Måttenheter
* Artikelspårningskod
* Kundprisgrupp

Om du flyttar konton, flyttas även följande uppgifter:

* Lagerbokföringsinställning
* Bokföringsinställningar
* Artikeljournaler
* Öppna transaktioner (artikeltransaktioner)

> [!Note]
> Om det finns öppna transaktioner med utländska valutor flyttas även valutakurserna för dessa valutor. Andra valutakurser överförs inte.

## <a name="to-migrate-data"></a>Migrera data
Det är bara några steg för att exportera data från C5 och importera den i [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. I C5 använd funktionen **exportera databas** för att exportera data. Skicka sedan exportmappen till en komprimerad mapp.  
2. I [!INCLUDE[d365fin](includes/d365fin_md.md)], välj ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Sök efter sida eller rapport"), ange **Datamigrering** och välj sedan **Datamigrering**.  
3. Följ instruktionerna i assisterad konfiguration. Se till att använda **Importera från Microsoft Dynamcis C5 2012** som datakälla.  

> [!Note]
> Företag lägger ofta till fält för att anpassa C5 till deras specifika verksamhet. [!INCLUDE[d365fin](includes/d365fin_md.md)] flyttar inte över data från anpassade fält. Migreringen misslyckas även om det finns fler än 10 anpassade fält.

## <a name="viewing-the-status-of-the-migration"></a>Visa status för migreringen.
Använd sidan **översikt över datamigrering** för att övervaka flyttningen. På sidan visas information som till exempel antal enheter som migreringen omfattar, flyttning och antalet artiklar som har överförts och om de lyckades. Den visar antalet fel, låter dig ta reda på vad som orsakade problemet och, när det är möjligt, gör det enkelt att gå till enheten för att lösa problemen. Mer information finns i nästa avsnitt i den här artikeln.  

> [!Note]
> Medan du väntar på resultat från migreringen, måste du uppdatera sidan för att visa resultatet.

## <a name="correcting-errors"></a>Felkorrigering
Om något går fel och ett fel uppstår kommer fältet **Status** att visa **Slutförd med fel** och fältet **Antal fel** visar hur många. Om du vill visa en lista över felen, öppnar du sidan **migreringsfel** genom att välja:  

* Numret i fältet **antal fel** för enheten.  
* Enheten och åtgärden **Visa fel**.  

På sidan **migreringsfel**, om du vill korrigera ett fel kan du välja ett felmeddelande och sedan välja **redigera post** för att öppna en sida som visar de migrerade data för enheten. När du har korrigerat ett eller flera fel kan du välja **Migrera** för att endast överföra de enheter som har fastställts, utan att behöva starta om flyttningen helt.  

> [!Tip]
> Om du har kopplat mer än ett fel, kan du använda funktionen **Välj flera** om du vill markera flera rader att migrera. Om det finns fel som inte är viktiga att fixa kan du välja dem och sedan välja **hoppa över val**.

> [!Note]
> Om du har artiklar som ingår i en struktur kan du behöva migrera flera gånger om det ursprungliga objektet inte skapas innan alla varianter som refererar till den. Om en artikelvariant skapas först blir kan referensen till det ursprungliga objektet orsaka ett felmeddelande.  

## <a name="verifying-data-after-migrating"></a>Kontrollera data efter migrering
Ett sätt att kontrollera att informationen överförs på rätt sätt är att titta på följande sidor i C5 och [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|Kundtransaktioner| Redovisningsjournaler|
|Leverantörstransaktioner| Redovisningsjournaler|
|Artikeltransaktioner| Artikeljournaler|

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kallas journalen för migrerade data för **C5MIGRATE**.

## <a name="stopping-data-migration"></a>Stoppa datamigrering
Du kan förhindra migrering av data genom att välja **Stoppa alla migreringar**. Om du gör det kommer alla väntande migreringar också stoppas.

## <a name="see-also"></a>Se även
[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  
[Komma igång](product-get-started.md) 

