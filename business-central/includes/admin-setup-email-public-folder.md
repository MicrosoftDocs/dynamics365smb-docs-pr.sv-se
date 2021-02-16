---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: 1b9f60eab5b0bcf812343e82389087ac5535301a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749786"
---
<span data-ttu-id="e827b-101">Innan du kan konfigurera e-postloggning måste du förbereda Exchange Online med [offentliga mappar](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ).</span><span class="sxs-lookup"><span data-stu-id="e827b-101">Before you can set up email logging, you must prepare your Exchange Online with [public folders](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ).</span></span> <span data-ttu-id="e827b-102">Det kan du göra i [administrationscenter för Exchange](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ) eller använda [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).</span><span class="sxs-lookup"><span data-stu-id="e827b-102">You can do this in the [Exchange admin center](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ), or you can use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).</span></span>  

> [!TIP]
> <span data-ttu-id="e827b-103">Om du vill använda [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ) kan du hitta inspiration för hur du konfigurerar skriptet i ett exempelskript som vi publicerat på [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span><span class="sxs-lookup"><span data-stu-id="e827b-103">If you want to use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ), you can find inspiration for how to set up your script in a sample script that we published to [the BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span></span>

<span data-ttu-id="e827b-104">I följande lista beskrivs de viktigaste stegen med länkar för att få mer information.</span><span class="sxs-lookup"><span data-stu-id="e827b-104">The following list describes the main steps with links to learn more.</span></span>  

- <span data-ttu-id="e827b-105">Skapa en administratörsroll för gemensamma mappar baserat på informationen i följande tabell:</span><span class="sxs-lookup"><span data-stu-id="e827b-105">Create an admin role for public folders based on the information in the following table:</span></span>

  |<span data-ttu-id="e827b-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="e827b-106">Property</span></span>        |<span data-ttu-id="e827b-107">Värde</span><span class="sxs-lookup"><span data-stu-id="e827b-107">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="e827b-108">Name</span><span class="sxs-lookup"><span data-stu-id="e827b-108">Name</span></span>            |<span data-ttu-id="e827b-109">Hantering av delade mappar</span><span class="sxs-lookup"><span data-stu-id="e827b-109">Public Folders Management</span></span> |
  |<span data-ttu-id="e827b-110">Valda roller</span><span class="sxs-lookup"><span data-stu-id="e827b-110">Selected roles</span></span>  |<span data-ttu-id="e827b-111">Gemensamma mappar</span><span class="sxs-lookup"><span data-stu-id="e827b-111">Public Folders</span></span>            |
  |<span data-ttu-id="e827b-112">Valda medlemmar</span><span class="sxs-lookup"><span data-stu-id="e827b-112">Selected members</span></span>|<span data-ttu-id="e827b-113">E-postmeddelandet för användar kontot som Business Central använder för att köra e-postloggningsjobbet</span><span class="sxs-lookup"><span data-stu-id="e827b-113">The email of the user account that Business Central will use to run the email logging job</span></span>|

  <span data-ttu-id="e827b-114">Mer information finns i [Hantera rollgrupper](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="e827b-114">For more information, see [Manage role groups](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).</span></span>

- <span data-ttu-id="e827b-115">Skapa en ny postmapp för allmän mapp baserad på informationen i följande tabell:</span><span class="sxs-lookup"><span data-stu-id="e827b-115">Create a new public folder mailbox based on the information in the following table:</span></span>

  |<span data-ttu-id="e827b-116">Egenskap</span><span class="sxs-lookup"><span data-stu-id="e827b-116">Property</span></span>        |<span data-ttu-id="e827b-117">Värde</span><span class="sxs-lookup"><span data-stu-id="e827b-117">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="e827b-118">Name</span><span class="sxs-lookup"><span data-stu-id="e827b-118">Name</span></span>            |<span data-ttu-id="e827b-119">Offentlig postlåda</span><span class="sxs-lookup"><span data-stu-id="e827b-119">Public MailBox</span></span>            |

  <span data-ttu-id="e827b-120">Mer information finns i [Skapa en offentlig postmapp i Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="e827b-120">For more information, see [Create a public folder mailbox in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span></span>  

- <span data-ttu-id="e827b-121">Skapa nya offentliga mappar</span><span class="sxs-lookup"><span data-stu-id="e827b-121">Create new public folders</span></span>

  - <span data-ttu-id="e827b-122">Skapa en ny offentlig mapp med namnet *e-postloggning* i roten så att den fullständiga sökvägen till mappen blir ```\Email Logging\```</span><span class="sxs-lookup"><span data-stu-id="e827b-122">Create a new public folder with the name *Email Logging* in the root so that the full path to the folder becomes ```\Email Logging\```</span></span>
  - <span data-ttu-id="e827b-123">Skapa två undermappar så att resultatet blir följande fullständiga sökvägar till mapparna:</span><span class="sxs-lookup"><span data-stu-id="e827b-123">Create two subfolders so that the the result is the following full paths to the folders:</span></span>
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  <span data-ttu-id="e827b-124">Mer information finns i [Skapa en offentlig mapp](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="e827b-124">For more information, see [Create a public folder](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).</span></span>

- <span data-ttu-id="e827b-125">Postaktivera den offentliga mappen *Kö*</span><span class="sxs-lookup"><span data-stu-id="e827b-125">Mail-enable the *Queue* public folder</span></span>

  <span data-ttu-id="e827b-126">Mer information finns i [postaktivera eller skicka e-post-inaktivera en offentlig mapp](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="e827b-126">For more information, see [Mail-enable or mail-disable a public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)</span></span>

- <span data-ttu-id="e827b-127">Postaktivera utskick av e-post till den offentliga mappen *Kö* med Outlook eller Exchange Management Shell</span><span class="sxs-lookup"><span data-stu-id="e827b-127">Mail-enable sending emails to the *Queue* public folder using Outlook or the Exchange Management Shell</span></span>

  <span data-ttu-id="e827b-128">Mer information finns i [tillåta anonyma användare att skicka e-post till en offentlig mapp i e-postfunktionen](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)</span><span class="sxs-lookup"><span data-stu-id="e827b-128">For more information, see [Allow anonymous users to send email to a mail-enabled public folder](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)</span></span>

- <span data-ttu-id="e827b-129">Ange e-postloggning som ägare till både offentliga mappar *Kö* och *Lager* med Outlook eller Exchange Management Shell baserat på informationen i följande tabell:</span><span class="sxs-lookup"><span data-stu-id="e827b-129">Set the email logging user as an owner of both public folders, *Queue* and *Storage* public folders  using Outlook or the Exchange Management Shell based on the information in the following table:</span></span>

  |<span data-ttu-id="e827b-130">Egenskap</span><span class="sxs-lookup"><span data-stu-id="e827b-130">Property</span></span>        |<span data-ttu-id="e827b-131">Värde</span><span class="sxs-lookup"><span data-stu-id="e827b-131">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="e827b-132">Användare</span><span class="sxs-lookup"><span data-stu-id="e827b-132">User</span></span>            |<span data-ttu-id="e827b-133">E-postmeddelandet för användar kontot som Business Central använder för att köra e-postloggningsjobbet</span><span class="sxs-lookup"><span data-stu-id="e827b-133">The email of the user account that Business Central will use to run the email logging job</span></span>|
  |<span data-ttu-id="e827b-134">Behörighetsnivå</span><span class="sxs-lookup"><span data-stu-id="e827b-134">Permission level</span></span>|<span data-ttu-id="e827b-135">Ägare</span><span class="sxs-lookup"><span data-stu-id="e827b-135">Owner</span></span>                     |

  <span data-ttu-id="e827b-136">Mer information finns i [Tilldela behörigheter till den offentliga mappen](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span><span class="sxs-lookup"><span data-stu-id="e827b-136">For more information, see [Assign permissions to the public folder](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span></span>

- <span data-ttu-id="e827b-137">Skapa två postflödesregler baserad på informationen i följande tabell</span><span class="sxs-lookup"><span data-stu-id="e827b-137">Create two mail flow rules based on the information in the following table</span></span>

  |<span data-ttu-id="e827b-138">Syfte</span><span class="sxs-lookup"><span data-stu-id="e827b-138">Purpose</span></span>  |<span data-ttu-id="e827b-139">Name</span><span class="sxs-lookup"><span data-stu-id="e827b-139">Name</span></span> |<span data-ttu-id="e827b-140">Villkor</span><span class="sxs-lookup"><span data-stu-id="e827b-140">Conditions</span></span>                        |<span data-ttu-id="e827b-141">Åtgärd</span><span class="sxs-lookup"><span data-stu-id="e827b-141">Action</span></span>                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |<span data-ttu-id="e827b-142">En regel för inkommande e-post</span><span class="sxs-lookup"><span data-stu-id="e827b-142">A rule for incoming email</span></span> |<span data-ttu-id="e827b-143">Logga e-post som skickats till den här organisationen</span><span class="sxs-lookup"><span data-stu-id="e827b-143">Log Email Sent to This Organization</span></span>|<span data-ttu-id="e827b-144">*Avsändaren* finns *utanför organisationen* och *mottagaren* finns *inne i organisationen*</span><span class="sxs-lookup"><span data-stu-id="e827b-144">*The sender* is located *Outside the organization*, and *the recipient* is located *Inside the organization*</span></span>|<span data-ttu-id="e827b-145">Skicka hemlig kopia det e-postkonto som har angetts för den offentliga mappen *kö*</span><span class="sxs-lookup"><span data-stu-id="e827b-145">BCC the email account that is specified for the *Queue* public folder</span></span>|
  |<span data-ttu-id="e827b-146">En regel för utgående e-post</span><span class="sxs-lookup"><span data-stu-id="e827b-146">A rule for outgoing email</span></span> | <span data-ttu-id="e827b-147">Logga e-post som skickats från den här organisationen</span><span class="sxs-lookup"><span data-stu-id="e827b-147">Log Email Sent from This Organization</span></span> |<span data-ttu-id="e827b-148">*Avsändaren* finns *inne i organisationen* och *mottagaren* finns *utanför organisationen*</span><span class="sxs-lookup"><span data-stu-id="e827b-148">*The sender* is located *Inside the organization*, and *the recipient* is located *Outside the organization*</span></span>|<span data-ttu-id="e827b-149">Skicka hemlig kopia det e-postkonto som har angetts för den offentliga mappen *kö*</span><span class="sxs-lookup"><span data-stu-id="e827b-149">BCC the email account that is specified for the *Queue* public folder</span></span>|
  
  <span data-ttu-id="e827b-150">Mer information finns i [Hantera postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) och [åtgärder för postflödesregler i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span><span class="sxs-lookup"><span data-stu-id="e827b-150">For more information, see [Manage mail flow rules in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) and [Mail flow rule actions in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).</span></span>

> [!NOTE]
> <span data-ttu-id="e827b-151">Om du gör ändringar i Exchange Management Shell blir ändringarna synliga i Exchange Admin Center efter en fördröjning.</span><span class="sxs-lookup"><span data-stu-id="e827b-151">If you make changes in the Exchange Management Shell, the changes become visible in the Exchange admin center after a delay.</span></span> <span data-ttu-id="e827b-152">Dessutom kommer de ändringar som gjorts i Exchange att vara tillgängliga [!INCLUDE[prod_short](prod_short.md)] efter en fördröjning.</span><span class="sxs-lookup"><span data-stu-id="e827b-152">Also, the changes made in Exchange will be available in [!INCLUDE[prod_short](prod_short.md)] after a delay.</span></span>
