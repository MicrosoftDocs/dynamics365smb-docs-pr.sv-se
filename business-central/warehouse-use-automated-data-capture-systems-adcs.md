---
title: Använda ADCS-grunden (Automatiskt datainsamlingssystems)
description: Läs hur du använda ADCS (automatiska datainsamlingssystem) för att registrera transport av artiklar i distributionslagret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7700, 7703, 7704, 7706, 7707, 7710, 9813, 9814'
---
# Använda ADCS-grunden (Automatiskt datainsamlingssystems)

> [!Important]
> Med hjälp av ADCS-lösningen (Automated Data Capture System) ger en väg [!INCLUDE[prod_short](includes/prod_short.md)] kan du kommunicera med handburna enheter via webbtjänster. Du måste arbeta med en Microsoft-partner som kan tillhandahålla länken mellan webbtjänsten och den specifika handhållen enheten. 

Du kan använda det automatiska datainsamlingssystemet (ADCS eller Automatiskt datainsamlingssystem) för att registrera förflyttningen av alla artiklar i distributionslagret och för att registrera några journalaktiviteter, däribland kvantitetsjusteringar i artikeljournalen för distributionslagret, inventeringsjournalen och fysisk inventering. ADCS inbegriper vanligen streckkod.

Om du ska använda ADCS måste du ge varje artikel i distributionslagret en artikelidentifierare. Du måste även lägga upp miniformulär, handdatorfunktioner, datautbyten och specificeras inställningar för fältet som kontrollerar ADCS. Du anger om du ska använda ADCS på lagerställekortet för ett lager.

Baserat på behovsnivån i lagret definierar du den mängd information som ska visas i miniformulärinställningarna för den aktuella handenheten. Följande är exempel information som du kan visa:  

- Data från tabeller i [!INCLUDE[prod_short](includes/prod_short.md)], till exempel en lista över plockningsdokument som användaren kan välja från.  
- Textinformation.  
- Meddelanden som innehåller bekräftelser eller fel om aktiviteter som utförts och registrerats av handenheter användaren.

## Så här aktiverar du webbtjänster för ADCS

Om du vill använda det automatiska datainsamlingssystemet måste du aktivera ADCS-webbtjänst. Du måste arbeta med en Microsoft-partner som kan implementera en webbtjänst som kan koppla ihop ADCS och en specifik handhållen enhet. Du kan lära dig mer om webbtjänsten för ADCS genom att undersöka codeunit 7714. 
 
## Så här konfigurerar ett lager att använda ADCS  

Om du ska använda ADCS måste du ange vilka distributionslagerställen som använder teknologin.  

> [!NOTE]  
> Vi rekommenderar att du inte ställer in ett distributionslager som ska använda ADCS, om det dessutom har en lagerplats kapacitetsprincip.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **placeringar** och väljer sedan relaterad länk.
2. Välj ett lagerställe som du vill aktivera för ADCS för och välj åtgärden **redigera**.
3. På sidan **lagerställekort** aktiverar du växlingsknapp **använda ADCS**.  

## Ange ett objekt för att använda ADCS  

Varje distributionslagerartiklar som ska användas med ADCS, måste tilldelas en identitetskod för att koppla den till dess artikelnummer. Du kan t.ex använda artikelns Streckkod som identitetskoden. En artikel kan också använda flera identitetskoder. Det kan vara praktisk i de fall där en artikel är disponibel i olika måttenheter, t.ex stycken och pallar. Tilldela varje en identitetskod, i det här fallet.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Artiklar** och väljer sedan relaterad länk.  
2. Markera ett objekt i listan som ingår i ADCS-lösningen och välj åtgärden **redigera**.
3. På sidan **Artikelkort** väljer du åtgärden **Identifierare**.
4. PÅ sidan **Artikelidentifierare** väljer du åtgärden **Ny**.
5. I fältet **Kod** ange identifierare för artikeln. Du kan t.ex använda artikelns Streckkod som identitetskoden.  

    Du kan även definiera ett **Variantkod** och en **Enhet** kod.  

6. Ange flera koder för varje artikel, om det behövs.
7. Välj knappen **OK**.  
8. För att granska informationen väljer du fältet **identitetskod** för att öppna sidan **Artikelidentifierare**.

## Om du vill lägga till en ADCS-användare  

Du kan lägga till en användare i en ADCS. När du gör det, måste du ange ett lösenord. Om du vill kan du även ange en koppling som identifierar ADCS-användaren som distributionslageranvändare. ADCS-användarlösenord kan vara olika från deras inloggningslösenord. Läs mer i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **ADCS-användare** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Ange ett **Namn** på användaren. Namnet kan inte ha fler än 20 tecken, inklusive blanksteg.  
4. Ange ett **Lösenord** i fältet.  

### Om du vill ange att lagerpersonalen är en ADCS-användare  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
2. Lägga till en ny lagerpersonalen, om det behövs. Läs mer i [Konfigurera distributionslagerarbetare](warehouse-how-to-set-up-warehouse-employees.md).  
3. Välj åtgärden **Redigera lista**.  
4. Välj en lagerpersonal i listan. I fältet **ADCS-användare** väljer du namnet på en ADCS-användare från listan.  

> [!NOTE]  
> Standarddistributionslagret för den anställde ska vara en som använder ADCS.

## Så här: Skapa och anpassa Miniformulär

Du använder miniformulär som beskriver den information som du vill presentera på en handenheter. Du kan till exempel skapa miniformulär för att hantera lageraktiviteten att plocka artiklar. När du har skapat en miniformulär, kan du lägga till funktioner för den vanliga åtgärder för en användare med handenheter, till exempel flytta uppåt eller en rad.  

> [!NOTE]
> För att använda eller ändra funktionen i en miniformulärfunktion måste du skapa en ny kodmodul för fältet **Hantera codeunit** för att utföra lämplig åtgärd eller svar. Du kan lära dig mer om ADCS-funktioner genom att undersöka följande codeunits:
>
> * 7705
> * 7706
> * 7712
> * 7713  

### Så här skapar du en miniformulär för ADCS  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Miniformulär** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. I fältet **Kod** anger du en kod på Miniformuläret. Ange värden i alla övriga fält, om du vill.  

    Aktivera växlingsknappen **Starta miniformulär** för att ange att miniformuläret är det första formulär som är tillgänglig när användaren loggar in.  

4. Definiera fälten som visas på miniformuläret på **Rader** Snabbfliken. Ordningen där du anger rader, är den ordning som raderna ska visas på handenheten.  

När du har skapat en miniformulär, nästa steg är att skapa operationer och att koppla funktioner för olika tangentbord indata.  

### Om du vill anpassa miniformulärfunktioner

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Miniformulär** och väljer sedan relaterad länk.  
2. Välj ett miniformulär från listan, välj åtgärden **Redigera**.  
3. Välj åtgärden **Funktioner**.  
4. I listrutan **Funktionskod** väljer du en kod för att representera en funktion som du vill koppla till miniformuläret. Du kan till exempel välja **ESC**, som associerar funktionen med **ESC**-tangenten.  

## Se även  

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
