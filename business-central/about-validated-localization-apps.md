---
title: Utveckling av validerade lokaliseringsappar
description: Uppfyll regelkraven i Dynamics 365 Business Central som en validerad lokaliseringsapp.
author: altotovi
ms.date: 06/04/2024
ms.reviewer: bholtorf
ms.topic: conceptual
ms.author: altotovi
---

# Utveckling av validerade lokaliseringsappar

I den här artikeln beskrivs kraven och riktlinjerna för att utveckla en validerad lokaliseringsapp för [!INCLUDE[prod_short](includes/prod_short.md)].

## Vad är en validerad lokaliseringsapp?

[!INCLUDE[prod_short](includes/prod_short.md)] är tillgängligt [globalt på 170+ marknader](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json). På en uppsättning marknader arbetar Microsoft med ISV-partner för att lokalisera [!INCLUDE[prod_short](includes/prod_short.md)] via lokaliseringsappar som är tillgängliga på [Microsoft AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). För dessa regioner kan lokaliseringar vara tillgängliga via det föredragna lokaliseringsprogrammet. Det föredragna lokaliseringsprogrammet känner igen de appar som är byggda enligt Microsofts specifika kvalitetsriktlinjer. ISV-partners som följer dessa programkrav och riktlinjer kan dra nytta tekniskt och kommersiellt för att tjäna sina återförsäljare och kunder.  

I följande avsnitt hittar du krav och riktlinjer. Du kan kontakta programteamet om du vill delta i programmet och uppfylla nedanstående krav genom att kontakta oss via [Microsofts lokaliseringsteam](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> Initiativet för [!INCLUDE[prod_short](includes/prod_short.md)] validerade lokaliseringsappar distribueras för närvarande som ett pilotprogram. Nedanstående krav och förmåner kan ändras baserat på feedback från partner och kund.  

Appar i pilotprogrammet för validerad lokalisering innehåller en uppsättning funktioner som hanterar lokala myndighetskrav som faller inom någon av kategorierna i följande lista.  

- **Regelkrav** – lokal funktion som hjälper företag att uppfylla sina juridiska krav, till exempel skatterapportering, lokala e-faktureringsformat, lokala allmänt vedertagna bokföringsregler och andra regelkrav.
- **Nationella standardkrav** – lokal funktion som hanterar lokala standarder, till exempel adressformat, nationella bankformat eller lokala tolkningar av globala standarder.
- **Lokalt språk** – lokalt språk i lokaliseringsappen, men även för en basapp om det här språket för närvarande inte finns med på listan över [språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

> [!NOTE]
> Lokala marknadsbehov eller branschkrav bör inte inkluderas i de föredragna lokaliseringsapparna. Om appar innehåller dessa funktioner kan apparna inte godkännas som validerade lokaliseringsappar.

> [!NOTE]
> Lokal funktion är fördelaktig för produktivitetsaffärsprocesserna i ett land och tillför därmed värde till verksamheten men krävs inte ur ett regleringsperspektiv, till exempel specifika bank- och betalningsformat, utgiftsrapporter, HR-funktioner, löner och liknande mindre eller större funktioner och funktioner som är bra att ha bör isoleras i andra appar. Om appar innehåller dessa funktioner kan de inte godkännas som validerade lokaliseringsappar.   

## Affärskrav för validerade lokaliseringsappar  

- Leverantören för validerad applokalisering uppfyller alla krav för att vara en indirekt CSP-leverantör.  
- Leverantören av validerad lokaliseringsapp introducerar ett minsta antal erbjudanden på marknaden i fem länder/regioner, som paketerar Dynamics 365 Business Central med en validerad lokaliseringsapp. 
- Leverantören för validerad applokalisering har minst 10 [!INCLUDE[prod_short](includes/prod_short.md)] onlinekunder med produktionsmiljöer som aktivt använder appen för validerad lokalisering. 
- Leverantören för validerad applokalisering skickar årligen in en affärsplan till programmets v-team. Detta omfattar planerade marknadsförings- och beredskapsaktiviteter för att marknadsföra det paketerade erbjudandet med CSP indirekta återförsäljare i tillämpliga länder/regioner. Planen kan skickas in i början av varje kvartal till [Microsofts lokaliseringsteam](mailto:d365bcloc@microsoft.com).  
- Validerade lokaliseringsappar görs tillgängliga för alla kunder och partner som vill dra nytta av det.     
- Leverantören av den validerade lokaliseringsappen använder återkommande arbetsflöden med Microsoft.

## Validerade funktions- och tekniska krav för lokaliseringsappen  

### Krav på funktionalitet   

Förutom att uppfylla de tekniska kraven för den föredragna lokaliseringsappen är det minsta genomförbara produktomfånget för föredragen lokaliseringsapp:  

- Funktioner för lokala föreskrifter   
  - Lokala föreskrifter.   
  - Officiellt obligatoriska funktioner. 
  - Endast horisontella funktioner (inte branschspecifika).  
  - Gäller i de flesta företag.  
  - Inom följande skiss:   
    - Områden med de vanligaste lagändringarna. 
    - Spåras redan som en lokalisering i Microsoft-lokaliseringar. 
    - Funktionsreferenser – sällan nya.  
    - Inga leverantörs-/bankspecifika format, löner eller liknande. 
    - Inga globala funktioner om de inte har skapats av Microsoft. 
- Översättningar: 
  - Översättning av en lokaliseringsapp till lokala språk. 
  - Översättning av en basapp till lokala språk – om språket inte redan [stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  
  - Översättning av lokaliseringsappens dokumentation till lokala språk. 
- Även om de båda är en del av lokaliseringen rekommenderar vi att nationella standardfunktioner (lokal del) byggs som separata appar från lokala regleringsfunktioner. 
- Demodata på det lokala språket som gäller för den specifika marknaden.   
- Alla funktioner måste utformas för att behålla ett förenklat användargränssnitt. Observera att de främst är avsedda för marknaden för små och medelstora företag.  
- Undvik att skapa nya funktioner om samma eller liknande funktioner redan finns i den basappen, till exempel elektronisk fakturering, granskningsexport, momsfunktioner, datautbyte och andra där de flesta funktioner är gemensamma för alla länder/regioner men det finns vissa lokala regler eller affärsformat som är tillägg till globala ramverk eller format. Istället för att bygga nya funktioner, utökar du befintliga.  
- Förbered installationsguider för områden som är komplexa att konfigurera för att hjälpa användarna att aktivera, upptäcka och få bra första erfarenhet av att använda din lokaliseringsapp.  
- Partner måste tillhandahålla funktionsdokumentation för alla aspekter av lokaliseringen.  

### Tekniska krav  

Nedan finns en lista över alla krav som måste uppfyllas innan du skickar den validerade lokaliseringsappen som ett tillägg för validering. Den här listan ändrar inte [listan över teknisk validering](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) och utökar bara kraven därifrån.  

- Leverantörerna av validerad lokaliseringsapp måste skapa den validerade lokaliseringsappen baserat på W1-basappen.  
- Leverantörerna av validerad lokaliseringsapp måste följa Microsofts livscykel- och supportpolicyer.   
- Obligatorisk testautomatisering måste täcka minst 80 % av koden och alla affärsprocesser som ändras med validerad lokaliseringsapp måste omfattas av testautomatisering.  
- Leverantörerna av validerad lokaliseringsapp måste uppdatera och/eller testa sin validerade lokaliseringsapp innan den officiella lanseringen av den nya versionen (minst med RC före den nya versionen) för att bekräfta att det inte finns några problem. 
- Alla objekt i koden för validerad lokaliseringsapp måste vara på engelska.   
- Leverantörerna av validerad lokaliseringsapp måste följa Microsofts policy för föråldrade objekt och större ändringar samt metodtips för utfasning av AL-koden.  
- Leverantörerna av validerad lokaliseringsapp bör lägga till nya händelser om det krävs av marknaden (andra implementeringspartner eller kunder) om det är rimligt affärsmässigt, i enlighet med Microsoft-policyn och praxis. Annars måste leverantörerna av validerade lokaliseringsappar svara på sådana förfrågningar med en korrekt motivering till varför det inte är rimligt att lägga till. 
- Leverantörerna av validerad lokaliseringsapp måste tillhandahålla skriftliga testscenarier på engelska och göra det möjligt för Microsoft att utföra manuella tester om Microsoft kräver det.  
- Om en validerad lokaliseringsapp utökar [!INCLUDE[prod_short](includes/prod_short.md)] datamodellen med nya tabeller och/eller fält måste leverantören för validerad lokaliseringsapp ange egenskapen **DataClassification** korrekt.

> [!NOTE]  
> Du kan också skapa en integration om du tycker att det är fördelaktigt att ha viss funktionalitet placerad utanför [!INCLUDE[prod_short](includes/prod_short.md)] miljön och istället ansluta till [!INCLUDE[prod_short](includes/prod_short.md)] med till exempel API:er eller webbtjänster.

## Se även

[Teknisk validering](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Utveckling av en standardlokaliseringslösning](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Tillgänglighet för land/region och språk som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Vad är lokal funktionalitet i Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]?](about-localization.md)  
[Internationella tillgängligheten för Microsoft Dynamics 365](/dynamics365/get-started/availability)  
[Regelefterlevnad – översikt](compliance/compliance-overview.md)  
[Geografisk tillgänglighet för Dynamics 365](https://dynamics.microsoft.com/en-us/availability-reports/georeport/)  
