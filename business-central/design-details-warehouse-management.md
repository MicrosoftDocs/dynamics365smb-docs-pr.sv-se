---
title: Hantera lageraktiviteter
description: Förutom inleveranser och utleveranser stöder Business Central en serie interna lageraktiviteter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/13/2023
ms.custom: bap-template
---

# Översikt över hantering av distributionslager

Det finns två saker som är viktiga för alla företag som fysiskt flyttar varor till och från sitt distributionslager.

* De har en översikt över lagernivåer och artikelplacering i distributionslagret.
* De kan snabbt och korrekt ta emot, plocka och leverera artiklar.

För att hjälpa företag uppnår dessa saker, lägger distributionslagerfunktioner i [!INCLUDE[prod_short](includes/prod_short.md)] till följande möjligheter till lagerhantering:

* Lagerställen
* Utleveranser från distributionslager
* Lagerplockningar
* Transportförslag

Implementera dessa funktioner i olika kombinationer för att skräddarsy dina distributionslagerprocesser i företaget. Möjliggör en ökad komplexitet när företaget växer och processerna ändras.

## Översikt över olika konfigurationsalternativ

Du kan konfigurera distributionslagerfunktioner på olika sätt. Det är viktigt att du väljer en förbättring av dina processer utan att orsaka omkostnader. I tabellen nedan finns en översikt över typiska konfigurationer som används vid hantering av fysiska varor.

|Komplexitetsnivå|Description|Inställningar|Lagerställeskod|Exempel på inkommande flöde|Exempel på utgående flöde|Exempel på internt flöde|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Ingen tilldelad distributionslageraktivitet.|Bokför från order och journaler.||Valfritt. Kontrolleras av växlingsknappen **Lagerställeskod är obligatorisk**.|Inköpsorder|Försäljningsorder| Produktionsorder -> förbrukningsjournal|  
|Grundläggande|Konsoliderad inleverans-/utleveransbokföring för flera order.|**Begär inleverans**<br>**Begär utleverans**.|Valfritt. Kontrolleras av växlingsknappen Lagerställeskod är obligatorisk|Inköpsorder -> Dist.lager inleverans|Försäljningsorder -> Distributionslagerutleverans|Samma som ovan.|
|Grundläggande|Order för order.|Kräver artikelinförsel eller Kräver plockning. </br><br/> **Obs**! Även om inställningarna kallas **Begär plockning** och **Begär artikelinförsel** kan du fortfarande bokföra inleveranser och utleveranser direkt från källdokument på platser där du markerar dessa kryssrutor.|Valfritt. Kontrolleras av växlingsknappen **Lagerställeskod är obligatorisk**.|Inköpsorder -> Lager, artikelinförsel|Försäljningsorder -> Lagerplockning|Produktionsorder -> Lagerplockning|
|Avancerat|Konsoliderad inleverans-/utleveransbokföring för flera order.<br /><br />Konsoliderade aktiviteter för plockning/artikelnförsel för flera källdokument.|Kräver inleverans + Kräver artikelinförsel,</br> Begär utleverans + begär plockning|Valfritt. Kontrolleras av växlingsknappen Lagerställeskod är obligatorisk|Inköpsorder -> Dist.lager inleverans -> Dist.lager artikelinförsel|Försäljningsorder -> Distributionslagerutleverans -> Plockningskalkylark -> Lagerplockningar| Produktionsorder -> Plockningskalkylark -> Lagerplockningar -> Förbrukningsjournal|
|Avancerat|Samma som ovan + Dirigerad art.inf. och plock. aktiviteter|Dirigerad art.inf. och plock. (beroende växlingar aktiveras automatiskt)|Obligatoriskt|Samma som ovan.|Samma som ovan.| Produktionsorder -> Plockningskalkylark -> Lagerplockningar -> Förbrukningsjournal|

Komplexiteten ökar med företagets storlek och hur många avdelningar och människor som är inblandade. En process kan vara enkel, till exempel när samma person skapar och bokför ett försäljningsdokument. Processer kan också vara mer komplicerade och innefatta flera steg och personer. Följande steg är ett exempel på en mer komplex procedur:

1. Orderhandläggare skapar en försäljningsorder.
1. En lagerchef skapar plockningsinstruktioner.
1. En lagerpersonal avslutar flödet genom att bokföra distributionslagerutleveransen.

Komplexitetsnivån påverkas också av de dokumenttyper som du använder i distributionslagrets aktiviteter. Du kan till exempel använda dokument för distributionslagerinleveransen och dist.lager artikelinförsel för det inkommande flödet, men använda lagerplockningsdokument för det utgående flödet.

En annan faktor som påverkar komplexitet är hur ditt fysiska lagerställe visas i [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer på [Modellering av det fysiska lagerstället](#modeling-the-physical-warehouse).

## Modellering av det fysiska lagerstället

Det finns flera alternativ för att representera den verkliga inställningen av distributionslagret i [!INCLUDE[prod_short](includes/prod_short.md)]. Dina val bestämmer hur du ska arbeta med distributionslagerfunktioner.

Placeringen av artiklar kan vara hyllor, lagerställen eller lagerplatser och det finns fördelar och nackdelar för varje alternativ.

### Lagerställen och lagerplatser

För att kunna hantera fysiska varor måste du ha minst ett lagerställe. Du kan använda flera lagerställen eller använda lagerplatser för att modellera distributionslagret och organisationsstrukturen.

Lagerställen är vanligtvis det bästa sättet att organisera åtgärder som är distribuerade över olika geografiska områden. I vissa fall kanske du vill skapa flera lagerställen som ligger på samma plats. Att använda lagerställen har följande fördelar:

* Bevilja åtkomst med hjälp av sidorna **Distributionslagerpersonal** och **Ansvarsenheter**.
* Definiera kalendrar, verksamhetsföljder och ankommande och avgående hanteringstider för datumberäkning och planering. Läs mer på [Om planeringsfunktionen](production-about-planning-functionality.md).
* Ange standarddimensioner och använd olika lagerbokföringsinställningar.
* Ange planeringsparametrar. Läs mer i [planeringsparametrar](production-about-planning-functionality.md#planning-parameters).  
* Använd olika funktioner för distributionslager för varje lagerställe.

### Hyllor och lagerplatser

Om du alltid lagrar en artikel på samma plats kan du använda fältet **hyllnummer.** på **Artikelkortet** eller **Lagerställeenhetskort**. Detta fält kan användas som ett grundläggande manuellt lagringssystem i miljöer utan lagerplatser. Fältets värde kopieras från artikelkortet till dokumentrader och rapporter, men det är endast information. Värdet används inte i distributionslageraktiviteter eller vid beräkningar av tillgänglighet.

Lagerställen representerar den grundläggande lagerstrukturen och används för att lägga förslag om artiklarnas specifika placering av artiklar:

* En eller flera fasta lagerplatser för en artikel.
* Lagerplatser för specifika åtgärder, till exempel utleveranslagerplats eller produktionsutflödets lagerplats.
* Lagerplatskapacitet och viktbegränsningar (endast för dirigerad artikelinförsel och plockning).
* Klassificering av lagerplats (för dirigerad artikelinförsel och plockning).

## Vanligt arbetsflöde för distributionslager

I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.

|**Om du vill**|**Se**|  
|------------|-------------|  
|I ett grundläggande flöde på en order-för-order-basis, använd en lagerinförsel för att registrera inleverans av artiklar på lagerställen, inklusive eventuella överinleverans. Om du konsoliderar flera order i inleveransen ska du använda en distributionslagerinleverans.|[inkommande flöde](design-details-inbound-warehouse-flow.md)|
|Registrera leverans av artiklar från lagerställen. Vid orderbasis använder du en lagerplockning. Om du konsoliderar flera order i utleverans ska du använda en distributionslagerutleverans.|[utgående flöde](design-details-outbound-warehouse-flow.md)|
|Hantera artiklar på distributionslagerstället. Exempelvis flyttar du komponenter till produktionen eller utför en inventering.|[Internt flöde](design-details-internal-warehouse-flows.md)|

Ställ in de lagerprocesser som är rätt för ditt företag. Läs mer på [Ställa in lagerstyrning](warehouse-setup-warehouse.md).

## Terminologi relaterad till Warehouse Management

### Komplexitetsnivåer

Vi använder termerna grundläggande och avancerad för att skilja mellan olika nivåer av komplexitet. Denna enkla differentiering täcker flera nivåer av komplexitet i lagerställekonfigurationen, var och en stöds av olika distributionslagerdokument. Den mest avancerade lager nivån kallas för "dirigerad artikelinförsel och plockning". Om du vill använda dirigerad artikelinförsel och plockning för en plats, aktivera växlingsknappen **dirigerad artikelinförsel och plockning** på sidan **Lagerställekort**.

### Distributionslagerflöden

* Inkommande flöde – Flytta artiklar i till distributionslagerstället och göra dem tillgängliga, till exempel inköp och inkommande överföringar.
* Utgående flöde – Plocka och utleverera artiklar till kunder eller andra lagerställen.
* Internt flöde – Hantera artiklar på ett lagerställe. Exempelvis flytta komponenter till produktionen eller utföra en inventering.

### Grundläggande dokument  

Följande dokument används i grundläggande distributionslagerflöden.

* Lagerinförsel
* Lagerplockning
* Lagertransport
* Artikeljournal
* Artikelgrupperingsjournal

### Avancerade dokument  

Följande dokument används i avancerade distributionslagerflöden.

* Dist.lager inleverans
* Artikelinförsel kalkylark
* Dist.lager artikelinförsel
* Plockningskalkylark
* Dist.lager plockning
* Transportkalkylark
* Dist.lager transport
* Interna plockningar för distributionslager
* Interna artikelinförslar för distributionslager
* lagerplatsuppläggningskalkylark
* Lagerställesinnehålluppl kalkylark
* Artikeljournal för distributionslager
* Distributionslagrets artikelgrupperingsjournal

### Sidor och inställningar

I det här avsnittet beskrivs begreppen bakom nyckelsidorna och lagerinställningarna.

#### Lagerplatser och lagerplatsinnehåll

En lagerplats är en lagringsenhet som har utformats för att innehålla åtskilda delar. Det är den minsta behållarenheten i [!INCLUDE[prod_short](includes/prod_short.md)]. Antalet artiklar på lagerplatser kallas för *lagerplatsinnehåll*. En sökning från fältet **Artikel** eller fältet **Lagerställeskod** i ett distributionslagerrelaterat dokument visar den beräknade tillgängligheten av artikeln på lagerstället.  

Lagerplatsinnehåll kan få egenskapen **Fast**, **Dedikerad** eller **Standard** för att definiera hur lagerplatsinnehåll kan användas. Lagerplatser utan dessa egenskaper kallas för *flytande* lagerplatser.  

En fast lagerplats innehåller artiklar som har tilldelats till lagerplatskoden. Egenskapen fast lagerplats gör att lagerplatsinnehållet inte försvinner även om lagerplatsen töms. Du kan välja lagerplatsen igen så snart innehållet har återanskaffas.  

En dedikerad lagerplats med lagerplatsinnehåll som bara kan plockas för dedikerad resurs som använder lagerplatsen. Till exempel en maskingrupp. Annat icke-plockningsinnehåll, t.ex. avgående antal på en leveransbokföring, kan förbrukas från en dedikerad lagerplats. Endast lagerställesinnehåll som beaktas av algoritmen **Skapa plockning** skyddas i en dedikerad lagerplats.  

[!INCLUDE [prod_short](includes/prod_short.md)] använder lagerplatsegenskapen **Standard** för att föreslå lagerställen för distributionslageraktiviteter. På lagerställen som använder dirigerad artikelinförsel och plockning används inte egenskapen standardlagerplats. På lagerställen där lagerställen krävs anger egenskapen var artiklar ska placeras i inkommande flöden. I utgående arbetsflöden anger egenskapen varifrån artiklar ska hämtas.  

> [!NOTE]  
> Om de utgående artiklarna placeras på flera lagerställen hämtas artiklar först från lagerställena som inte är standard, för att tomma dessa lagerställen, och sedan hämtas återstående artiklar från standardlagerstället.  

Du kan ha en standardlagerplats per artikel per lagerställe.  

#### Lagerplatstyp

Lagerställen som använder dirigerad artikelinförsel och plockning kan använda lagerplatstyper. Lagerplatstyper styr de aktiviteter som du tillåter för en lagerplats. 

Följande typer av lagerplatser finns tillgängliga:  

|Lagerplatstyp|Beskrivning|  
|------------------|---------------------------------------|  
|INLEVNS|Artiklar som har inlevererats men inte förts in.|  
|LEVERERA|Artiklar som har plockats till utleveransrader, men som inte har bokförts som levererade.|  
|ARTIKELINFÖRSEL|Artiklar som normalt ska lagras i stora enheter, men som du inte vill att programmet ska använda vid plockning. Dessa lagerplatser används inte för plockning, antingen för produktionsorder eller leveranser, så deras användning kan vara begränsad. Den här typen av lagerplats är användbar när du köper ett stort antal artiklar. Lagerplatserna ska alltid ha en låg lagerplatsordning så att artiklar med ARTINFPLOC lagerplatser med högre rangordning förs in först. Regelbundet återanskaffa den här typen av lagerplats så att deras artiklar blir tillgängliga i ARTINFPLOC eller PLOCK lagerplatser.|  
|PLOCKNING|Artikel som endast ska användas för plockning. Du kan endast använda transport för återanskaffning av de här lagerplatserna, inte artikelinförsel.|  
|ARTINFPLOC|Artiklar på lagerplatser som föreslås för både artikelinförsel och plockning. Lagerställen av den här typen har förmodligen olika lagerplatsordning. Ställ in volymlagerplatser med lägre lagerplatsordning än de vanliga plocklagerplatser eller lagerplatser för framåtplockning.|  
|KS|Den här lagerstället används för lagerjusteringar om du anger lagerstället i fältet **Justering lagerställeskod** på lagerställekortet. Du kan även skapa lagerställen av den här typen för felaktiga artiklar och artiklar om ska kontrolleras. Du kan flytta artiklar till den här lagerplatstypen om du vill isolera dem från det vanliga artikelflödet. **Obs!** Till skillnad från andra lagerplatstyper har lagerplatstypen **KS** inga av kryssrutorna för artikelhantering markerade som standard. Innehåll du placerar i en KS lagerplats undantas från artikelflöden.|  

Du kan använda alla åtta olika lagerplatstyperna i distributionslagret, eller välja att endast använda lagerplatstyperna INLEVERERA, ARTINFPLOC, LEVERERA och KS. De här fyra lagerplatstyperna aktiverar förslag på hur artikelflödet ska se ut och du kan även registrera lageravvikelser.
Med undantag av lagerplatstyperna PLOCKA, ARTINFPLOC och ARTINFÖRS, definierar lagerplatstypen den aktivitet som tillåts för en lagerplats. Du kan till exempel bara använda en lagerplats av typen INLEVNS för att inleverera artiklar eller plocka artiklar från.  

> [!NOTE]  
> Du måste använda transport för att flytta artiklar till lagerplatserna INLEVNS och KS, använd transport för att flytta artiklar från lagerplatserna UTLEVNS och KS.  

#### Lagerplatsordning

I avancerad lagerhantering kan du automatisera och optimera hur artiklar samlas i artikelinförsel- och plockningskalkylark genom att ranka lagerplatser. Artiklar föreslås för plockningar och införsel baserat på lagerplatsordning.

Artikelinförselprocesser optimeras enligt lagerplatsordning, genom att föreslå lagerplatser med högre rang före lägre rankade lagerplatser. Plockningsprocesserna förslår artiklar med högsta lagerplatsordning lagerställesinnehåll först. Lagerplatspåfyllningar föreslår lägre rankade lagerplatser före högre rankade lagerplatser.  

Lagerplatsordning och lagerplatsinnehåll är de grundläggande egenskaper som guidar lagerpersonalen i distributionslagret.  

#### Lagerplatsinställning

I avancerad lagerstyrning kan du ange följande kapacitetsvärden för att styra hur och på vilka lagerplatser du lagrar artiklar:

* Antal
* Total volym
* Vikt  

Du kan tilldela en basenhet (UOM) för artiklar. En basenhet kan vara stycken, lastpallar, liter, gram eller lådor. Du kan också skapa större UOM baserat på basenheten. Om t.ex. stycken är basenheten kan en lastpall vara lika med 16 enheter.  

Om en artikel har mer än en basenhet anger du det högsta antalet för varje basenhet på artikelkortet. Om en artikel har ställts in för att hanteras i stycken och pallar måste fältet **Max. ant.** på sidan **Lagerplatsinnehåll** för artikeln också vara i stycken och pallar. Annars beräknas det tillåtna antalet lagerstället inte korrekt.  

Om du har angett kapacitetsbegränsningar för lagerställesinnehåll för en lagerplats, måste du kontrollera att artikelns enhet och mått har ställts in på artikelkortet.  

> [!NOTE]  
> Du kan bara använda flera basenheter på lagerställen som använder dirigerad artikelinförsel och plockning. I alla andra konfigurationer kan du endast använda lagerplatsinnehåll i basenheten. I alla transaktioner med en basenhet som är större än artikelns basenhet konverteras antalet till basenheten.  

#### Zon

I avancerad lagerhantering kan lagerplatser grupperas i zoner för att hantera hur arbetsflödet med lageraktiviteter dirigeras för lagerställen.  

En zon kan vara en inleveranszon eller en lagerhållningszon, och varje zon kan bestå av en eller flera lagerställen.  

De flesta egenskaper som har kopplats till en zon ska tilldelas de lagerställen som skapas för zonen.  

#### Dist.lagerklass

I avancerad lagerhantering kan du tilldela klasskoder för distributionslager för följande entiteter: 

* Artiklar
* Lagerställen
* Zoner

Klasskoder för distributionslager styr var artiklarna ska lagras. Du kan dela en zon i flera distributionslagerklasser. Du kan till exempel lagra artiklar i inleveranszonen som frysta, farliga eller en annan klass.

När du arbetar med distributionslagerklasser och en leverans-/utleveranslagerplats som är standard, måste du manuellt välja de lämpliga lagerplatserna på inleverans- och utleveransraderna för distributionslagret.  

I inkommande arbetsflöden är klasskoden bara markerad på inkommande rader där artikelklasskoden inte stämmer med standardlagerstället för inleveranser. Om rätt standardlagerställen inte har kopplats kan antalet som inte har inlevereras.  

#### Plats

En plats är en fysisk struktur eller plats där lager tas emot, lagras och levereras. Ett lagerställe kan vara ett distributionslager, en servicebil, en visningslokal, en anläggning eller ett område i en anläggning. Lagret är ofta organiserat i lagerplatser och zoner.

#### First Expiry First Out

Om du markerar kryssrutan **Plocka enligt FEFO** på snabbfliken **Lagerplatsprinciper** på sidan **Lagerställekort** plockas spårade artiklar på lagerstället enligt deras utgångsdatum. Artiklar med de tidigaste förfallodatumen plockas först.  

Distributionslageraktiviteter i alla plock- och transportdokument sorteras enligt FEFO, om inte artiklarna är tilldelade serie- eller partinummer. Om en del, men inte allt av antalet på raden har parti- eller serienummer tilldelade, sorteras det återstående antalet enligt FEFO.  

När du plockar med FEFO kommer artiklarna som förfaller först att samlas i en tillfällig artikelspårninglista baserat på förfallodatumet. Om två artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie – eller partinummer först. Om serie- eller partinummer är samma, väljs först den artikel som registrerades först. Standardvillkor för att välja artiklar i plocklagerställen, till exempel lagerplatsordning och enhetsbrytning, som kopplas till den tillfälliga FEFO-artikelspårninglistan.  

#### Artikelinförselmall

Artikelinförselmallen anger en uppsättning prioriterade regler som gäller när du skapar artikelinförslar. En artikelinförselmall kan till exempel kräva att du placerar artiklar på en lagerplats med lagerplatsinnehåll som har samma basenhet. Om en liknande lagerplats med tillräcklig kapacitet inte kan hittas måste artikeln placeras på en tom lagerplats. Du tilldelar en artikelinförselmall till en artikel och ett lagerställe.  

## Se även

[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
