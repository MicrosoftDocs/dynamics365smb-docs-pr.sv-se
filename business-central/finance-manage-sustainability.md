---
title: Översikt över hållbarhetsstyrning
description: Lära dig om funktionen för hållbarhetshantering genom att använda den information och resurser som tillhandahålls.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 06/19/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-management-overview"></a>Översikt över hållbarhetsstyrning

> [!IMPORTANT]
> Den här funktionen blir tillgänglig i Business Central från **utgivningscykel 1 för 2024**. Alla referenslänkar aktiveras när de är tillgängliga.

Business Central tillhandahåller en funktion för hållbarhetshantering hjälper dig övervaka och hantera organisationen och dess miljöpåverkan. Den här funktionen är utformad för att övervaka och reglera en organisations miljöavtryck genom att spåra olika utsläpp av växthusgaser (GHG). På detta sätt underlättar det rätt insikter. Funktionen stöder den grundläggande processen att samla in utsläppsdata via hållbarhetsjournaler. Du kan antingen ange kända data manuellt eller använda inbyggda metoder för att beräkna utsläppsavtryck.

> [!NOTE]
> Den här första versionen är en grund och är helt oberoende av andra Business Central-funktioner. Framtida versioner kommer emellertid att sträva efter närmare integration och kan automatisera vissa manuella processer.

Den första versionen av funktionen fokuserar på utsläpp av växthusgaser. ESG-standarden (miljö, socialt ansvar och styrning) definierar tre utsläpps-scopes:

- **Scope 1 utsläpp** inkluderar utsläpp från stationär och mobil förbränning och från oavsiktliga flyktiga utsläpp.
- **Scope 2 utsläpp** inkluderar indirekta utsläpp från den energigenerering som köps från elleverantörer.
- **Scope 3 utsläpp** inkluderar ett brett spektrum av utsläpp, från köpta varor och tjänster och kapitalvaror, bränsle- och energirelaterade aktiviteter, uppströms och nedströms transporter, genererat avfall, affärsresor och personalpendling, etc.

Med denna funktion kan du:

- Ställa in emissionsfaktorer för olika källor och kategorier av växthusgasutsläpp.
- Registrera utsläppsdata i hållbarhetsjournaler, antingen manuellt eller med hjälp av fördefinierade beräkningsmetoder.
- Bokför utsläppstransaktioner i hållbarhetsredovisningen, där du kan visa och analysera utsläppsdata efter olika dimensioner.
- Skapa hållbarhetsrapporter som visar organisationens prestanda för utsläpp av växthusgaser.

När du vill börja med hållbarhetshantering, se följande artiklar.

| Artikel | Description |
|---------|-------------|
| **Funktion** |             |
| [Hållbarhetskonfiguration](finance-sustainability-setup.md) | Den här artikeln innehåller information som hjälper dig att korrekt konfigurera hela hållbarhetsmodulen. |
| [Kontoplan för hållbarhetskonton och huvudbok](finance-sustainability-accounts-ledger.md) | Den här artikeln innehåller information om hur du ställer in diagram för hållbarhetskonton (CoSA), kontokategorier och underkategorier. Och även hur man analyserar information i hållbarhetstransaktioner. |
| [Registrera hållbarhetstransaktioner](finance-sustainability-journal.md) | Använd den här artikeln för att lära dig hur du arbetar med alla typer av hållbarhetsjournaler. |
| **Rapportering** |             |
| [Ad hoc-analys av data för hållbarhet](ad-hoc-analysis-sustainability.md) | Den här artikeln tillhandahåller information hur du använder ad-hoc-funktionen Dataanalys för att analysera data för hållbarhet direkt från listsidor och frågor. |
| [Hållbarhetsrapport och analys i Business Central](sustainability-reports.md) | Den här artikeln innehåller information om hur du använder integrerade rapporter och analyser relaterade till hållbarhet i Business Central. |
| **Integrationer** |             |
| [Hållbarhets-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json) | Använd den här artikeln för att lära dig hur du skapar anslutna appar som upprättar en punkt-till-punkt-anslutning mellan Business Central och hållbarhetslösningar eller tjänster som inte kommer från Microsoft med hjälp av API:er. |

## <a name="see-also"></a>Se även

[Hållbarhetskonfiguration](finance-sustainability-setup.md)    
[Kontoplan för hållbarhetskonton och huvudbok](finance-sustainability-accounts-ledger.md)    
[Registrera hållbarhetstransaktioner](finance-sustainability-journal.md)    
[Ad hoc-analys av data för hållbarhet](ad-hoc-analysis-sustainability.md)    
[Hållbarhetsrapport och analys i Business Central](sustainability-reports.md)   
[Hållbarhets-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Ekonomi](finance.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
