---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
---

När du lägger upp användare för godkännande arbetsflöden är det viktigt att samma användare inte har en beställare och en godkännare i en arbetsflödesanvändargrupp. När en användare är både en begärande och en godkännare fungerar godkännanden för dem enligt följande:

* Deras förfrågningar godkänns alltid automatiskt.
* Om det finns flera godkännare kan endast godkännare med ett högre sekvensnummer i arbetsflödesanvändargruppen ändra status för en begäran till Godkänd. Godkännare med ett lägre sekvensnummer kan godkänna förfrågningar, men deras godkännanden påverkar inte statusen för en förfrågan.