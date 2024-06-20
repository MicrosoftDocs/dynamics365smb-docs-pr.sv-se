---
title: Rapport om betalningsrutiner
description: Lär dig hur du enkelt skapar rapporten Betalningsrutiner för leverantörer och kunder.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment, practices, vendor, customer, report'
ms.search.form: '686, 687, 689'
ms.date: 04/23/2024
ms.author: altotovi
ms.reviewer: bholtorf
--- 

# Rapport om betalningsrutiner  

Vissa länder/regioner kräver att företag rapporterar betalningstider för sina leverantörer enligt lokala myndigheters definition. Denna rapportering kan baseras på olika källor och kan sortera leverantörer baserat på deras storlek eller definierade betalningsvillkor, vilket ger rapportering för leverantörer för följande enligt krav från lokala myndigheter:  

- Genomsnittlig överenskommen betalningsperiod.  
- Genomsnittlig faktisk betalningsperiod.   
- Andelen fakturor som betalats efter utgången av den överenskomna betalningsperioden. 

Användare kan välja den period som de vill köra en beräkning för och hitta detaljer baserat på en gruppering som du väljer. För var och en av dessa grupperingar kan du hitta källposter. 

> [!NOTE]
> Denna rapportering krävs hittills i vissa länder, men detta är en global funktion och kan användas överallt. För närvarande måste svenska företag med 250 eller fler anställda varje år rapportera till Bolagsverket vilka betalningstider de har för inköp från företag som är mindre än dem själva. Liknande handlingar finns i Storbritannien, Australien och Nya Zeeland.  

## Skapa rapporten 

Använd följande steg för att köra rapporten **Betalningsrutiner**:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Betalningsrutiner** och väljer sedan relaterad länk. 
2. Välj **Ny**.
3. På snabbfliken **Allmänt** anger du värden i följande fält:

   | Fält | Description |
   |---------|-----------------------------------|
   | Nr. | Ange numret på transaktionen eller posten för rapporten. |
   | Aggregeringstyp | Ange hur data aggregeras. Om du väljer alternativet **Periodrapporten** baseras på olika perioder, men om du väljer alternativet **Företagsstorlek** skapas rapporten baserat på företagsstorlekar som konfigurerats i fältet **Företagsstorlekskod** på kortet **Leverantör**. |
   | Rubriktyp | Anger källan för transaktioner i betalningsrutinen och du kan välja Leverantörer, Kunder eller båda. |
   | Startdatum | Anger startdatumet för betalningsrutinen. |
   | Slutdatum | Anger slutdatumet för betalningsrutinen. |

> [!NOTE]
> Om du bestämmer dig för att använda alternativet **Företagsstorlek** måste du först skapa transaktioner på sidan **Företagsstorlekar** och lägga till dem hos alla leverantörer som du vill spåra med den här metoden.

4. När du har fyllt i alla fält i huvudet måste du köra åtgärden **Generera** för att generera data på raderna och statistik för vald typ av rapportering.
5. Baserat på **Aggregeringstyp** får du olika rader. Du kan ändra vissa värden manuellt, men i det här fallet markeras varje ändrad rad och hela rapporten som **Ändrad manuellt**.
6. Från alla beräknade fält kan du gå djupare för att se hur resultatet har beräknats genom att öppna sidan **Lista över data för betalningsrutinen**.
7. Om du vill skriva ut dokumentet kan du göra det genom att köra åtgärden **Skriv ut**.

## Se även

[Ekonomiska rapporter](finance-reports.md)  
[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Kundreskontra, rapporter och analyser](receivables-reports.md)  
[Leverantörsreskontra, rapporter och analyser](payables-reports.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Ekonomi](finance.md)  
[Översikt över lokala funktioner](about-localization.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
