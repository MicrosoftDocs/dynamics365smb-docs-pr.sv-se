---
title: "Designdetaljer - Disposition av artikelspårning | Microsoft Docs"
description: "Fönstren **Artikelspårningsrader** och **Artikelspårning sammandrag** ger dynamisk dispositionsinformationen för serie- / partinummer. Avsikten med detta är att öka transparensen för användare på avgående dokument, t.ex. försäljningsorder, genom att visa dem vilka serienummer eller hur många enheter av partinumret som för närvarande tilldelas på andra öppna dokument. Det minskar osäkerhet som orsakas av dubbel fördelning, och gör att orderhandläggarna kan känna sig säkra på att artikelspårningsnumren och datumen som utlovas på försäljningsorder som inte har bokförts kan uppfyllas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bd69a3da7a0a5e766a232e8999056ac60109e7b1
ms.openlocfilehash: cdfb96475c46d56f32e5f0133efc7852a10ae446
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-availability"></a>Designdetaljer: Disposition av artikelspårning
Fönstren **Artikelspårningsrader** och **Artikelspårning sammandrag** ger dynamisk dispositionsinformationen för serie- / partinummer. Avsikten med detta är att öka transparensen för användare på avgående dokument, t.ex. försäljningsorder, genom att visa dem vilka serienummer eller hur många enheter av partinumret som för närvarande tilldelas på andra öppna dokument. Det minskar osäkerhet som orsakas av dubbel fördelning, och gör att orderhandläggarna kan känna sig säkra på att artikelspårningsnumren och datumen som utlovas på försäljningsorder som inte har bokförts kan uppfyllas. Mer information finns i [Designdetaljer:  Fönster för artikelspårningsrader](design-details-item-tracking-lines-window.md).  

 När du öppnar fönstret **Artikelspårningsrader** hämtas tillgänglighetsdata från tabellen **Artikeltransaktion** och tabellen **Reservationstransaktion** utan datumfilter. När du väljer fältet **Serienr** eller fältet **Partinr** öppnas fönstret **Artikelspårning sammandrag** och en översikt av informationen om artikelspårning visas i tabellen **Reservationstransaktion**. Översikten innehåller följande information om varje serie- eller partinummer på artikelspårningsraden:  

|Fält|Beskrivning|  
|---------------------------------|---------------------------------------|  
|**Totalt antal**|Det totala antalet av det parti- eller serienummer som för närvarande finns i lager.|  
|**Totalt begärt antal**|Det totala antalet av det parti- eller serienummer som för närvarande har beställts i alla dokument.|  
|**Aktuellt pågående antal**|Antalet som anges i aktuell instans av fönstret **Artikelspårningsrader** mens som inte ännu har skickats till databasen.|  
|**Totalt disponibelt antal**|Antalet av serie- eller partinumret som är tillgängligt för användaren att begära.<br /><br /> Antalet beräknas från andra fält i fönstret enligt följande:<br /><br /> totalt antal – (totalt begärt antal + aktuellt pågående antal).|  

> [!NOTE]  
>  Du kan också se information i den föregående tabellen med hjälp av funktionen **Markera transaktioner** i fönstret **Artikelspårningsrader**.  

 För att bevara databasprestanda hämtas tillgänglighetsdata bara en gång från databasen när du öppnar fönstret **Artikelspårningsrader** och använder funktionen **Uppdatera tillgänglighet** i fönstret.  

## <a name="calculation-formula"></a>Beräkningsformel  
 Som beskrivs i föregående tabell beräknas tillgängligheten av ett visst serie- eller partinummer så här.  

 totalt disponibelt antal = antal i lager – (alla behov + antal som ännu inte allokerats till databasen)  

> [!IMPORTANT]  
>  Följande formel betyder att dispositionsberäkningar för serie- eller partinummer endast beaktar lager och ignorerar planerade inleveranser. Leveranser som inte ännu har bokförts till lagret påverkar inte artikelspårningsdisposition, i motsats till vanlig artikeldispositionen där planerade inleveranser inkluderas.  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Objektspårning](design-details-item-tracking.md)

