---
title: Introduktion till Contoso Coffee
description: Översikt över scenarier som kan vara till hjälp när demonstrationsdatan för Contoso Coffee ska hjälpa dig lära dig hur du använder lagerstyrningsfunktionerna i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Introduktion till lagerstyrning för Contoso Coffee

Contoso Coffee är ett fiktivt företag som tillverkar kaffemaskiner för privat och kommersiellt bruk. **Contoso Coffee**-apparna för Business Central lägger till demonstrationsdata som du kan använda för att lära dig använda lagerstyrningsfunktionerna i Business Central. Du kan konfigurera lagerstyrningsfunktioner på olika sätt, se [Översikt över olika konfigurationsalternativ](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Appen tillhandahåller tre lagerställen som är optimerade för olika scenarier:

- **SILVER**  

  Detta lagerställe har konfigurerats till att använda lagerplatser. Det kan enkelt konfigureras för att stödja Grundläggande eller Avancerad. 

- **GUL**  

  Detta lagerställe använder den avancerade lagerkonfigurationen, men använder inte lagerplatser. Den kan konfigureras för att stödja grundläggande konfigurationer.

- **VIT**  

  Detta lagerställe använder den avancerade lagerkonfigurationen med dirigerad artikelinförsel och plockning, som möjliggör mer avancerade regler för hur artiklar flyttas i hela distributionslagret.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Konfigurera lagerstyrningsdata för Contoso Coffee

Om du vill använda demonstrationsdata för lagerstyrning för Contoso Coffee måste du installera två appar i det aktuella företaget i [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Demonstrationsdatauppsättning för Contoso Coffee**  

    Den här appen levererar demonstrationsdata för basprogrammet.  
- **Demonstrationsdatauppsättning för Contoso Coffee (lands-ID)**  

    Den här appen lägger till landsspecifika innehåll ovanpå basprogrammet.

Lägg till programmen i ett tomt företag i en betald prenumeration eller som en del av en utvärderingsversion. Du kan till exempel skapa ett nytt företag utan exempeldata från den assisterade konfigurationsguiden **Skapa nytt företag** som du kan öppna från listan **Företag**. Lägg sedan till programmen från [marknadsplatsen](../../ui-extensions-install-uninstall.md#install) om de inte redan anges på sidan **Tilläggshantering**.  

När de relevanta apparna har installerats går du till sidan [Demonstrationsdata för lagerstyrning för Contoso Coffee](https://businesscentral.dynamics.com/?page=4761) i [!INCLUDE [prod_short](../../includes/prod_short.md)] och ändrar standardinställningarna så att de passar dina behov. Inställningarna beskrivs i följande tabell:  

|Fält  |Beskrivning  |
|---------|---------|
|**Startår** |Anger det första år som du vill använda för demonstrationsdata för Contoso Coffee. Beroende på företagets konfiguration är året antingen ett kalender år eller ett räkenskapsår.|
|**Lagerplats**  |Lagerstället för grundläggande scenarier.|
|**Lagerställe av. logistik**  |Lagerstället för enkla logistikscenarier.|
|**Lagerställe för dirigerad plockning och artikelinförsel**  |Lagerstället för avancerad logistikscenarier.|
|**Lagerställe, på väg**  |Det lagerställe som ska användas för transitlagerstället i överföringsscenarier.|
|**Kundnr**  |Kunden som ska användas för grundläggande och enkla scenarier vid försäljningsåtgärder.|
|**Leverantörsnr**  |Den leverantör som ska användas för alla scenarier i inköpsåtgärder.|
|**Huvudartikelnr.**  |Den artikel som ska användas för alla försäljningsåtgärder.|
|**Artikel 1 nr.**  |Huvudartikel att använda för alla scenarier.|
|**Artikel 2 nr.**  |Extra artikel att använda för alla scenarier.|
|**Kundbokföringsmall**|Anger en företagskod för inrikes kunder. Affärskoderna används när transaktionerna bokförs. |
|**Kund – generell rörelsebokföringsmall**|Anger en företagskod för inrikes kunder. Affärskoderna används när transaktionerna bokförs. |
|**Leverantörsbokföringsmall**|Anger en företagskod för inrikes kunder och leverantörer. Affärskoderna används när transaktionerna bokförs. |
|**Leverantör – generell rörelsebokföringsmall**|Anger en företagskod för inrikes kunder och leverantörer. Affärskoderna används när transaktionerna bokförs. |
|**Inrikes – Rörelsebokföringsmall för moms**|Anger en momsrörelsekod för kunder och leverantörer för bokföring av moms om moms är aktiverad.|
|**Återförsäljning – Lagerbokföringsmall**    |Anger en kod för artiklar som måste användas för bokföring av återförsäljning.|
|**Detaljhandel – generell produktbokföringsmall**    |Anger en kod för artiklar som måste användas för bokföring av återförsäljning.|
|**Moms produktbokföringsmall**    |Anger en momsproduktkod för artiklar för bokföring av moms om moms är aktiverad.|
|**Prisfaktor**     |Anger en faktor för att omvandla ett pris från USD/EUR till lokal valuta. *1* innebär att priset är samma belopp i alla valutor. Ett högre värde används för att hämta priset i lokal valuta. |
|**Avrundningsprecision**  |Definierar hur de beräknade förbrukningskvantiteterna avrundas när de registreras på förbrukningsjournalrader. Kvantiteter mindre än 0,5 avrundas nedåt. Kvantiteter lika med eller högre än 0,5 avrundas uppåt.|

Välj åtgärden **Skapa demonstrationsdata** när du är klar. Det tar några minuter att lägga till data i den underliggande databasen, men sedan är det dags att köra de olika scenarierna.  

> [!IMPORTANT]
> Om du kör scenarierna kanske du vill kontrollera att användaren har lagts till som för valda lagerställen. Mer information finns i [Så här skapar du dist.lager personal](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Scenarierna

Demonstrationsdata för Contoso Coffee stöder för närvarande följande lagerstyrningsscenarier för test och utbildning:

1.  [Genomgång av ankommande och avgående flöde i grundläggande distributionslagerkonfigurationer](warehouse-basic-flow-putaway-pick.md)
2.  [Genomgång av ankommande och avgående flöde i blandade distributionslagerkonfigurationer](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Genomgång av ankommande och avgående flöde i avancerad distributionslagerkonfiguration med dirigerad artikelinförsel och plockning](warehouse-directed-flow.md)

Läs stegen för respektive scenario i den relevanta artikeln.  

## <a name="see-also"></a>Se även

[Ställa in lager](../../inventory-setup-inventory.md) 
[Hur du ställer in lager](../../inventory-how-setup-locations.md) 
[Lagerstyrning](../../warehouse-manage-warehouse.md) 
[Designdetaljer](../../design-details-warehouse-overview.md) 
