---
title: Koppling och synkronisering (innehåller video)
description: Genom att synkronisera en mappning av integreringstabellen möjliggörs datasynkronisering i alla poster i en tabell i Business Central eller Dynamics 365 Sales som är kopplade.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
---

# Koppla och synkronisera poster mellan Dataverse och Business Central

I det här avsnittet beskrivs hur du kopplar en eller flera transaktioner i [!INCLUDE[prod_short](includes/prod_short.md)] med transaktioner i Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)]. Koppling av poster låter dig visa Dataverse information från [!INCLUDE[prod_short](includes/prod_short.md)] och vice versa. Kopplingen låter dig också synkronisera data mellan posterna. Du kan koppla befintliga poster eller skapa och koppla nya poster.

> [!NOTE]
> Du kan bara koppla och synkronisera data om din systemadministratör har skapat en anslutning mellan [!INCLUDE[prod_short](includes/prod_short.md)] och Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)]. Ett snabbt sätt att kontrollera är att öppna kortet **kund** och leta efter åtgärden **konfigurera koppling**. Om åtgärden är tillgänglig är apparna sammankopplade.

## Videoexempel

Det här videoklippet visar kopplings-och synkroniseringsdata vid integrering med [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## Om du vill koppla en post  

1. I [!INCLUDE[prod_short](includes/prod_short.md)] öppnar du kortet för den post du vill koppla. Till exempel kund- eller kontaktkort.  

    Du kan också bara öppna listsidan och välja den post som du vill koppla.  

2. Välj åtgärden **konfigurera koppling**.  
3. Fyll i fälten och välj sedan **OK**.  

## Om du vill synkronisera en enda post  

1. I [!INCLUDE[prod_short](includes/prod_short.md)] öppnar du kortet för den post du vill koppla. Till exempel kund- eller kontaktkort.  
2. Välj åtgärden **synkronisera nu**.  
3. Om en transaktion kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## Om du vill synkronisera en enda transaktion från [!INCLUDE[crm_md](includes/crm_md.md)]  

1. I [!INCLUDE[crm_md](includes/crm_md.md)] öppnar du formuläret för den transaktion du vill koppla. Till exempel formuläret Kontokort eller Kontaktkort.  
2. Välj åtgärden **[!INCLUDE[prod_short](includes/prod_short.md)]** i menyfliksområdet för att öppna och koppla transaktioner automatiskt.

    > [!Note]
    > Du kan endast synkronisera en enskild transaktion automatiskt från [!INCLUDE[crm_md](includes/crm_md.md)] när **Synka endast kopplade transaktioner** är inaktiverat och synkroniseringen har angetts som dubbelriktad eller Från integreringstabell på sidan **Registermappning för integrering** för transaktionen. Mer information finns i [Mappa de tabeller och fält som ska synkroniseras](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).     

## För at koppla flera poster med matchningsbaserad koppling

Ange vilka data som ska synkroniseras för en entitet, t.ex. en kund eller kontakt, genom kopplingsposter som baseras på matchningar. Förfina matchningarna genom att göra sökningen skifteslägeskänslig och tilldela varje matchning en prioritet. Om ingen matchning hittas kan du även ange att du vill skapa entiteten i Dataverse. Mer information finns i [Anpassa matchningsbaserad koppling](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

> [!NOTE]
> Den matchningsbaserad koppling hoppar över poster som redan har matchats. Ta med dessa poster när du kör en matchningsbaserad koppling, koppla bort posterna och försök igen. För att lära dig mer om att koppla från poster, gå till [Frånkopplingsposter](#uncoupling-records).

1. I [!INCLUDE[prod_short](includes/prod_short.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.
2. Välj åtgärden **matchningsbaserad koppling**.
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Om du vill synkronisera flera poster  

1. I [!INCLUDE[prod_short](includes/prod_short.md)] öppna listsidan för posten, till exempel listsidan kunder eller kontakter.  
2. Markera den post du vill synkronisera och välj sedan åtgärden **Synkronisera nu**.  
3. Om transaktioner kan synkroniseras åt endast ett håll, välj då det alternativ som anger riktningen för datauppdateringen, och välj sedan **OK**.  

## Frånkopplingsposter

Du kan koppla bort en eller flera poster från listsidor eller sidan **Kopplade datasynkroniseringsfel** genom att välja en eller flera rader och välja **Radera koppling**. Du kan också ta bort alla kopplingar för en eller flera registermappningar på sidan **Mappningar för integrationstabeller**.

## Se även  

[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]