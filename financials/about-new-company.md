---
title: "Skapa nya företag med en assisterad konfiguration | Microsoft Docs"
description: "Det är enkelt att skapa ett nytt, tomt företag i Dynamics 365 Business edition. En assisterad konfiguration hjälper dig genom stegen och du kan importera dina befintliga affärsdata."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 07/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c4152a77fcd3e5995aaf09c17b0a3a2c227aa2fa
ms.contentlocale: sv-se
ms.lasthandoff: 11/10/2017

---
# <a name="creating-new-companies-in-included365finlongincludesd365finlongmdmd"></a>Skapa nya företag i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
I [!INCLUDE[d365fin](includes/d365fin_md.md)] tillhör behållaren för affärsdata en affärsenhet eller juridisk person som kallas ett *företag*. När du registrerar dig för [!INCLUDE[d365fin](includes/d365fin_md.md)] får du ett demonstrationsföretag och ett tomt företag, *Mitt företag*. Att växla mellan företag är enkelt - gå bara till **Mina inställningar** och flytta till det andra företaget. Men du kan också skapa nya företag i [!INCLUDE[d365fin](includes/d365fin_md.md)], beroende på dina affärsbehov. När du skapar ett nytt företag får du hjälp med de grundläggande inställningarna av en assisterad konfiguration. Du kan sedan importera relevanta data från ditt gamla system eller från något annat företag i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="create-new-company"></a>Skapa nytt företag
Om du bestämmer dig för att lägga till ett företag till din [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du använda den assisterade konfigurationen **Skapa nytt företag** för att komma igång. Assisterad konfiguration är tillgänglig från fönstret **Företag** och från sökfunktionen i fältet **Företag** i **Mina inställningar**.  

Den assisterade konfigurationen erbjuder tre mallar:

-   **Suite-utvärdering**  
    Detta skapar ett företag som liknar demonstrationsföretaget med exempeldata och inställningsdata.  
-   **Suite-produktion**  
    Detta skapar ett företag som liknar **Mitt företag** med inställningsdata, men utan exempeldata.  
-   **Ny**  
    Detta skapar ett tomt företag utan inställningsdata.  

Om du vill komma igång snabbt med ett nytt företag, väljer du **Suite-produktion** och importerar sedan dina egna affärsdata, till exempel kunder, artiklar och leverantörer. Välj mallen **Nytt** om du vill ställa in allt från början. Om så är fallet kan du använda assisterade konfigurationen **Företagsinställningar** som hjälper dig att komma igång med grundläggande inställningsdata.  

> [!NOTE]  
>   När du skapar ett nytt företag tar detnågra minuter innan du kan öppna det i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Inställningsstatus i fönstret **Företag** visas när det nya företaget är redo för dig. Sedan kan du växla till det nya företaget med hjälp av **Mina inställningar**.  

Du kan skapa valfritt antal nya företag under en utvärderingsversion på 30 dagar, men de kan bara användas under utvärderingsperioden. Kontakta din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner för mer information.  

## <a name="company-setup"></a>Företagsinställning
När du loggar in på ett nytt företag körs guiden **företagsinställningar** automatiskt och hjälper dig att komma igång. Du kommer att få information om företaget, till exempel adress, bankuppgifter och lagervärderingsprincip. Vi ber om denna information eftersom den används som grund för många områden i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du sedan inte måste konfigurera manuellt senare.  

Till exempel din företagsadress ingår i fakturor och andra dokument, din bankinformation används i betalningar och värderingsprincipen används för att beräkna priser och även lagervärdering.  

När du har grundläggande inställningar på plats kan du ställa in återstående huvudområden. Sedan är du redo att lägga till affärsdata som t.ex. kunder och leverantörer. Mer information finns i [Konfigurera Dynamics 365 Business edition](setup.md).  

## <a name="see-also"></a>Se även
[Konfigurera Dynamics 365 Business edition](setup.md)  
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

