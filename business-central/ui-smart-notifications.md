---
title: Arbeta med smarta meddelanden och ange när du ser den | Microsoft Docs
description: Du kan få meddelanden som informerar dig om statusändringar eller händelser, till exempel en skuld eller låg lagernivå.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 11/29/2019
ms.author: bholtorf
ms.openlocfilehash: 4839de7b4deff107d8a1644367e28216eb8a789e
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881948"
---
# <a name="manage-notifications"></a><span data-ttu-id="d0ec0-103">Hantera meddelanden</span><span class="sxs-lookup"><span data-stu-id="d0ec0-103">Manage Notifications</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d0ec0-104">hjälper dig att arbeta mer smart genom att meddela dig om vissa evenemang eller stausändringar som t.ex. när du ska fakturera en kund som har en skuld som har förfallit, eller när det tillgängliga lagret är lägre än kvantiteten som du håller på att sälja.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-104">can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="d0ec0-105">Dessa meddelanden visas som diskreta tips i kontexten för uppgiften som du gör, och du kan välja att ignorera meddelandet eller visa detaljer om utskick.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="d0ec0-106">Om du väljer att visa detaljer för ett meddelande, kan du vidta vill att lösa problemet, som till exempel kontakta kunden, köpa mer lager och så vidare.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="d0ec0-107">Det är du som väljer vad som ska göras och [!INCLUDE[d365fin](includes/d365fin_md.md)] ger dig råd och rekommendationer.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-107">It's your choice what to do, and [!INCLUDE[d365fin](includes/d365fin_md.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="d0ec0-108">Meddelandena hjälper otränade användare att slutföra obekanta uppgifter och minskar inte produktiviteten för den mer tränade användaren.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="d0ec0-109">Aktivera eller inaktivera meddelanden och kontrollera när de skickas</span><span class="sxs-lookup"><span data-stu-id="d0ec0-109">To turn notifications on or off, and control when they are sent</span></span>

<span data-ttu-id="d0ec0-110">När du först börjar med [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiveras alla meddelanden, men du kan aktivera dem eller inaktivera dem, till exempel om du inte är intresserad av en viss händelse eller status.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-110">When you first start with [!INCLUDE[d365fin](includes/d365fin_md.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="d0ec0-111">Dessutom låter dig vissa meddelanden ange de villkor enligt vilka de ska skickas.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="d0ec0-112">Exempelvis om du vill få ett meddelande när lagret är slut, men endast för de artiklar du vill köpa från en viss leverantör.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="d0ec0-113">Aktivera meddelanden och inaktivera dem och ange villkor som bara gäller för dig.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="d0ec0-114">I det övre högra hörnet väljer du ikonen **inställningar** ![inställningar](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och välj åtgärden **Mina inställningar**.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-114">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose the **My Settings** action.</span></span>  
2. <span data-ttu-id="d0ec0-115">På sidan **Mina inställningar** i fältet **meddelanden**, välj *Ändra när jag får meddelanden.*</span><span class="sxs-lookup"><span data-stu-id="d0ec0-115">On the **My Settings** page, in the **Notifications** field, choose the *Change when I receive notifications.*</span></span> <span data-ttu-id="d0ec0-116">länk.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-116">link.</span></span>  
3. <span data-ttu-id="d0ec0-117">Aktivera eller inaktivera ett meddelande på sidan som visas genom att markera eller avmarkera kryssrutan **aktiverad**.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-117">In the page that appears, turn on or turn off a notification by selecting or clearing the **Enabled** check box.</span></span>  
4. <span data-ttu-id="d0ec0-118">Ange villkor som ska utlösa meddelanden genom att välja länken **Visa filterdetaljer** och fyll sedan i fälten.</span><span class="sxs-lookup"><span data-stu-id="d0ec0-118">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0ec0-119">Se även</span><span class="sxs-lookup"><span data-stu-id="d0ec0-119">See Also</span></span>

<span data-ttu-id="d0ec0-120">[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0ec0-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
