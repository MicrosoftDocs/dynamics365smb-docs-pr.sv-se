---
title: Använda arbetsflöden
description: Du kan ställa in och använda arbetsflöden som ansluter affärs processer på samma sätt som automatisk bokföring eller förfrågan och beviljande av godkännande för nya poster.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 51079e65deda165869d946b5efc11da85fb720e4
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6446525"
---
# <a name="using-workflows"></a>Använda arbetsflöden

Ett arbetsflöde är en serie uppgifter som utlöses av en åtgärd, ett villkor eller en regel. Arbetsflöden används vanligtvis för att integrera affärslogiken i en organisation, till exempel separation av uppgifter, förena processer eller för att öka förtroende och ansvarsområden.  

Arbetsflödena har utformats för att skapa begäran om godkännande av ett nytt värde och behålla det gamla värdet om begäran inte godkänns. Det nya värdet kommer inte att implementeras förrän den sista begäran har godkänts.  

Affärslogiken kan godkännas av följande:

- Nya huvuddata som redovisningskonton, kunder, leverantörer eller artiklar
- Ändringar av fält i befintliga poster som innehåller känslig information **Leverantörsbankkontonr.** eller **Kundens kreditlimit**
- Ändringar av fält i befintliga poster som innehåller affärsviktig information, till exempel **artikelförsäljningspriser**
- Nya användare eller ändringar av användarbehörigheter
- Inköpsdokument
- Försäljningsdokument
- Inkommande dokument
- Finansiell journal före bokföring

I följande illustration visas ett exempel på ett arbetsflöde med sekventiellt godkännande som utlösts av en användare. När arbetsflödet utlöses skapas en godkännandebegäran för den första godkännaren.  

![Illustration av ett arbetsflöde med sekventiellt godkännande.](media/Workflows/approval-flow.png)

I det här exemplet måste begäran godkännas av den första godkännaren innan begäran skickas vidare till nästa godkännare. Om begäran inte godkänns av den första godkännaren kommer förfrågan aldrig att gå vidare till nästa godkännare.  

Vägen som tas från den inledande utlösaren av arbetsflödet kan variera beroende på typ av godkännande.  

Följande illustration visar ett parallellt godkännande som utlöstes av användaren. När arbetsflödet utlöses skickas en godkännandebegäran till alla godkännare samtidigt.  

![Illustration av ett arbetsflöde med parallellt godkännande.](media/Workflows/approval-flow-2.png)

Arbetsflödet godkänns dock inte förrän alla begäranden har godkänts av godkännarna, vilket visas i bilden nedan:  

![Illustration av ett avisat arbetsflöde med parallellt godkännande.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> Det går inte att skapa ett arbetsflöde med flera godkännare och förvänta dig att hela arbetsflödet godkänns efter att den första begäran har godkänts. Alla begäranden måste godkännas för att arbetsflödet ska godkännas.

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Det går också att skapa samma arbetsflöde mer än en gång. Varje arbetsflöde som utlöstes av en händelse med hjälp av olika filter. Detta är användbart om en godkännande förfrågan på en avdelning måste godkännas av en godkännare, där godkännande begäranden på andra avdelningar måste godkännas av en annan godkännare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

 Innan du kan börja använda arbetsflöden måste du konfigurera arbetsflödesanvändare, skapa arbetsflöden, eventuellt tillämpa föregående kodanpassning och ange hur användarna ska meddelas. Mer information finns i [Konfigurera arbetsflöden](across-set-up-workflows.md).  

> [!NOTE]  
> Vanliga arbetsflödessteg är när användare begär godkännande av aktiviteter och godkännare accepterar eller avvisar godkännandebegäranden. Därför handlar många avsnitt om hur du använder arbetsflöden i godkännande.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.  

|**För att**|**Gå till**|  
|------------|-------------|  
|Ange ett arbetsflöde för att starta när den första instegshändelsen inträffar.|[Så här aktiverar du arbetsflöden](across-how-to-enable-workflows.md)|  
|Begär godkännande för en aktivitet, som en godkännare, acceptera, avvisa eller delegera godkännanden och skicka eller visa godkännandemeddelanden.|[Använda arbetsflöden för godkännande](across-how-use-approval-workflows.md)|  
|Skapa arbetsflödessteg som begränsar en viss posttyp från att användas innan en viss händelse uppstår, till exempel att posten godkänns.|[Begränsa och tillåt användningen av en post](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|Visa avslutade arbetsflödessteginstanser med statusen Avslutat.|[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)|  
|Ta bort ett arbetsflöde som du vet inte ska användas längre.|[Ta bort arbetsflöden](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a>Se även  
[Konfigurera arbetsflöden](across-set-up-workflows.md)   
[Arbetsflöde](across-workflow.md)   
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]