---
title: Ställa in analysvy för kassaflöde
description: 'Använd diagram för rollcentret Revisor för att analysera flödet av pengar i företaget, inklusive utgifter och inkomster, likviditet och inbetalningar minus utbetalningar.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 08/23/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="setting-up-cash-flow-analysis"></a>Ställa in analysvy för kassaflöde

Om du vill ha hjälp att bestämma vad som ska ske med dina likvida medel kan du titta på diagrammen i rollcentret Revisor:

* **Kassacykel**  
* **Inkomst och utgift**  
* **Kassaflöde**  
* **Kassaflödesprognoser**  

Den här artikeln beskriver var informationen i diagrammen kommer från och, vid behov, vad du gör om du vill börja använda diagrammen.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Kassacykeln och diagram för inkomster och utgifter

Diamgrammen **Kassacykel** och **Inkomster och utgifter** är klara, beroende på kontoplan och ekonomiska rapporter. Kontona är var informationen kommer från och ekonomiska rapporter beräknar förhållandet mellan försäljning och kundfordringar. Vissa konton och ekonomiska rapporter tillhandahålls. Du kan använda dem som de är, ändra dem och lägga till nya. Om du lägger till redovisningskonton i kontoplanen, till exempel genom att importera dem från QuickBooks, behöver du mappa till kontona på sidan **Ekonomiska rapporter** för följande rapporter:

| Namn på ekonomisk rapport | Där den används |
| --- | --- |
| **I_CACYCLE** |Kassacykel |
| **I_CASHFLOW** |Kassaflöde |
| **I_INCEXP** |Inkomst och utgift |
| **I_MINTRIAL** |Som en resultaträkning om du inte använder kontoplanen |

> [!NOTE]
> Det är en bra idé att behålla beräkningarna som ges för den ekonomiska rapporten.

Ange konton i fältet **Summeringsintervall** för **Totala intäkter**, **Totala kundfordringar**, **Totala leverantörsskulder**, och **Totalt lager**. Om du vill mappa till ett kontointervall anger du kontonumren avgränsade med ".." som i **1111.. 4444**. Alternativt kan du mappa till specifika konton genom att ange kontonumren avgränsade med lodräta staplar, som i **2222|3333|5555**.  

> [!TIP] 
> Kontrollera en mappning genom att välja åtgärden **Översikt**.  

## <a name="set-up-the-cash-flow-chart"></a>Konfigurera kassaflödesdiagrammet

Kassaflödesdiagrammet baseras på följande:  

* Ett diagram med kassaflödeskonton.
* En eller flera kassaflödeinstallationer. Dessa inställningar anger kontona som ska användas för redovisning, inköp, försäljning, tjänster och anläggningstillgångar.  

För att hjälpa dig att komma igång, finns vissa konto- och kassaflödeinstallationer. Du kan lägga till, ändra eller ta bort dem.  

Du anger dessa konton genom att söka efter **Diagram över kassaflödeskonton**, väljer länken och fyller sedan i fälten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Upprepa stegen för **Kassaflödesinställningar**.

## <a name="set-up-cash-flow-forecasts"></a>Konfigurera kassaflödesprognoser.

Diagrammet **kassaflödesprognos** använder kassaflödeskonton, kassaflödesinställningar för kassaflödesprognoser. Vissa tillhandahålls, men du kan ställa in egna med hjälp av en assisterade konfigurationsguiden. Guiden hjälper dig att ange saker som till exempel hur ofta du uppdaterar prognosen, kontona som du vill basera den på, information om när du betalar skatter och om du ska använda [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Kassaflödesprognoser kan använda Azure AI för att skapa en mer omfattande prognos. Anslutningen till Azure AI redan ställts in åt dig. Du måste aktivera den. När du loggar in i [!INCLUDE[prod_short](includes/prod_short.md)] visas ett meddelande i en blå stapel och innehåller en länk till standardinställning för kassaflödesinställningen. Meddelandet visas endast en gång. Om du stänger den och bestämmer dig för att aktivera Azure AI använder du den assisterade inställningsguiden eller en manuell process.  

> [!NOTE]
>
> Du kan alternativt använda förebyggande webbtjänsten. Mer information finns i [skapa och använda egna förebyggande webbtjänsten för kassaflödesprognoser](#AnchorText).  

Så här använder du guiden för assisterad konfiguration:  

1. I rollcentret Revisor, under diagrammet **kassaflödesprognos** väljer du åtgärden **Öppna assisterad konfiguration**.
2. Fyll i fälten som behövs i varje steg i guiden. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Tillbaka i rollcentret Revisor väljer du åtgärden **Omberäkna prognos** under diagrammet **Kassaflödesprognos**.

Så här använder du en manuell process:  

1. I rollcentret Revisor väljer du ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") och anger **Kassaflödesinställningar** och väljer sedan relaterad länk.
2. Expandera snabbfliken **Azure AI** och välj fältet **Azure AI aktiverad**.
3. Tillbaka i rollcentret Revisor väljer du åtgärden **Omberäkna prognos** under diagrammet **Kassaflödesprognos**.

> [!TIP]  
> Beakta längden för perioderna som tjänsten ska använda i dess beräkningar. Ju mer information som du anger, desto mer exakta kommer prognoserna att vara. Se upp för stora avvikelser i perioder. De kommer också att påverka prognoserna. Om Azure AI inte hittar tillräckligt med data, eller om data varierar mycket, kommer tjänsten inte att utföra någon prognos.  

## <a name="design-details"></a>Designinformation

Prenumerationer på [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar åtkomst till ett flertal prediktiva webbtjänster i alla regioner där [!INCLUDE[prod_short](includes/prod_short.md)] finns tillgängligt. Mer information finns i Microsoft Dynamics 365 Business Central-licensguiden. Guiden kan hämtas på webbplatsen för [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Dessa webbtjänster är tillståndslösa, vilket innebär att de endast använder data för att beräkna förutsägelser vid behov. Inga data lagras.

> [!NOTE]
>
> Du kan använda din egen prediktiva webbtjänst i stället för vår. Mer information finns i [skapa och använda egna förebyggande webbtjänsten för kassaflödesprognoser](#AnchorText).

### <a name="data-required-for-forecast"></a>Data som krävs för prognoser

Om du vill göra förutsägelser om framtida intäkter och kostnader kräver webbtjänsterna historiska data från kundreskontra, leverantörsreskontra och moms.

#### <a name="receivables"></a>Kundreskontra

Fälten **Förfallodatum** och **Belopp (BVA)** på sidan **Transaktioner för kundreskontra**, där:

* Dokumenttypen är *Faktura* eller *Kreditnota*.
* Förfallodatumet infaller mellan det datum som beräknas baserat på värdena i fälten **Historiska perioder** och **Periodtyp** på sidan **Inställningar för kassaflöde** och arbetsdatum.

Innan du använder den prediktiva webb-tjänsten komprimerar [!INCLUDE[prod_short](includes/prod_short.md)] transaktioner efter **Förfallodatum** baserat på värdet i fältet **Periodtyp** på sidan **Inställningar för kassaflöde**.

#### <a name="payables"></a>Leverantörsreskontra

Fälten **Förfallodatum** och **Belopp (BVA)** på sidan **Transaktioner för leverantörsreskontra**, där:

* Dokumenttypen är *Faktura* eller *Kreditnota*.
* Förfallodatumet infaller mellan det datum som beräknas baserat på värdena i fälten **Historiska perioder** och **Periodtyp** på sidan **Inställningar för kassaflöde** och arbetsdatum.

Innan du använder den prediktiva webb-tjänsten komprimerar [!INCLUDE[prod_short](includes/prod_short.md)] transaktioner efter **Förfallodatum** baserat på värdet i fältet **Periodtyp** på sidan **Inställningar för kassaflöde**.

#### <a name="tax"></a>Moms

Fälten **Dokumentdatum** och **Belopp** på sidan **Transaktioner för moms**, där:

* Dokumenttypen är *Försäljning*.
* Dokumentdatumet infaller mellan det datum som beräknas baserat på värdena i fälten **Historiska perioder** och **Periodtyp** på sidan **Inställningar för kassaflöde** och arbetsdatum.

Innan du använder den prediktiva webb-tjänsten komprimerar [!INCLUDE[prod_short](includes/prod_short.md)] transaktioner efter **Dokumentdatum** baserat på värdet i fältet **Periodtyp** på sidan **Inställningar för kassaflöde**.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"></a>Skapa och använda en egen prediktiv webbtjänst för kassaflödesprognoser

Du kan också skapa en egen förebyggande webbtjänst som bygger på en allmän modell kallad **Prognosmodell för Microsoft Business Central**. Den här förebyggande modellen finns online i Azure AI-galleriet. För att använda modellen gör du följande:  

1. Öppna en webbläsare och gå du till [Azure AI-galleriet](https://go.microsoft.com/fwlink/?linkid=828352)  
2. Sök efter **Prognosmodell för Microsoft Business Central** och öppna sedan modellen i Microsoft Azure Machine Learning Studio.  
3. Använd ditt Microsoft-konto för att registrera dig för en arbetsyta och kopiera sedan modellen.  
4. Kör modellen och publicera den som en webbtjänst.  
5. Gör en anteckning av API-URL och API-nyckel. Du använder denna information för en kassaflödesinställningar.  
6. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kassaflödesinställningar** och väljer sedan relaterad länk.  
7. Expandera snabbfliken för **Azure AI** och fyll sedan i fälten, inklusive API-URL och API-nyckel från Azure Machine Learning Studio. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. I rollcentret Revisor väljer du åtgärden **Omberäkna prognos** under diagrammet **Kassaflödesprognos**.

## <a name="see-also"></a>Se även

[Analysera kassaflödet i företaget](finance-analyze-cash-flow.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
