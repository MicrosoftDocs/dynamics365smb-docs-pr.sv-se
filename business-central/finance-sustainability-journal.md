---
title: Så här registrerar du hållbarhetstransaktioner
description: Lär dig hur du registrerar utsläpp av växthusgaser.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="record-sustainability-entries"></a>Så här registrerar du hållbarhetstransaktioner

För närvarande är det enda sättet att registrera utsläpp av växthusgaser till **hållbarhetsredovisningen** att använda **hållbarhetsjournalerna**.   

## <a name="sustainability-journals"></a>Hållbarhetsjournal

**Hållbarhetsjournaler** är utformade för att spåra och registrera hållbarhetsrelaterade aktiviteter med samma användarupplevelse som andra journaler i Business Central. Inom journalen har användarna möjlighet att mata in utsläpp manuellt om de har nödvändig information. Om de saknar dessa data, kan de alternativt använda inbyggda formler för att exakt beräkna utsläpp baserat på specifika kända parametrar som motsvarar olika typer av källor och konton. 

Den information som du anger i en journal är tillfällig och kan ändras så länge den finns i journalen. När du bokför journalen, överförs informationen till transaktioner på **Hållbarhetstransaktioner** eller enskilda **Hållbarhetskonton**, där den inte kan ändras. Du kan emellertid bokföra återföring eller rättning av transaktioner.  

### <a name="use-journal-templates-and-batches"></a>Använd journalmallar och journaler

Det finns som standard två **Mallar för hållbarhetsjournaler**, den vanliga och den återkommande. För varje journalmall kan du skapa din egen personliga journal som en journal. Om du vill göra det måste du välja åtgärden **Journaler** på sidan **Mallar för hållbarhetsjournaler** och skapa den nya **Hållbarhetsjournalen** på den nya sidan. Du kan till exempel definiera en egen journal för varje utsläpps-scope med alternativet **Utsläpps-scope** där du kan välja mellan tre befintliga scope. Du kan också lägga till eller ändra **Ursprungskod** och **Uppföljningskod** för var och en av journalerna. 

>[!TIP]
>Du kan ha en journal för varje utsläppstyp om du har många rader eftersom det kan minska risken för misstag, men du kan även använda den gemensamma journalen för alla typer av utsläpp.   

### <a name="validate-sustainability-journals"></a>Validera hållbarhetsjournaler

Du kan aktivera en bakgrundskontroll på sidan **Hållbarhetskonfiguration** som förhindrar fördröjningar vid bokföring. Kontrollen meddelar vid eventuellt misstag när du arbetar med **Hållbarhetsjournalen** och detta hindrar dig från att bokföra journalen.  

När du aktiverar valideringen visas faktaboxen **Journalkontroll** på den aktuella raden och i hela partiet. Valideringen sker när du läser in en journal och väljer en annan journalrad. Panelen **Ärenden totalt** i faktaboxen visar det totala antalet ärenden som [!INCLUDE [prod_short](includes/prod_short.md)] hittade, och du kan välja att den öppnar en översikt över ärendena. 

### <a name="work-with-sustainability-journals"></a>Arbeta med hållbarhetsjournaler

För att börja arbeta med **hållbarhetsjournalerna** följer du stegen:   

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Hållbarhetsjournal** och väljer sedan relaterad länk. 
2. På sidan **Hållbarhetsjournal** kan du ange så många rader som du planerar att bokföra med samma journal.  
3. Som **Dokumenttyp** kan du behålla tomt alternativet eller välja att använda **Faktura** eller **Kreditnota**.  
4. I fältet **Kontonr.** kan du bara välja **Hållbarhetskonton** med valt fält för **Direktbokföring**, **Bokföring** som **Bokföringstyp** och icke-spärrat konto. Konton måste också ha konfigurerats med kategori och underkategori.  

>[!NOTE]
>Om du använder journalen där utsläpps-scope har konfigurerats måste **Utsläpps-scope** i **Hållbarhetskonto** vara lika med **Utsläpps-scope** i den använda journalen.  

5. Du har två alternativ: antingen bokföra beloppen manuellt eller använda formler.   

    1. Om du har korrekt information om utsläppet, vill bokföra det (dvs. du har det på den mottagna fakturan), måste du välja fältet **Manuell inmatning** för att ange att beloppen ska matas in manuellt. I det här fallet kan du inte fylla i dina data i fälten **Bränsle/el**, **Avstånd**, **Anpassat belopp**, **Installationsmultiplikator** och **Tidsfaktor** , eftersom de inte kan redigeras för det här valet. Men fälten **Utsläpp CO2**, **Utsläpp CH4** och **Utsläpp N2O** kommer att kunna redigeras och du kan fylla i dina uppgifter direkt där. 
    2. Om du inte känner till ditt utsläpp korrekt måste du beräkna det och du kan inte välja fältet **Manuell inmatning** och fälten **Utsläpp CO2**, **Utsläpp CH4** och **Utsläpp N2O** kan inte redigeras, men du kan ange dina beräkningsuppgifter baserat på formeln du använder. Du kan läsa mer om de formler som används och definieras i **Kategori för hållbarhetskonto** här i [Diagram över hållbarhetskonton och redovisning](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Om du vill bokföra journalen väljer du åtgärden **Bokför**. När du bokför i en **Hållbarhetsjournal** genereras transaktioner i **hållbarhetsredovisningen**. 

Om formeln baseras på **Beräkna från redovisning** i **Kategori för hållbarhetskonto** måste du använda åtgärden **Samla in belopp från redovisningstransaktioner** innan du bokför journalen för att beräkna utsläppen baserat på den här datakällan. Om du har gjort några ändringar i emissionsfaktorerna efter att du fyllt i journalraderna måste du dessutom välja åtgärden **Omberäkna** för att få rätt belopp i journalen.  

### <a name="recurring-journals"></a>Återkommande journaler

En återkommande journal är en **Hållbarhetsjournal** med specifika fält för hantering av transaktioner som du ofta bokför med få eller inga ändringar. Till exempel hållbarhetstransaktioner som el, värme eller andra liknande transaktioner. Med hjälp av återkommande journaler kan du bokföra fasta och variabla belopp. Med en återkommande journal skapar du transaktioner som ska bokföras regelbundet endast en gång. Till exempel konton, dimensioner och dimensionsvärden, etc. finns kvar i journalen efter bokföring. Om ändringar behövs kan du göra det varje gång du bokför. 

Fältet **Återkommande metod** är viktigt. Det bestämmer hur du behandlar beloppet på journalraden efter bokföring. Om du t.ex. använder samma belopp varje gång du bokför raden kan du låta beloppet stå kvar och i så fall bör du använda alternativet **F Fast**. Om du vill använda samma konton och samma text på raden och bara ändra beloppet varje gång du bokför, kan du låta beloppet raderas varje gång du har bokfört och i detta fall väljer du alternativet **V Variabel**. 

Du måste även konfigurera fältet **Återkommande frekvens** eftersom fältet datumformel bestämmer hur ofta transaktionen ska bokföras på journalraden och måste fyllas i. Läs mer i [Använd dataformulär](ui-enter-date-ranges.md#use-date-formulas).  

Fältet **Utgångsdatum** bestämmer vilket datum raden ska bokföras för sista gången. Raden kommer inte att bokföras efter detta datum. Fördelen med att använda fältet **Utgångsdatum** är att raden inte kommer att raderas från journalen direkt. Du kan ange ett senare datum så att du kan använda raden i framtiden. Om fältet är tomt kommer raden att bokföras varje gång du bokför tills raden tas bort från journalen.  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)    
[Översikt över hållbarhetshantering](finance-manage-sustainability.md)   
[Hållbarhetskonfiguration](finance-sustainability-setup.md)   
[Diagram över hållbarhetskonton och redovisning](finance-sustainability-accounts-ledger.md)   
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
