---
title: Export av verifieringsfil
description: 'I den här artikeln beskrivs hur du lägger upp olika exportformat och sedan använder dem, baserat på revisor- eller myndighetskrav.'
author: altotovi
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.devlang: al
ms.search.keywords: 'audit, export, SIE, SAF-T, FAC, GDPdU, file export'
ms.search.form: '5260, 5261, 5264, 5266, 5267, 5270'
ms.date: 04/04/2023
ms.author: altotovi
ms.reviewer: kfend
---

# Export av verifieringsfil

Export av bokföringsinformation från systemet är en gemensam begäran från vissa lokala myndigheter eller revisorer. Export av format och information som krävs kan skilja sig från varandra. Transaktioner för export är vanligtvis redovisningstransaktioner (redovisning) momstransaktioner. Ytterligare information krävs dock ibland.

**Export av verifieringsfiler**är ett förinstallerat tillägg som gör att du kan exportera olika poster, baserat på revisor- eller myndighetskrav. Oavsett formattyp eller poster kan du styra dataexporten med hjälp av tilläggets funktioner. Funktionen har inte ett förinstallerat filformat för export. Därför måste du antingen installera en app som har ett visst format (t.ex. SIE, SAF-T eller FAC) eller utveckla din egen.

> [!NOTE]
> För närvarande kan du välja SIE (Sverige), FEC (Frankrike) och SAF-T-format som en extra app. Partner kan också utveckla ett anpassat format. Antalet tillgängliga format kommer att öka över tiden.

## Ställ in export av verifieringsfil

1. Välj sökknappen ![Förstoringsglas som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Exportkonfiguration för verifieringsfil** och välj sedan den relaterade länken.
2. På sidan **Exportkonfiguration för verifieringsfil**, följ dessa steg:

    1.  På snabbfliken **Allmänt** i fältet **Exportformatkod för verifieringsfil** anger du koden för standardformatet för export av verifieringsfilen. Endast de format som har aktiverats när ett visst fil format installerats från funktionshantering och de som har lagts till som ett anpassat format är tillgängliga.
    2. På snabbfliken **Datakvalitet**, markera kryssrutan **Kontrollera företagsinformation** för att få meddelande om företagsinformationsfält som inte har ställts in korrekt.
    3. Markera kryssrutan **Kontrollera kund** om du vill bli meddelad om fält som inte har konfigurerats korrekt för vissa kunder.
    4. Markera kryssrutan **Kontrollera leverantör** om du vill bli meddelad om fält som inte har konfigurerats korrekt för vissa leverantörer.
    5. Markera kryssrutan **Kontrollera bankkonton** om du vill bli meddelad om fält som inte har konfigurerats korrekt för vissa bankkonton.
    6. Markera kryssrutan **Kontrollera postnummer** om du vill bli meddelad om ett postnummer som inte har konfigurerats korrekt.
    7. Markera kryssrutan **Kontrollera adress** om du vill bli meddelad om en adress inte har konfigurerats korrekt.
    8. I fältet **Standard postnummer**, ange det postnummer som ska användas om inget postnummer anges på kund- eller leverantörskortet.

3. Välj sökknappen ![Förstoringsglas som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Konfiguration av exportformat för verifieringsfil** och välj sedan den relaterade länken.
4. På sidan **Konfiguration av exportformat för verifieringsfil**, följ dessa steg:

    1. Välj det exportformat för verifieringsfilen som du vill konfigurera. Endast de format som har aktiverats när ett visst fil format installerats från funktionshantering och de som har lagts till som ett anpassat format är tillgängliga.
    2. I fältet **Namn på verifieringsfil**, ange standardfilnamnet eller filnamnsmallen för granskningsfilen som du vill exportera.
    3. Markera kryssrutan **Arkivera i zip-format** om du vill att zip-filer ska exporteras automatiskt.

## Ange redovisningskontomappningen för exporten av verifieringsfilen

De flesta format som krävs av myndigheterna för redovisningskonton kräver en specifik standardkontoplan. När du har konfigurerat redovisningskontona kommer därför den exporterade filen att baseras på mappningarna. Du kan använda fler mappningar i systemet.

Följ dessa steg för att tillhandahålla redovisningskontomappningen för exporten av verifieringsfilen.

1. Välj sökknappen ![Förstoringsglas som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Mappning av redovisningskonto** och välj sedan den relaterade länken.
2. På sidan **Mappning av redovisning**, välj **Ny** för att skapa en mappning.
3. I fältet **Kod**, ange mappningskoden som representerar rapporteringsperioden.
4. I fältet **Standardkontotyp** väljer du typ av standardredovisningskonto.
5. I fältet **Exportformat för verifieringsfil**, ange exportformat för verifieringsfilen som standardredovisningskonto är länkade till.
6.  I fältet **periodtyp** anger systemet en bokföringsperiod eller en anpassad periodtyp som har ett flexibelt startdatum och en flexibel tid, baserat på ditt val. Om du väljer en viss bokföringsperiod kommer fältet att vara inställt på **bokföringsperiod**. Annars kommer den att ställas in på **Dataområde**.
7.  I fältet **bokföringsperiod** anger du startdatum för bokföringsperioden som ska användas som rapporterings period, om du vill att de ska vara identiska.
8. Om du ställer in fältet **Bokföringsperiod** är fälten **Startdatum** och **Slutdatum** automatiskt, baserat på den angivna perioden. Annars kan du ange start- och slutdatum för din rapportering manuellt.
9. Om du redan har lagt till en standardkontoplan gör du så här:

    1. I **Kategorinummer för standardkonto.** anger kategorin för standardkontot eller grupperingskoden som används för mappning.
    2. I fältet **Standardkontonummer.**, ange standardkontokoden eller grupperingskoden som används för mappning.

10. Markera kryssrutan **Ta med ingående saldo** för att överväga det inkommande saldot på huvudbokkontot för typen **Motkonto** mappningen i stället för rapporteringsperiodens nettoförändring.
11. För att börja mappningen gör du följande:

    1. För att generera rader på sidan **Mappning av redovisningskonto**, baserat på en befintlig kontoplan, välj **Initiera källa för mappning**. Om du vill kopiera kontomappningen från en annan mappningskod väljer du **Kopiera från en annan mappning**. När du är klar med att skapa rader markeras alla redovisningskonton med bokförda transaktioner i grönt.
    2. Om du bara vill markera huvudkonton som har poster väljer du **Uppdatera disposition för redovisningstransaktioner**. Om alternativet **Ta med ingående saldo** är aktiverat, beaktas alla bokförda bokföringsposter för beräkning. I annat fall beaktas endast redovisningstransaktioner för rapporteringsperioden.

## Export av verifieringsfilen

1. Välj sökknappen ![Förstoringsglas som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Exportdokument för verifieringsfil** och välj sedan den relaterade länken.
2. På sidan **Exportdokument för verifieringsfil**, välj **Ny**.
3. På snabbfliken **Allmänt**, följ stegen:

    1. I fältet **Exportformat för verifieringsfil** väljer du det format som används för att exportera granskningsfilen.
    2. På fältet **Mappningskod för redovisningskonto**, välj redovisningskontokoden för rapportperioden.
    3. Markera kryssrutan **Dela per månad** om flera verifieringsfiler ska skapas per månad.
    4. Markera kryssrutan **Dela per datum** om flera verifieringsfiler ska skapas per dag.
    5.  I fältet **Rubrikkommentar** anger du den kommentar som ska ingå i rubriken verifieringsfil.
    6. På fältet **Kontakt**, anger kontakten som exporteras till verifieringsfilens rubrik.
    7. Markera kryssrutan **Skapa flera zip-filer** om du vill generera flera zip-filer.

        > [!IMPORTANT]
        > Markera den här kryssrutan bara om du tidigare har installerat några av formatapparna eller skapat en anpassad. Installation av ett eller flera av de specifika formaten kommer sannolikt att lägga till fält och funktioner till **Export av verifieringsfiler**, baserat på formatkraven.

4. På snabbfliken **Bearbeta**, följ stegen:

    1. Markera kryssrutan för **parallell bearbetning** om du vill att generering av granskningsfiler ska bearbetas av parallella bakgrundsjobb. Avmarkera kryssrutan om du vill exportera data i den aktuella sessionen.
    2. Om du markerade kryssrutan **Parallell bearbetning** i fältet **Max. antal jobb** anger du det maximala antalet bakgrundsjobb som kan köras samtidigt.
    3. I fältet **Tidigaste startdatum/starttid** anger du tidigaste datum och tid då bakgrundsjobbet måste köras. Om du kör processen genom att välja **Start** kan du spåra statusen på snabbflikarna **bearbetning** och **rader**.

5. När du är klar kan du välja **Hämta som fil** för att hämta granskningsfilen för den markerade raden.

> [!IMPORTANT]
> Om du har flera transaktioner att exportera rekommenderar vi inte att du exporterar dem i den aktuella sessionen på grund av eventuella prestandaproblem. I stället rekommenderar vi att du använder parallell bearbetning under lediga dagar eller timmar.

## Se även
[Ekonomihantering](finance.md)  
[Förstå redovisningen och kontoplanen](finance-general-ledger.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Arbeta med Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
