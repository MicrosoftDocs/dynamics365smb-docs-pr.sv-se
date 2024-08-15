---
title: Förutsäga sen betalning för försäljningsdokument
description: Denna artikel förklarar hur du använder vår prediktiva modell för att förutsäga om en kund kommer att betala en faktura i tid eller inte.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 07/11/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="the-late-payment-prediction-extension"></a>Tillägget för prediktion om sen betalning

Det är viktigt för den övergripande ekonomiska situationen i ett företag att effektivt hantera kundfordringar. För att minska utestående fordringar och hjälpa dig att finjustera din inkassostrategi, förutsäger tillägget om sena betalningar kan förväntas. Om till exempel om en betalning förutsägs att bli försenad kanske du bestämmer dig för att ändra villkoren för kundens betalningsmetod.

## <a name="get-started"></a>Kom i gång

När du öppnar ett bokfört försäljningsdokument, visas ett meddelande längst upp på sidan. Om du vill använda tillägget för prediktion om sen betalning kan du ansluta dig genom att välja **Aktivera** i meddelandet. Alternativt kan konfigurera tillägget manuellt. Om du till exempel ångrar att du avfärdat meddelandet.

Om du vill aktivera tillägget manuellt följer du dessa steg:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inställningar för prediktion om sen betalning** och väljer sedan relaterad länk.  
2. Fyll i fälten om det behövs.

> [!NOTE]
> Om du väljer att aktivera tillägget manuellt bör du tänka på att [!INCLUDE[prod_short](includes/prod_short.md)] inte tillåter detta om modellens kvalitet är låg. Modellkvaliteten anger hur exakta modellens prediktioner kan antas vara. Flera faktorer kan påverka kvaliteten på en modell. Till exempel kanske datamängden är otillräcklig, eller också det fanns inte tillräcklig variation i data. Du kan visa kvaliteten på den modell som du för närvarande använder på sidan **Inställningar för prediktion om sen betalning**. Du kan också ange ett lägsta tröskelvärde för modellkvalitet.

## <a name="view-all-payment-predictions"></a>Visa alla betalningsprediktioner

Om du aktiverar tillägget visas panelen **Betalningen förutsägs vara försenad** i rollcentret för **chef**. Panelen visar antalet betalningar som förutsägs vara försenade och låter dig öppna sidan **Kundreskontratransaktioner** där du kan gå på djupet med de bokförda fakturorna. Det finns tre kolumner att ta hänsyn till:  

* **Sen betalning** – anger om betalningen av fakturan förutsägs vara försenad.
* **Prediktionssäkerhet** – anger hur tillförlitlig bör anse att prediktionen är. **Hög** innebär att prediktionen är minst 90 % säker, **mellan** ligger mellan 80 % och 90 % och **låg** är lägre än 80 %.
* **Prediktionssäkerhet %** – visar den faktiska procentsatsen bakom säkerhetsgraden. Den här kolumnen är som standard dold, men du kan lägga till den om du vill. Mer information finns i [Anpassa din arbetsyta](ui-personalization-user.md).

> [!TIP]
> Sidan Kundreskontratransaktioner visar en faktabox. När du granskar prediktioner kan informationen i avsnittet **kunddetaljer** vara till hjälp. När du väljer fakturan i listan visar i avsnittet information om kunden. Du kan även vidta omedelbara åtgärder. Om en kund t. ex. tappar sin plånbok kan du öppna kundkortet från faktaboxen och spärra kunden för framtida försäljning.  

## <a name="design-details"></a>Designdetaljer

Microsoft distribuerar och driver prediktiva webbtjänster i alla regioner där [!INCLUDE[prod_short](includes/prod_short.md)] finns tillgängligt. Åtkomsten till dessa webbtjänster ingår i din [!INCLUDE[prod_short](includes/prod_short.md)]-prenumeration. Mer information finns i Licensieringsguiden för Microsoft Dynamics 365 Business Central. Guiden kan hämtas på webbplatsen för [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Webbtjänsterna fungerar i tre olika lägen:

* Träningsmodell. Webbtjänsten tränar modellen baserat på den angivna datamängden.
* Utvärderingsmodell. Webbtjänsten kontrollerar huruvida modellen returnerar pålitliga data för den angivna datauppsättningen.
* Förutsägelse. Webbtjänsten applicerar modellen på den angivna datauppsättningen i syfte att skapa en förutsägelse.

Dessa webbtjänster är tillståndslösa, vilket innebär att de endast använder data för att beräkna förutsägelser vid behov. Inga data lagras.

> [!NOTE]  
> Du kan använda din egen prediktiva webbtjänst i stället för vår. Mer information finns i [Skapa och använda din egen webbtjänst för prediktioner om sen betalning](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model"></a>Uppgifter som krävs för att utbilda och utvärdera modellen

För varje **Kundreskontratransaktion** med en relaterad **bokförd försäljningsfaktura**:

* Belopp i lokal valuta, inklusive skatt
* Betalningsvillkoren i dagar beräknas som **Förfallodatum** minus **Bokföringsdatum**
* Om det finns en tillämpad kreditnota

Dessutom har transaktionen berikats med sammanlagda data från andra fakturor som hör till samma kund.

- Totalt antal betalda fakturor och dessas belopp
- Totalt antal fakturor som betalats för sent, samt dessas belopp
- Totalt antal utestående fakturor och dessas belopp
- Totalt antal utestående fakturor som redan försenats, samt dessas belopp
- Genomsnittlig försening i dagar
- Förhållande: antal sent betalda/betalda fakturor
- Förhållande: belopp för sent betalda/betalda fakturor
- Förhållande: antal utestående sena/utestående fakturor
- Förhållande: belopp utestående sena/utestående fakturor

> [!NOTE]
> Informationen om kunden ingår inte i datauppsättningen.

### <a name="standard-model-and-my-model"></a>Standardmodell och min modell

Tillägget för prediktion om sen betalning med en prediktiv modell som utvecklas genom att använda data som representerar ett antal små och medelstora företag. När du börjar bokföra fakturor och tar emot betalningar kommer [!INCLUDE[prod_short](includes/prod_short.md)] att utvärdera huruvida standard modellen passar ditt affärsflöde.

Om dina processer inte matchar standardmodellen kan du ändå använda tillägget, men du måste då skaffa mer information. Bara fortsätt använda [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Vi använder lite av din bearbetningstid varje vecka när vi utvärderar modellen och uppdaterar modellen.

[!INCLUDE[prod_short](includes/prod_short.md)] kör utbildning och utvärdering automatiskt när tillräckligt många betalda och sena fakturor finns tillgängliga. Du kan dock köra den manuellt när du vill.

#### <a name="to-train-and-use-your-model"></a>Att träna och använda din modell

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inställningar för prediktion om sen betalning** och väljer sedan relaterad länk.  
2. I fältet **Vald modell**, välj **Min modell**.
3. Välj åtgärden **Skapa min modell** för att träna modellen på dina data.  

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Skapa och använda din egen webbtjänst för prediktioner om sen betalning

För [!INCLUDE[prod_short](includes/prod_short.md)] online publiceras modellen av Microsoft och är ansluten till Microsoft-prenumerationen. För andra distributionsalternativ måste du skapa Machine Learning-resurser i din egen Azure-prenumeration. Exempelstegen finns på [exempellagringsplatsen](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Syftet med den här uppgift är att hämta API-URI:n och API-nyckeln.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inställningar för prediktion om sen betalning** och väljer sedan relaterad länk.  
2. Markera kryssrutan **Använd Min Azure prenumeration**.
3. På snabbfliken **Använd min Azure-prenumeration** anger du API-URL:en och API-nyckeln för din modell.  

## <a name="see-also"></a>Se även

[Anpassa Business Central med tillägg](ui-extensions.md)    
[Välkommen till [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)    
[Använda artificiell intelligens i Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)    
[Översikt över prediktions-API](/dynamics365/business-central/dev-itpro/developer/ml-prediction-api-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
