---
title: Introduktion till produktion för Contoso Coffee
description: Översikt över scenarier som kan vara till hjälp när demonstrationsdatan för Contoso Coffee ska hjälpa dig lära dig hur du använder produktionsfunktionerna i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# Introduktion till produktion för Contoso Coffee

Contoso Coffee är ett fiktivt företag som tillverkar kaffemaskiner för privat och kommersiellt bruk. **Contoso Coffee**-apparna för Business Central lägger till demonstrationsdata som du kan använda för att lära dig använda produktionsfunktionerna i Business Central.  

Appen tillhandahåller fyra produkter som är optimerade för olika scenarier:

- **SP-SCM1009 Airpot**  

  Den här produkten är en strukturlista med ett detaljmontage, **Operationsföljd**. Använd denna för att visa standardproduktionsflödet. Den är inställd med alternativa operationsföljder som du kan använda för att demonstrera olika scenarier som innehåller underleverantörer. Värderingsmetoden är *Standard*.  

- **SP-SCM1011 Airpot Duo**  

  För den här produkten krävs artikelspårning, och den har en komponent som också kräver artikelspårning. Värderingsmetoden är *Specifik*.  

- **SP-SCM1004 Autodrip**  

  Den här produkten är en struktur med ett detaljmontage, **Operationsföljd**. Vi rekommenderar detta för att demonstrera de olika "flushing"-metoderna för såväl komponenter som åtgärder. Värderingsmetoden är *Standard*.

- **SP-SCM1006 AutoDripLite**

  Denna produkt har tre varianter och tre strukturlistor som kan tilldelas lagerställeenheter. Produkten använder det fiktiva strukturkonceptet. Värderingsmetoden är *Standard*.

Tillverkningsaktiviteterna för alla scenarier använder platsen *NORR*.  

> [!IMPORTANT]
> Innan du kör något av scenarierna för Contoso Coffee bokför du eventuella artikeljournalrader med ingående balanser. Mer information finns i avsnittet [Konfigurera data för Contoso Coffee](#set-up-contoso-coffee-manufacturing-data).

## Ställ in data för produktion för Contoso Coffee

Om du vill använda demonstrationsdata för produktion för Contoso Coffee måste du installera två appar i det aktuella företaget i [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Demonstrationsdatauppsättning för Contoso Coffee**  

    Den här appen levererar demonstrationsdata för basprogrammet.  
- **Demonstrationsdatauppsättning för Contoso Coffee (lands-ID)**  

    Den här appen lägger till landsspecifika innehåll ovanpå basprogrammet.

Lägg till programmen i ett tomt företag i en betald prenumeration eller som en del av en utvärderingsversion. Du kan till exempel skapa ett nytt företag utan exempeldata från den assisterade konfigurationsguiden **Skapa nytt företag** som du kan öppna från listan **Företag**. Lägg sedan till programmen från [marknadsplatsen](../../ui-extensions-install-uninstall.md#install) om de inte redan anges på sidan **Tilläggshantering**.  

När de relevanta apparna har installerats går du till sidan [Demonstrationsdata för Contoso Coffee](https://businesscentral.dynamics.com/?page=4760) i [!INCLUDE [prod_short](../../includes/prod_short.md)] och ändrar standardinställningarna så att de passar dina behov. Inställningarna beskrivs i följande tabell:  

|Fält  |Beskrivning  |
|---------|---------|
|**Startår** |Anger det första år som du vill använda för demonstrationsdata för Contoso Coffee. Beroende på företagets konfiguration är året antingen ett kalender år eller ett räkenskapsår.|
|**Produktionsplats** |Anger det distributionslager som du vill använda för produktionsåtgärder. Standardvärdet är *NORR*, men du kan ändra detta så att det passar dina behov.|
|**Företagstyp**    |Anger om det aktuella företaget måste rapportera moms eller omsättningsskatt. |
|**Inrikes – generell rörelsebokföringsmall**|Anger en företagskod för inrikes kunder och leverantörer. Affärskoderna används när transaktionerna bokförs. |
|**Kapacitet – generell produktbokföringsmall**    |Anger en kod för artiklar eller resurser som måste användas för bokföringskapacitet.|
|**Detaljhandel – generell produktbokföringsmall**    |Anger en kod för artiklar eller resurser som måste användas för bokföring av detaljhandel.|
|**Rå – generell produktbokföringsmall**    |Anger en kod för artiklar eller resurser som måste användas för bokföring av råmaterial. |
|**Basmomskod**    |Anger en befintlig produkgrupp för moms som ska användas för artiklar.|
|**Färdig kod**    |Anger en befintlig produktgrupp som ska användas för färdiga artiklar.|
|**Prisfaktor**     |Anger en faktor för att omvandla ett pris från USD/EUR till lokal valuta. *1* innebär att priset är samma belopp i alla valutor. Ett högre värde används för att hämta priset i lokal valuta. |
|**Avrundningsprecision**  |Definierar hur de beräknade förbrukningskvantiteterna avrundas när de registreras på förbrukningsjournalrader. Kvantiteter mindre än 0,5 avrundas nedåt. Kvantiteter lika med eller högre än 0,5 avrundas uppåt.|

Välj åtgärden **Skapa demonstrationsdata** när du är klar. Det tar några minuter att lägga till data i den underliggande databasen, men sedan är det dags att köra de olika scenarierna.  

## Scenarierna

Demonstrationsdata för produktion för Contoso Coffee stöder för närvarande följande produktionsscenarier för test och utbildning:

1. [Skapa en ny produktionsstruktur och strukturversion](create-new-production-bom-version.md)  
2. [Skapa en ny operationsföljd](create-new-routing.md)  
3. [Skapa en fast planerad produktionsorder och ändra den](create-firm-planned-production-order-change.md)  
4. [Kombinera automatisk och manuell "flushing"](combine-automatic-manual-flushing.md)  
5. [Använda orderplanering för att skapa och reservera leverans](order-planning-create-reserve-supply.md)  
6. [Ställ in och hantera en legotillverkningsoperation](set-up-process-subcontracting-operation.md)  
7. [Skapa en ny kapacitet](set-up-new-capacity.md)  
8. [Prognostisera behov för artikelvarianter med olika strukturer tilldelade](variants.md)  

Läs stegen för respektive scenario i den relevanta artikeln.  

> [!IMPORTANT]
> Dessa genomgångar kräver att användarupplevelsen är inställd på *Premium* på sidan **Företagsinformation**.

## Se även

[Produktion](../../production-manage-manufacturing.md)  
[Produktionsrapporter och analyser i Business Central](../../production-reports.md)  
