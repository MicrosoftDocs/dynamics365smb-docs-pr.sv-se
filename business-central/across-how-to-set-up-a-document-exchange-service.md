---
title: Så här konfigurerar du en dokumentväxlingstjänst | Microsoft Docs
description: Du kan använda en tjänstleverantör för att utbyta elektroniska dokument med dina handelspartner.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 75880e3315933831bf20fa9c5e8ce6a1528b935e
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785102"
---
# <a name="set-up-a-document-exchange-service"></a>Konfigurera en tjänst för dokumentutbyte
Du kan använda en tjänstleverantör för att utbyta elektroniska dokument med dina handelspartner. Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Konfigurera en dokumentväxlingstjänst  
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för dokumentöverföring** och välj sedan tillhörande länk.  
2. Fyll i fälten enligt beskrivningen i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Användare**|Ange valfri text som kan användas för att identifiera ditt företag i dokumentväxlingsprocesser.|  
    |**Klientorganisations-ID för dok.väx.**|Ange den klientorganisation i dokumentväxlingstjänsten som representerar ditt företag. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  
    |**Aktiv**|Ange om tjänsten är aktiverad. **Obs!** Så fort du aktiverar tjänsten skapas minst två jobbköposter för att bearbeta trafiken med elektroniska dokument in i och ut ur [!INCLUDE[d365fin](includes/d365fin_md.md)]. När du inaktiverar servicen tas jobbköposterna bort.|  
    |**Registrerings-URL**|Ange webbsidan där du registrerade dig för dokumentväxlingstjänsten.|  
    |**Servicesida**|Ange adressen till dokumentväxlingstjänsten som ska anropas när du skickar och tar emot elektroniska dokument.|  
    |**InloggningsURL**|Ange inloggningssidan för dokumentväxlingstjänsten, det vill säga där du anger företagets användarnamn och lösenord för att logga in till tjänsten.|  
    |**Användarnyckel**|Ange den 3-ledade OAuth-nyckeln för konsumentnyckeln. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  
    |**Konsumenthemlighet**|Ange hemligheten som skyddar konsumentnyckeln. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  
    |**Token**|Ange den 3-ledade OAuth-nyckeln för token. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  
    |**Tokenhemlighet**|Ange hemligheten som skyddar token. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  

    > [!NOTE]  
    > Dina inloggningsdata krypteras automatiskt.

## <a name="see-also"></a>Se även  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md)
