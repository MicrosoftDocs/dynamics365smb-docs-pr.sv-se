---
title: Hållbarhetskort och mål
description: Lär dig hur du ställer in och använder styrkort och mål för hållbarhet.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, scorecard, goal, forecast, budget'
ms.search.form: null
ms.date: 08/19/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# Översikt över styrkort och mål för hållbarhet

Den här artikeln innehåller vägledning om hur du skapar styrkort och mål och hur du uppdaterar statusen för mål. Styrkort och mål gör det möjligt för organisationer att kurera hållbarhetsmått och spåra dem mot viktiga affärsmål. Mål kan skapas baserat på nuvarande och målvärden, så att användarna kan hålla reda på utvecklingen av nuvarande utsläpp jämfört med tidigare perioder.  

## Skapa ett styrkort  

Följ stegen för att skapa ett *nytt styrkort* för hållbarhet:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") , ange **Styrkort** för hållbarhet och Välj sedan relaterad länk. 
2.  **På sidan Styrkort** för hållbarhet Välj **Ny** för att skapa ett nytt styrkort.  
3. Ange **nr.** Och fälten Namn på snabbfliken Allmänt **och lägg sedan till Ägare** . **·**  **·** 

> [NOTERA!]  **I fältet Ägare** kan du bara välja användare som har valt fältet **Hållbarhetsansvarig** i **tabellen Användarinställningar** . 

## Skapa mål  

För att skapa ett *nytt hållbarhetsmål*, följ stegen:

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") , ange **Styrkort** för hållbarhet och Välj sedan relaterad länk.
2.  **Välj åtgärden Mål** för att skapa ett nytt **hållbarhetsmål** för det valda styrkortet.  
3. Välj **Nytt** att börja skapa ett nytt mål.
4.  **Styrkort: nr.** Läggs till automatiskt baserat på värdet från det anslutna **hållbarhetsstyrkortet**, och användaren kommer inte att kunna redigera det här fältet. Systemet ställer också in **fältet Enhet** baserat på **koden Utsläppsenhet** på **sidan Hållbarhetsinställningar** .  
5. Du måste fylla i **Nej.** och **Namn** på nytt **hållbarhetsmål**. Fältet **Ägare** fylls i automatiskt baserat på värdet från det anslutna **hållbarhetskortet**.   
6. Användare kan välja att skapa *hållbarhetsmål* för hela företaget, ett specifikt land/en specifik region eller en anläggning. Om användarna vill skapa ett specifikt mål måste de välja land eller region i fältet Lands-/regionkod eller anläggningen i **fältet** Ansvarsenhet **.**   
7.  **VäljStartdatum** och **Slutdatum** fält för att ställa in dedikerad period för spårning av aktuella värden. Den här konfigurationen bestämmer värdena i följande fält: **Aktuellt värde för CO2**, **Aktuellt värde för CH4** och **Aktuellt värde för N2O**. 
8.  **VäljFälten Originalstartdatum** och **Originalplan slutdatum** om du vill ställa in en särskild originalperiod för jämförelse av aktuella värden. Den här konfigurationen bestämmer värdena i följande fält: **Baslinje för CO2**, **Baslinje för CH4** och **Baslinje för N2O**.
9. Användare kan också lägga till målvärden i det valda **fältet** Måttenhet för den aktuella perioden med hjälp av följande fält: **Målvärde för CO2**, **Målvärde för CH4** och **Målvärde för N2O**.   
10. Ett av dessa mål kan väljas som **huvudmål**. Värden från huvudmålet används i rollcentret **Hållbarhetsansvarig** .  

Om du har många mål på sidan kan du använda **åtgärden Visa mina mål** för att bara visa dina mål, och om du vill visa alla måste du köra **åtgärden Visa alla mål** .  

> [!NOTE]
> *Hållbarhetsmål* kan bara skapas för ett specifikt *hållbarhetsstyrkort* och du kan inte skapa mål som inte är relaterade till styrkortet, men du kan skapa fler mål för ett styrkort. Du kan bara ha ett **hållbarhetsmål** markerat som **huvudmål**.

> [!NOTE]
> Användare kan ställa in olika kombinationer av mål för hela företaget, specifika länder eller regioner och en ansvarsenhet för ett styrkort för *hållbarhet*. Användare kan också använda olika perioder för samma spårningsmodell. 

## Se även

[Hållbarhetskonfiguration](finance-sustainability-setup.md)    
[Kontoplan för hållbarhetskonton och huvudbok](finance-sustainability-accounts-ledger.md)    
[Så här registrerar du hållbarhetstransaktioner](finance-sustainability-journal.md)    
[Ad hoc-analys av data för hållbarhet](ad-hoc-analysis-sustainability.md)    
[Hållbarhetsrapport och analys i Business Central](sustainability-reports.md)   
[Hållbarhets-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Ekonomi](finance.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
