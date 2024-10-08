---
title: Hantera synkronisering av huvuddata
description: Lär dig hantera synkronisering av huvuddata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 04/05/2024
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# <a name="manage-master-data-synchronization"></a>Hantera synkronisering av huvuddata

När du har ställt in synkronisering av huvuddata och synkroniserats för första gången är posterna i de valda tabellerna kopplade och en återkommande Jobbkötransaktion skapas för varje register. Jobbkötransaktioner synkroniserar automatiskt data i dotterbolagen när någon gör en ändring i källföretaget. Annars behöver du inte göra någonting.

> [!NOTE]
> Som standard planeras jobbkötransaktioner med en gång per minut och du kan inte ändra schemat.

Ibland kan det emellertid hända att saker går fel och det kan finnas situationer som du behöver hantera eller undersöka. Om till exempel flera personer ändrar samma post i både källföretaget och ett dotterbolag, kommer synkroniseringen att misslyckas så att du kan ange rätt ändring. Eller så kan källföretaget installera ett tillägg som ändrar schemat för en av tabellerna som synkroniseras genom att lägga till ett fält eller två. Om du vill synkronisera de nya fälten i dotterbolagen måste du installera samma tillägg och uppdatera schemat i inställningarna.

I den här artikeln beskrivs verktygen som du kan använda för att fortsätta köra synkroniseringen på ett smidigt sätt.

## <a name="overwrite-local-changes"></a>Skriv över lokala ändringar

Du kan använda kryssrutan **Skriv över lokal ändring** i de fält och tabeller som du synkroniserar om du vill tillåta att data från källföretaget skriver över data i dotterbolaget.

> [!NOTE]
> Du kan inte aktivera synkronisering av ett fält och tillåta dotterbolaget att skriva värden i fältet oberoende av källföretaget. Du måste antingen inaktivera synkroniseringen för fältet eller låta källföretaget skriva över lokala ändringar.

## <a name="update-table-schemas"></a>Uppdatera tabellscheman

Om källföretaget ändrar en tabell, till exempel genom att lägga till ett fält som du vill synkronisera måste dotterbolagens fältmappningar uppdateras. På sidan **synkronisera fält** använd åtgärden **uppdatera fält**.

## <a name="enable-or-disable-couplings-between-records"></a>Aktivera eller inaktivera kopplingar mellan poster

För att starta eller stoppa koppling på specifika poster på en tabell, på sidan **synkronisera fält**, välj fälten och använd sedan antingen åtgärderna **aktivera** eller **inaktivera**.

> [!TIP]
> Ett snabbt sätt att aktivera eller inaktivera flera fält samtidigt, är att markera dem i listan och sedan använda åtgärderna **aktivera** eller **inaktivera**.

## <a name="run-a-full-synchronization"></a>Kör en fullständig synkronisering

Åtgärden **Kör fullständig synkronisering** schemalägger en synkronisering för alla tabellposter i källföretaget och synkroniserar om alla poster villkorslöst. Omsynkronisering är till exempel användbart om du aktiverar ett extra fält i en synkroniseringstabell eller lägger till ett extra fält med hjälp av åtgärden **Uppdatera fält**. Åtgärden synkroniserar data i dessa fält retroaktivt.

## <a name="synchronize-modified-records"></a>Synkronisera ändrade poster

Om du ändrar en inställning för en tabell eller ett dotterbolag måste du uppdatera synkroniseringen. För att uppdatera synkroniseringen, använd åtgärden **synkronisera ändrade poster** på sidan **synkronisera tabeller**.

Åtgärden **Synkronisera ändrade poster** schemalägger en synkronisering av följande tabellposter:

* Poster som inte kunde synkroniseras vid det senaste försöket.
* Poster som har ändrats i källföretaget efter den senaste schemalagda synkroniseringen. Du kan granska den senaste schemalagda synkroniseringstiden på sidan **Synkroniseringstabeller** i fältet **Synkronisera ändringar sedan**.

Åtgärden fungerar på samma sätt som en schemalagd synkronisering och du kan använda den som ett sätt att synkronisera utanför schemat. Om du till exempel markerar kryssrutan **Skriv över lokal ändring** i ett fält så att data från källföretaget kan skriva över lokala ändringar uppdaterar åtgärden denna data. Du kan också bara vänta tills nästa schemalagda synkronisering inträffar.

## <a name="investigate-the-status-of-synchronization"></a>Undersök status för synkronisering

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

## <a name="clean-up-old-entries"></a>Rensa gamla poster

Med tiden kommer antalet poster i synkroniseringsloggen att bli stort, så du kanske vill rensa lite för att ta bort onödiga poster. Om du vill göra det enklare att rensa gamla poster kan du utföra följande åtgärder på sidan **Integreringssynkroniseringsjobb**:

* **Ta bort transaktioner som är äldre än sju dagar**
* **Ta bort alla transaktioner**

## <a name="adding-extensions"></a>Lägga till tillägg

Om källföretaget installerar ett nytt tillägg, måste dotterbolaget också installera det om det vill synkronisera data för det. Dotterbolaget kan använda åtgärden **Uppdatera fält** på sidan **synkronisera fält** för att lägga till tabellerna från tillägget i listan.

> [!NOTE]
> En del tabeller hämtar data från relaterade tabeller. Om du lägger till ett tillägg som inte innehåller relaterade tabeller kommer fälten i dessa tabeller inte att vara tillgängliga. Kontrollera att du har lagt till alla relaterade tabeller.

<!--
## <a name="recreate-a-deleted-job-queue-entry"></a>Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## <a name="see-also"></a>Se även

[Kom i gång med synkronisering av huvuddata](admin-set-up-data-sync.md)
