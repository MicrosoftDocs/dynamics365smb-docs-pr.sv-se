---
title: Registrera hållbarhetstransaktioner
description: Lär dig hur du registrerar utsläpp av växthusgaser (GHG).
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Registrera hållbarhetstransaktioner

För närvarande är det enda sättet att registrera utsläpp av växthusgaser (GHG) i hållbarhetsredovisningen att använda hållbarhetsjournalerna.

## Hållbarhetsjournaler

Hållbarhetsjournaler är utformade för att spåra och registrera hållbarhetsrelaterade aktiviteter med samma användarupplevelse som andra journaler i Business Central. Användare som har nödvändig information kan manuellt ange utsläpp i en journal. Om de saknar denna information kan de alternativt använda inbyggda formler för att exakt beräkna utsläpp baserat på specifika kända parametrar som motsvarar olika typer av källor och konton.

Den information som du anger i en journal är tillfällig och kan ändras så länge den finns i journalen. När du bokför journalen, överförs informationen till transaktioner på hållbarhetstransaktioner eller enskilda hållbarhetskonton, där den inte kan ändras. Du kan emellertid bokföra återföring eller rättning av transaktioner.

### Använd journalmallar och journaler

Det finns som standard två mallar för hållbarhetsjournaler: standardmallen och återkommande mallen.

För varje journalmall kan du skapa din egen personliga journal som en journal. Om du vill göra det måste du välja åtgärden **Journaler** på sidan **Mallar för hållbarhetsjournaler** och skapa den nya **Hållbarhetsjournalen** på den nya sidan. Du kan till exempel definiera en egen journal för varje utsläpps-scope med alternativet **Utsläpps-scope** och sedan välja mellan tre befintliga scope. För varje journal kan du också lägga till eller ändra värdena **Ursprungskod** och **Uppföljningskod**.

> [!TIP]
> Om du har många rader kan du minska risken för misstag genom att ha en journal för varje utsläppstyp. Alternativt kan du använda den gemensamma journalen för alla utsläppstyper.

### Validera hållbarhetsjournaler

På sidan **Hållbarhetskonfiguration** kan du aktivera en bakgrundskontroll som förhindrar fördröjningar vid bokföring. Om några misstag inträffar när du arbetar i hållbarhetsjournalen meddelar valideringen dig och hindrar dig från att bokföra journalen.

När du aktiverar valideringen visas faktaboxen **Journalkontroll** på den aktuella raden och i hela partiet. Valideringen sker när du läser in en journal och väljer en annan journalrad. Panelen **Ärenden totalt** i faktaboxen visar det totala antalet problem som [!INCLUDE [prod_short](includes/prod_short.md)] hittat. Du kan välja panelen för att öppna en översikt över problemen.

### Arbeta med hållbarhetsjournaler

För att börja arbeta med hållbarhetsjournalerna följer du stegen:

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Hållbarhetsjournal** och väljer sedan relaterad länk.
2. På sidan **Hållbarhetsjournal** kan du ange så många rader som du planerar att bokföra med samma journal.
3. Du kan lämna fältet **Dokumenttyp** tomt eller välja **Faktura** eller **Kreditnota**.
4. I fältet **Kontonr.** kan du bara välja icke-spärrade hållbarhetskonton där fältet **Direktbokföring** är markerat och fältet **Bokföringstyp** anges till **Bokföring**. Kontona måste också ha konfigurerats med kategori och underkategori.

    > [!NOTE]
    > Om du använder journalen där utsläpps-scope har konfigurerats måste **Utsläpps-scope** i hållbarhetskontot vara lika med värdet för **Utsläpps-scope** i journalen.

5. Du kan antingen bokföra beloppen manuellt eller använda formler.

    - Om du har korrekt information om utsläppet och vill lägga upp den (det vill säga om du har informationen på den mottagna fakturan), välj fältet **Manuell inmatning** för att ange att beloppen ska matas in manuellt. I det här fallet kan du inte ange dina data i fälten **Bränsle/el**, **Avstånd**, **Anpassat belopp**, **Installationsmultiplikator** och **Tidsfaktor** , eftersom de inte kan redigeras. Men fälten **Utsläpp CO2**, **Utsläpp CH4** och **Utsläpp N2O** kommer att kunna redigeras och du kan fylla i dina uppgifter direkt i dem.
    - Om du inte har exakt kunskap om utsläppet och måste beräkna det, välj inte fältet **Manuell inmatning**. I det här fallet blir fälten **Utsläpp CO2**, **Utsläpp CH4** och **Utsläpp N2O** icke-redigerbara. Du kan emellertid ange dina beräkningsuppgifter baserat på den formel du använder. Lär dig mer om formlerna som finns och definieras i **kategori för hållbarhetskonto** i [Diagram över hållbarhetskonton och redovisning](finance-sustainability-accounts-ledger.md#account-categories).

6. Välj åtgärden **Bokför** om du vill bokföra journalen. När du bokför i en hållbarhetsjournal genereras transaktioner i hållbarhetsredovisningen.

Om formeln baseras på **Beräkna från redovisning** i kategori för hållbarhetskonto måste du använda åtgärden **Samla in belopp från redovisningstransaktioner** innan du bokför journalen för att beräkna utsläppen baserat på den här datakällan. Om du har gjort några ändringar i emissionsfaktorerna efter att du fyllt i journalraderna måste du dessutom välja åtgärden **Omberäkna** för att få rätt belopp i journalen.

### Återkommande journaler

En återkommande journal är en hållbarhetsjournal med specifika fält för hantering av transaktioner som du ofta bokför med få eller inga ändringar. Exempel inkluderar hållbarhetstransaktioner som el eller värme eller andra liknande transaktioner. Du kan använda återkommande journaler kan du bokföra fasta och variabla belopp.

När du använder en återkommande journal måste poster som du regelbundet lägger upp endast skapas en gång. Information som konton, dimensioner och dimensionsvärden finns kvar i journalen efter bokföring. Varje gång du postar kan du göra de ändringar som behövs.

Fältet **Återkommande metod** är viktigt. Det bestämmer hur du behandlar beloppet på journalraden efter bokföring. Om du t.ex. använder samma belopp varje gång du bokför raden kan du välja alternativet **F Fast** för att låta beloppet vara kvar efter bokföring. Om du använder samma konton och text på raden, men beloppet varierar varje gång du postar, kan du välja alternativet **V Variabel** för att ta bort beloppet efter bokföring.

Fältet **Återkommande frekvens** är också viktigt och måste ställas in. Det är ett formelfält för datum som bestämmer hur ofta transaktionen ska bokföras på journalraden. Läs mer i [Använd dataformulär](ui-enter-date-ranges.md#use-date-formulas).

Fältet **Utgångsdatum** bestämmer vilket datum raden ska bokföras för sista gången. Raden kommer inte att bokföras efter detta datum. Fördelen med att använda fältet **Utgångsdatum** är att raden inte kommer att raderas från journalen direkt. Du kan ange ett senare datum så att du kan använda raden i framtiden. Om fältet är tomt kommer raden att bokföras varje gång du bokför tills raden tas bort från journalen.

## Se även

[Ekonomi](finance.md)  
[Översikt över hållbarhetsstyrning](finance-manage-sustainability.md)  
[Hållbarhetskonfiguration](finance-sustainability-setup.md)  
[Diagram över hållbarhetskonton och redovisning](finance-sustainability-accounts-ledger.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
