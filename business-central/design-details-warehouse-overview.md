---
title: Designdetaljer – Översikt över distributionslager
description: För att stödja den fysiska hanteringen av artiklar i zonen och på lagerplatsnivån måste all information spåras för varje transaktion eller transport i distributionslagret.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 95e6e88f1f448546a7c1b0e4e49d33e54c642932
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141261"
---
# <a name="design-details-warehouse-overview"></a>Designdetaljer: Översikt över distributionslager
För att stödja den fysiska hanteringen av artiklar i zonen och på lagerplatsnivån måste all information spåras för varje transaktion eller transport i distributionslagret. Det hanteras i tabellen **Dist.lager transaktion**. Varje transaktion lagras i ett distributionslagerregister.  

Distributionslagerdokument och en distributionslagerjournal används för att registrera artikeltransporter i distributionslagret. Varje gång en artikel i distributionslagret flyttas, tas emot, förs in, plockas, utlevereras eller justeras, registreras distributionslagertransaktioner för att lagra den fysiska informationen om zon, lagerplats och antal.

Tabellen **Lagerställesinnehåll** används för att hantera alla olika dimensioner av innehållet i en lagerplats per artikel, t.ex enhet, maximal antal och lägsta antal. Tabellen **Lagerställesinnehåll** innehåller även flödesfält till distributionslagertransaktionerna, distributionslagerinstruktionerna och distributionslagerjournalraderna, som säkerställer att tillgängligheten för en artikel per lagerplats och en lagerplats för en artikel kan beräknas snabbt. Mer information finns i [Designdetaljer: disposition i distributionslagret](design-details-availability-in-the-warehouse.md).  

När artikeltransaktioner uppstår utanför distributionslagerenheten används en standardjusteringlagerplats per lagerställe för att synkronisera distributionslagerposter med lagerposter. Under inventeringen av distributionslagret registreras alla avvikelser mellan de beräknade och inventerade kvantiteterna på justeringslagerstället och sedan bokförs de som korrigerande artikeltransaktioner. Mer information finns i [Designdetaljer: Integrering med lager](design-details-integration-with-inventory.md)  

Följande illustration ger en översikt över typiska distributionslagerflöden.  

![Översikt över lagerprocesser.](media/design_details_warehouse_management_overview.png "Översikt över lagerprocesser")  

## <a name="basic-or-advanced-warehousing"></a>Grundläggande eller avancerad lagerstyrning  
Distributionslagerfunktion i [!INCLUDE[prod_short](includes/prod_short.md)] kan implementeras i olika komplexitetsnivåer, beroende på ett företag processer och ordervolym. Den huvudsakliga skillnaden är att aktiviteter utförs order-för-order i grundläggande lagerstyrning, när de konsolideras för flera order i avancerad lagerstyrning.  

 För att skilja mellan de olika komplexitetsnivåerna refererar denna dokumentation till två allmänna benämningar, grundläggande och avancerad lagerstyrning. Den här enkla differentieringen täcker flera olika komplexitetsnivåer som definieras av produktpartiklar och lagerplatsinställningar, där var och en stöds av olika användargränssnittsdokument . Mer information finns i [Designdetaljer: Lagerstyrningsinställningar](design-details-warehouse-setup.md).  

> [!NOTE]  
>  Den mest avancerade nivån av lagerstyrning kallas för ”WMS-installationer” i denna dokumentation, eftersom den här nivån kräver den mest avancerade partikeln, lagerstyrningssystem (Warehouse Management Systems).  

 Följande olika användargränssnittsdokument används i grundläggande och avancerade lagerhantering.  

## <a name="basic-ui-documents"></a>Grundläggande gränssnittsdokument  

-   **Lagerinförsel**  
-   **Lagerplockning**  
-   **Lagertransport**  
-   **Artikeljournal**  
-   **Artikelgrupperingsjournal**  
-   (Olika rapporter)  

## <a name="advanced-ui-documents"></a>Avancerade UI-dokument  

-   **Dist.lager inleverans**  
-   **Artikelinförsel kalkylark**  
-   **Dist.lager artikelinförsel**  
-   **Plockningskalkylark**  
-   **Dist.lager plockning**  
-   **Transportkalkylark**  
-   **Dist.lager transport**  
-   **Intern dist.lager plockning**  
-   **Intern dist.lager art.införsel<**  
-   **lagerplatsuppläggningskalkylark**  
-   **Lagerställesinnehålluppl kalkylark**  
-   **Dist.lager artikeljournal**  
-   **Dist.lager Artikelgrupperingsjnl**  
-   (Olika rapporter)  

Se respektive sidavsnitt för mer information om varje dokument.  

### <a name="terminology"></a>Terminologi  
För att anpassas till de ekonomiska begreppen för inköp och försäljningar refererar lagerdokumentationen för [!INCLUDE[prod_short](includes/prod_short.md)] till följande villkor för objektflöde i distributionslagret.  

|Term|Description|  
|----------|---------------------------------------|  
|inkommande flöde|Artiklar som transporteras in till distributionslagerstället, till exempel inköp och inkommande överföringar.|  
|Internt flöde|Artiklar som transporteras inom distributionslagerstället, till exempel produktionskomponenter och utflöde.|  
|utgående flöde|Artiklar som transporteras ut ur distributionslagerstället, till exempel försäljningar och utgående överföringar.|  

## <a name="see-also"></a>Se även  
 [Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]