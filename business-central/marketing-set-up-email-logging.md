---
title: Ställa in e-postloggning | Microsoft Docs
description: Lär dig hur du kan omvandla e-postinteraktioner mellan säljare och kunder till verkliga affärsmöjligheter.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 13699c002402b6b6d32edc13dca3710fefff2129
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181268"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>Spåra utbyte av e-postmeddelanden mellan säljare och kontakter
Få ut mer av kommunikationen mellan säljare och dina befintliga eller potentiella kunder genom att följa upp e-postutbyten och sedan omvandla dem till olika affärsmöjligheter. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan tillsammans med Exchange Online spara en logg över de inkommande och utgående meddelandena. Du kan visa och analysera innehållet i varje meddelande på sidan **Interaktionslogg**.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-d365fin-to-log-email-messages"></a>Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)] för att logga e-postmeddelanden
Kom igång med e-postloggning i två enkla steg:

1. Anslut [!INCLUDE[d365fin](includes/d365fin_md.md)] till Exchange Online för din Office 365-prenumeration. Exchange Online hanterar dina e-postmeddelanden. Detta steg är enkelt att utföra med hjälp av en guide för assisterad konfiguration. Du behöver bara ha administratörsbehörigheter för ditt administratörskonto i Office 365. Du startar guiden genom att gå till **Assisterad konfiguration** och sedan välja **Konfigurera e-postloggning**. 
2. Kontrollera att du har angett giltiga e-postadresser i [!INCLUDE[d365fin](includes/d365fin_md.md)] för dina säljare och kontakter, beroende på om de är potentiella eller befintliga kunder. Det gör du genom att för varje kund eller säljare öppna kortet **Kontakt** eller **Säljare/Inköpare** och titta i fältet **E-post**.

> [!Tip]
> När du har slutfört stegen i guiden kan du kontrollera om kopplingen har lyckats. Sök efter **Marknadsföringsinställningar**, välj **Process**, sedan **Funktioner** och därefter **Validera konfiguration för e-postloggning**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Visa e-postutbyten i interaktionsloggen
[!INCLUDE[d365fin](includes/d365fin_md.md)] skapar en transaktion på sidan **Interaktionslogg** varje gång en säljare och en kontakt utbyter e-postmeddelanden. Om du vill visa interaktionsloggen öppnar du kortet **Kontakt** eller **Säljare/Inköpare** för den personen och väljer sedan **Navigera**, **Historik** och därefter **Interaktionslogg**. Det finns några saker som du kan göra med posterna i loggen, till exempel:

* Visa innehållet i e-postmeddelandet som utbytts genom att klicka på åtgärden **Visa bilagor**.
* Omvandla ett e-postutbyte till en affärsmöjlighet - Om en transaktion verkar lovande kan du omvandla den till en affärsmöjlighet och sedan hantera förloppet fram till en försäljning. Välj posten och välj sedan åtgärden **Skapa affärsmöjlighet**. Mer information finns i [Hantera försäljningsmöjligheter](marketing-manage-sales-opportunities.md).

## <a name="see-also"></a>Se även
[Hantera relationer](marketing-relationship-management.md)

