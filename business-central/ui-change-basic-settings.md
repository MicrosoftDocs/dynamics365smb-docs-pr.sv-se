---
title: Visa och redigera grundläggande inställningar | Microsoft Docs
description: Lär dig hur du ändrar några av de grundläggande inställningarna, till exempel, rollcenter, företag eller arbetsdatumet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 61d0ddfd19dede42497607dd0f1897598ac61b80
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573332"
---
# <a name="change-basic-settings"></a>Ändra grundinställningar

PÅ sidan **Mina inställningar** kan du visa och ändra grundläggande inställningar för [!INCLUDE[prod_short](includes/prod_short.md)]. De ändringar du gör påverkar bara din arbetsyta, inte arbetsytor för andra användare.  

## <a name="role-center"></a><a name="role-center"></a> Rollcenter

Rollcentret representerar startsidan eller startskärmen. Den är utformad för behoven tillhörande en specifik roll i en organisation. Beroende på din roll ger rollcentret en översikt över verksamheten, din avdelning eller dina personliga uppgifter. Rollcentret kan också hjälpa dig att navigera till dina dagliga uppgifter och söka efter arbete som har tilldelats dig.

- Längst upp låter navigeringen dig växla mellan kunder, leverantörer, artiklar och andra viktiga listor med information. På samma sätt låte åtgärder dig starta aktiviteter, till exmepel att skapa en ny försäljningsfaktura, direkt från Rollcentret.

- I mitten hittar du området **Aktiviteter**, som visar aktuella data. Du kan välja eller trycka på datan för att visa mer detaljerad information. Nyckelindikatorer (KPI:er) kan ställas in i fältet för att visa ett valt diagram för en visuell representation av, till exempel, kassaflöde eller intäkter och kostnader. Du kan också upprätta en lista över favoritkunder på Rollcenter-startsidan för företagskonton som du samarbetar med ofta eller behöver ge extra uppmärksamhet.

### <a name="to-change-the-role"></a>Så här ändrar du rollen

Standardrollen är **Chef**, men du kan välja en annan roll för att använda ett rollcenter som passar bättre till dina önskemål.
1. I det övre högra hörnet väljer du ikonen **Inställningar** ![Inställningar](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och sedan åtgärden **Mina inställningar**.
2. På sidan **Mina inställningar** i fältet **Roll** väljer du den roll du vill använda som standard. Välj till exempel **Revisor**.
3. Välj **OK**.

## <a name="company"></a><a name="company"></a>Företag

Ett företag fungerar som en behållare för data i [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan finnas åtskilliga företag i en databas, men endast ett kan väljas i taget.

Standardföretaget kallas CRONUS och innehåller endast demonstrationsdata. Du kan skapa ett nytt företag med egna data. Mer information finns i [Skapa nya företag](about-new-company.md).

## <a name="to-change-the-company-name"></a>Så här ändrar du företagsnamnet

Företagsnamnet visas alltid i det övre vänstra hörnet. Det fungerar som en åtgärd som du kan välja för att gå tillbaka till Rollcentret. Du kan ändra det här namnet på sidan **företagsinformation**.

1. Välj ikonen ![Kugghjulsikon för att öppna menyn Inställningar](media/ui-experience/settings_icon_small.png) och sedan åtgärden **Företagsinformation**.
2. Ange det nya företagsnamnet i fältet **Namn**.
3. Lämna sidan. Systemet startas om och det nya företaget visas i det övre vänstra hörnet.

## <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>Så här visar du ett företagsbricka för snabb åtkomst till företagsinformation

Du kan lägga till en anpassad bricka i det övre högra hörnet, som du kan välja för att snabbt visa företagsnamn och klientorganisationens information i en popup-ruta. Företagsbrickan är också användbart när [!INCLUDE[prod_short](includes/prod_short.md)] finns inbäddat i ett annat program, exempelvis Microsoft Teams eller i något annat webbprogram. Eftersom [!INCLUDE[web_client](includes/web_client.md)] visar mindre omgivande kontextuell information i dessa fall, utgör företagsbrickan det enda sättet att avgöra vilket företag eller vilken miljö en post tillhör.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Företagsinformation** och välj sedan relaterad länk.
2. I snabbfliken **Företagsbricka** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Om en företagsbricka definieras kan du inte ändra företagsnamnet enligt beskrivningen i [så här ändrar du företagsnamnet](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a><a name="work-date"></a>Arbetsdatum

Det vanligaste arbetsdatumet är dagens datum. För att utföra uppgifter, exempelvis att slutföra transaktioner för ett datum som inte är aktuellt datum, kan det vara nödvändigt att tillfälligt ändra dagens datum.

> [!TIP]  
> I alla datafält skriver du **t** för att snabbt ange dagens datum och skriv **w** för att snabbt ange arbetsdatum vilket är värdet i fältet **Arbetsdatum** på sidan **Mina inställningar**.

> [!IMPORTANT]  
>  När du har ändrat arbetsdatumet, om du loggar ut eller växlar till ett annat företag, ändras arbetsdata tillbaka till standardarbetsdatum. Så nästa gång du loggar in eller går tillbaka till det ursprungliga företaget, kan du behöva ange arbetsdatumet igen.

### <a name="work-date-indication"></a>Indikering av arbetsdatum

Arbetsdatumet är kritiskt på sidor som kan redigeras. När arbetsdatumet inte är inställt på dagens datum på en redigerbar sida, visas två typer av indikatorer på sidan:

- En påminnelse visas högst upp på sidan som anger vad arbetsdagens datum är. Betalnings påminnelsen innehåller en direkt länk till inställningen arbetsdatum på sidan **mina inställningar** så att du kan ändra datumet om du vill. Du kan också välja att stänga påminnelsen för resten av sessionen. Om du inte ändrar arbetsdatumet till "idag" visas påminnelsen nästa gång du loggar in.

- Om du avmarkerar påminnelsen visas arbetsdatumet i titeln på sidan.  

Om arbetsdatumet inte anges för den aktuella dagen (idag) kommer arbetsdatumet att anges i det övre vänstra hörnet på samtliga sidor där du kan redigera data.

## <a name="region"></a><a name="region"></a> Region

Inställningen **Region** bestämmer hur datum, tid, tal och valutor visas eller formateras.

## <a name="language"></a><a name="language"></a> Språk

Ändra displayspråk. Detta fält visas bara om det finns flera språk att välja mellan.

Startspråket bestäms antingen av administratören eller i webbläsaren när du registrerar dig för [!INCLUDE[prod_short](includes/prod_short.md)]. Det språk som du anger används för alla enheter som du loggar in från, till exempel en telefon eller surfplatta.

Fler språk för [!INCLUDE[prod_short](includes/prod_short.md)] kan installeras från AppSource. Även om alla visningsspråk som stöds visas i listan måste administratören installera relevant språkapp innan användarna kan växla till det nya språket i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="changing-when-i-receive-notifications"></a>Ändra när jag får meddelanden

Välj den här länken om du vill visa eller ändra aviseringarna som du får angående vissa händelser eller ändringar i status. Du kan till exempel få en avisering när du ska fakturera en kund som har en skuld som har förfallit, eller när det tillgängliga lagret är lägre än kvantiteten som du håller på att sälja. Mer information finns i [Hantera meddelanden](ui-smart-notifications.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Skapa nya företag](about-new-company.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]