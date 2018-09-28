---
title: Visa anpassade Power BI-rapporter | Microsoft Docs
description: "Du kan använda Power BI-rapporter för att få ytterligare information om data i listor."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 595e6fb7cc8239ea33cf57aadfd8b0f3419323e5
ms.contentlocale: sv-se
ms.lasthandoff: 06/01/2018

---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Visa listdata i Power BI-rapporter i Business Central 
[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller ett faktaboxkontrollelement på flera viktiga listsidor som ger ytterligare information om data i listan. När du flyttar mellan rader i listan uppdateras rapporten och filtrerats för den valda transaktionen. Du kan skapa anpassade rapporter som ska visas i kontrollen, men det finns några regler som gäller när du skapar rapporter för att se till att de ger önskat beteende.  

> [!NOTE]  
>   Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med Power BI. Dessutom måste du hämta [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Mer information finns i [Använda [!INCLUDE[d365fin](includes/d365fin_md.md)] som Power BI-datakälla](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Rapportdatauppsättning
När du skapar rapporten i Power BI Desktop, anger du dattakällan eller webbtjänsten som innehåller de data som är relaterade till listan som du vill associera med rapporten. Om du vill skapa en rapport för försäljningslistan ser du till att datauppsättningen innehåller information om försäljning.  

För att filtrera data i rapporter baserat på den post som valts från listsidan, måste primärnyckeln användas som ett rapportfilter. Primärnycklar måste ingå i datauppsättningen för rapporterna du ska filtrera. Oftast är primärnyckeln för en lista **nr.** .  

## <a name="defining-the-report-filter"></a>Definiera rapportfilter
Rapporten krävs för ett grundläggande rapportfilter (inte en sida eller grafiskt filter och inte avancerat filter) för att filtrera korrekt i Power BI faktaboxkontroll. Filtret som passeras till Power BI-rapporten från varje listsida baseras på primärnyckeln som beskrivs i föregående avsnitt.  

Om du vill definiera ett filter för rapporten, markera primärnyckel i listan över tillgängliga fält och dra och släpp fältet i avsnittet **rapportfilter**.  

![Ange rapportfiltret för rapporten Försäljningsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Rapportens storlek och färg
Storleken på rapporten måste anges till 325 x 310 pixlar. Detta är nödvändigt för korrekt skalering av rapporten i tillgängligt utrymme som tillåts av den Power BI faktaboxkontrollen. Om du vill definiera storleken på rapporten, lägger du fokus utanför rapportens layoutområde och klickar på ikonen färgrulle.

![Ange rapportens bredd och höjd för rapporten Försäljningsfakturaaktivitet](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Du kan ändra bredd och höjd på rapporten genom att välja **anpassaval** i fältet **typ**.

På samma sätt, om du vill att bakgrunden för rapporten ska blandas med bakgrundsfärgen för Power BI faktaboxkontroll definierar du en anpassad rapportbakgrundsfärgen i *E5E5E5*. Detta är valfritt.  

## <a name="reports-with-multiple-pages"></a>Rapporter med flera sidor
Du kan skapa en rapport med flera sidor med Power BI. Bilder som du vill ska visas i [!INCLUDE[d365fin](includes/d365fin_md.md)]-listsidor måste finnas på den första sidan i rapporten i Power BI.  

> [!NOTE]  
>  Power BI faktaboxen kan bara visa den första sidan i en rapport. Om du vill visa andra sidor måste du expandera rapporten och använda flikarna längst ned i rapporten för att navigera till andra sidor.  

## <a name="saving-your-report"></a>Spara rapporten

När du sparar din rapport är det en bra metod att namnet på rapporten innehåller namnet på listsidan som ska visas i rapporten. Till exempel ordet *leverantör* måste finnas någonstans i rapportnamnet för rapporter som du vill göra tillgängliga i leverantörslistan.  

Detta är inte ett krav. Det gör däremot valet av rapporter snabbare. Vi skickar in ett filter som baseras på sidans namn för att begränsa de rapporter som visas när rapportsidan öppnas från en listsida.  Du kan ta bort filtret om du vill ha en lista över rapporter som är tillgängliga för dig i Power BI.  

## <a name="troubleshooting"></a>Felsökning
Det här avsnittet beskriver en lösning för de vanligaste problemen som kan uppstå när du skapar BI Power-rapporten.  

**Användaren ser inte en rapport på sidan Välj rapport som de vill markera** Om du inte kan välja en rapport, är en möjlig lösning att kontrollera namnet på rapporten så att den innehåller namnet på listsidan. Du kan också ta bort filtret om du vill ha en fullständig lista över Power BI-rapporter som är tillgängliga.  

**Rapporten är laddad men tom. inte filtrerad eller felaktigt filtrerad** Kontrollera att rapportfiltret innehåller rätt primärnyckel. I de flesta fall är detta fältet **nr.** men i tabellen **Redovisningstransaktion**, till exempel måste du använda fältet **Löpnr**.

**Rapporten laddas och visas inte på sidan som förväntat** Kontrollera att sidan som du vill visa är den första sidan i rapporten.  

**Rapporten visas med oönskade grå kanter, är för liten eller för stor**

Kontrollera att rapportens storlek är 325 pixlar x 310 pixlar. Spara rapporten och uppdatera sedan listsidan.  

## <a name="see-also"></a>Se även
[Med hjälp av [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI-datakälla](across-how-use-financials-data-source-powerbi.md)  
[Komma igång](product-get-started.md)    
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)    
[Ekonomi](finance.md)  

