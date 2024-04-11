---
title: Omvärdera saldon på redovisningskonto
description: Lära dig hur du omvärderar redovisningskontosaldon innan du upprättar dina finansiella rapporter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 03/14/2024
ms.custom: bap-template
ms.search.form: null
ms.service: dynamics-365-business-central
---

# Omvärdera saldon på redovisningskonto

Om du använder redovisningskonton för att registrera balansposter i utländsk valuta, bör du omvärdera kontosaldona innan du upprättar finansiella rapporter. Valutakurser ändras ofta och omvärdering hjälper till att göra dina finansiella rapporter mer exakta.

## Ställ in omvärderingar

Du skapar varje konto som du vill inkludera i omvärderingar på sidan **Redovisningskontokort**. Du kan välja om omvärderingsjusteringar ska bokföras på konton för realiserade eller orealiserade vinster/förluster. Bokföring av vinster och förluster under en valutakursjustering följer den normala bokföringsrutinen. Du kan till exempel göra det för varje inställning på sidan **Valutor**. Mer information om valutakursjusteringar finns i [Uppdatera valutakurser](finance-how-update-currencies.md).

För att minimera felen kan du i fältet **Bokföring i källvaluta** ställa in en validering för de valutor som du vill tillåta att bokföra på enskilda redovisningskonton:

* Alla valutor (tomt)
* Flera valutor
* Samma valuta
* Lokal valuta

## Kör en omvärdering

För att omvärdera beloppen i utländsk valuta i lokal valuta för huvudbokens saldon, på sidan **Kontoplaner** använd åtgärden **Omräkning i redovisningsvaluta** för att starta ett batch-jobb. Batch-jobbet skapar justeringstransaktioner i den journal som du väljer. När du bokför transaktionerna justerar du saldot i lokal valuta (BVA) för kontot. Redovisningskontosaldon som alltid visas i BVA återspeglar nu ändringar i de valutor som transaktionerna bokfördes i. Denna omvärdering gör att du kan producera en mer exakt finansiell rapport med mindre ansträngning.

Om du använder en alternativ rapporteringsvaluta (ACY) har redovisningsomvärderingstransaktionerna ett ACY-belopp. Det belopp som endast motsvarar BVA-beloppet på dessa transaktioner, inte ACY-saldot på redovisningskontot. Om du justerar ACY-kurserna efter att du har bokfört justeringarna kör du valutakursjusteringen en gång till för att justera alla redovisningstransaktioner.

> [!IMPORTANT]
> Omvärdering av redovisningskonton kanske inte uppfyller alla krav för transaktions- och tillgångsregistreringar som behöver omvärderas. Till exempel för finansiella instrument, värdepapper, leasade tillgångar eller om du använder dem för specifika eller stora volymer av transaktioner eller tillgångar. Vi rekommenderar att du diskuterar med din revisor om du kan använda funktionen och i så fall hur du ska använda den. Till exempel om du tillåter att valutor blandas för ett konto, eller om du behöver ha ett separat konto för varje tillgång du vill spåra.

> [!NOTE]
> Omvärdering ger inte möjlighet att koppla eller ta bort kopplingar, som du kan med kund- och leverantörsreskontraposterna. Justeringar sker på saldo per valutabasis.

## Omvärdera konton kontra kund- och leverantörsvalutakursjusteringar

Omvärdering förenklar justeringen av redovisningskontots saldon. Funktionen omvärderar saldot per valuta per redovisningskonto ungefär som du gör för justeringar av redovisningskonton som är kopplade till bankkonton. Om du använder ett redovisningskonto för att spåra flera tillgångar bör du överväga att använda ett leverantörs- eller kundkonto i stället.

> [!NOTE]
> Omvärdering av redovisningskonton kanske inte uppfyller alla krav för transaktions- och tillgångsregistreringar som behöver omvärderas. Till exempel för finansiella instrument, värdepapper, leasade tillgångar eller om du använder dem för specifika eller stora volymer av transaktioner eller tillgångar. Vi rekommenderar att du diskuterar med din revisor om du kan använda funktionen och i så fall hur du ska använda den. Till exempel om du tillåter att valutor blandas för ett konto, eller om du behöver ha ett separat konto för varje tillgång du vill spåra.

Följande exempel illustrerar skillnaden mellan att använda ett redovisningskonto och att använda ett leverantörskonto för att hålla reda på saldot för två monetära tillgångar som använder en utländsk valuta.

**Använda ett redovisningskonto** Om du använder ett redovisningskonto för att spåra antingen flera tillgångar (t.ex. lån eller anläggningstillgångar) i samma valuta, eller enskilda deltransaktioner för samma tillgång men fortfarande i samma valuta, görs en transaktion per omvärdering för valutan. Det innebär att du inte kan spåra justeringar relaterade till enskilda tillgångar eller enskilda transaktioner för samma tillgång.

**Använd ett leverantörskonto** Om du ställer in flera tillgångar som leverantörer och bokför transaktioner till dem, antingen i samma eller olika valutor, får du en justering per valuta per leverantör. Om du aktiverar växlingsknappen **Bokföring per transaktion** i jobbkötransaktionen **Justera valutakurs** får du en justeringstransaktion för varje separat leverantörsreskontratransaktion.

Den här skillnaden är viktig när du bedömer om redovisningsomvärdering är rätt funktion för dina rapporteringsbehov.

> [!TIP]
> Vi rekommenderar att du frågar din revisor vilken typ av konto som är bäst för ditt företag. Det kan också finnas en app för [!INCLUDE [prod_short](includes/prod_short.md)] på [AppSource](https://appsource.microsoft.com/en-us/marketplace/apps?page=1&product=dynamics-365-business-central) som är precis rätt för dina affärsscenarier.

## Se även

[Granska belopp på redovisningskonton](finance-review-accounts.md)  
[Förstå redovisningen och kontoplanen](finance-general-ledger.md)  
