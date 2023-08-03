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
    > Du kan endast synkronisera en enskild transaktion automatiskt från [!INCLUDE[crm_md](includes/crm_md.md)] när **Synka endast kopplade transaktioner** är inaktiverat och synkroniseringen har angetts som **dubbelriktad** eller **Från integreringstabell** på sidan **Registermappning för integrering** för transaktionen. Mer information finns i [Mappa de tabeller och fält som ska synkroniseras](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

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

## Massinfoga och koppla poster

Om du har ett stort antal Dataverse-enheter som motsvarar posterna i [!INCLUDE [prod_short](includes/prod_short.md)] kan du infoga och koppla dem i bulk. Du kanske till exempel vill lägga in och koppla poster när du ställer in synkronisering för första gången.

Du ska använda **Guiden för dataimport** i **Microsoft Power Platform administrationscenter**.

I följande exempel beskrivs hur du lägger till och koppla kunder med konton i Dataverse. Använd samma procedur för andra typer av entiteter, t.ex. leverantörer, artiklar och resurser.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.
2. Välj åtgärden **Öppna i Excel** för att öppna kunddata i Excel. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Om du vill mappa och importera data till entiteten i **konto** i Dataverse följer du de steg som beskrivs i [Importera data (alla post typer) från flera källor](/power-platform/admin/import-data-all-record-types).  

    Om entiteten konto har en kolumn för **bcbi_companyid** och du mappar data kolumnerna, bör du kontrollera att rätt företags-ID tilldelas i kolumnen för varje importerad post. Så här söker du efter företags-ID i [!INCLUDE [prod_short](includes/prod_short.md)]:

    1. Öppna sidan **integreringstabellens mappningslista**.
    2. Välj **KUND** och välj sedan **Redigera lista**.
    3. Bläddra åt höger och välj knappen redigeringshjälp :::image type="icon" source="media/assist-edit-icon.png" border="false"::: i fältet **Filter för integreringsregister**. Detta visar standardfiltret för kundmappning och innehåller företags-ID. Företags-ID är den första delen av värdet. Kopiera endast den delen och bortse från 0. I följande exempel markeras den del som ska kopieras.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Visar den del av företags-ID som ska kopieras":::

    > [!NOTE]
    > Alla namn på  Dataverse -entiteter och Business Central-poster matchar inte. Beroende på vad du importerar, kontrollera att följande kolumner har följande värden när du har importerat:
    >
    >* För kunderna ska kolumnen **CustomerTypeCode** innehålla **Kund**.
    >* För leverantörerna ska kolumnen **CustomerTypeCode** innehålla **Leverantörer**. 
    >* För artiklar bör kolumnen **ProductTypeCode** innehålla **Försäljningslager**.
    >* För resurser ska kolumnen **ProductTypeCode** innehålla **Tjänst**.
 
4. När du har importerat data till Dataverse-miljön i [!INCLUDE [prod_short](includes/prod_short.md)], följ dessa steg [För att koppla flera poster med matchningsbaserad koppling](#to-couple-multiple-records-using-match-based-coupling) för att koppla Dataverse-entiteterna med [!INCLUDE [prod_short](includes/prod_short.md)]-poster. 

## Frånkopplingsposter

Du kan koppla bort en eller flera poster från listsidor eller sidan **Kopplade datasynkroniseringsfel** genom att välja en eller flera rader och välja **Radera koppling**. Du kan också ta bort alla kopplingar för en eller flera registermappningar på sidan **Mappningar för integrationstabeller**.

## Se även  

[Använda Dynamics 365 Sales från Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]