---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
---
När du har lagt till alla artiklar på rader kan du beräkna fakturarabatten för hela försäljningsdokumentet genom att välja åtgärden **Beräkna fakturarabatt**.

Rabatten beräknas baserat på alla rader i försäljnings dokumentet där kryssrutan **beräkna fakturarabatt** har valts. Som standard är fakturarabatter tillåtna. Men rader med artikelomkostnader ingår till exempel inte i beräkningen av fakturarabatten. Om du vill tillämpa en rabatt på sådana rader anger du ett värde i fältet **Radrabattbelopp** på raderna.  

> [!NOTE]
> Som standard är fälten **Pris inklusive moms** och **Radrabattbelopp** är gömda på rader. Om fälten inte är tillgängliga kan du lägga till dem genom att anpassa sidan. Mer information finns i [Anpassa din arbetsyta](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

> [!TIP]
> Om fältet **Beräkna fakturarabatt** är markerat på sidan **Försäljningsinställningar** beräknas fakturarabatten automatiskt. När beräkningen sker varierar beroende på vilken typ av försäljningsdokument du använder.
>
> Om du använder en försäljningsorder beräknas rabatten när du lägger till en rad. För alla andra försäljningsdokument, till exempel försäljningsfakturor, beräknas rabatten när du gör något av följande:
>
> * Visa statistik
> * Visa en testrapport
> * Skriv ut
> * Post

Du definierar fakturarabatt för en kund definieras på sidan **Kundfakturarabatter**. Valutakoden i försäljningsdokumentet används för att hitta villkoren för fakturarabatt i motsvarande valuta.

Om du inte har definierat fakturarabatter för utländska valutor används rabattvillkoren på sidan **Kundfakturarabatter** för att beräkna rabatten. I beräkningen används den lokala valutan och den valutakurs som gäller på dokumentets bokföringsdatum.
