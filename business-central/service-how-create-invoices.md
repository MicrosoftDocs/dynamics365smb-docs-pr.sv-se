---
title: Skapa servicefakturor eller kreditnotor för tjänster
description: Lär dig hur du skapar fakturor och kreditnotor för dina tjänster.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Skapa servicefakturor eller kreditnotor

Enkel fakturering av serviceorder är en nyckelfunktion i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan också konfigurera [!INCLUDE[prod_short](includes/prod_short.md)] så att en servicetekniker på fältet kan skapa en faktura för en tjänst som inte är kopplad till ett kontrakt eller en order. Du kan också ställa in [!INCLUDE[prod_short](includes/prod_short.md)] så att du regelbundet fakturerar servicekontrakt. Faktureringsperioden för respektive kontrakt anger hur ofta du skickar ut den.

## Så här fakturerar du servicekontrakt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Skapa servicekontraktsfakturor** och väljer sedan relaterad länk.  
2. Ange de filter som du vill använda.  
3. I fältet **Bokföringsdatum** anger du det datum som du vill använda som bokföringsdatum på servicefakturorna.  
4. I fältet **Fakturera till datum** anger du det sista datumet på kontraktet som du vill skicka fakturor för. Batch-jobbet kommer att innehålla kontrakt med nästa fakturadatum fram till detta datum.  
5. Markera **Skapa fakturor** i fältet **Åtgärd**.  
6. Skapa servicefakturor genom att klicka på **OK**.  
  
Du kan också fakturera ett servicekontrakt direkt från sidan **Servicekontrakt** om nästa fakturadatum på kontraktet infaller tidigare än arbetsdagen.

## Fakturera ett servicekontrakt från servicekontraktsidan   

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekontrakt** och väljer sedan relaterad länk.  
2. Välj det servicekontrakt du vill fakturera och öppna kontraktskortet.  
3. Välj åtgärden **Skapa servicekontrakt**. 
4. Skapa servicefakturor genom att klicka på **Ja**.  
  
  > [!NOTE]  
  > Det går inte att skapa servicefakturor för servicekontrakt om fältvärdet för **Ändra status** anges till **Öppen**.  

## Så här bokför du förbrukning från en serviceorder  

Nedan beskrivs hur du definierar den del av en service som du debiterar kunden för.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Serviceorder** och väljer sedan relaterad länk.  
2. Välj serviceorder som du vill fakturera och öppna orderkortet.  
3. Välj åtgärden **Servicerader**.  
4. Hitta transaktionerna och ange de antal som du debiterar kunden för i fältet **Ant. att fakturera**.  
  
   > [!NOTE]  
   > Du kan fakturera kunden helt eller delvis för en registrerad service. Om du väljer att fakturera kunden helt måste värdet i fältet **Ant. att fakturera** vara lika med värdet i fältet **Antal**. Observera att du kan bokföra en fullständig faktura tillsammans med en fullständig leverans, och att du kan bokfört fullständig försändelse som inte är fakturerad eller förbrukad.  
   >  
   > När du bokför en delfaktura kan du ange antalet att fakturera på två olika sätt. Om du ska bokföra service med alternativet **Leverera och fakturera** måste värdet i fältet **Ant. att fakturera** vara lika med värdet i fältet  **Ant. att utleverera**. Om du vill fakturera en redan bokförd leverans får antalet att fakturera inte vara större än värdet i fältet **Utlevererat antal**.  
  
5. Välj **Bokför**, och sedan antingen **faktura** eller **leverera och fakturera**. Läs mer på [Bokföra tjänstehantering](service-service-posting.md).  
  
 Den valda serviceraden bokförs. Du kan bokföra flera servicerader samtidigt, genom att markera dem och välja **Bokför**. Om du gör detta måste du se till att du har fyllt i all nödvändig information på de rader.  
  
 När du bokför ordern med alternativet **Fakturera** skapas en bokförd servicefaktura samtidigt som motsvarande transaktioner automatiskt, och alla relevanta fält på serviceraderna i ordern uppdateras. Dessutom uppdateras det/de tidigare bokförda leveransdokumentet/-dokumenten automatiskt med de antal som har fakturerats. Om du väljer bokföringsalternativet **Leverera och fakturera** skapas också en bokförd leverans automatiskt.

## Så här skapar du en servicefaktura manuellt  

När du bokför en serviceorder med alternativet **Fakturera** eller **Leverera och fakturera** bokförs typiskt en servicefaktura automatiskt. Det kan hända att du behöver skapa en faktura som inte är kopplad till ett servicekontrakt eller en order. Här beskrivs hur du skapar en faktura samtidigt som kunden tar emot service.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicefakturor** och väljer sedan relaterad länk.  
2. Skapa en ny servicefaktura.  
3. Fyll i fälten **Nr.** .  
  
    > [!NOTE]  
    >  Om du har angett nummerserier för servicefakturor på sidan **Serviceinställningar** kan du trycka på **Retur**, så väljs nästa tillgängliga servicefakturanummer.  
  
4. I fältet **Kundnr.** anger du ett nummer för kontakten. Välj relevant kund i listan.  
  
    Kundfälten fylls i automatiskt med information från kortet **Kund**.  
  
5. Ange ett datum i fältet **Bokföringsdatum**. Detta datum visas i de bokförda transaktionerna. I det här fältet visas ditt aktuella arbetsdatum, men du kan ändra datumet.  
6. Fyll i fältet  **Dokumentdatum**. Det datum du anger här visas på den utskrivna fakturan och används för att beräkna förfallodatum.  
7. Fyll i serviceraderna för fakturan. Fyll i fälten **Typ**, **Nr** och **Antal** för att registrera de artiklar, resurser och kostnader som har använts för service.

## Så här skapar du en faktura som kombinerar bokförda leveransrader från en eller flera serviceorder 

Du kan behöva skapa en servicefaktura för den service som redan har levererats från en eller flera serviceorder, men inte fakturerats eller förbrukats. Du kan fylla i fakturaraderna automatiskt med de valda bokförda utleveransraderna för en specifik kund.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicefakturor** och väljer sedan relaterad länk.  
2. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Skapa fakturarader för service som har levererats men inte fakturerats. Du kan använda åtgärden **Hämta leveransrader** för att lägga till bokförda leveransrader till fakturan.  
4. Bokför servicefakturan.  
  
 Den bokförda servicefakturan skapas samtidigt som motsvarande transaktioner. De tidigare bokförda utleveransdokumenten uppdateras med de fakturerade antalen och de antalen på serviceraderna i källorderna.  

## Så här skapar du servicekreditnotor  

Du använder vanligtvis en servicekreditnota när en kund returnerar en artikel. Men du kan också använda dem för att ersätta en kund eller för att korrigera en faktura som var ett misstag.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Servicekreditnotor** och väljer sedan relaterad länk.  
2. Fyll i fälten på den första raden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Visa arbetsdatum i fälten **Bokföringsdatum** och **Dokumentdatum**. Du kan ändra informationen vid behov.    
4. Ange information om artiklarna som har returnerats eller tagits bort, eller om kompensationen som ska skickas, på kreditnoteraderna.  

## Korrigera fel i servicefakturor

Du kan ta bort servicefakturor som är kopplade till servicetransaktioner. Det innebär att du kan korrigera fel eller göra ändringar i servicefakturor utan att fastna eller förlora data. Om du till exempel glömmer att tilldela en produktbokföringsmall till ett redovisningskonto kan du lägga till den senare och återskapa servicefakturan.

Använd åtgärden :::image type="content" source="media/copilot-delete-trash-can.png" alt-text="Ta bort åtgärdsikon"::: för att ta bort en tjänstefaktura. 

När du tar bort en servicefaktura händer följande:

* Bokföra en korrigerande servicetransaktion
* Återställ faktureringsdatum och faktureringsperiod i kontraktet, så att du kan skapa fakturan igen.

> [!NOTE]
> Du kan återställa flera fakturor, men du måste göra det sekventiellt, med början från den sista fakturan.
>
> Du kan inte ta bort en servicefaktura om dess uppgifter, till exempel faktureringsperioden eller växlingsknappen **Förutbetald**, har ändrats i det relaterade servicekontraktet. Se till att du tar bort fakturor innan du ändrar inställningarna i servicekontraktet.

## Se även

[Så här bokför du fakturor](service-how-to-post-service-orders.md)  
[Ställa in tjänstehantering](service-setup-service.md)  
[Bokföring av service](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]