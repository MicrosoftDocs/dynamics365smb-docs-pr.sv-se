---
title: Designdetaljer – Lagerstyrningsinställningar
description: 'Lagerställefunktionen innehåller olika komplexitetsnivåer, som till stor del definieras av lagerplatsinställningarna på lagerställekort.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Designdetaljer: Lagerstyrningsinställningar

Distributionslagerfunktion i [!INCLUDE[prod_short](includes/prod_short.md)] innehåller olika nivåer av komplexitet, enligt definitionen av licensbehörigheter i de offererade partiklarna. Nivån av komplexitet i en lagerlösning definieras i hög grad av den lagerplatsinställningen på lagerställekort, som i sin tur är licenskontrollerat så att åtkomsten till inställningsfält för lagerstället definieras av licensen. Dessutom ska kopplingsobjekten i licensen styra vilka användargränssnittsdokument som ska användas för de distributionslageraktiviteter som stöds.  
<!--
The following warehouse-related granules exist:  

- Basic Inventory (4010)  
- Bin (4170)  
- Put Away (4180)  
- Warehouse Receipt (4190)  
- Pick (4200)  
- Warehouse Shipment (4210)  
- Warehouse Management Systems (4620)  
- Internal Picks and Put-aways (4630)  
- Automated Data Capture System (4640)
- Bin Setup (4660)  

For more information about each granule, see [[!INCLUDE[prod_short](includes/prod_short.md)] Price Sheets](https://go.microsoft.com/fwlink/?LinkId=238341) (requires PartnerSource account). -->

Efterföljande tabell visar vilka partiklar som krävs för att definiera olika komplexitetsnivåer för distributionslager, vilka användargränssnittsdokument som stöder varje nivå och vilka lagerställekoder som avspeglar dessa nivåer i [!INCLUDE[prod_short](includes/prod_short.md)]-demonstrationsdatabas.  

[!INCLUDE [locations-cronus](includes/locations-cronus.md)]

|Komplexitetsnivå|Beskrivning|Användargränssnittsdokument|Exempelplats|Lägsta partikelkrav|  
|----------------|-----------|-----------|---------------|---------------------------|  
|1|Ingen tilldelad distributionslageraktivitet.<br /><br /> Ta emot/leverera från order.|Order|BLÅ|Grundläggande lager|  
|2|Ingen tilldelad distributionslageraktivitet.<br /><br /> Ta emot/leverera från order.<br /><br /> Lagerställeskoden krävs.|Order med lagerställeskod|SILVER|Grundläggande lager/Lagerplats|  
|3 <br /><br /> **Observera**: även om inställningarna kallas **Begär plockning** och **Begär artikelinförsel** kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor.|Grundläggande distributionslageraktivitet, en order i taget.<br /><br /> Ta emot/leverera bokföring från lagerartikelinförsel/plockdokument. <br /><br /> Lagerställeskoden krävs.|Lagerartikelinförsel/lagerförflyttning/lagerplockning med lagerställeskod|(SILVER + Kräver artikelinförsel eller Kräver artikelinförsel)|Grundläggande lager/Lagerplats/Artikelinförsel/Plockning|  
|4|Avancerad distributionslageraktivitet, för flera order.<br /><br /> Konsoliderad inleverans-/leveransbokföring baserad på artikelinförsel-/plockregistreringar för distributionslager.|Distributionslagerinleverans/Distributionslager artikelinförsel/Distributionslagerplockning/Distributionslagerutleverans/Plockningskalkylark|GRÖN|Grundläggande lager/Distributionslager inleverans/Artikelinförsel/Plockning/Distributionslager utleverans|  
|5|Avancerad distributionslageraktivitet, för flera order.<br /><br /> Konsoliderad inleverans-/leveransbokföring baserad på artikelinförsel-/plockregistreringar för distributionslager.<br /><br /> Lagerställeskoden krävs.|Distributionslagerinleverans/Distributionslager artikelinförsel/Distributionslagerplockning/Distributionslagerutleverans/Plockningskalkylark/Artikelinförselkalkylark, men lagerställeskod|(GRÖN + Lagerplats obligatorisk)|Grundläggande lager/Lagerplats/Distributionslager inleverans/Artikelinförsel/Plockning/Distributionslager utleverans|  
|6 <br /><br /> **Obs!** Den här nivån kallas för "WMS”,eftersom den kräver den mest avancerade underavdelningen, lagerledningsystem (Warehouse Management Systems).|Avancerad distributionslageraktivitet för flera order<br /><br /> Konsoliderad inleverans-/utleveransbokföring baserad på artikelinförsels-/plockregistreringar<br /><br /> Lagerställeskoden krävs.<br /><br /> Kod för zon/klass är valfritt.<br /><br /> Lagerarbetare som styrs av arbetsflödet<br /><br /> Återanskaffningsplan för binge<br /><br /> Lagerplatsordning<br /><br /> Konfiguration för binge efter kapacitet<br /><br /> Skapa luckor <!-- Hand-held device integration -->|Distributionslagerinleverans/Distributionslager artikelinförsel/Distributionslagerplockning/Dist.lager transport/Plockningskalkylark/Artikelinförsel kalkylark/Intern dist.lager plockning /intern artikelinförsel, med lagerplats/klass/zonkod<br /><br /> Olika kalkylark för lagerplatshantering<br /><br /> ADCS-skärmar|VIT|Grundläggande lager/Lagerplats/Artikelinförsel/Inleverans för distr.lager/Plock/Utleverans för distr.lager/Administreringssystem för lager/Internt plock och artikelinförsel/Lagerplatsinställning<!-- Automated Data Capture System/ -->Lagerplatsinställning|  

Se [Designdetaljer: inkommande distributionslagerflöde](design-details-inbound-warehouse-flow.md) för exempel på hur användargränssnittsdokumenten används per lagerkomplexitetsnivå.  

## Lagerplats och lagerställesinnehåll

En lagerplats är en lagringsenhet som har utformats för att innehålla åtskilda delar. Det är den minsta behållarenheten i [!INCLUDE[prod_short](includes/prod_short.md)]. Antalet artiklar på lagerställen kallas för lagerställesinnehåll. En sökning från fältet **Artikel** eller fältet **Lagerställeskod** i ett distributionslagerrelaterat dokument visar den beräknade tillgängligheten av artikeln på lagerstället.  

Ett lagerställesinnehåll kan få egenskapen Fast, Dedikerad eller Standard för att definiera hur lagerställesinnehåll kan användas. Lagerställen utan dessa egenskaper kallas för flytande lagerställen.  

En fast lagerplats innehåller artiklar som har tilldelats till lagerställeskoden i fråga. Egenskapen Fast lagerplats garanterar att även om lagerställesinnehållet tillfälligt är tomt försvinner inte lagerställesinnehållet, och lagerstället väljs därför igen så snart den har fyllts på.  

En dedikerad lagerplats med lagerställesinnehåll som bara kan plockas för dedikerad resurs, till exempel en maskingrupp, som använder lagerstället i fråga. Annat icke-plockningsinnehåll, t.ex antal som är utgående på en leveransbokföring, kan fortfarande förbrukas från en dedikerad lagerplats. Endast lagerställesinnehåll som beaktas av algoritmen **Skapa plockning** skyddas i en dedikerad lagerplats.  

Egenskapen Standardlagerplats används i systemet för att föreslå lagerställen för distributionslageraktiviteter. Vid WMS-lagerställen används inte egenskapen Standardlagerplats. På lagerställen där lagerställen krävs används egenskapen i inkommande flöden för att ange var artiklar ska placeras. I utgående arbetsflöden används egenskapen för att ange varifrån artiklar ska hämtas.  

> [!NOTE]  
>  Om de utgående artiklarna placeras på flera lagerställen hämtas artiklar först från lagerställena som inte är standard, för att tomma dessa lagerställen, och sedan hämtas återstående artiklar från standardlagerstället.  

Det kan bara finnas en standardlagerplats per artikel per lagerställe.  

## Lagerplatstyp

I WMS-installationer kan du begränsa distributionslageraktiviteter som tillåts för en lagerplats genom tilldela en lagerplatstyp till den. Följande typer av lagerställen förekommer:  

|Lagerplatstyp|Beskrivning|  
|------------------|---------------------------------------|  
|INLEVNS|Artiklar som har bokförts som inleveranser, men som ännu inte har förts in.|  
|UTLEVNS|Artiklar som har plockats till utleveransrader, men som ännu inte har bokförts som levererade.|  
|ARTIKELINFÖRSEL|Artiklar som normalt ska lagras i stora enheter, men som du inte vill att programmet ska använda vid plockning. Eftersom de här lagerställena inte används för plockning, varken för produktionsorder eller utleveranser, kan användningen av en lagerplats av typen Artikelinförsel vara begränsad, men den är användbar om du har köpt ett stort antal artiklar. Lagerställen av den här typen bör alltid ha en låg lagerplatsordning, så att när mottagna artiklar förs in, görs det först med andra högprioriterade ARTINFPLOC-lagerställen som är kopplade till artikeln. Om du använder den här typen av lagerplats måste du regelbundet utföra återanskaffningar för lagerstället, så att de artiklar som lagras där också är tillgängliga på lagerställen av typen ARTINFPLOC och PLOCKA.|  
|PLOCKA|Artikel som endast ska användas för plockning. Återanskaffningen för de här lagerställena kan bara utföras med transport, inte av artikelinförsel.|  
|ARTINFPLOC|Artiklar på lagerställen som föreslås för både artikelinförsel- och plockningsfunktioner. Lagerställen av den här typen har förmodligen olika lagerplatsordning. Du kan skapa volymlagerställen av den här typen med låg lagerplatsordning jämfört med de vanliga plocklagerställena eller lagerställena för framåtplockning.|  
|KS|Den här lagerstället används för lagerjusteringar om du anger lagerstället i fältet **Justering lagerställeskod** på lagerställekortet. Du kan även skapa lagerställen av den här typen för felaktiga artiklar och artiklar om ska kontrolleras. Du kan flytta artiklar till den här lagerplatstypen om du vill isolera dem från det vanliga artikelflödet. **OBS:**  Till skillnad från andra lagerplatstyper har **KS** lagerplatstypen inga av artikelhanteringskryssrutorna markerade som standard. Det betyder att lagerställesinnehåll som du placerar i en KS lagerplats undantas från artikelflöden.|  

För alla lagerställen utom PLOCKA, ARTINFPLOC och ARTINFÖRS tillåts inga andra aktivitet för lagerstället än vad som definieras av dess lagerplatstyp. En lagerplats av typen **Inleverera** kan endast användas för att ta emot artiklar i eller plocka artiklar från.  

> [!NOTE]  
> Endast transport kan göras på lagerställen av typen INLEVERERA och KS. På liknande sätt kan endast transport göras från lagerställen av typen LEVERERA och KS.  

## Lagerplatsordning

I avancerad lagerhantering kan du automatisera och optimera hur artiklar samlas i artikelinförsel- och plockningskalkylark genom att ranka lagerställen så att artiklar föreslås tagna eller placerade enligt rankningsvillkor för att använda lagerutrymmet optimalt.  

Artikelinförselprocesser optimeras enligt lagerplatsrang, genom att föreslå lagerställen med högre rang före lagerställen med lägre rang. På liknande sätt optimeras plockprocesser genom att först föreslå artiklar från lagerställesinnehåll med höga lagerplatsrang. Dessutom föreslås lagerplatspåfyllningar från lägre till högre rankade lagerställen.  

Lagerplatsordningen tillsammans med information om lagerställesinnehåll är de grundläggande egenskaper som gör att användare kan placera artiklar i distributionslagret.  

## Lagerplatsinställning  
I avancerade distributionslagerfunktioner kan lagerställen ställas in med kapacitetsvärden, t.ex antal, total volym och vikt för att kontrollera vilka och hur artiklar lagerförs på lagerstället.  

På varje artikelkort kan du ange en enhet (UOM) för artikeln, t.ex stycken, pallar, liter, gram eller lådor. Du kan också välja basenhet för en artikel och ange större enheter som baseras på den. Du kan till exempel ange att en lastpall motsvarar 16 enheter, där den sistnämnda är basenheten.  

Om du vill ange ett maximal antal av en viss artikel som ska lagras på en enskild lagerplats, och artikeln har fler än en enhetskod, måste du ange det maximala antalet för varje enhetskod som finns på artikelkortet. Om en artikel har ställts in för att hanteras i stycken och pallar måste fältet **Max. ant.** på sidan **Lagerställesinnehåll** för artikeln också vara i stycken och pallar. Annars beräknas det tillåtna antalet lagerstället inte korrekt.  

Om du har angett kapacitetsbegränsningar för lagerställesinnehåll för en lagerplats, måste du först kontrollera att artikelns enhet och mått har ställts in på artikelkortet.  

> [!NOTE]  
> Det är endast möjligt att arbeta med flera enhetskoder i WMS-installationer. I alla andra konfigurationer kan lagerställesinnehåll endast kan vara basenheten. I alla transaktioner med en enhetskod som är större än artikelns basenhet konverteras antalet till basenheten.  

## Zon

I avancerade lagerhantering kan lagerställen grupperas i zoner för att hantera hur arbetsflödet med lageraktiviteter dirigeras.  

En zon kan vara en inleveranszon eller en lagerhållningszon, och varje zon kan bestå av en eller flera lagerställen.  

De flesta egenskaper som har kopplats till en zon ska tilldelas som standard på den lagerplats som skapas från zonen.  

## Klass  
I avancerad lagerhantering kan du tilldela klasskoder för distributionslager till artiklar, lagerställen och zoner för att kontrollera var olika artikelklasser lagras, till exempel djupfrysta varor. Du kan dela en zon i flera distributionslagerklasser. Till exempel kan artiklar i inleveranszonen lagras som frysta, farliga eller en annan klass.  

När du arbetar med distributionslagerklasser och en leverans-/utleveranslagerplats som är standard, måste du manuellt fylla i de lämpliga lagerställena på inleverans- och utleveransraderna för distributionslagret.  

I inkommande arbetsflöden är klasskoden bara markerad på inkommande rader där artikelklasskoden inte stämmer med standardlagerstället för inleveranser. Om rätt standardlagerställen inte har kopplats kan antalet som inte har inlevereras.  

## Lagerställe

Ett lagerställe är en fysisk struktur eller en plats där lagret tas emot, lagras och skickas, potentiellt organiserat i lagerställen. Ett lagerställe kan vara ett distributionslager, en servicebil, en visningslokal, en fabrik eller ett område i en fabrik.  

## First Expiry First Out

Om du markerar kryssrutan **Plocka enligt FEFO** på snabbfliken **Lagerplatsprinciper** på lagerställekortet plockas artikelspårade artiklar plockas utifrån sina utgångsdatum. Artiklarna med de tidigaste förfallodatumen plockas först.  

Distributionslageraktiviteter i alla plock- och transportdokument sorteras enligt FEFO, om inte artiklarna i fråga är tilldelade serie-/partinummer. Om endast en del av antalet på raden redan har parti- eller serienummer tilldelade, sorteras det återstående antalet som ska plockas enligt FEFO.  

När du plockar med FEFO kommer de tillgängliga artiklarna som förfaller först att samlas i en tillfällig artikelspårninglista baserat på förfallodatumet. Om två artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie – eller partinummer först. Om serie- eller partinummer är samma, väljs först den artikel som registrerades först. Standardvillkor för att välja artiklar i plocklagerställen, till exempel lagerplatsordning och enhetsbrytning, som kopplas till den tillfälliga FEFO-artikelspårninglistan.  

## Artikelinförselmall

Artikelinförselmallen kan tilldelas en artikel och till ett lagerställe. Artikelinförselmallen anger en uppsättning prioriterade regler som måste respekteras när du vill skapa artikelinförslar. Artikelinförselmallen kan till exempel kräva att artikeln placeras på en lagerplats med lagerställesinnehåll som matchar enheten, och om en liknande lagerplats med tillräckligt med kapacitet inte kan hittas måste artikeln placeras i en tom lagerplats.  

## Se även

[Warehouse Management – översikt](design-details-warehouse-management.md)
[Designdetaljer: tillgänglighet i distributionslagret](design-details-availability-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]