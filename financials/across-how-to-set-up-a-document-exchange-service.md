---
title: "Så här konfigurerar du en dokumentväxlingstjänst | Microsoft Docs"
description: "Du kan använda en tjänstleverantör för att utbyta elektroniska dokument med dina handelspartner."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: c014e3ee7ed580fd893470c0e0b89273eaceb429
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-set-up-a-document-exchange-service"></a>Så här konfigurerar du en dokumentväxlingstjänst
Du kan använda en tjänstleverantör för att utbyta elektroniska dokument med dina handelspartner. Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Konfigurera en dokumentväxlingstjänst  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "ikonen Söka efter sida eller rapport"), ange **Serviceinställningar för dok.väx.** och välj sedan relaterad länk.  
2. Fyll i fälten enligt beskrivningen i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Användare**|Ange valfri text som kan användas för att identifiera ditt företag i dokumentväxlingsprocesser.|  
    |**Klientorganisations-ID för dok.väx.**|Ange den klientorganisation i dokumentväxlingstjänsten som representerar ditt företag. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  
    |**Aktiv**|Ange om tjänsten är aktiverad. **Obs!**Så fort du aktiverar tjänsten skapas minst två jobbköposter för att bearbeta trafiken med elektroniska dokument in i och ut ur [!INCLUDE[d365fin](includes/d365fin_md.md)]. När du inaktiverar servicen tas jobbköposterna bort.|  
    |**Registrerings-URL**|Ange webbsidan där du registrerade dig för dokumentväxlingstjänsten.|  
    |**Servicesida**|Ange adressen till dokumentväxlingstjänsten som ska anropas när du skickar och tar emot elektroniska dokument.|  
    |**InloggningsURL**|Ange inloggningssidan för dokumentväxlingstjänsten, det vill säga där du anger företagets användarnamn och lösenord för att logga in till tjänsten.|  
    |**Användarnyckel**|Ange den 3-ledade OAuth-nyckeln för konsumentnyckeln. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  
    |**Konsumenthemlighet**|Ange hemligheten som skyddar konsumentnyckeln. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  
    |**Token**|Ange den 3-ledade OAuth-nyckeln för token. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  
    |**Tokenhemlighet**|Ange hemligheten som skyddar token. Den tillhandahålls av leverantören av dokumentväxlingstjänsten.|  

> [!NOTE]  
>  Du rekommenderas att skydda de inloggningsuppgifter som du anger i fönstret **VAN-serviceinställningar**. Du kan kryptera data på servern genom att skapa nya eller importera befintliga krypteringsnycklar som aktiverar på serverinstansen med anslutningen till databasen. Beskriv i följande procedur.  

## <a name="to-encrypt-your-logon-information"></a>Så här krypterar du dina inloggningsuppgifter  
1. I fönstret **VAN-serviceinställningar** väljer du åtgärden **Krypteringshantering**.  
2. Aktivera krypteringen av dina data i fönstret **Datakrypteringshantering**. <!--For more information, see [Manage Data Encryption](../manage-data-encryption.md).-->  

## <a name="see-also"></a>Se även  
[Konfigurera datautbyte](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md).

