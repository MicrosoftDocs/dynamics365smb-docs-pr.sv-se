---
title: Resultat av överföringen | Microsoft Docs
description: Det här avsnittet beskriver vad som händer när du överför redovisningstransaktioner till kostnadstransaktioner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 590c1501f9da2c7c343b5c2f3617df873fcd3b7a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2019
ms.locfileid: "926718"
---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="49191-103">Resultat av överföring av redovisningstransaktioner till kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="49191-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="49191-104">Under överföringen av redovisningstransaktioner till kostnadstransaktioner skapar [!INCLUDE[d365fin](includes/d365fin_md.md)] anslutningar i transaktionerna i tabellen **Redov.trans**, tabellen **kostnadstransaktion** och tabellen **Bokförd journal för kostnad** för att göra det möjligt att spåra anslutningar mellan kostnadstransaktioner och redovisningstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="49191-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="49191-105">Redovisningstransaktioner</span><span class="sxs-lookup"><span data-stu-id="49191-105">General Ledger Entries</span></span>  
<span data-ttu-id="49191-106">För varje redovisningstransaktion som har överförts till kostnadsredovisning fyller fältet [!INCLUDE[d365fin](includes/d365fin_md.md)] i kostnadsfältet **Trans. nr.**</span><span class="sxs-lookup"><span data-stu-id="49191-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="49191-107">Kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="49191-107">Cost Entries</span></span>  
<span data-ttu-id="49191-108">För varje kostnadstransaktion sparar [!INCLUDE[d365fin](includes/d365fin_md.md)] löpnumret för motsvarande redovisningstransaktion i fältet **Löpnr redovisning** i tabellen **Kostnadstransaktion**.</span><span class="sxs-lookup"><span data-stu-id="49191-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="49191-109">För kombinerade kostnadstransaktioner sparar [!INCLUDE[d365fin](includes/d365fin_md.md)] transaktionsnumret för den senaste redovisningstransaktionen, som är transaktionen med det högsta numret.</span><span class="sxs-lookup"><span data-stu-id="49191-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="49191-110">Fältet **Redovisningskonto** i tabellen **Kostnadstransaktion** innehåller numret på det redovisningskonto som kostnadstransaktionen kommer ifrån.</span><span class="sxs-lookup"><span data-stu-id="49191-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="49191-111">För enstaka kostnadstransaktioner överför [!INCLUDE[d365fin](includes/d365fin_md.md)] bokföringstexten från redovisningstransaktionen till textfältet **Beskrivning**.</span><span class="sxs-lookup"><span data-stu-id="49191-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="49191-112">För kombinerade transaktioner visar textfältet dessa transaktioner överförda som kombinerade transaktioner.</span><span class="sxs-lookup"><span data-stu-id="49191-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="49191-113">Till exempel för en kombinerad transaktion för månaden Oktober 2013 kan texten vara **Kombinerade transaktioner, Oktober 2013**.</span><span class="sxs-lookup"><span data-stu-id="49191-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="49191-114">Bokförd journal för kostnad</span><span class="sxs-lookup"><span data-stu-id="49191-114">Cost Register</span></span>  
<span data-ttu-id="49191-115">I tabellen **Bokförd journal för kostnad** skapar [!INCLUDE[d365fin](includes/d365fin_md.md)] en transaktion med källöverföringen från redovisningen.</span><span class="sxs-lookup"><span data-stu-id="49191-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="49191-116">Transaktionen registrerar första och sista löpnumret för redovisningstransaktionerna som har överförts, i tillägg till första och sista löpnumret för kostnadstransaktionerna som skapas.</span><span class="sxs-lookup"><span data-stu-id="49191-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="49191-117">Se även</span><span class="sxs-lookup"><span data-stu-id="49191-117">See Also</span></span>  
[<span data-ttu-id="49191-118">Överföra och bokföra kostnadstransaktioner</span><span class="sxs-lookup"><span data-stu-id="49191-118">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)   
