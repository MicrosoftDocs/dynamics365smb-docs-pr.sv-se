---
title: Hantera synkronisering av huvuddata
description: Lär dig hantera synkronisering av huvuddata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization" />Hantera synkronisering av huvuddata

När du har ställt in synkronisering av huvuddata och synkroniserats för första gången är posterna i de valda tabellerna kopplade och en återkommande Jobbkötransaktion skapas för varje register. Jobbkötransaktioner synkroniserar automatiskt data i dotterbolagen när någon gör en ändring i källföretaget. Annars behöver du inte göra någonting.

> [!NOTE]
> Som standard planeras jobbkötransaktioner med en gång per minut och du kan inte ändra schemat.

Ibland kan det emellertid hända att saker går fel och det kan finnas situationer som du behöver hantera eller undersöka. Om till exempel flera personer ändrar samma post i både källföretaget och ett dotterbolag, kommer synkroniseringen att misslyckas så att du kan ange rätt ändring. Eller så kan källföretaget installera ett tillägg som ändrar schemat för en av tabellerna som synkroniseras genom att lägga till ett fält eller två. Om du vill synkronisera de nya fälten i dotterbolagen måste du installera samma tillägg och uppdatera schemat i inställningarna.

I den här artikeln beskrivs verktygen som du kan använda för att fortsätta köra synkroniseringen på ett smidigt sätt.

## <a name="investigate-the-status-of-synchronization" />Undersök status för synkronisering

Det finns två åtgärder på sidan **synkronisera tabeller** som kan hjälpa dig att övervaka synkroniseringen:

* **Integreringssynkroniseringsjobb**
* **Jobbkötransaktioner**

Följande tabell beskriver åtgärderna.

|Sida  |Beskrivning  |
|---------|---------|
|**Integreringssynkroniseringsjobb**     | Öppna sidan **Integreringssynkroniseringsjobb** för att undersöka vad som hände varje gång en jobbkötransaktion kördes. Om du vill ha mer information om nya poster som har lagts till eller utforska varför det inte gick att synkronisera en post, väljer du numren i kolumnerna **infogad** eller **misslyckad**. Du kan också använda den här sidan för att rensa bort äldre poster som du kanske inte behöver. För att lära dig mer om att rensa, gå till [rensa gamla transaktioner](#clean-up-old-entries).        |
|**Jobbkötransaktioner**     | Åtkomst information om jobbkötransaktionen som synkroniserar data för en vald tabell. Du kan t. ex. använda den här sidan för att hantera statusen på jobbkötransaktionen för att lära dig mer om jobbkötransaktioner, gå till [Använda jobbköer för att schemalägga aktiviteter](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Om du hittar ett fel på sidan **Integreringssynkroniseringsjobb** som du inte kan matcha själv, om du kontaktar partnern eller Microsoft för support, kan det vara bra att ange felmeddelandet och anropsstack information.

## <a name="synchronize-modified-records" />Synkronisera ändrade poster

Om du ändrar en inställning för en tabell eller ett dotterbolag måste du uppdatera synkroniseringen. Om du till exempel väljer alternativet **Skriv över lokal ändring** i ett fält så att data från källföretaget kan skriva över lokala ändringar. För att uppdatera synkroniseringen, använd åtgärden **synkronisera ändrade poster** på sidan **synkronisera tabeller**.

## <a name="update-table-schemas" />Uppdatera tabellscheman

Om källföretaget ändrar en tabell, till exempel genom att lägga till ett fält som du vill synkronisera måste dotterbolagens fältmappningar uppdateras. På sidan **synkronisera fält** använd åtgärden **uppdatera fält**. 

## <a name="enable-or-disable-couplings-between-records" />Aktivera eller inaktivera kopplingar mellan poster

För att starta eller stoppa koppling på specifika poster på en tabell, på sidan **synkronisera fält**, välj fälten och använd sedan antingen åtgärderna **aktivera** eller **inaktivera**. 

> [!TIP]
> Ett snabbt sätt att aktivera eller inaktivera flera fält samtidigt, är att markera dem i listan och sedan använda åtgärderna **aktivera** eller **inaktivera**.

## <a name="adding-extensions" />Lägga till tillägg

Om källföretaget installerar ett nytt tillägg, måste dotterbolaget också installera det om det vill synkronisera data för det. Dotterbolaget kan använda åtgärden **Uppdatera fält** på sidan **synkronisera fält** för att lägga till tabellerna från tillägget i listan.

> [!NOTE]
> En del tabeller hämtar data från relaterade tabeller. Om du lägger till ett tillägg som inte innehåller relaterade tabeller kommer fälten i dessa tabeller inte att vara tillgängliga. Kontrollera att du har lagt till alla relaterade tabeller.

## <a name="clean-up-old-entries" />Rensa gamla poster

Med tiden kommer antalet poster i synkroniseringsloggen att bli stort, så du kanske vill rensa lite för att ta bort onödiga poster. Om du vill göra det enklare att rensa gamla poster kan du utföra följande åtgärder på sidan **Integreringssynkroniseringsjobb**:

* **Ta bort transaktioner som är äldre än 7 dagar**
* **Ta bort alla transaktioner**

<!--
## <a name="recreate-a-deleted-job-queue-entry" />Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also" />Se även

[Kom i gång med synkronisering av huvuddata](admin-set-up-data-sync.md)
