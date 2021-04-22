---
title: Skapa nya företag med en assisterad konfiguration | Microsoft Docs
description: Det är enkelt att skapa ett nytt, tomt företag i Business Central. En assisterad konfiguration hjälper dig genom stegen och du kan importera dina befintliga affärsdata.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: cb1639a57dcfed21b71d9c9cd57cd6090e5e81d7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776378"
---
# <a name="creating-new-companies-in-prod_short"></a>Skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] tillhör behållaren för affärsdata en affärsenhet eller juridisk person som kallas ett *företag*. När du registrerar dig för [!INCLUDE[prod_short](includes/prod_short.md)] får du ett demonstrationsföretag och ett tomt företag, *Mitt företag*. Att växla mellan företag är enkelt: gå bara till **Mina inställningar** och flytta till det andra företaget. Men du kan också skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)] beroende på dina affärsbehov. När du skapar ett nytt företag får du hjälp med de grundläggande inställningarna av en assisterad konfiguration. Du kan sedan importera relevanta data från ditt gamla system eller från något annat företag i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="creating-a-new-company"></a>Skapa ett nytt företag

Om du bestämmer dig för att lägga till ett företag till din [!INCLUDE[prod_short](includes/prod_short.md)] kan du använda den assisterade inställningsguiden **Skapa nytt företag** för att komma igång. Assisterad konfiguration är tillgänglig från sidan **Företag** och från sökfunktionen i fältet **Företag** på sidan **Mina inställningar**.  

I installationsguiden finns tre mallar och ett tomt alternativ:

- **Utvärdering – exempeldata**  
    Detta skapar ett företag som liknar demonstrationsföretaget med exempeldata och inställningsdata.  
- **Produktion – endast inställningsdata**  
    Detta skapar ett företag som liknar **Mitt företag** med inställningsdata, men utan exempeldata.
- **Avancerad utvärdering – fullständiga exempeldata** Detta skapar ett företag med inställningar och fullständig exempeldata för alla funktioner, till exempel produktion och service.
- **Skapa ny – Inga data**  
    Detta skapar ett tomt företag utan inställningsdata.  

Om du vill komma igång snabbt med ett nytt företag väljer du **Produktion – endast inställningsdata** och importerar sedan dina egna affärsdata, till exempel kunder, artiklar och leverantörer. Välj mallen **Nytt** om du vill ställa in allt från början. Om så är fallet kan du använda den assisterade konfigurationen **Företagsinställningar** som hjälper dig att komma igång med grundläggande inställningsdata.  

> [!NOTE]  
> När du skapar ett nytt företag tar detnågra minuter innan du kan öppna det i [!INCLUDE[prod_short](includes/prod_short.md)]. Inställningsstatus på sidan **Företag** visas när det nya företaget är redo för dig. Sedan kan du växla till det nya företaget med hjälp av **Mina inställningar**.  

Du kan skapa valfritt antal nya företag under en utvärderingsversion på 30 dagar, men de kan bara användas under utvärderingsperioden. Kontakta din [!INCLUDE[prod_short](includes/prod_short.md)]-partner för mer information.  

## <a name="copying-a-company"></a>Kopiera ett företag

På sidan **Företag** kan du använda åtgärden **Kopiera** för att skapa ett andra företag baserat på innehållet i ett befintligt företag. Detta är användbart om du t. ex. vill testa ett företag utan att störa produktionsdata.

> [!Important]
> Den här funktionen kan inte användas för att göra en säkerhetskopia av ett företag. När du gör en säkerhetskopia av ett företag börjar du genom att exportera databasen som en .bacpac-fil. Mer information finns i [Exportera databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjälpen för utvecklare och administration.

## <a name="company-setup"></a>Företagsinställning

När du loggar in på ett nytt företag körs guiden **företagsinställningar** automatiskt och hjälper dig att komma igång. Du kommer att få information om företaget, till exempel adress, bankuppgifter och lagervärderingsprincip. Vi ber om denna information eftersom den används som grund för många områden i [!INCLUDE[prod_short](includes/prod_short.md)] som du sedan inte måste konfigurera manuellt senare.  

Till exempel din företagsadress ingår i fakturor och andra dokument, din bankinformation används i betalningar och värderingsprincipen används för att beräkna priser och även lagervärdering.  

När du har grundläggande inställningar på plats kan du ställa in återstående huvudområden. Sedan är du redo att lägga till affärsdata som t. ex. kunder och leverantörer. Mer information finns i [Skapa [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Företag och miljöer

[!INCLUDE [company_environment](includes/company_environment.md)]

Mer information finns i [byta till ett annat företag eller annan miljö](ui-organization-switch.md). 

## <a name="changing-a-companys-name"></a>Ändra ett företags namn

När ett företag har skapats kan du inte ändra namnet. Du kan emellertid ändra dess **Visningsnamn**, d.v.s. den text som ska visas för företaget i hela programmet.  

> [!TIP]
> Du kan byta namn på ett företag om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.

## <a name="see-also"></a>Se även

[Anpassa Business Central](ui-customizing-overview.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importera affärsdata från andra finanssystem](across-import-data-configuration-packages.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]