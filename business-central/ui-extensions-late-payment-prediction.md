---
title: Förutsäga sen betalning för försäljningsdokument
description: Detta ämne förklarar hur du använder vår prediktiva modell för att förutsäga om en faktura kommer att betalas i tid eller inte.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 12/20/2021
ms.author: bholtorf
ms.openlocfilehash: dd943c5ad9464b9ebd1629c5dbc8a3f5545e9d9c
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940832"
---
# <a name="the-late-payment-prediction-extension"></a>Tillägget för prediktion om sen betalning

Det är viktigt för den övergripande ekonomiska situationen i ett företag att effektivt hantera kundfordringar. Tillägget för prediktion om sen betalning hjälper dig att minska utestående kundfordringar och finjustera din insamlingsstrategi genom att förutsäga om försäljningsfakturor kommer att betalas i tid eller inte. Om till exempel om en betalning förutsägs att bli försenad kanske du bestämmer dig för att ändra villkoren för kundens betalningsmetod.

## <a name="getting-started"></a>Komma igång

När du öppnar ett bokfört försäljningsdokument, visas ett meddelande längst upp på sidan. Om du vill använda tillägget för prediktion om sen betalning kan du ansluta dig genom att välja **Aktivera** i meddelandet. Alternativt kan konfigurera tillägget manuellt. Om du till exempel ångrar att du avfärdat meddelandet.  

Om du vill aktivera tillägget manuellt följer du dessa steg:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inställningar för prediktion om sen betalning** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.

> [!Note]
> Om du väljer att aktivera tillägget manuellt bör du tänka på att [!INCLUDE[prod_short](includes/prod_short.md)] inte tillåter detta om modellens kvalitet är låg. Modellkvaliteten anger hur exakta modellens prediktioner kan antas vara. Flera faktorer kan påverka kvaliteten på en modell. Till exempel kanske datamängden är otillräcklig, eller också innehöll inte datan tillräcklig variation. Du kan visa kvaliteten på den modell som du för närvarande använder på sidan **Inställningar för prediktion om sen betalning**. Du kan också ange ett lägsta tröskelvärde för modellkvalitet.   

## <a name="viewing-all-payment-predictions"></a>Visa alla betalningsprediktioner
Om du aktiverar tillägget visas panelen **Betalningen förutsägs vara försenad** i rollcentret för **chef**. Panelen visar antalet betalningar som förutsägs vara försenade och låter dig öppna sidan **Kundreskontratransaktioner** där du kan gå på djupet med de bokförda fakturorna. Det finns tre kolumner att ta hänsyn till:  

* **Sen betalning** – anger om betalningen av fakturan förutsägs vara försenad.
* **Prediktionssäkerhet** – anger hur tillförlitlig bör anse att prediktionen är. **Hög** innebär att prediktionen är minst 90 % säker, **mellan** ligger mellan 80 % och 90 % och **låg** är lägre än 80 %.
* **Prediktionssäkerhet %** – visar den faktiska procentsatsen bakom säkerhetsgraden. Den här kolumnen visas inte som standard, men du kan lägga till den om du vill. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

> [!Tip]
> Sidan Kundreskontratransaktioner visar också en faktabox till höger. När du granskar prediktioner kan informationen i avsnittet **kunddetaljer** vara till hjälp. När du väljer fakturan i listan visar i avsnittet information om kunden. Du kan även vidta omedelbara åtgärder. Om en kund t. ex. tappar sin plånbok kan du öppna kundkortet från faktaboxen och spärra kunden för framtida försäljning.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Visa Betalningsprediktion för ett visst försäljningsdokument
Du kan också förutsäga sena betalningar i förväg. På sidorna **försäljningsofferter**, **försäljningsorder** och **försäljningsfakturor** kan du använda åtgärden **förutsäga betalning** för att generera en prediktion för det försäljning dokument som du visar.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="design-details"></a>Designinformation
Microsoft distribuerar och driver ett antal prediktiva webbtjänster i alla regioner där [!INCLUDE[prod_short](includes/prod_short.md)] finns tillgängligt. Åtkomsten till dessa webbtjänster ingår i din [!INCLUDE[prod_short](includes/prod_short.md)]-prenumeration. Mer information finns i Licensieringsguiden för Microsoft Dynamics 365 Business Central. Guiden kan hämtas på webbplatsen för [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/).

Webbtjänsterna fungerar i tre olika lägen:
- Träningsmodell. Webbtjänsten tränar modellen baserat på den angivna datamängden.
- Utvärderingsmodell. Webbtjänsten kontrollerar huruvida modellen returnerar pålitliga data för den angivna datauppsättningen.
- Förutsägelse. Webbtjänsten applicerar modellen på den angivna datauppsättningen i syfte att skapa en förutsägelse.

Dessa webbtjänster är tillståndslösa, vilket innebär att de endast använder data för att beräkna förutsägelser vid behov. Inga data lagras. 

> [!NOTE]  
>   Du kan använda din egen prediktiva webbtjänst i stället för vår. Mer information finns i [Skapa och använda din egen webbtjänst för prediktioner om sen betalning](#AnchorText). 

### <a name="data-required-to-train-and-evaluate-the-model"></a>Uppgifter som krävs för att utbilda och utvärdera modellen 
För varje **Kundreskontratransaktion** med en relaterad **bokförd försäljningsfaktura**:
- Belopp (BVA) inkl. moms
- Betalningsvillkoren i dagar beräknas som **Förfallodatum** minus **Bokföringsdatum**.
- Om det finns en tillämpad kreditnota. 

Dessutom har transaktionen berikats med sammanlagda data från andra fakturor som hör till samma kund. Detta omfattar följande:

- Totalt antal betalda fakturor och dessas belopp
- Totalt antal fakturor som betalats för sent, samt dessas belopp
- Totalt antal utestående fakturor och dessas belopp
- Totalt antal utestående fakturor som redan försenats, samt dessas belopp
- Genomsnittlig försening i dagar
- Förhållande: antal sent betalda/betalda fakturor
- Förhållande: belopp för sent betalda/betalda fakturor
- Förhållande: antal utestående sena/utestående fakturor
- Förhållande: belopp utestående sena/utestående fakturor
> [!Note]
> Informationen om kunden ingår inte i datauppsättningen.

### <a name="standard-model-and-my-model"></a>Standardmodell och min modell
Tillägget för prediktion om sen betalning innehåller en prediktiv modell som utvecklas genom att använda data som representerar ett antal små och medelstora företag. När du börjar bokföra fakturor och tar emot betalningar kommer [!INCLUDE[prod_short](includes/prod_short.md)] att utvärdera huruvida standard modellen passar ditt affärsflöde. 

Om det verkar som om dina processer inte matchar standardmodellen kan du ändå använda tillägget, men du måste då skaffa mer information. Bara fortsätt använda [!INCLUDE[prod_short](includes/prod_short.md)].
> [!Note]
> Vi använder lite av din bearbetningstid varje vecka när vi utvärderar modellen och uppdaterar modellen. 

[!INCLUDE[prod_short](includes/prod_short.md)] kör utbildning och utvärdering automatiskt när det finns tillräckligt med betalda och sena fakturor, men du kan också köra det manuellt när du vill.

#### <a name="to-train-and-use-your-model"></a>Att träna och använda din modell
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inställningar för prediktion om sen betalning** och väljer sedan relaterad länk.  
2. I fältet **Vald modell**, välj **Min modell**.
3. Välj åtgärden **Skapa min modell** för att träna modellen på dina data.  

## <a name="create-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Skapa och använda din egen webbtjänst för prediktioner om sen betalning
Du kan också skapa din egen förebyggande webbtjänst som bygger på en allmän modell med namnet **Prognosexperiment för Dynamics 365 Business Central**. Den här förebyggande modellen finns online i Azure AI-galleriet. För att använda modellen gör du följande:  

1. Öppna en webbläsare och gå du till [Azure AI-galleriet](https://go.microsoft.com/fwlink/?linkid=2086310)  
2. Sök efter **Prognosexperiment för Dynamics 365 Business Central** och öppna sedan modellen i Azure Machine Learning Studio.  
3. Använd ditt Microsoft-konto för att registrera dig för en arbetsyta och kopiera sedan modellen.  
4. Kör modellen och publicera den som en webbtjänst.  
5. Gör en anteckning av API-URL och API-nyckel. Du använder denna information för en kassaflödesinställningar.  
6. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inställningar för prediktion om sen betalning** och väljer sedan relaterad länk.  
7. Markera kryssrutan **Använd Min Azure prenumeration**.
8. På snabbfliken **mina autentiseringsuppgifter för modell**, ange API-URL och API-nyckel för din modell.  .  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/predict-late-payments-sales-documents/)

## <a name="see-also"></a>Se även

[Azure Machine Learning Studio-dokumentation](/azure/machine-learning/classic/)  
[Anpassa Business Central med tillägg](ui-extensions.md)  
[Välkommen till [!INCLUDE[prod_long](includes/prod_long.md)]](index.md)  
[Använd artificiell intelligens i Microsoft Dynamics 365 Business Central (Microsoft Learn)](/learn/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]