---
title: Copilot-dataflytt över geografiska områden
description: Lär dig hur data som används i copilot-funktioner i Dynamics 365 Business Central flyttas över geografiska områden där Azure OpenAI Service inte är tillgänglig som standard.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 11/30/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="copilot-data-movement-across-geographies"></a>Copilot-dataförflyttning mellan geografiska områden

Copilot är tillgängligt i alla geografiska [Business Central länder/regioner som stöds](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Copilot använder Microsoft Azure OpenAI Service, som för närvarande endast är tillgänglig för Business Central i vissa geografiska regioner. Det innebär att om din miljö finns någon annanstans måste data från Copilot- och generativa AI-funktioner överföras utanför din geografiska region och kan bearbetas och lagras utanför efterlevnadsgränsen. Data omfattar AI-uppmaningar och dina affärsdata som används av eller genereras av Copilot. I det här fallet måste du välja att tillåta dataförflyttning till en Azure OpenAI Service i ett annat geografiskt område. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Om din miljö finns i samma Azure-region som Azure OpenAI Service ansluter den automatiskt till Azure OpenAI Service, det finns inget alternativ och ingen engångskonfiguration krävs.

> [!NOTE]
> Enskilda Copilot- och generativa AI-funktioner kanske inte är tillgängliga i alla Business Central miljöländer/regioner. Kontakta utgivaren av varje funktion för att förstå tillgängligheten.
> 
> Copilot- och generativa AI-funktioner från utgivare som inte kommer från Microsoft, till exempel de som kommer från anpassningar eller AppSource-appar som du installerar, definierar var och en sina egna specifika Azure OpenAI Service. Kontakta tilläggsutgivaren för att förstå vilka regionala Azure-tjänster som används av tillägget. 

### <a name="azure-openai-service-geographies"></a>Geografiska områden för Azure OpenAI Service

I följande tabell visas Azure OpenAI Service geografiska område som används av Copilot, baserat på Azure-region för en Business Central-miljö. Den här informationen är viktig när du bestämmer om du ska välja dataförflyttning mellan geografiska områden. Du kan identifiera Azure-region för din miljö i administrationscentret för Business Central (se [Hantera miljöer i administrationscentret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Miljö Azure-regionen| Geografiska områden för Azure OpenAI Service|Administratörsåtgärd krävs för att låsa upp Copilot| 
| - | - | - |
|Asien (öst, sydöst) |USA|Ja|
|Australien (sydöstra)| USA |Ja |
|Brasilien (södra) |USA|Ja|
|Kanada (centrala, östra)|USA|Ja|
|Europa (väst, norr)| Sverige eller Schweiz |Nej\*|
|Frankrike (central, södra)| Sverige eller Schweiz |Ja|
|Tyskland (norra, västra centrala)| Sverige eller Schweiz |Ja|
|Indien (centrala, södra)|USA|Ja|
|Japan (öst, väst)|USA|Ja|
|Sydkorea (centrala, södra)|USA|Ja|
|Norge (öst, väst)|Sverige eller Schweiz |Ja|
|Sydafrika (nord, väst)|USA|Ja|
|Schweiz (nord, väst) |Sverige eller Schweiz |Ja|
|Förenade Arabemiraten (nord, väst)|USA|Ja|
|Storbritannien (syd, väst)|Storbritannien|Ja|
|USA (centrala, östra, norra centrala, södra centrala, västra) |USA|Nej|

\* För miljöer i Azure-regionerna Europa, västra och Europa, norra väljer Business Central automatiskt att flytta data mellan geografiska områden, men administratörer kan när som helst välja att avanmäla sig.

> [!NOTE]
> När en Azure OpenAI Service blir tillgänglig i ditt Business Central-geografiska område övergår din miljö automatiskt till att använda Azure OpenAI Service och det är inte nödvändigt eller ens möjligt att välja.
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## <a name="next-steps"></a>Nästa steg

Du väljer att tillåta (eller välja bort) dataförflyttning mellan geografiska områden från sidan [Copilot och AI-funktioner](https://businesscentral.dynamics.com/?page=7775). Mer information finns i [Tillåt dataförflyttning mellan geografiska områden](enable-ai.md#allow-data-movement-across-geographies).
