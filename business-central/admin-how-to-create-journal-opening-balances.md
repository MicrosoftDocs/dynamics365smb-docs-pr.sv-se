---
title: Så här skapar du ingående saldon för journalen | Microsoft Docs
description: Business Central innehåller flera batch-jobb som tillhandahålls som hjälp vid överföringen av bakåtkompatibla kontosaldon till ett nykonfigurerat företag. Du kan enkelt överföra data med bokföring i journaler.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e1bb8e34e70d1d906850c157107b9b9701c6c50
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779863"
---
# <a name="create-journal-opening-balances"></a>Skapa ingående saldon för journalen

[!INCLUDE[prod_short](includes/prod_short.md)] innehåller flera batch-jobb som tillhandahålls som hjälp vid överföringen av bakåtkompatibla kontosaldon till ett nytt konfigurerat företag. Det är enkelt att överföra dessa data för kundjournalen, leverantörsjournalen, artikeljournalen och redovisningsjournalen.

Det första steget är att skapa ett konfigurationspaket som innehåller inställningstabeller för dessa journaler. I följande procedur förutsätts att detta steg har utförts. Mer information finns i [Skapa redovisningsjournaler](admin-set-up-company-configuration.md). Denna procedur beskriver de efterföljande stegen, bland annat koppling av paketet som tillhandahålls av en partner.  

Innan du börjar rekommenderar vi att du använder administreringssidan för Rollcenter, detta då denna ger rätt sammanhang för ditt konfigurationsarbete. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Så här kan du koppla transaktionerna i en journal till ett nytt företag

1. Konfigurera ett nytt företag och koppla ett konfigurationspaket till det. Mer information finns i [Konfigurera ett företag med RapidStart-guiden](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Det nya företaget innehåller inte information om IB till journalen.  

2. Öppna konfigurationskalkylarket och importera befintliga data om kunder, artiklar, leverantörer och redovisningen. Mer information finns också i  [Så här migrerar du kunddata](admin-migrate-customer-data.md).  

    Nu finns det huvuddata på plats. Sedan lägger du till ingående saldo. Följande steg beskriver hur du skapar journalrader för redovisningskonton, men samma gäller för att skapa journalrader för kunder, leverantörer och artiklar.  
3. Välj åtgärden **Skapa kontojournalrader för redovisning**.  
4. Fyll i snabbfliken **Alternativ** och ange filter efter behov. Skriv till exempel ett namn i fältet **Journalmall**.  
5. Välj knappen **OK**. Posterna är nu i journalen, men beloppen är tomma.  
6. Exportera journaltabellen till Excel och ange bokförings- och motkontoinformationen manuellt från bakåtkompatibla data.
7. Importera och koppla tabellinformationen till det nya företaget. Journalraderna är klara för bokföring.  
8. Välj journalradtabellen i konfigurationskalkylarket och välj sedan åtgärden **Databasdata**.  
9. Granska informationen och välj sedan åtgärden **Bokför**.  
10. Upprepa stegen för att importera och bokföra alla ingående saldon.  

> [!TIP]
> Du kan använda samma batch-jobb för att lägga till ingående saldo när du registrerar en ny kund eller leverantör som du har gjort affärer med tidigare men inte registrerat i [!INCLUDE [prod_short](includes/prod_short.md)]. Sök bara efter den relevanta uppgiften och välj sedan önskad länk.

## <a name="see-also"></a>Se även

[Koppla konfigurationen till nya företag](admin-apply-configuration-to-new-companies.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]