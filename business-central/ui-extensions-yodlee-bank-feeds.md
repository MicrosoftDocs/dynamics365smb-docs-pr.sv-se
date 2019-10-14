---
title: Betalningsavstämning med tillägget Envestnet Yodlee Bank Feeds | Microsoft Docs
description: Beskriver tillägget Envestnet Yodlee Bank Feeds, som länkar till bankkonton så att du kan stämma av betalningar snabbt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d79ef7c076ec3a529aeb0c679b8b61658ef65af5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315354"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="aa8a8-103">Tillägget Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="aa8a8-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="aa8a8-104">För att snabbt avstämma utbetalningar som gjorts till dina bankkonton, låter dig Envestnet Yodlee Bank Feeds länka ditt systembankkonto till ditt onlinebankkonto.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="aa8a8-105">Det betyder att det senaste kontoutdraget automatiskt eller manuellt matas in i din avstämningsjournal och ser till att du alltid behandlar de senaste utbetalningarna med minsta risk för fel.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="aa8a8-106">Tjänsten Envestnet Yodlee Bank Feeds stöds bara i USA och Kanada.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="aa8a8-107">Funktionen stöds bara i online-versionen av Business Central.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-107">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="aa8a8-108">Om du vill använda den här funktionen på plats, måste du skaffa ett cobrand-konto från Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-108">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />

> [!IMPORTANT]
> <span data-ttu-id="aa8a8-109">På grund av det nya direktivet om betalningstjänster i Europa (PSD2), efter den 14 september 2019, kan du inte längre automatiskt importera bankutdrag från banker i Storbritannien till [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="aa8a8-109">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="aa8a8-110">Vi undersöker möjligheten att erbjuda denna funktion igen i framtiden.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-110">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="aa8a8-111">Tjänsten Envestnet Yodlee Bank Feeds ger följande fördelar:</span><span class="sxs-lookup"><span data-stu-id="aa8a8-111">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="aa8a8-112">Tar bort behovet av manuell inmatning.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-112">Removes the need for manual entry.</span></span>
* <span data-ttu-id="aa8a8-113">Förbättrar effektivitet och ökar noggrannheten när du gör betalningsavstämning.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-113">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="aa8a8-114">Stöder ett stort antal banker.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-114">Supports a large number of banks.</span></span>
* <span data-ttu-id="aa8a8-115">Tillåter aktuell information om banktransaktioner inifrån [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="aa8a8-115">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="aa8a8-116">Stöder manuella samt automatiska bankfeeder.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-116">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="aa8a8-117">Aktiverar utkontraktering av utbetalningxavstämning till en revisor genom att ge åtkomst till kontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="aa8a8-117">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="aa8a8-118">Mer information finns i [Ställ in tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="aa8a8-118">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="aa8a8-119">Se även</span><span class="sxs-lookup"><span data-stu-id="aa8a8-119">See Also</span></span>
<span data-ttu-id="aa8a8-120">[Anpassa [!INCLUDE[d365fin](includes/d365fin_md.md)] med tillägg](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="aa8a8-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="aa8a8-121">Koppla utbetalningar automatiskt och stämma av bankkonton</span><span class="sxs-lookup"><span data-stu-id="aa8a8-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="aa8a8-122">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aa8a8-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
