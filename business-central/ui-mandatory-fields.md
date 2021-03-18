---
title: Fält som krävs för att slutföra processer | Microsoft Docs
description: Få mer information om de fält som är markerade med en röd asterisk som anger att de är obligatoriska och måste fyllas i för att slutföra en process.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 8c631dcbb2c6afa6abec9ace86df0f0babb23b2d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385505"
---
# <a name="detecting-mandatory-fields"></a><span data-ttu-id="60562-103">Identifiera obligatoriska fält</span><span class="sxs-lookup"><span data-stu-id="60562-103">Detecting Mandatory Fields</span></span>
<span data-ttu-id="60562-104">När du anger data på sidor i [!INCLUDE[prod_short](includes/prod_short.md)], markeras vissa fält med en röd asterisk.</span><span class="sxs-lookup"><span data-stu-id="60562-104">When you enter data on pages in [!INCLUDE[prod_short](includes/prod_short.md)], certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="60562-105">Den röda asterisken betyder att fältet måste fyllas för att slutföra en viss process som använder fältet, till exempel bokföra en transaktion som använder värdet i fältet.</span><span class="sxs-lookup"><span data-stu-id="60562-105">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>

<span data-ttu-id="60562-106">Även om fältet innehåller en asterisk tvingas du inte att fylla u fältet innan du fortsätter till andra fält eller avslutar sidan.</span><span class="sxs-lookup"><span data-stu-id="60562-106">Even though the field contains a red asterisk, you are not forced to fill in the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="60562-107">Den röda asterisken fungerar endast som en påminnelse att du kommer att spärras från att slutföra en viss process.</span><span class="sxs-lookup"><span data-stu-id="60562-107">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>

## <a name="examples"></a><span data-ttu-id="60562-108">Exempel</span><span class="sxs-lookup"><span data-stu-id="60562-108">Examples</span></span>
<span data-ttu-id="60562-109">På sidan **Kundkort** visas den röda asterisken i fältet **Namn** i fältet **Skatteområdeskod** och i fälten för bokföringsmallar för att visa att du inte kan bokföra en försäljningstransaktion för kunden om inte fälten fylls i.</span><span class="sxs-lookup"><span data-stu-id="60562-109">On the **Customer Card** page, the red asterisk appears in the **Name** field, in the **Tax Area Code** field, and in the posting group fields to indicate that you cannot post a sales transaction for the customer unless the fields are filled.</span></span>

<span data-ttu-id="60562-110">På sidan **Artikelkort** visas den röda asterisken i fälten **Beskrivning** och Basenhet för att visa att du inte kan ange artikeln på en dokumentrad, t.ex försäljningsorder, om inte detta fält fylls i.</span><span class="sxs-lookup"><span data-stu-id="60562-110">On the **Item Card** page, the red asterisk appears in the **Description** field to indicate that you cannot enter the item on a document line, such as a sales order, unless this field is filled.</span></span>

## <a name="see-also"></a><span data-ttu-id="60562-111">Se även</span><span class="sxs-lookup"><span data-stu-id="60562-111">See Also</span></span>
<span data-ttu-id="60562-112">[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="60562-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]