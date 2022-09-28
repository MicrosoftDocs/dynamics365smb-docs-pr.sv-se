---
title: Ändra grundläggande inställningar för den aktuella användaren
description: Lär dig mer om hur du ändrar vissa grundläggande inställningar i Business Central, t.ex. roll och rollcenter, företag, arbetsdatum och tidszoner.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date, decimal separator
ms.search.form: 9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: 36bf0ca4de4fb7caef9c26ae60ed6013387adca4
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528659"
---
# <a name="change-basic-settings"></a>Ändra grundinställningar

PÅ sidan **Mina inställningar** kan du visa och ändra grundläggande inställningar för [!INCLUDE[prod_short](includes/prod_short.md)]. De ändringar du gör påverkar bara din arbetsyta, inte arbetsytor för andra användare.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role"></a><a name="role-center"></a>Roll

Rollcentret bestämmer startsidan, en startskärm som har utformats för den specifika rollens behov i en organisation. Beroende på din roll ger startsidan eller rollcentret en översikt över verksamheten, din avdelning eller dina personliga uppgifter. Du kan också navigera till ditt dagliga arbete och söka efter arbete som har tilldelats dig.

* Längst upp låter navigeringen dig växla mellan kunder, leverantörer, artiklar och andra viktiga listor med information. På samma sätt kan du starta aktiviteter, såsom skapa en ny försäljningsfaktura direkt från startsidan.

* I mitten hittar du området **aktiviteter**, som visar aktuella data och som du kan klicka på eller knacka på för att visa mer detaljerad information. Nyckelindikatorer (KPI:er) kan ställas in i fältet för att visa ett valt diagram för en visuell representation av, till exempel, kassaflöde eller intäkter och kostnader. Du kan också att upprätta en lista över favoritkunder på startsidan för affärskonton som du arbetar med ofta eller behöver ge extra uppmärksamhet till.

### <a name="to-change-the-role"></a>Så här ändrar du rollen

Standardrollen är **Chef**, men du kan välja en annan roll för att använda ett rollcenter som passar bättre till dina önskemål.  

1. I det övre högra hörnet väljer du ikonen **inställningar** ![inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och välj åtgärden **Mina inställningar**.
2. På sidan **Mina inställningar** i fältet **Roll** väljer du den roll du vill använda som standard. Välj till exempel **Revisor**.
3. Välj **OK**.

## <a name="company"></a><a name="company"></a>Företag

Ett företag fungerar som en behållare för data i [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan finnas åtskilliga företag i en databas, men endast ett kan väljas i taget.

Standardföretaget kallas CRONUS och innehåller endast demonstrationsdata. Du kan skapa ett nytt företag med egna data. Mer information finns i [Skapa nya företag](about-new-company.md).

### <a name="to-change-the-company-name"></a>Så här ändrar du företagsnamnet

Företagsnamnet visas alltid i det övre vänstra hörnet och fungerar som en åtgärd som du kan välja att gå tillbaka till rollcentret. Du kan ändra det här namnet på sidan **företagsinformation**.

1. Välja ![Kugghjulsikon för att öppna menyn Inställningar.](media/ui-experience/settings_icon_small.png) och sedan åtgärden **Företagsinformation**.
2. Ange det nya företagsnamnet i fältet **Namn**.
3. Lämna sidan. Systemet startas om och det nya företaget visas i det övre vänstra hörnet.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>Så här visar du ett företagsbricka för snabb åtkomst till företagsinformation

Du kan lägga till en anpassad bricka i det övre högra hörnet, som du kan välja för att snabbt visa företagsnamn och klientorganisationens information i en popup-ruta. Företagsbrickan är också användbart när [!INCLUDE[prod_short](includes/prod_short.md)] finns inbäddat i ett annat program, exempelvis Microsoft Teams eller i något annat webbprogram. Eftersom [!INCLUDE[web_client](includes/web_client.md)] visar mindre omgivande kontextuell information i dessa fall, utgör företagsbrickan det enda sättet att avgöra vilket företag eller vilken miljö en post tillhör.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Företagsinformation** och väljer sedan relaterad länk.
2. I snabbfliken **Företagsbricka** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Om en företagsbricka definieras kan du inte ändra företagsnamnet enligt beskrivningen i [så här ändrar du företagsnamnet](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a><a name="work-date"></a>Arbetsdatum
Det vanligaste arbetsdatumet är dagens datum. För att utföra uppgifter som att slutföra transaktioner för ett datum som inte är aktuellt datum, kan det vara nödvändigt att tillfälligt ändra dagens datum.

> [!TIP]  
> I alla datafält skriver du **t** för att snabbt ange dagens datum och skriv **w** för att snabbt ange arbetsdatum vilket är värdet i fältet **Arbetsdatum** på sidan **Mina inställningar**.

> [!IMPORTANT]  
> När du har ändrat arbetsdatumet, om du loggar ut eller växlar till ett annat företag, ändras arbetsdata tillbaka till standardarbetsdatum. Så nästa gång du loggar in eller går tillbaka till det ursprungliga företaget, kan du behöva ange arbetsdatumet igen.

### <a name="work-date-indication"></a>Indikering av arbetsdatum

Arbetsdatumet är kritiskt på sidor som kan redigeras. När arbetsdatumet inte är inställt på dagens datum på en redigerbar sida, visas två typer av indikatorer på sidan:

* En påminnelse visas högst upp på sidan som anger vad arbetsdagens datum är. Betalnings påminnelsen innehåller en direkt länk till inställningen arbetsdatum på sidan **mina inställningar** så att du kan ändra datumet om du vill. Du kan också välja att stänga påminnelsen för resten av sessionen. Om du inte ändrar arbetsdatumet till "idag" visas påminnelsen nästa gång du loggar in.

* Om du avmarkerar påminnelsen visas arbetsdatumet i titeln på sidan.  

Om arbetsdatumet inte anges för den aktuella dagen (idag) kommer arbetsdatumet att anges i det övre vänstra hörnet på samtliga sidor där du kan redigera data.

## <a name="region"></a><a name="region"></a> Region

Inställningen **Region** bestämmer hur datum, tid, tal och valutor visas eller formateras. Det avgör också vilket tecken som används som decimalavgränsare när du använder ett numeriskt tangentbord för att ange data. Mer information finns i [Ange data](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a> Språk

Ändra displayspråk. Detta fält visas bara om det finns flera språk att välja mellan.

Startspråket bestäms antingen av administratören eller i webbläsaren när du registrerar dig för [!INCLUDE[prod_short](includes/prod_short.md)]. Det språk som du anger används för alla enheter som du loggar in från, till exempel en telefon eller surfplatta.

Ytterligare språk för [!INCLUDE[prod_short](includes/prod_short.md)] kan installeras från AppSource. Även om alla visningsspråk som stöds visas i listan måste administratören installera relevant språkapp i klientorganisationen innan användarna kan växla till det nya språket i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone"></a>Tidszon

Definierar tidszonen där du befinner dig. När du loggar in på [!INCLUDE [prod_short](includes/prod_short.md)] för första gången anges tidszonen baserat på företagets adress. Ändra den om den inte passar din fysiska plats.  

## <a name="notifications"></a>Meddelanden

Välj länken *Ändra när jag får meddelanden* för att visa eller ändra meddelandena som du får om vissa evenemang eller stausändringar som t.ex. när du ska fakturera en kund som har en skuld som har förfallit, eller när det tillgängliga lagret är lägre än kvantiteten som du håller på att sälja. Mer information finns i [Hantera meddelanden](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Undervisningstips

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Skapa nya företag](about-new-company.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
