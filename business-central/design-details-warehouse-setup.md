---
title: "Designdetaljer - Lagerstyrningsinställning | Microsoft Docs"
description: "Distributionslagerfunktion i Business Central innehåller olika nivåer av komplexitet enligt definitionen av licensbehörigheter i de erbjudna partiklarna. Nivån av komplexitet i en lagerlösning definieras i hög grad av den lagerplatsinställningen på lagerställekort, som i sin tur är licenskontrollerat så att åtkomsten till inställningsfält för lagerplatsen definieras av licensen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: ff625189c5004f682f45fe1c1796ba6afe2e7fdb
ms.contentlocale: sv-se
ms.lasthandoff: 08/06/2018

---
# <a name="design-details-warehouse-setup"></a>Designdetaljer: Lagerstyrningsinställningar
Distributionslagerfunktion i [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller olika nivåer av komplexitet, enligt definitionen av licensbehörigheter i de offererade partiklarna. Nivån av komplexitet i en lagerlösning definieras i hög grad av den lagerplatsinställningen på lagerställekort, som i sin tur är licenskontrollerat så att åtkomsten till inställningsfält för lagerplatsen definieras av licensen. Dessutom ska kopplingsobjekten i licensen styra vilka användargränssnittsdokument som ska användas för de distributionslageraktiviteter som stöds.  

Följande lagerrelaterade partiklar finns:  

-   Grundläggande lager (4010)  
-   Lagerplats (4170)  
-   Artikelinförsel (4180)  
-   Dist.lager inleverans (4190)  
-   Plockning (4200)  
-   Distributionslagerutleverans (4210)  
-   Lagerstyrningssystem (4620)  
-   Intern plockning och artikelinförsel (4630)  
-   <!-- Automated Data Capture System (4640) -->  
-   Lagerplatsinställning (4660)  

Läs mer om varje partikel i [[!INCLUDE[d365fin](includes/d365fin_md.md)] prislistor](http://go.microsoft.com/fwlink/?LinkId=238341) (kräver ett PartnerSource-konto).  

Efterföljande tabell visar vilka partiklar som krävs för att definiera olika komplexitetsnivåer för distributionslager, vilka användargränssnittsdokument som stöder varje nivå och vilka lagerställekoder som avspeglar dessa nivåer i [!INCLUDE[d365fin](includes/d365fin_md.md)]-demonstrationsdatabas.  

|Komplexitetsnivå|Beskrivning|Användargränssnittsdokument|CRONUS-plats|Lägsta partikelkrav|  
|----------------------|---------------------------------------|-----------------|---------------------------------|---------------------------------|  
|1|Ingen tilldelad distributionslageraktivitet.<br /><br /> Ta emot/leverera från order.|Order|BLÅ|Grundläggande lager|  
|2|Ingen tilldelad distributionslageraktivitet.<br /><br /> Ta emot/leverera från order.<br /><br /> Lagerplatskoden krävs.|Order med lagerplatskod|SILVER|Grundläggande lager/Lagerplats|  
|3 <br /><br /> **Observera**: även om inställningarna kallas **Begär plockning** och **Begär artikelinförsel** kan du fortfarande bokföra inleveranser och utleveranser direkt från affärskälldokument på platser där du markerar dessa kryssrutor.|Grundläggande distributionslageraktivitet, en order i taget.<br /><br /> Ta emot/leverera bokföring från lagerartikelinförsel/plockdokument. <br /><br /> Lagerplatskoden krävs.|Lagerartikelinförsel/lagerförflyttning/lagerplockning med lagerplatskod|(SILVER + Kräver artikelinförsel eller Kräver artikelinförsel)|Grundläggande lager/Lagerplats/Artikelinförsel/Plockning|  
|4|Avancerad distributionslageraktivitet, för flera order.<br /><br /> Konsoliderad inleverans-/leveransbokföring baserad på artikelinförsel-/plockregistreringar för distributionslager.|Distributionslagerinleverans/Distributionslager artikelinförsel/Distributionslagerplockning/Distributionslagerutleverans/Plockningskalkylark|GRÖN|Grundläggande lager/Distributionslager inleverans/Artikelinförsel/Plockning/Distributionslager utleverans|  
|5|Avancerad distributionslageraktivitet, för flera order.<br /><br /> Konsoliderad inleverans-/leveransbokföring baserad på artikelinförsel-/plockregistreringar för distributionslager.<br /><br /> Lagerplatskoden krävs.|Distributionslagerinleverans/Distributionslager artikelinförsel/Distributionslagerplockning/Distributionslagerutleverans/Plockningskalkylark/Artikelinförselkalkylark, men lagerplatskod|(GRÖN + Lagerplats obligatorisk)|Grundläggande lager/Lagerplats/Distributionslager inleverans/Artikelinförsel/Plockning/Distributionslager utleverans|  
|6 <br /><br /> **Obs!** Den här nivån kallas för "WMS”, eftersom den kräver den mest avancerade partikeln, lagerledningsystem (Warehouse Management Systems).|Avancerad distributionslageraktivitet för flera order<br /><br /> Konsoliderad inleverans-/utleveransbokföring baserad på artikelinförsels-/plockregistreringar<br /><br /> Lagerplatskoden krävs.<br /><br /> Kod för zon/klass är valfritt.<br /><br /> Lagerarbetare som styrs av arbetsflödet<br /><br /> Återanskaffningsplan för binge<br /><br /> Lagerplatsordning<br /><br /> Konfiguration för binge efter kapacitet<br /><br /> Skapa luckor <!-- Hand-held device integration -->|Distributionslagerinleverans/Distributionslager artikelinförsel/Distributionslagerplockning/Dist.lager transport/Plockningskalkylark/Artikelinförsel kalkylark/Intern dist.lager plockning /intern artikelinförsel, med lagerplats/klass/zonkod<br /><br /> Olika förslag för administrering av bingar <!-- ADCS screens  -->|VIT|Grundläggande lager/Binge/Plats/Inleverans för distr.lager/Plock/Utleverans för distr.lager/Administreringssystem för lager/Internt plock och artikelinförsel/Konfiguration för bingar/<!-- Automated Data Capture System/ -->Konfiguration för bingar|  

Se [Designdetaljer: Ankommande distributionslagerflöde](design-details-outbound-warehouse-flow.md) för exempel på hur användargränssnittsdokumenten används per lagerkomplexitetsnivå.  

## <a name="bin-and-bin-content"></a>Lagerplats och lagerplatsinnehåll  
En lagerplats är en lagringsenhet som har utformats för att innehålla åtskilda delar. Det är den minsta behållarenheten i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Antalet artiklar på lagerplatser kallas för lagerplatsinnehåll. En sökning från fältet **Artikel** eller fältet **Lagerplatskod** i ett distributionslagerrelaterat dokument visar den beräknade tillgängligheten av artikeln på lagerplatsen.  

Ett lagerplatsinnehåll kan få egenskapen Fast, Dedikerad eller Standard för att definiera hur lagerplatsinnehåll kan användas. Lagerplatser utan dessa egenskaper kallas för flytande lagerplatser.  

En fast lagerplats innehåller artiklar som har tilldelats till lagerplatskoden i fråga. Egenskapen Fast lagerplats garanterar att även om lagerplatsinnehållet tillfälligt är tomt försvinner inte lagerplatsinnehållet, och lagerplatsen väljs därför igen så snart den har fyllts på.  

En dedikerad lagerplats med lagerplatsinnehåll som bara kan plockas för dedikerad resurs, till exempel en maskingrupp, som använder lagerplatsen i fråga. Annat icke-plockningsinnehåll, t.ex antal som är avgående på en leveransbokföring, kan fortfarande förbrukas från en dedikerad lagerplats. Endast lagerplatsinnehåll som beaktas av algoritmen **Skapa plockning** skyddas i en dedikerad lagerplats.  

Egenskapen Standardlagerplats används i systemet för att föreslå lagerplatser för distributionslageraktiviteter. Vid WMS-lagerställen används inte egenskapen Standardlagerplats. På lagerställen där lagerplatser krävs används egenskapen i ankommande flöden för att ange var artiklar ska placeras. I utgående arbetsflöden används egenskapen för att ange varifrån artiklar ska hämtas.  

> [!NOTE]  
>  Om de utgående artiklarna placeras på flera lagerplatser hämtas artiklar först från lagerplatserna som inte är standard, för att tomma dessa lagerplatser, och sedan hämtas återstående artiklar från standardlagerplatsen.  

Det kan bara finnas en standardlagerplats per artikel per lagerställe.  

## <a name="bin-type"></a>Lagerplatstyp  
I WMS-installationer kan du begränsa distributionslageraktiviteter som tillåts för en lagerplats genom tilldela en lagerplatstyp till den. Följande typer av lagerplatser förekommer:  

|Lagerplatstyp|Beskrivning|  
|------------------|---------------------------------------|  
|INLEVNS|Artiklar som har bokförts som inleveranser, men som ännu inte har förts in.|  
|UTLEVNS|Artiklar som har plockats till utleveransrader, men som ännu inte har bokförts som levererade.|  
|ARTIKELINFÖRSEL|Artiklar som normalt ska lagras i stora enheter, men som du inte vill att programmet ska använda vid plockning. Eftersom de här lagerplatserna inte används för plockning, varken för produktionsorder eller utleveranser, kan användningen av en lagerplats av typen Artikelinförsel vara begränsad, men den är användbar om du har köpt ett stort antal artiklar. Lagerplatser av den här typen bör alltid ha en låg lagerplatsordning, så att när mottagna artiklar förs in, görs det först med andra högprioriterade ARTINFPLOC-lagerplatser som är kopplade till artikeln. Om du använder den här typen av lagerplats måste du regelbundet utföra återanskaffningar för lagerplatsen, så att de artiklar som lagras där också är tillgängliga på lagerplatser av typen ARTINFPLOC och PLOCKA.|  
|PLOCKA|Artikel som endast ska användas för plockning. Återanskaffningen för de här lagerplatserna kan bara utföras med transport, inte av artikelinförsel.|  
|ARTINFPLOC|Artiklar på lagerplatser som föreslås för både artikelinförsel- och plockningsfunktioner. Lagerplatser av den här typen har förmodligen olika lagerplatsordning. Du kan skapa volymlagerplatser av den här typen med låg lagerplatsordning jämfört med de vanliga plocklagerplatserna eller lagerplatserna för framåtplockning.|  
|KS|Den här lagerplatsen används för lagerjusteringar om du anger lagerplatsen i fältet **Justering lagerplatskod** på lagerställekortet. Du kan även skapa lagerplatser av den här typen för felaktiga artiklar och artiklar om ska kontrolleras. Du kan flytta artiklar till den här lagerplatstypen om du vill isolera dem från det vanliga artikelflödet. **OBS:**  Till skillnad från andra lagerplatstyper har **KS** lagerplatstypen inga av artikelhanteringskryssrutorna markerade som standard. Det betyder att lagerplatsinnehåll som du placerar i en KS lagerplats undantas från artikelflöden.|  

För alla lagerplatser utom PLOCKA, ARTINFPLOC och ARTINFÖRS tillåts inga andra aktivitet för lagerplatsen än vad som definieras av dess lagerplatstyp. En lagerplats av typen **Inleverera** kan endast användas för att ta emot artiklar i eller plocka artiklar från.  

> [!NOTE]  
>  Endast transport kan göras på lagerplatser av typen INLEVERERA och KS. På liknande sätt kan endast transport göras från lagerplatser av typen LEVERERA och KS.  

## <a name="bin-ranking"></a>Lagerplatsordning  
I avancerad lagerhantering kan du automatisera och optimera hur artiklar samlas i artikelinförsel- och plockningskalkylark genom att ranka lagerplatser så att artiklar föreslås tagna eller placerade enligt rankningsvillkor för att använda lagerutrymmet optimalt.  

Artikelinförselprocesser optimeras enligt lagerplatsrang, genom att föreslå lagerplatser med högre rang före lagerplatser med lägre rang. På liknande sätt optimeras plockprocesser genom att först föreslå artiklar från lagerplatsinnehåll med höga lagerplatsrang. Dessutom föreslås lagerplatspåfyllningar från lägre till högre rankade lagerplatser.  

Lagerplatsordningen tillsammans med information om lagerplatsinnehåll är de grundläggande egenskaper som gör att användare kan placera artiklar i distributionslagret.  

## <a name="bin-setup"></a>Lagerplatsinställning  
I avancerade distributionslagerfunktioner kan lagerplatser ställas in med kapacitetsvärden, t.ex antal, total volym och vikt för att kontrollera vilka och hur artiklar lagerförs på lagerplatsen.  

På varje artikelkort kan du ange en enhet (UOM) för artikeln, t.ex stycken, pallar, liter, gram eller lådor. Du kan också välja basenhet för en artikel och ange större enheter som baseras på den. Du kan till exempel ange att en lastpall motsvarar 16 enheter, där den sistnämnda är basenheten.  

Om du vill ange ett maximal antal av en viss artikel som ska lagras på en enskild lagerplats, och artikeln har fler än en enhetskod, måste du ange det maximala antalet för varje enhetskod som finns på artikelkortet. Om en artikel har ställts in för att hanteras i stycken och pallar måste fältet **Max. ant.** i fönstret **Lagerplatsinnehåll** för artikeln också vara i stycken och pallar. Annars beräknas det tillåtna antalet lagerplatsen inte korrekt.  

Om du har angett kapacitetsbegränsningar för lagerplatsinnehåll för en lagerplats, måste du först kontrollera att artikelns enhet och mått har ställts in på artikelkortet.  

> [!NOTE]  
>  Det är endast möjligt att arbeta med flera enhetskoder i WMS-installationer. I alla andra konfigurationer kan lagerplatsinnehåll endast kan vara basenheten. I alla transaktioner med en enhetskod som är större än artikelns basenhet konverteras antalet till basenheten.  

## <a name="zone"></a>Zon  
I avancerade lagerhantering kan lagerplatser grupperas i zoner för att hantera hur arbetsflödet med lageraktiviteter dirigeras.  

En zon kan vara en inleveranszon eller en lagerhållningszon, och varje zon kan bestå av en eller flera lagerplatser.  

De flesta egenskaper som har kopplats till en zon ska tilldelas som standard på den lagerplats som skapas från zonen.  

## <a name="class"></a>Klass  
I avancerad lagerhantering kan du tilldela klasskoder för distributionslager till artiklar, lagerplatser och zoner för att kontrollera var olika artikelklasser lagras, till exempel djupfrysta varor. Du kan dela en zon i flera distributionslagerklasser. Till exempel kan artiklar i inleveranszonen lagras som frysta, farliga eller en annan klass.  

När du arbetar med distributionslagerklasser och en leverans-/utleveranslagerplats som är standard, måste du manuellt fylla i de lämpliga lagerplatserna på inleverans- och utleveransraderna för distributionslagret.  

I ankommande arbetsflöden är klasskoden bara markerad på ankommande rader där artikelklasskoden inte stämmer med standardlagerplatsen för inleveranser. Om rätt standardlagerplatser inte har kopplats kan antalet som inte har inlevereras.  

## <a name="location"></a>Lagerställe  
Ett lagerställe är en fysisk struktur eller en plats där lagret tas emot, lagras och skickas, potentiellt organiserat i lagerplatser. Ett lagerställe kan vara ett distributionslager, en servicebil, en visningslokal, en fabrik eller ett område i en fabrik.  

## <a name="first-expired-first-out"></a>First Expiry First Out  
Om du markerar kryssrutan **Plocka enligt FEFO** på snabbfliken **Lagerplatsprinciper** på lagerställekortet plockas artikelspårade artiklar plockas utifrån sina utgångsdatum. Artiklarna med de tidigaste förfallodatumen plockas först.  

Distributionslageraktiviteter i alla plock- och transportdokument sorteras enligt FEFO, om inte artiklarna i fråga är tilldelade serie-/partinummer. Om endast en del av antalet på raden redan har parti- eller serienummer tilldelade, sorteras det återstående antalet som ska plockas enligt FEFO.  

När du plockar med FEFO kommer de tillgängliga artiklarna som förfaller först att samlas i en tillfällig artikelspårninglista baserat på förfallodatumet. Om två artiklar har samma utgångsdatum, väljs artikeln med det lägsta serie - eller partinummer först. Om serie- eller partinummer är samma, väljs först den artikel som registrerades först. Standardvillkor för att välja artiklar i plocklagerplatser, till exempel lagerplatsordning och enhetsbrytning, som kopplas till den tillfälliga FEFO-artikelspårninglistan.  

## <a name="put-away-template"></a>Artikelinförselmall  
Artikelinförselmallen kan tilldelas en artikel och till ett lagerställe. Artikelinförselmallen anger en uppsättning prioriterade regler som måste respekteras när du vill skapa artikelinförslar. Artikelinförselmallen kan till exempel kräva att artikeln placeras på en lagerplats med lagerplatsinnehåll som matchar enheten, och om en liknande lagerplats med tillräckligt med kapacitet inte kan hittas måste artikeln placeras i en tom lagerplats.  

## <a name="see-also"></a>Se även  
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)   
[Designdetaljer: Disposition i distributionslagret](design-details-availability-in-the-warehouse.md)

