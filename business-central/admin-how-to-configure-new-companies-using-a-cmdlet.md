---
title: "Så här konfigurerar du nya företag som använder en Cmdlet | Microsoft Docs"
description: "I ett antal scenarier kanske du vill läsa in och importera ett konfigurationspaket utan att blanda in dina användare eller använda RapidStart Services-användargränssnittet. Du kan göra detta genom att använda en Windows PowerShell-cmdlet."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Så här konfigurerar du nya företag med Cmdlet
I ett antal scenarier kanske du vill läsa in och importera ett konfigurationspaket utan att blanda in dina användare eller använda RapidStart Services-användargränssnittet. Du kan göra detta genom att använda en Windows PowerShell-cmdlet. Scenarier där det kan vara användbart, inkluderar:  

- Utföra dataimport på olika [!INCLUDE[d365fin](includes/d365fin_md.md)]-installationer.
- Konfigurera ytterligare moduler för flera kunder.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Så här distribuerar du ett konfigurationspaket med hjälp av en cmdlet  

1. Förbereda ett RapidStart Services-paket. Du kan till exempel skapa ett paket för att importera vissa värden och namnen på tabellen och fälten att infoga dessa värden i.  
2. Markera paketet på en dator där du vill köra cmdleten.  
3. Öppna [!INCLUDE[d365fin](includes/d365fin_md.md)]-administrationsgränssnittet.  
4. Ange **Anropa-NAVCodeUnit** och ange information som är liknande till följande exempel.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
Cmdleten importerar godset till varje företag. Användare kan börja använda den nya funktionenomedelbart.  

## <a name="see-also"></a>Se även  
[Konfigurera nya företag](admin-how-to-configure-new-companies.md)  
[Koppla konfigurationen till nya företag](admin-apply-configuration-to-new-companies.md)  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV Windows PowerShell-Cmdlet:ar](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

