---
title: Tidsplanera projekt för justering och avstämning av lagerkostnad
description: lära dig hur du kan använda projektkön för att flytta aktiviteterna för att justera lagerkostnaden eller stämma av den med redovisningen till bakgrunden. Om ditt företag till exempel kör många aktiviteter eller behandlar många transaktioner.
author: brentholtorf
ms.topic: article
ms.devlang: al
ms.reviewer: bholtorf
ms.search.form: 461
ms.date: 09/19/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="schedule-jobs-to-adjust-and-reconcile-inventory-cost"></a>Tidsplanera projekt för justering och avstämning av lagerkostnad

Tidsplanera projekt för automatisk kostnadsjustering med redovisningen – bokföring till redovisningen är aktiverat som standard.
I takt med att data ansamlas över tid kan detta emellertid påverka prestandan. För att minska belastningen på programmet är det ofta praktiskt att använda projektkötransaktioner för att låta aktiviteter köras i bakgrunden.

## <a name="move-the-task-of-adjusting-item-costs-to-the-background-with-the-help-of-assisted-setup"></a>Flytta aktiviteten för justering av artikelkostnader till bakgrunden med hjälp av assisterad konfiguration

Det kan vara knepigt att skapa projektkötransaktioner, även för en erfaren konsult, varför vi har en assisterad konfiguration som gör det enklare att justera artikelkostnaden.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Lagerinställningar** och välj sedan relaterad länk.  
2. På sidan **Lagerkonfiguration** växlar du inställningen för fältet **Automatisk kostnadsbokföring** eller anger **Aldrig** i fältet **Automatisk kostnadsjustering**.  
3. I meddelandet som visas högst upp på sidan väljer du länken **Schemalägg projektkötransaktion**. Då öppnas guiden assisterad konfiguration för **Schemalägg kostnadsjustering och bokföring**.  
4. Öppna den uppgift som du vill schemalägga.  

  > [!NOTE]
  > Du kan inte skapa en ny Jobbkötransaktion om det redan finns en projektkötransaktion för den angivna aktiviteten.

5. Välj fältet **Visa projektkötransaktioner efter slutförande** för att granska och justera inställningarna. Mer information finns i [Använda projektköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-job-queue-entry-for-adjusting-and-reconciling-inventory-cost-manually"></a>Så här skapar du en projektkötransaktion för att justera och stämma av lagerkostnader manuellt

Du kan också skapa projektkötransaktioner manuellt. I följande procedur beskrivs hur du ställer in batchprojektet **Justera inmatningar för kostn. artikel** så att detta automatiskt körs dagligen, men samma steg även gäller batchprojektet **Bokför lagerkostnad i redovisning**.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **projektkötransaktioner** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Objekttyp som ska köras** väljer du *Rapport*.  
4. I fältet **Objekt-ID som ska köras** väljer du *795*, **Justera transaktioner för kostn. artikel**.  
5. I fältet **Formel för Nästa körningsdatum** anger du *1D*.
6. I fältet **Starttid** anger du *2 AM*.
7. Välj åtgärden **Ställ in status till klar**.

Lagerkostnaden kommer nu att uppdateras varje natt.  

Om du vill schemalägga en aktivitet för avstämning av lager med redovisningen väljer du codeunit 2846 **Bokför lagerkostnad i redovisning**.

> [!TIP]
> För att undvika låsning ska du inte schemalägga aktiviteter för batchprojektet **Justera kostn. – artikeltrans.**, codeunit **Bokför lagerkostnad i redovisning** och aktiviteter för bokföring av försäljnings- eller inköpstransaktioner på samma gång. Kontrollera också att de använder samma projektkökategori.

## <a name="see-also"></a>Se även

[Justera artikelkostnader](inventory-how-adjust-item-costs.md)  
[Stämma av lagerkostnader med redovisningen](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Använda projektköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md)  
[Söka efter sidor och information med berätta](ui-search.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
