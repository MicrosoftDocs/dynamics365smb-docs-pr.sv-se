---
title: Designdetaljer - Disposition av artikelspårning | Microsoft Docs
description: Sidorna Artikelspårningsrader och Artikelspårning sammandrag dynamisk dispositionsinformationen för serie-/partinummer. Avsikten med detta är att öka transparensen för användare på avgående dokument, t. ex. försäljningsorder, genom att visa dem vilka serienummer eller hur många enheter av partinumret som för närvarande tilldelas på andra öppna dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8fd2fc7c6eb3a4c413691d4eb0b9f5f86aba3fe9
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215884"
---
# <a name="design-details-item-tracking-availability"></a>Designdetaljer: Disposition av artikelspårning
Sidorna **Artikelspårningsrader** och **Artikelspårning sammandrag** ger dynamisk dispositionsinformationen för serie-/partinummer. Avsikten med detta är att öka transparensen för användare på avgående dokument, t. ex. försäljningsorder, genom att visa dem vilka serienummer eller hur många enheter av partinumret som för närvarande tilldelas på andra öppna dokument. Det minskar osäkerhet som orsakas av dubbel fördelning, och gör att orderhandläggarna kan känna sig säkra på att artikelspårningsnumren och datumen som utlovas på försäljningsorder som inte har bokförts kan uppfyllas. Mer information finns i [Designdetaljer: Sida för artikelspårningsrader](design-details-item-tracking-lines-window.md).  

 När du öppnar sidan **Artikelspårningsrader** hämtas tillgänglighetsdata från tabellen **Artikeltransaktion** och tabellen **Reservationstransaktion** utan datumfilter. När du väljer fältet **Serienr** eller fältet **Partinr** öppnas sidan **Artikelspårning sammandrag** och en översikt av informationen om artikelspårning visas i tabellen **Reservationstransaktion**. Översikten innehåller följande information om varje serie- eller partinummer på artikelspårningsraden:  

|Fält|Beskrivning|  
|---------------------------------|---------------------------------------|  
|**Totalt antal**|Det totala antalet av det parti- eller serienummer som för närvarande finns i lager.|  
|**Totalt begärt antal**|Det totala antalet av det parti- eller serienummer som för närvarande har beställts i alla dokument.|  
|**Aktuellt pågående antal**|Antalet som anges i aktuell instans av sidan **Artikelspårningsrader** men som inte ännu har skickats till databasen.|  
|**Totalt disponibelt antal**|Antalet av serie- eller partinumret som är tillgängligt för användaren att begära.<br /><br /> Antalet beräknas från andra fält på sidan enligt följande:<br /><br /> totalt antal – (totalt begärt antal + aktuellt pågående antal).|  

> [!NOTE]  
>  Du kan också se information i den föregående tabellen med hjälp av funktionen **Markera transaktioner** på sidan **Artikelspårningsrader**.  

 För att bevara databasprestanda hämtas tillgänglighetsdata bara en gång från databasen när du öppnar sidan **Artikelspårningsrader** och använder funktionen **Uppdatera tillgänglighet** på sidan.  

## <a name="calculation-formula"></a>Beräkningsformel  
 Som beskrivs i föregående tabell beräknas tillgängligheten av ett visst serie- eller partinummer så här.  

 totalt disponibelt antal = antal i lager – (alla behov + antal som ännu inte allokerats till databasen)  

> [!IMPORTANT]  
>  Följande formel betyder att dispositionsberäkningar för serie- eller partinummer endast beaktar lager och ignorerar planerade inleveranser. Leveranser som inte ännu har bokförts till lagret påverkar inte artikelspårningsdisposition, i motsats till vanlig artikeldispositionen där planerade inleveranser inkluderas.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Objektspårning](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]