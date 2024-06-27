---
title: Ändra grundläggande inställningar för den aktuella användaren
description: 'Lär dig mer om hur du ändrar vissa grundläggande inställningar i Business Central, t.ex. roll och rollcenter, företag, arbetsdatum och tidszoner.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---
# <a name="change-basic-settings"></a>Ändra grundinställningar

PÅ sidan **Mina inställningar** för att hantera grundläggande inställningar för din [!INCLUDE[prod_short](includes/prod_short.md)]. De ändringar du gör påverkar bara din arbetsyta, inte arbetsytor för andra användare.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role"></a><a name="role-center"></a>Roll

Rollcentret bestämmer startsidan, en startskärm som har utformats för den specifika rollens behov i en organisation. Beroende på din roll ger startsidan eller rollcentret en översikt över verksamheten, din avdelning eller dina personliga uppgifter. Du kan också navigera till ditt dagliga arbete och söka efter arbete som har tilldelats dig.

* Längst upp låter navigeringen dig växla mellan kunder, leverantörer, artiklar och andra viktiga listor med information. På samma sätt kan du starta aktiviteter, såsom skapa en ny försäljningsfaktura direkt från startsidan.

* I mitten hittar du området **Aktiviteter**, som visar aktuella data och som kan väljas för att visa mer detaljerad information. Nyckelindikatorer (KPI:er) kan ställas in i fältet för att visa ett valt diagram för en visuell representation av, till exempel, kassaflöde eller intäkter och kostnader. Du kan också att upprätta en lista över favoritkunder på startsidan för affärskonton som du arbetar med ofta eller behöver ge extra uppmärksamhet till.

### <a name="change-the-role"></a>Ändra rollen

Standardrollen är **Chef**, men du kan välja en annan roll för att använda ett rollcenter som passar bättre till dina önskemål.  

1. I det övre högra hörnet väljer du ikonen **inställningar** ![inställningar.](media/ui-experience/settings_icon_small.png "Inställningsikon för rollcenter") och välj åtgärden **Mina inställningar**.
2. På sidan **Mina inställningar** i fältet **Roll** väljer du den roll du vill använda som standard. Välj till exempel **Revisor**.
3. Välj **OK**.

## <a name="company"></a><a name="company"></a>Företag

Ett företag fungerar som en behållare för data i [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan finnas åtskilliga företag i en databas, men endast ett kan väljas i taget. Standardföretaget kallas CRONUS och innehåller endast demonstrationsdata.

I fältet **Företag** visas det företag som du arbetar på för tillfället, och du kan använda det för att växla till ett annat företag. Företagsnamnet visas alltid i det övre vänstra hörnet och fungerar som en åtgärd som du kan välja att gå tillbaka till rollcentret.

> [!TIP]
> Du kan också ändra företaget genom att använda företagsväxlaren (Crtl + O). Mer information om den här funktionen och andra sätt att ändra företaget eller miljön finns i [Växla till ett annat företag eller en annan miljö](ui-organization-switch.md).

Standardföretaget kallas CRONUS och innehåller endast demonstrationsdata. Du kan skapa ett nytt företag med egna data. Mer information finns i [Skapa nya företag](about-new-company.md).

<!--
### <a name="to-change-the-company-name"></a>To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## <a name="work-date"></a><a name="work-date"></a>Arbetsdatum

Det vanligaste arbetsdatumet är dagens datum. För att utföra uppgifter som att slutföra transaktioner för ett datum som inte är aktuellt datum, kan det vara nödvändigt att tillfälligt ändra arbetsdatum.

> [!TIP]  
> I alla datafält skriver du **t** för att snabbt ange dagens datum och skriv **w** för att snabbt ange arbetsdatum vilket är värdet i fältet **Arbetsdatum** på sidan **Mina inställningar**.

> [!IMPORTANT]  
> När du har ändrat arbetsdatumet, om du loggar ut eller växlar till ett annat företag, ändras arbetsdata tillbaka till standardarbetsdatum. Så nästa gång du loggar in eller går tillbaka till det ursprungliga företaget, kan du behöva ange arbetsdatumet igen.

### <a name="work-date-indication"></a>Indikering av arbetsdatum

Arbetsdatumet är kritiskt på sidor som kan redigeras. När arbetsdatumet inte är inställt på dagens datum på en redigerbar sida, visas två typer av indikatorer på sidan:

* En påminnelse visas högst upp på sidan som anger vad arbetsdagens datum är. Betalnings påminnelsen innehåller en direkt länk till inställningen arbetsdatum på sidan **mina inställningar** så att du kan ändra datumet om du vill. Du kan också välja att stänga påminnelsen för resten av sessionen. Om du inte ändrar arbetsdatumet till "idag" visas påminnelsen nästa gång du loggar in.

* Om du avmarkerar påminnelsen visas arbetsdatumet i titeln på sidan.  

Om arbetsdatumet inte anges för den aktuella dagen (idag) kommer arbetsdatumet att anges i det övre vänstra hörnet på samtliga sidor där du kan redigera data.

## <a name="region"></a><a name="region"></a>Region

Inställningen **Region** bestämmer hur datum, tid, tal och valutor visas eller formateras. Det avgör också vilket tecken som används som decimalavgränsare när du använder ett numeriskt tangentbord för att ange data. Läs mer på [Ange data](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a>Språk

Ändra displayspråk. Detta fält visas bara om det finns flera språk att välja mellan.

Startspråket bestäms antingen av administratören eller i webbläsaren när du registrerar dig för [!INCLUDE[prod_short](includes/prod_short.md)]. Det språk som du anger används för alla enheter som du loggar in från, till exempel en telefon eller surfplatta.

Fler språk för [!INCLUDE[prod_short](includes/prod_short.md)] kan installeras från AppSource. Även om alla visningsspråk som stöds visas i listan måste administratören installera relevant språkapp i klientorganisationen innan användarna kan växla till det nya språket i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone"></a>Tidszon

Definierar tidszonen där du befinner dig. När du loggar in på [!INCLUDE [prod_short](includes/prod_short.md)] för första gången anges tidszonen baserat på företagets adress. Ändra den om den inte passar din fysiska plats.  

## <a name="notifications"></a>Aviseringar

Välj länken **Ändra när jag erhåller meddelanden** för att hantera aviseringarna som du får angående vissa händelser eller ändringar i status. Till exempel när du ska fakturera en kund som har en skuld som har förfallit, eller när det tillgängliga lagret är lägre än kvantiteten som du håller på att sälja. Läs mer på [Hantera meddelanden](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Undervisningstips

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-also"></a>Se även

[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
[Skapa nya företag](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
