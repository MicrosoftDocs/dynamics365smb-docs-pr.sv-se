---
title: Använda arbetsflöden för godkännande
description: Du kan ställa in och använda arbetsflöden som ansluter affärs processer på samma sätt som automatisk bokföring eller förfrågan och beviljande av godkännande för nya poster.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '1500, 1501, 1503, 1504, 1505'
ms.date: 09/13/2022
ms.author: bholtorf
---
# Använda arbetsflöden för godkännande

Ett arbetsflöde är en serie uppgifter som utlöses av en åtgärd, ett villkor eller en regel. Arbetsflöden används vanligtvis för att integrera affärslogiken i en organisation, till exempel separation av uppgifter, förena processer eller för att använda bästa praxis.

Arbetsflödena kan utformats för att skapa begäran om godkännande av post fält ändring och behålla det gamla värdet om begäran inte godkänns. Det nya värdet kommer inte att implementeras förrän den sista begäran har godkänts.

Affärslogiken kan godkännas av följande:

- Nya huvuddata som redovisningskonton, kunder, leverantörer eller artiklar.
- Ändringar av fält i befintliga poster som innehåller känslig information **Leverantörsbankkontonr.** eller **Kundens kreditlimit**.
- Ändringar av fält i befintliga poster som innehåller affärsviktig information, till exempel **artikelförsäljningspriser**.
- Nya användare eller ändringar av användarbehörigheter.
- Inköpsdokument.
- Försäljningsdokument.
- Inkommande dokument.
- Finansiell journal före bokföring.

I följande illustration visas ett exempel på ett arbetsflöde med sekventiellt godkännande som utlösts av en användare. När arbetsflödet utlöses skapas en godkännandebegäran för den första godkännaren.  

![Illustration av ett arbetsflöde med sekventiellt godkännande.](media/Workflows/approval-flow.png)

Du ser i bilden ovan hur begäran godkännas av den första godkännaren innan begäran skickas vidare till nästa godkännare. Om begäran inte godkänns av den första godkännaren kommer förfrågan aldrig att gå vidare till nästa.

Vägen som tas från den inledande utlösaren av arbetsflödet kan variera beroende på typ av godkännande.  

Följande illustration visar ett parallellt godkännande som utlöstes av användaren. Ett parallellt godkännande innebär att en godkännandebegäran skickas till alla godkännare samtidigt.  

![Illustration av ett arbetsflöde med parallellt godkännande.](media/Workflows/approval-flow-2.png)

Arbetsflödet slutförs dock inte förrän alla begäranden har godkänts, vilket visas i bilden nedan:  

![Illustration av ett avisat arbetsflöde med parallellt godkännande.](media/Workflows/approval-flow-3.png)

> [!NOTE]  
> För ett arbetsflöde med flera godkännare måste alla godkännare godkänna varje steg innan arbetsflödet kan flyttas vidare till nästa händelse. Godkännandet av en godkännare flyttar inte arbetsflödet framåt.

Du kan konfigurera och använda arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Det går också att skapa samma arbetsflöde mer än en gång. Varje arbetsflöde som utlöstes av en händelse med hjälp av olika filter. Detta är användbart om en godkännande förfrågan på en avdelning måste godkännas av en godkännare, där godkännande begäranden på andra avdelningar måste godkännas av en annan godkännare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

Innan du kan börja använda arbetsflöden måste du konfigurera arbetsflödesanvändare, skapa arbetsflöden, eventuellt tillämpa föregående kodanpassning och ange hur användarna ska meddelas. Läs mer i [Ställa in arbetsflöden](across-set-up-workflows.md).

> [!NOTE]  
> Typiska arbetsflödessteg involverar användare som begär godkännande av aktiviteter och godkännare accepterar eller avvisar godkännandebegäranden. Därför handlar många avsnitt om hur du använder arbetsflöden i godkännande.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de artiklar där de beskrivs.  

| **Om du vill** | **Se** |
|--|--|
| Ange ett arbetsflöde för att starta när den första instegshändelsen inträffar. | [Aktivera arbetsflöden för godkännande](across-how-to-enable-workflows.md) |
| Begär godkännande för en aktivitet, som en godkännare, acceptera, avvisa eller delegera godkännanden och skicka eller visa godkännandemeddelanden. | [Så här använder du godkännande av arbetsflöden](across-how-use-approval-workflows.md) |
| Skapa arbetsflödessteg som begränsar en viss posttyp från att användas innan en viss händelse uppstår, till exempel att posten godkänns. | [Begränsa och tillåt användningen av en post](across-how-to-restrict-and-allow-usage-of-a-record.md) |
| Visa avslutade instans för arbetsflödessteg med statusen **Avslutat**. | [Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md) |
| Ta bort ett arbetsflöde för godkännande som du vet inte ska användas längre. | [Ta bort arbetsflöden för godkännande](across-how-to-delete-workflows.md) |

## Se relaterad [Microsoft utbildning](/training/modules/create-workflows/)

## Se även

[Konfigurera arbetsflöden för godkännande](across-set-up-workflows.md)  
[Arbetsflöde](across-workflow.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
