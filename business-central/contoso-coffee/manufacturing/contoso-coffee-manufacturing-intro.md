---
title: Introduktion till produktion för Contoso Coffee
description: Översikt över scenarier som kan vara till hjälp när demonstrationsdatan för Contoso Coffee ska hjälpa dig lära dig hur du använder produktionsfunktionerna i Business Central.
ms.date: 04/01/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '4765,'
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a>Introduktion till produktion för Contoso Coffee

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

Tillverkningsaktiviteterna för alla scenarier använder platsen *HUVUD*.  

> [!IMPORTANT]
> Innan du kör något av scenarierna för Contoso Coffee bokför du eventuella artikeljournalrader med ingående balanser. Mer information finns i avsnittet [Konfigurera data för Contoso Coffee](#set-up-contoso-coffee-manufacturing-data).

## <a name="set-up-contoso-coffee-manufacturing-data"></a>Ställ in data för produktion för Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

|Fält  |Beskrivning  |
|---------|---------|
|**Produktionsplats** |Anger det distributionslager som du vill använda för produktionsåtgärder. Standardvärdet är *HUVUD*, men du kan ändra detta så att det passar dina behov.|


Välj åtgärden **Skapa demonstrationsdata** när du är klar. Det tar några minuter att lägga till data i den underliggande databasen, men sedan är det dags att köra de olika scenarierna.  

## <a name="scenarios"></a>Scenarierna

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

## <a name="see-also"></a>Se även

[Produktion](../../production-manage-manufacturing.md)  
[Produktionsrapporter och analyser i Business Central](../../production-reports.md)  
