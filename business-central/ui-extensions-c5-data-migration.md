---
title: Använda tillägget C5 Data-migrering | Microsoft Docs
description: 'Använd det här tillägget för att flytta över kunder, leverantörer, artiklar och redovisningskonton från Microsoft Dynamics C5 2012 till Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'extension, migrate, data, C5, import'
ms.search.form: '1860, 1861, 1862, 1863, 1864, 1867, 1868, 1869, 1874, 1882, 1883, 1884, 1885, 1886, 1888, 1890, 1891, 1892, 1893, 1894, 1898, 1899, 1900, 1901, 1902, 1903, 1904, 1905, 1906'
ms.date: 12/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-c5-data-migration-extension"></a>Tillägget C5 datamigrering

Det här tillägget gör det enkelt att flytta över kunder, leverantörer, artiklar och dina redovisningskonton från Microsoft Dynamics C5 2012 till [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan också migrera historiska transaktioner för redovisningskonton.

> [!NOTE]
> Företag i [!INCLUDE[prod_short](includes/prod_short.md)] får inte innehålla några data. Dessutom, när du har startat en flyttning ska du inte skapa kunder, leverantörer, artiklar eller konton förrän migreringen har slutförts.

## <a name="what-data-is-migrated"></a>Vilka data migreras?

Följande data överförs för respektive enhet:

### <a name="customers"></a>Kunder

* Kontakter  
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

### <a name="vendors"></a>Leverantör

* Kontakter
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

### <a name="items"></a>Artiklar

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
* Monteringsstrukturer

Om du flyttar konton, flyttas även följande uppgifter:

* Lagerbokföringsinställning
* Bokföringsinställningar
* Artikeljournaler
* Öppna transaktioner (artikeltransaktioner)

> [!NOTE]
> Om det finns öppna transaktioner med utländska valutor flyttas även valutakurserna för dessa valutor. Andra valutakurser överförs inte.

### <a name="chart-of-accounts"></a>Kontoplan

* Standarddimensioner: avdelning, kostnadsställe, ändamål  
* Historiska redovisningstransaktioner  

> [!NOTE]
> Historiska redovisningstransaktioner hanteras på olika sätt. När du migrerar data ställer du in en parameter för **aktuell period**. Den här parametern anger hur du behandlar redovisningstransaktioner. Transaktioner efter detta datum migreras individuellt. Transaktioner före det här datumet läggs samman per konto och flyttas över som ett enstaka belopp. Låt oss anta att det finns transaktioner i 2015, 2016, 2017, 2018, och du anger 01 januari 2017 i fältet Aktuell period. För varje konto samlas belopp för transaktioner på eller före den 31 december 2106 i en enda redovisningsjournalrad för varje redovisningskonto. Alla transaktioner efter detta datum migreras individuellt.

## <a name="file-size-requirements"></a>Storlekskraven i filen

Den största filstorleken som du kan överföra till [!INCLUDE[prod_short](includes/prod_short.md)] är 150 MB. Om filen du exporterar från C5 är större än detta kan du flytta över data i flera filer. Till exempel exportera en eller två typer av enheter från C5, såsom kunder och leverantörer, till en fil och sedan exportera objekt till en annan fil och så vidare. Du kan importera filer var för sig i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-migrate-data"></a>Migrera data

Det är bara några steg för att exportera data från C5 och importera den i [!INCLUDE[prod_short](includes/prod_short.md)]:  

1. I C5 använd funktionen **exportera databas** för att exportera data. Skicka sedan exportmappen till en komprimerad mapp.  
2. I [!INCLUDE[prod_short](includes/prod_short.md)] välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **datamigrering** och välj **datamigrering**.  
3. Följ instruktionerna i assisterad konfiguration. Se till att använda **Importera från Microsoft Dynamics C5 2012** som datakälla.  

## <a name="viewing-the-status-of-the-migration"></a>Visa status för migreringen

Använd sidan **översikt över datamigrering** för att övervaka flyttningen. På sidan visas information som till exempel antal enheter som migreringen omfattar, flyttning och antalet artiklar som har överförts och om de lyckades. Den visar antalet fel, låter dig ta reda på vad som orsakade problemet och, när det är möjligt, gör det enkelt att gå till enheten för att lösa problemen. Mer information finns i nästa avsnitt i den här artikeln.  

> [!NOTE]
> Medan du väntar på resultat från migreringen, måste du uppdatera sidan för att visa resultatet.

## <a name="how-to-avoid-double-posting"></a>Så här undviker du dubbel bokföring

För att undvika dubbel bokföring i redovisningen används följande balansräkningskonton för öppna transaktioner:  

* För leverantörer använder vi A/P-konto från leverantörsbokföringsmallen.  
* För kunder använder vi A/P-konto från kundbokföringsmallen.  
* För artiklar skapar vi en bokföringsinställning där kontot för lagerjusteringar är det konto som anges som lagerkontot i fönstret Lagerbokföringsinställning.  

## <a name="correcting-errors"></a>Felkorrigering

Om något går fel och ett fel uppstår kommer fältet **Status** att visa **Slutförd med fel** och fältet **Antal fel** visar hur många. Om du vill visa en lista över felen, öppnar du sidan **migreringsfel** genom att välja:  

* Numret i fältet **antal fel** för enheten.  
* Enheten och åtgärden **Visa fel**.  

På sidan **migreringsfel**, om du vill korrigera ett fel kan du välja ett felmeddelande och sedan välja **redigera post** för att visa de migrerade data för enheten. Om du har flera fel att fixa kan du välja **reparera flera fel** för att redigera poster i en lista. Du behöver öppna enskilda poster om felet orsakades av en relaterad post. Om t. ex. en leverantör inte vill migrera om en e-postadress för en av deras kontakter har ett felaktigt format.

När du har korrigerat ett eller flera fel kan du välja **Migrera** för att endast överföra de enheter som har fastställts, utan att behöva starta om flyttningen helt.  

> [!TIP]
> Om du har kopplat mer än ett fel, kan du använda funktionen **Välj flera** om du vill markera flera rader att migrera. Om det finns fel som inte är viktiga att fixa kan du välja dem och sedan välja **hoppa över val**.

> [!NOTE]
> Om du har artiklar som ingår i en struktur kan du behöva migrera flera gånger om det ursprungliga objektet inte skapas innan alla varianter som refererar till den. Om en artikelvariant skapas först blir kan referensen till det ursprungliga objektet orsaka ett felmeddelande.  

## <a name="verifying-data-after-migrating"></a>Kontrollera data efter migrering

Ett sätt att kontrollera att informationen överförs på rätt sätt är att titta på följande sidor i C5 och [!INCLUDE[prod_short](includes/prod_short.md)].

|Microsoft Dynamics C5 2012 | Dynamics 365 Business Central| Batch-jobb som ska användas |
|---------------------------|------------------------------|------------------|
|Kundtransaktioner| Redovisningsjournaler| CUSTMIGR |
|Leverantörstransaktioner| Redovisningsjournaler| VENDMIGR|
|Artikeltransaktioner| Artikeljournaler| ITEMMIGR |
|Redovisningstransaktioner| Redovisningsjournaler| GLACMIGR |

## <a name="stopping-data-migration"></a>Stoppa datamigrering

Du kan förhindra migrering av data genom att välja **Stoppa alla migreringar**. Om du gör det kommer alla väntande migreringar också stoppas.

## <a name="see-also"></a>Se även

[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
