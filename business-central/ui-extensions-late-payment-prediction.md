---
title: "Förutsäga sen betalning för försäljningsdokument | Microsoft Docs"
description: "Använda vår prediktiva modell för att förutsäga om en faktura kommer att betalas i tid eller inte."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4e47858bf1f7253f8fb8951fe8ea3cb611138852
ms.contentlocale: sv-se
ms.lasthandoff: 11/26/2018

---
# <a name="the-late-payment-prediction-extension"></a>Tillägget för prediktion om sen betalning  
Det är viktigt för den övergripande ekonomiska situationen i ett företag att effektivt hantera kundfordringar. Tillägget för prediktion om sen betalning hjälper dig att minska utestående kundfordringar och finjustera din insamlingsstrategi genom att förutsäga om försäljningsfakturor kommer att betalas i tid eller inte. Om till exempel om en betalning förutsägs att bli försenad kanske du bestämmer dig för att ändra villkoren för kundens betalningsmetod.

## <a name="what-are-predictions-based-on"></a>Vad baseras förutsägelser på?  
Tillägget för prediktion om sen betalning använder en prediktiv modell som vi har utvecklat i Azure Machine Learning Studio och utbildat genom att använda data som representerar ett antal små och medelstora företag. Även om vi redan har utbildat och utvärderat den kommer vår prediktiva modell fortsätta att lära sig av dina data. Ju mer du använder modellen och ju mer data du matar den med, desto mer exakta blir förutsägelserna. Som standard utvärderar tillägget modellen och uppdateras förutsägelser varje vecka. Du kan emellertid uppdatera förutsägelser när som helst genom att välja åtgärden **Uppdatera prediktion** på sidan **Kundreskontratransaktioner**.  

> [!Note]
> Vi använder lite av din bearbetningstid varje vecka när vi utvärderar modellen och uppdaterar dina prediktioner. Förutom att manuellt uppdatera dina prediktioner finns det andra åtgärder som förbrukar bearbetningstid, t.ex. när du utbildar modellen (som du kan göra om du nyligen har lagt till data) och när du utvärderar modellen (som tittar på modellens kvalitet).

## <a name="getting-started"></a>Komma igång
Tillägget är gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)] och vi erbjuder en prenumeration på Azure Machine Learning. Prenumerationen har 30 minuters bearbetningstid per månad. Om du behöver tid kan du skapa din egna prediktiva modell och använda den i stället. Mer information finns i avsnittet _Bygga din egen prediktiva modell_ senare i det här avsnittet.  

När du öppnar ett bokfört försäljningsdokument, visas ett meddelande längst upp på sidan. Om du vill använda tillägget för prediktion om sen betalning kan du ansluta dig genom att välja **Aktivera** i meddelandet. Alternativt kan konfigurera tillägget manuellt. Om du till exempel ångrar att du avfärdat meddelandet.  

Om du vill aktivera tillägget manuellt följer du dessa steg:

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Anslutningar till tjänst** och välj sedan relaterad länk.  
2. Välj alternativet **Inställningar för prediktion om sen betalning** och fyll sedan i fälten efter behov.

## <a name="viewing-all-payment-predictions"></a>Visa alla betalningsprediktioner
Om du aktiverar tillägget visas panelen **Betalningen förutsägs vara försenad** i rollcentret för **chef**. Panelen visar antalet betalningar som förutsägs vara försenade och låter dig öppna sidan **Kundreskontratransaktioner** där du kan gå på djupet med de bokförda fakturorna. Det finns tre kolumner att ta hänsyn till:  

* **Sen betalning** - anger om betalningen av fakturan förutsägs vara försenad.
* **Prediktionssäkerhet** - anger hur tillförlitlig bör anse att prediktionen är. **Hög** innebär att prediktionen är minst 90 % säker, **mellan** ligger mellan 80 % och 90 % och **låg** är lägre än 80 %.
* **Prediktionssäkerhet %** - visar den faktiska procentsatsen bakom säkerhetsgraden. Den här kolumnen visas inte som standard, men du kan lägga till den om du vill. Mer information finns i [Anpassa arbetsytan](ui-personalization-user.md).

> [!Tip]
> Sidan Kundreskontratransaktioner visar också en faktabox till höger. När du granskar prediktioner kan informationen i avsnittet **kunddetaljer** vara till hjälp. När du väljer fakturan i listan visar i avsnittet information om kunden. Den låter dig också vidta omedelbara åtgärder. Om en kund t.ex. tappar sin plånbok kan du öppna kundkortet från faktaboxen och spärra kunden för framtida försäljning.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Visa Betalningsprediktion för ett visst försäljningsdokument
Du kan också förutsäga sena betalningar i förväg. På sidorna **försäljningsofferter**, **försäljningsorder** och **försäljningsfakturor** kan du använda åtgärden **förutsäga betalning** för att generera en prediktion för det försäljning dokument som du visar.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Skapa din egen prediktiva modell
Är du intereserad av att skapa din egen prediktiva modell? Du kan använda Azure Machine Learning Studio för att bygga din egen prediktiva modell och använda den i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om du vill använda egna modeller, måste du prenumerera på Azure Machine Learning. Mer information finns i [Azure Machine Learning Studio-dokumentation](https://go.microsoft.com/fwlink/?linkid=861765).  

Vi tillhandahåller emellertid ett enklare sätt att skapa och använda din egen prediktiva modell. Du kan dela data från fakturor med våra förebyggande försöket i Azure Machine Learning och låt vårt försök skapa och utbilda en prediktiv modell utifrån informationen vid ett senare tillfälle. För att dela dina data, på sidan **Inställningar för prediktion om sen betalning** väljer du åtgärden **Skapa min modell**. Därefter kommer prediktioner att baseras på din modell och dina data, inte våra.  

> [!Note]
>   Kvaliteten på modellen är viktig. När vårt prediktiva försök använder dina data för att utbilda en modell bestämmer det kvalitetsvärdet för modellen för i procent. Modellkvaliteten anger hur exakt modellens prediktioner kan antas vara. Flera faktorer kan påverka kvaliteten på en modell. Till exempel kanske dessa faktorer är att det inte fanns tillräckligt med data eller data eller att data inte innehöll tillräcklig variation. Du kan visa kvaliteten på den modell som du för närvarande använder på sidan **Inställningar för prediktion om sen betalning**. Du kan också ange ett lägsta tröskelvärde för modellkvalitet. Modeller med kvalitetsvärde under tröskelvärdet kommer inte att ge prediktioner.  

### <a name="to-use-your-model-instead-of-ours"></a>Du använder din modell istället för vår  
Om du skapar en egen modell i Azure Machine Learning Studio utan att använda verktyg i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du ange dina autentiseringsuppgifter så att [!INCLUDE[d365fin](includes/d365fin_md.md)] har åtkomst till modellen. Detta kan göras med ett par steg:

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Glödlampa som öppnar funktionen Berätta") och ange **Inställningar för prediktion om sen betalning** och välj sedan relaterad länk.  
2. Markera kryssrutan **Använd Min Azure prenumeration**.  
3. I fältet **Vald modell**, välj **Min modell**.  
4. På snabbfliken **mina autentiseringsuppgifter för modell**, ange API-URL och API-nyckel för din modell.  

## <a name="see-also"></a>Se även  
[Azure Machine Learning Studio-dokumentation](https://go.microsoft.com/fwlink/?linkid=861765)  
[Anpassa Business Central med tillägg](ui-extensions.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

