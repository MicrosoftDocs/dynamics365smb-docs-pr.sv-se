---
title: Hantera koncerninterna transaktioner
description: Med de koncerninterna funktionerna förenklar du affärsprocesser och transaktioner mellan företag inom samma organisation.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
ms.service: dynamics-365-business-central
---
# Hantera koncerninterna transaktioner

Företag med fler än en juridisk person med separata redovisningsfunktioner kan utnyttja koncerninterna transaktioner. Det kan till exempel vara användbart för företag som har dotter bolag på flera internationella marknader eller regioner. Organisationen kan bestå av flera företag, men kanske inte har motsvarande antal team inom redovisning och administration. Koncerninterna transaktioner förenklar affärsprocesser och transaktioner mellan företag i koncerninterna partnerskap.

När du har angett kund- och leverantörsrelationer för koncerninterna transaktioner, registrerar partner information en gång i försäljnings- och inköpsdokument. Ett motsvarande dokument skapas i den andra partnern som är involverad i transaktionen. Genom att koppla funktioner för kontoplanen och dimensioner kan du försäkra dig om att informationen visas på rätt plats.  

Det finns fyra huvudsakliga fördelar med koncerninterna funktioner:  

* Ökad produktivitet till följd av tidsbesparingar och förenklade transaktioner  
* Mindre misstag eftersom informationen endast behöver registreras en gång och automatiserade processer över hela systemet  
* Fullständig redovisningsspårning och full insyn i affärsaktiviteter och transaktionshistorik  
* Effektiva, kostnadseffektiva transaktioner med dotterbolag  

## Förenkling av arbetsflödesaktiviteter  

Med hjälp av koncerninterna transaktioner kan du distribuera försäljnings- och inköpsdokument samt journaltransaktioner till alla satellitkontor, försäljningskontor och dotterbolag. Att fördela transaktioner sparar tid och ökar effektiviteten i hela organisationen genom att minska datainmatning. Det minskar behovet av att skicka, ta emot, skriva ut och arkivera försäljnings- och inköpsdokument.  

Du har full kontroll över alla transaktionsdokument. Du kan t. ex. avvisa ett dokument som har skickats till dig och använd åtgärderna **återföra journalbokningar** och **ångra inleveranser/utleveranser** för korrigeringar. När du gör ett inköp från en partner eller ett dotterbolag kan du uppdatera inköpsordern så länge som det säljande bolaget inte har levererat några varor.  

När du registrerar en transaktion behöver du inte ange vilka konton som ska användas. Du väljer just den koncerninterna partnern. De koncerninterna funktionerna skapar rader i redovisningsjournaler som balanserar räkenskaperna för de båda företag som är involverade i en transaktion. I Kundreskontra och Leverantörsreskontra tilldelar du en koncernintern partnerkod till kunder och leverantörer. Från det tillfället producerar alla order och fakturor för transaktioner mellan dessa företag motsvarande dokument i partnerföretaget. Resultatet är rätt balanserade konton.  

Koncernintern fokuserar på försäljnings- och inköpsdokument och redovisningsjournalrader och tillåter transaktioner mellan flera [!INCLUDE [prod_short](includes/prod_short.md)]-databaser. Som exempel:

* I olika länder/regioner
* Flera valutor
* Olika kontoplaner
* Olika dimensioner
* Olika artikelnummer  

I koncerninterna transaktioner används flera typer av transaktioner och dokument:  

* Redovisningsjournalposter
* Inköps- och försäljningsorder
* Inköps- och försäljningsfakturor
* Kreditnotor
* Returorder

När du ställer in koncerninterna transaktioner skapar du en lista över koncerninterna partner och en koncernintern kontoplan och koncerninterna dimensioner. Efteråt kan du skapa transaktioner i koncerninterna redovisningsjournaler.

> [!NOTE]
> Redovisningsjournalen innehåller i sig själva inga valutor. Alla belopp omvandlas till den aktuella valutakursen i den lokala valutan.

När du har ställt in affärspartner som kunder och leverantörer och tilldelat dem koncerninterna partnerkoder, är det möjligt att utbyta koncerninterna inköps – och försäljningsdokument, inklusive artiklar och artikelomkostnader. 

> [!NOTE]
> Företag kan inte använda koncernintern för att utbyta alla typer av data. Inköpsfakturor skickas inte till affärspartner via koncerninterna processer. Men försäljningsfakturor som skickas via koncerninterna processer kommer att skapas som inköpsfakturor i det mottagande företaget.

Att konsolidera ekonomiska data kan vara särskilt användbart för koncerninterna processer. Mer information finns i [Konsolidera ekonomiska data från flera företag](finance-consolidated-company-reporting.md).

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.

|Till |Gå till|
|---|---|
|Skapa dina koncerninterna leverantörer och kunder som partner och konfigurera en koncernintern kontoplan.|[Koncerninterna inställningar](intercompany-how-setup.md)|
|Du använder koncerninterna dokument eller journaler för att bokföra transaktioner med koncerninterna partner.|[Arbeta med koncerninterna dokument och journaler](intercompany-how-work-documents-journals.md)|
|Ordna och bearbeta ingående och utgående transaktioner som du skickar till din koncerninterna partner.|[Hantera koncerninterna in- och utkorgar](intercompany-how-manage-intercompany-inbox.md)|
|Använd koncerninterna transaktioner för att fördela kostnader mellan partnerföretag.|[Fördela kostnader till koncerninterna partner](intercompany-allocate-costs.md)|

## Se även

[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
