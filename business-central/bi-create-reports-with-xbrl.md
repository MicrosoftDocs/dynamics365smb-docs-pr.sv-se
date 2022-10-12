---
title: Så här skapar du rapporter med XBRL
description: XBRL, är ett XML-baserat språk för ekonomisk rapportering som gör det möjligt för företag att effektivt och korrekt behandla och dela med sig av sina data.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/14/2022
ms.author: edupont
ms.openlocfilehash: 3aabe61906cd6b8111a3fcadb616a4cdfae6277c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605306"
---
# <a name="create-reports-with-xbrl"></a>Skapa rapporter med XBRL

> [!NOTE]
> Vi håller på att ta bort funktionerna för XBRL-rapportering från [!INCLUDE[prod_short](includes/prod_short.md)]. Läs mer i [Ändringar i utgivningscykel 1 år 2022](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (e **X** tensible **B** usiness **R** eporting **L** anguage) är ett språk som baseras på eXtensible Markup Language (XML), för taggning av ekonomiska data, som gör det möjligt för företag att bearbeta och dela data på ett effektivt och korrekt sätt. Bakom XBRL-projektet för global ekonomisk rapportering står ett stort antal ERP-programvaruföretag och internationella revisionsbyråer. Målet med projektet är att tillhandahålla en standard för enhetlig rapportering av ekonomisk information för banker, investerare och statliga myndigheter. Sådan affärsrapportering kan inkludera följande:  

* Ekonomirapporter  
* Ekonomisk information  
* Icke-ekonomisk information  
* Lagreglerat uppgiftslämnande, till exempel årsredovisningar och kvartalsredovisningar  

> [!NOTE]
> Du kan importera redovisningsrelaterade uppställningar och skapa XBRL-instansdokument genom att mappa redovisningsdata från kontoplanen till element i taxonomier som har utformats för finansiella rapporter, till exempel balansräkningar, resultaträkningar och så vidare.
>
> XBRL-funktionerna i Business Central Support-taxonomier för specifikation 2.1. Taxonomier kan dock innehålla element som inte stöds, som t.ex. formellänkbaser eller iXBRL (infogade XBRL), eller ha andra strukturella skillnader. Vi rekommenderar att du validerar XBRL-funktionen innan du använder den för rapportering.
>
> Fullt stöd för taxonomier kan kräva XBRL-taggning och verktyg från tredje part. Den internationella organisationen XBRL har en lista över verktyg och tjänster. Beroende på XBRL-rapporteringskraven för en viss taxonomi kanske du vill utforska dessa resurser. Läs mer i [Komma igång för företag](https://go.microsoft.com/fwlink/?linkid=2153466) och [Verktyg och tjänster](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language

XBRL-taxonomier underhålls av www.xbrl.org. Du kan hämta taxonomier eller läsa mer på XBRL:s webbplats.  

Anta att någon vill ha ekonomisk information från dig. De skickar en taxonomi (ett XML-dokument) med ett eller flera uppställningar, vardera med en eller flera rader för ifyllning. Raderna motsvarar de individuella ekonomiska data som begärs av avsändaren. Du importerar taxonomin och fyller sedan i uppställningen (eller uppställningarna) genom att ange vilket eller vilka konton som anknyter till respektive rad, samt vilken beräkning som önskas, t.ex. nettoförändring eller saldo t.o.m. datum. Ibland kan du i stället ange en konstant, t. ex. antal anställda. Därefter kan du skicka instansdokumentet (ett XML-dokument) till begäranden. Förmodligen utgör detta en återkommande händelse och, om inga ändringar gjorts i taxonomin, exporterar du bara nya instansdokument för nya perioder vid begäran.

## <a name="xbrl-comprises-the-following-components"></a>XBRL består av följande komponenter

XBRL-**specifikationen** förklarar vad XBRL är, samt hur du skapar XBRL-instansdokument och -taxonomier. XBRL-specifikationen beskriver XBRL i mer tekniska termer och är avsedd för avancerade användare.  

XBRL- **uppställningen**, som motsvarar de grundläggande huvudkomponenterna i XBRL. Uppställningen utgör den fysiska XSD-fil (även kallad en XML-uppställningsdefinition) som anger hur XBRL-instansdokument och taxonomier ska byggas.

XBRL-**länkbaserna** utgör de fysiska XML-filer som innehåller information om elementen som definieras i XBRL-uppställningen, t.ex. rubriker på ett eller flera språk, hur dessa är kopplade till varandra, hur element ska summeras o.s.v.  

En XBRL-**taxonomi** är en "terminologi" eller "ordlista" som skapats av en grupp för utbyte av affärsinformation. Taxonomin är kompatibel med XBRL-specifikationen.  

Ett XBRL- **instansdokument** är en affärsrapport, t. ex. en ekonomisk rapport, som förberetts för XBRL-specifikationen. Innebörden av värdena i instansdokumentet beskrivs av taxonomin. Faktum är att ett instansdokument är praktiskt taget oanvändbart om du inte vet för vilken taxonomi det har förberetts.  

## <a name="layered-taxonomies"></a>Överlappande taxonomier

En taxonomi kan bestå av en bastaxonomi, t.ex. USA GAAP (allmänt accepterade redovisningsprinciper) eller IAS (internationella redovisningsstandarder) och har ett eller flera tillägg. För att återspegla detta refererar en taxonomi till en eller flera uppställningar som alla utgör separata taxonomier. När ytterligare taxonomier laddas in i databasen, läggs de nya elementen till i slutet av de redan befintliga.  

## <a name="linkbases"></a>Länkbaser

I XBRL-specifikation 2 beskrivs taxonomin i flera XML-filer. Den primära XML-filen är själva taxonomischemafilen (XSD-fil), som endast innehåller en oordnad lista med element eller information som ska rapporteras. Utöver detta finns ofta länkbasfiler (.xml). Länkbasfilerna innehåller data som kompletterar taxonomin (.xsd-fil). Det finns sex olika typer av länkbasfiler, och fyra av dessa är relevanta för [!INCLUDE[prod_short](includes/prod_short.md)]. Dessa är:

* Etikettlänkbas: Den här länkbasen innehåller etiketter eller namn för elementen. Filen kan innehålla etiketter på olika språk som identifieras med XML-egenskapen ”lang”. XML-språk-ID innehåller vanligtvis en förkortning på två bokstäver och även om det ska vara enkelt att gissa vad förkortningen betyder, finns det inget samband med språkkoderna i Microsoft Windows eller med språkkoderna som definieras i demonstrationsdata. När du slår upp språken för en viss taxonomi visas därför alla etiketter för det första elementet i taxonomin. Det betyder att ett exempel på varje språk visas. En taxonomi kan ha flera kopplade etikettlänkbaser, förutsatt att dessa länkbaser innehåller olika språk.  
* Presentationslänkbas: Den här länkbasen innehåller information om elementens struktur, d.v.s. hur taxonomins utfärdare föreslår att taxonomin ska presenteras för dig. Länkbasen innehåller en serie länkar som var och en kopplar två element i ett överordnad–underordnad-förhållande. När alla dessa länkar kopplats kan elementen visas i en hierarkisk struktur. Observera att presentationslänkbasen behandlar just detta, d.v.s. hur element presenteras för dig.
* Beräkningslänkbas: Den här länkbasen innehåller information om hur elementen summeras. Strukturen påminner om presentationslänkbasens struktur, med den skillnaden att varje länk, eller ”arc”, som de kallas, har en viktegenskap. Vikten kan antingen vara 1 eller -1, vilket betyder att elementet ska läggas till eller dras bort från det överordnade elementet. Observera att sammanslagningarna inte nödvändigtvis stämmer överens med den visuella presentationen.  
* Referenslänkbas: Den här länkbasen är en XML-fil med tilläggsinformation om de data som krävs av taxonomins utfärdare.

## <a name="set-up-xbrl-lines"></a>Ställ in XBRL-rader

När du har importerat eller uppdaterat taxonomin måste schemaraderna fyllas i med all information som krävs för att uppfylla specifika krav gällande ekonomisk rapportering. Den här informationen innefattar grundläggande företagsinformation, faktiska resultatrapporter, noteringar till resultatrapporterna, tilläggstabeller och så vidare.  

Du lägger upp XBRL-rader genom att mappa data i taxonomin till data i redovisningen.  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **XBRL-taxonomier** och väljer sedan relaterad länk.  
2. Välj en taxonomi i listan på sidan **XBRL-taxonomier**.  
3. Välj åtgärden **Rader**.  
4. Markera en rad och fyll i fälten.  
5. Om du vill läsa detaljerad information om vad som ska fyllas i väljer du åtgärden **Information**.  
6. Om du vill definiera mappningen av redovisningskontona i kontoplanen till XBRL-raderna väljer du åtgärden **Redov. def.rader**.  
7. Om du vill lägga till noteringar till ekonomirapporten väljer du åtgärden **anteckningar**.  

   > [!TIP]
   > Om du vill utelämna rader från exporterade data väljer du **EJ TILLÄMPBAR** som ursprungstyp.

   > [!NOTE]  
   > Du kan endast exportera data som motsvarar markeringen i fältet **Ursprungstyp**. Här ingår beskrivningar och anteckningar.  

   > [!NOTE]  
   > Taxonomier kan innehålla element som [!INCLUDE[prod_short](includes/prod_short.md)] inte stöder. Om ett element inte stöds kommer fältet **Ursprungstyp** att ange **Ej tillämpbart** och fältet **Beskrivning** att visa ett felmeddelande, till exempel **Oväntad typ: "specifik typ ej känd"**. Om du måste exportera elementet väljer du en matchande ursprungstyp. Vanligtvis är detta en konstant eller en beskrivning. På så sätt kan du ange och exportera data – sådana element kan emellertid ha verifieringsregler som inte kan kontrolleras före export.

## <a name="import-an-xbrl-taxonomy"></a>Importera en XBRL-taxonomi

Det första du måste göra när du arbetar med XBRL-funktionerna är att importera en taxonomi till företagets databas. En taxonomi består av ett eller flera scheman och länkbaser. När du har importerat ett eller flera uppställningar och länkbaser och kopplat länkbaserna till uppställningen, kan du lägga upp raderna och koppla redovisningskontona i kontoplanen till lämpliga taxonomirader.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **XBRL-taxonomier** och väljer sedan relaterad länk.  
2. På sidan **XBRL-taxonomier** skapa en ny rad och ange namnet och en beskrivning av taxonomin.  
3. Välj åtgärden **Uppställningar** och infoga beskrivningen av uppställningen.  
4. Du importerar uppställningen genom att på sidan **XBRL-uppställningar** välja åtgärden **Importera** och sedan välja en mapp och XSD-fil. Välj **Öppna**.  
5. Du importerar länkbasen genom att på sidan **XBRL-uppställningar** välja åtgärden **Länkbaser** och sedan välja en mapp och XML-fil. Välj **Öppna**.  
6. Du kan nu välja att koppla länkbasen till uppställningen. Upprepa stegen ovan för att importera resterande länkbaser.  
7. Välj åtgärden **Koppla till taxonomi** för att koppla länkbasen till uppställningen.  

> [!IMPORTANT]  
> I stället för att koppla länkbaserna separat efter importen kan du vänta tills du har importerat samtliga länkbaser och sedan koppla dem samtidigt. Gör det genom att välja **Nej** när du uppmanas att koppla den nyligen importerade länkbasen till uppställningen. Välj sedan raderna med länkbaserna som du vill koppla.  

## <a name="update-an-xbrl-taxonomy"></a>Uppdatera en XBRL-taxonomi

När en taxonomi ändras måste du uppdatera den aktuella taxonomin i enlighet därmed. Orsaken till uppdateringen kan vara ett ändrat schema, en ändrad länkbas eller en ny länkbas. När du har uppdaterat taxonomin behöver du bara koppla ihop raderna för de ändrade eller nya raderna.  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **XBRL-taxonomier** och väljer sedan relaterad länk.  
2. På sidan **XBRL-taxonomier** väljer du åtgärden **uppställningar**.  
3. Om du vill uppdatera en uppställning väljer du uppställningen och väljer sedan åtgärden **Importera**.  
4. Välj åtgärden **Länkbaser** när du vill uppdatera eller lägga till en ny länkbas.  
5. Välj lämplig länkbas eller tryck på Ctrl+N för att skapa en ny rad, välja länkbastyp och skriv sedan in en beskrivning.  
6. Importera länkbasen genom att välja åtgärden **importera**.  
7. Välj **Ja** när du vill koppla länkbasen till uppställningen.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index).

## <a name="see-also"></a>Se även

[Financial Business Intelligence](bi.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
