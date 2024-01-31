---
title: Ekonomisk information snabbstart
description: Förbered företaget för verksamheten genom att lägga upp den ekonomiska informationen i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Ekonomisk information snabbstart

När du har angett grundläggande företagsinformation i [!INCLUDE[prod_short](includes/prod_short.md)] är ett av nästa steg att fylla i det ekonomiska avsnittet. Du kan inte bara ta emot eller göra betalningar, utan även för att hantera och rapportera ditt företagsnummer.

## Kontoplanen

Kontoplan (COA) ger en överblick över företagets ekonomi, som visar konton i strukturerade grupper som tillgångar, skulder, intäkter, sålda varor och kostnader. [!INCLUDE[prod_short](includes/prod_short.md)] innehåller en standardkontoplan som du kan anpassa till ditt företags redovisningspraxis.

## Konfigurera kontoplan

I följande video visas hur du konfigurerar en kontoplan i [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### Lägg till ett konto i kontoplanen

Om du vill lägga till ett konto som inte ingår som standard i [!INCLUDE[prod_short](includes/prod_short.md)], t.ex. trädgårdstjänster – så följer du bara dessa steg:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.
2. I fönstret **Ny** väljer du sidan **Redovisningskontokort**.
3. Ange följande data i motsvarande fält på snabbfliken **Allmänt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Fält | Data |
   | --- | --- |
   | **Nr** | 61250 |
   | **Namn** | Trädgårdstjänster |
   | **Resultat/Balans** | Resultaträkning |
   | **Kontokategori** | Utgift |
   | **Underkategori Konto** | Reparations- och underhållsutgift |
   | **Debet/Kredit** | Båda |
   | **Kontotyp** | Bokföra |

4. På snabbfliken **Bokföring** anger du följande information:

   | Fält | Data |
   | --- | --- |
   | **Typ av bokföring** | Inköp |
   | **Gen. rörelsebokföringsmall** | Inrikes |
   | **Produktbokföringsmall** | Tjänster |

5. Fyll i återstående fält på sidan **Leverantörsbankkontokort** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Få en översikt över kontoplanen

Om du behöver en mer kompakt vy av kontoplanen, utan kolumner för bokföringsmallar, bokföringstyp eller kostnadstyp, visas huvudinformationen för varje konto i en mindre tabell i **översikten över kontoplan**. Du kan dessutom dölja eller expandera grupper så att de döljer kontona i dem.

Om du vill visa översikten väljer du åtgärden **Kontoplansöversikt** på sidan **Kontoplan** eller sök efter funktionen med ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra").

Lära dig mer om kontoplanen och redovisningen i [Förstå redovisningen och kontoplanen](finance-general-ledger.md).

## Skapa bankkonton

Bank konton i [!INCLUDE[prod_short](includes/prod_short.md)] registrera banktransaktioner och är kopplade till transaktioner i kontoplanen. I följande video visas hur du konfigurerar bankkonton.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.
2. På sidan **Bankkonton** väljer du åtgärden **Ny**.
3. I fältet **Nr.** en identifierare som *B010*, om det finns en lista med numrerade serier för bankkonton. Om inte, ange en unik kombination.

   Fältet skiljer sig från fältet **Bankkontonr.** på snabbfliken **Allmänt**.
4. På sidan **Bankkontokort** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Se även

[Konfigurera kontoplanen](finance-setup-chart-accounts.md)  
[Konfigurera bankkonton](bank-how-setup-bank-accounts.md)  
[Köra och skriva ut rapporter](ui-work-report.md)  
[Snabbstart för Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
