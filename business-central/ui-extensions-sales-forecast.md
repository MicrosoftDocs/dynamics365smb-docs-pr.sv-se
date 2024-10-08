---
title: Med hjälp av tillägget försäljning och lagerprognos för att hantera lager
description: 'Det här tillägget låter dig förutse försäljning, få en tydlig översikt över förväntat slut i lager och du kan till och med skapa återanskaffningsförfrågningar till leverantörer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'app, add-in, manifest, customize, budget'
ms.search.form: '1850, 1851, 1853,'
ms.date: 07/01/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="the-sales-and-inventory-forecast-extension"></a>Tillägget Försäljning och lagerprognos

Lagerhantering är en kompromiss mellan kundservice och hantering av din kostnad. Å ena sidan kräver ett lågt lager mindre rörelsekapital, men å andra sidan leder eventuellt slut i lager till missade försäljningar. Tilläggen för Försäljning och Lagerprognos förutsäger potentiella försäljningar med hjälp av historiska data och ger en tydlig översikt av förväntade slut i lager. Baserat på prognosen hjälper tilläggen till att skapa påfyllningförfrågningar till dina leverantörer, vilket sparar tid.  

## <a name="setting-up-forecasting"></a>Konfigurera prognoser

I [!INCLUDE[prod_short](includes/prod_short.md)] har anslutningen till [Azure AI](https://azure.microsoft.com/overview/ai-platform/) redan ställts in åt dig. Men du kan konfigurera prognosen till att använda en annan typ av period att rapportera efter, t.ex ändra från prognos per månad till prognos per kvartal. Du kan även välja antal perioder att beräkna prognosen efter, beroende på hur många detaljnivåer du vill att prognosen ska vara. Vi föreslår att du gör prognoser per månad och med en 12 månaders horisont för prognosen.

> [!TIP]  
> Beakta längden för perioderna som tjänsten ska använda i dess beräkningar. Ju mer information som du anger, desto mer exakta kommer prognoserna att vara. Se upp för stora avvikelser i perioder. De kommer också att påverka prognoserna. Om Azure AI inte hittar tillräckligt med data, eller om data varierar mycket, kommer tjänsten inte att utföra någon prognos.

## <a name="use-the-forecasts"></a>Att använda prognoserna

Detta tillägg använder funktionerna i Azure AI för att förutsäga framtida försäljningar som baseras på din försäljninghistorik för att undvika lagerbrist. När du till exempel väljer en artikel på sidan **Artiklar** visar diagrammet i fönstret **Prognostiserad artikel** de beräknade försäljningarna av artikeln i den kommande perioden. På så sätt kan du se om du förmodligen kommer att få slut på lagret av artikeln snart.  

Du kan också använda tillägget för att föreslå när du ska fylla på lagret. Du kan till exempel skapa en inköpsorder för att Fabrikam ska köpa deras nya skrivbordsstol. Tillägget Försäljnings- och lagerprognos kan föreslå att du också fyller på LONDON snurrstol som du brukar köpa från den här leverantören. Tillägget kan förutse att du snart kommer att få slut på lager av LONDON snurrstol, så du kanske vill beställa fler stolar redan nu.  

## <a name="design-details"></a>Designdetaljer

Prenumerationer på [!INCLUDE[prod_short](includes/prod_short.md)] inkluderar åtkomst till ett flertal prediktiva webbtjänster i alla regioner där [!INCLUDE[prod_short](includes/prod_short.md)] finns tillgängligt. Mer information finns i Licensieringsguiden för Microsoft Dynamics 365 Business Central. Guiden kan hämtas på webbplatsen för [Business Central](https://dynamics.microsoft.com/en-us/business-central/overview/). 

Dessa webbtjänster är tillståndslösa, vilket innebär att de endast använder data för att beräkna förutsägelser vid behov. Inga data lagras.

> [!NOTE]  
>   Du kan också använda din egen prediktiva webbtjänst i stället för vår. Mer information finns i [Skapa och använda din egen prediktiva webbtjänst för försäljnings- och lagerprognoser](#AnchorText). 

### <a name="data-required-for-forecast"></a>Data som krävs för prognoser

För att du ska kunna göra förutsägelser om framtida försäljning kräver webbtjänsten kvantitativa data om tidigare försäljning. Dessa data hämtas från fälten **Bokföringsdatum**, **Artikelnr** och **Antal** på sidan **Artikeltransaktioner**, där:

- Transaktionens typ är "Försäljning".
- Bokföringsdatumet infaller mellan det datum som beräknas baserat på värdena i fälten **Historiska perioder** och **Periodtyp** på sidan **Inställningar för försäljnings- och lager prognos** och arbetsdatum.

Innan den använder webbtjänsten komprimerar [!INCLUDE[prod_short](includes/prod_short.md)] transaktionerna efter **Artikelnr** och **Bokföringsdatum** baserat på värdet i fältet **Periodtyp** på sidan **Inställningar för försäljnings- och lagerprognos**.

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-sales-and-inventory-forecasts"></a><a name="AnchorText"> </a>Skapa och använda din egen prediktiva webbtjänst för försäljnings- och lagerprognoser

För [!INCLUDE[prod_short](includes/prod_short.md)] online publiceras modellen av Microsoft och är ansluten till Microsoft-prenumerationen. För andra distributionsalternativ måste du skapa Machine Learning-resurser i din egen Azure-prenumeration. Exempelstegen finns på [exempellagringsplatsen](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Syftet med den här uppgift är att hämta API-URI:n och API-nyckeln.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inställningar för försäljnings- och lagerprognoser** och väljer sedan relaterad länk.  
2. Expandera snabbfliken **Allmänt** och fyll sedan i fälten för API-URL och API-nyckel.  

## <a name="see-also"></a>Se även

[Försäljning](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Använd artificiell intelligens i Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  
[Försäljnings-API översikt](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
