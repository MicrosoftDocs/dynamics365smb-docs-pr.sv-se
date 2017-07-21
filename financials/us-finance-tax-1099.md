---
title: Rapportering av 1099-transaktioner i USA | Microsoft Docs
description: "IRS kräver skatteformuläret 1099 för betalning till leverantörer och du kan ange att ett inköpsdokument är 1099 skattepliktigt och ange koden 1099 för leverantören."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c20c52927aa979e56aeef7975fbcee1564ca4dd7
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-transactions-as-1099-liable-in-the-us"></a>Rapportering av skattepliktiga 1099-transaktioner i USA

Det amerikanska skatteverket (IRS) kräver en eller flera versioner av 1099-skatteblanketten för betalningar till leverantörer. Kopior av dessa blanketter måste skickas årligen till leverantörer på eller före den sista dagen i januari. I dina inköpsdokument kan du ställa in att dokumentet gäller under 1099, och du kan dessutom ställa in 1099-koden för leverantören.  

## <a name="1099-codes"></a>1099-koder
I [!INCLUDE[d365fin](includes/d365fin_md.md)] är de vanligaste 1099-koderna förinställda åt dig, så att du omgående kan skapa de rapporter som behövs. Koderna ställa in i fönstret **IRS 1099-blankettruta**, där du också kan lägga till nya 1099-koder. För varje skattepliktig leverantör kan du sedan ställa in relevant 1099-kod på snabbfliken **Betalningar** på leverantörskortet.  

Med rapporten **1099-information för leverantören** kan du granska 1099-transaktioner som betalats under en viss tidsperiod. I slutet av året kan du skriva ut 1099-transaktioner på förtryckta blanketter.  

## <a name="printing-1099-tax-forms"></a>Utskrift av 1099-skatteblanketter
Via fönstret **IRS 1099-blankettruta** får du åtkomst till följande skatteblanketter:  

* Leverantörens 1099-Div  

  Skriver ut den federala blanketten 1099-DIV för utdelning och distribution. Du kan skriva ut alla eller specifika 1099-DIV-blanketter. Rapporten använder koder som gäller för DIV-blankettens belopprutor från fönstret **IRS 1099-blankettruta**.  
* Leverantörens 1099 Int  

  Skriver ut den federala blanketten 1099-INT för ränteintäkter. Du kan skriva ut alla eller specifika 1099-INT-blanketter. Rapporten använder de koder som gäller för INT-blankettens belopprutor från fönstret **IRS 1099-blankettruta**.  
* Leverantörens 1099 Misc - diverse intäkter  

  Skriver ut den federala blanketten 1099-MISC för diverse intäkter. Du kan skriva ut alla eller specifika 1099-MISC-blanketter. Rapporten använder koder som gäller för MISC-blankettens belopprutor från fönstret **IRS 1099-blankettruta**.  

Lagstadgade ändringar som påverkar den här rapporten och tabelldatan administreras vanligtvis i uppdateringar i slutet av året.
Det kan vara till hjälp att köra rapporten **1099-information för leverantören** när du vill granska informationen innan du skriver ut blanketterna.

## <a name="submitting-1099-tax-forms-electronically"></a>Skicka 1099-skatteblankett elektroniskt
Om du vill skicka 1099-skatteblanketterna elektroniskt, använd då rapporten **1099-magnetiska medier för leverantören**. Anger de 1099-blanketter som kan exporteras. Blankettinformationen som exporteras av den här rapporten är densamma som de rapporter som skriver ut 1099-blanketter som beskrivs i föregående avsnitt.  

Rapporten använder koder som gäller för blankettens belopprutor från fönstret **IRS 1099-blankettruta**. Koderna är kopplade till blankettrutorna i rapportens fillayouter, och därför måste tabelldata och rapportversion för ett visst taxeringsår överensstämma. Om anpassade koder läggs till i tabellen måste dessa mappas till blankettrutorna i detta objekt.  

Lagstadgade ändringar som påverkar den här rapporten och tabelldatan administreras vanligtvis i uppdateringar i slutet av året.
Det kan vara till hjälp att köra rapporten **1099-information för leverantören** när du vill granska informationen innan du skapar den elektroniska filen.  

## <a name="see-also"></a>Se även
[Så här registrerar du nya leverantörer](purchasing-how-register-new-vendors.md)  
[Så här registrerar du inköp](purchasing-how-record-purchases.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

