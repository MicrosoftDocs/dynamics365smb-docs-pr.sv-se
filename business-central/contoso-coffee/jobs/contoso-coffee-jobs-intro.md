---
title: Introduktion till projekthantering för Contoso Coffee
description: Den här artikeln introducerar dig till Consoso Coffee-demonstrationsdata för projekt och projekthantering.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Introduktion till projekt och projekthantering för Contoso Coffee

Contoso Coffee är ett fiktivt företag som tillverkar kaffemaskiner för privat och kommersiellt bruk. **Contoso Coffee**-programmen för Business Central lägger till demonstrationsdata som du kan använda för att lära dig använda funktionerna för projekt och projekthanterin i Business Central.

Detta program innehåller flera element som används för de viktigaste genomgångarna:

- Resurser med tilldelade färdigheter och zoner
- Artiklar konfigurerade att skapa serviceartiklar

> [!IMPORTANT]
> Innan du kör något av scenarierna för Contoso Coffee bokför du eventuella artikeljournalrader med ingående balanser. Mer information finns i avsnittet [Konfigurera data för Contoso Coffee](#set-up-contoso-coffee-jobs-and-project-management-data).
>
> 
## Konfigurera projekt och projekthanteringsdata för Contoso Coffee

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

När de relevanta programmen väl har installerats går du till sidan [Projektdemonstrationsdata för Contoso Coffee](https://businesscentral.dynamics.com/?page=4767) i [!INCLUDE [prod_short](../../includes/prod_short.md)] och ändrar standardinställningarna så att de passar dina behov. Inställningarna beskrivs i följandetabeller:  

|Fält  |Beskrivning  |
|---------|---------|
|**Startår** |Anger det första år som du vill använda för demonstrationsdata för Contoso Coffee. Beroende på företagets konfiguration är året antingen ett kalender år eller ett räkenskapsår.|
|**Kundnr**  |Den kund som ska användas för scenarierna i försäljningsåtgärderna.|
|**Artikel 1 nr.**  |Den artikel som ska användas för kontraktscenarierna.|
|**Artikel 2 nr.**  |Den artikel som ska användas för reparationsscenarierna.|
|**Lokal resurs nummer 1**  |Den resurs som ska användas för kontraktscenarierna.|
|**Fjärresurs nummer 1**  |Den resurs som ska användas för reparationsscenarierna.|
|**Kundbokföringsmall**|Anger en företagskod för inrikes kunder. Affärskoderna används när transaktionerna bokförs. |
|**Kund – generell rörelsebokföringsmall**|Anger en företagskod för inrikes kunder. Affärskoderna används när transaktionerna bokförs. |
|**Inrikes – generell rörelsebokföringsmall**|Anger en företagskod för inrikes kunder och leverantörer. Affärskoderna används när transaktionerna bokförs. |
|**Återförsäljning – lagerbokföringsmall**    |Anger en kod för artiklar som måste användas för bokföring av återförsäljning.|
|**Detaljhandel – generell produktbokföringsmall**    |Anger en kod för artiklar som måste användas för bokföring av återförsäljning.|
|**Moms produktbokföringsmall**    |Anger en momsproduktkod för artiklar för bokföring av moms om moms är aktiverat.|
|**Prisfaktor**     |Anger en faktor för att omvandla ett pris från USD/EUR till lokal valuta. *1* innebär att priset är samma belopp i alla valutor. Ett högre värde används för att hämta priset i lokal valuta. |
|**Avrundningsprecision**  |Definierar hur de beräknade förbrukningskvantiteterna avrundas när de registreras på förbrukningsjournalrader. Kvantiteter mindre än 0,5 avrundas nedåt. Kvantiteter lika med eller högre än 0,5 avrundas uppåt.|

Välj åtgärden **Skapa demonstrationsdata** när du är klar. Det tar några minuter att lägga till data i den underliggande databasen, men sedan är det dags att köra de olika scenarierna.  

## Se även
