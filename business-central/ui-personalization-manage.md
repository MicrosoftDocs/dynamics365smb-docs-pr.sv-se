---
title: Hantera anpassning som administratör i Business Central | Microsoft Docs
description: Lär dig mer om att anpassa användargränssnittet så att det passar ditt sätt att arbeta.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250601"
---
# <a name="managing-personalization-as-an-administrator"></a>Hantera anpassning som administratör

 Användare kan anpassa sin arbetsyta efter eget behov. Som administratör kan du styra och hantera anpassning av:

-   Aktivera eller inaktivera funktionen anpassning för hela programmet (endast lokal installation).
-   Aktivera eller inaktivera funktionen anpassning för användare med en viss profil.
-   Ta bort alla anpassningar på sidan som användare har gjort.

## <a name="EnablePersonalization"></a>Så här aktiverar eller inaktiverar anpassningar (endast lokalt)

Som standard aktiveras inte anpassning i klienten. Du aktiverar eller inaktiverar anpassningar genom att ändra konfigurationsfil (navsettings.json) för den Business Central Web Server-instans som används av klienterna.

1. Aktivera anpassning genom att lägga till följande rad i filen navsettings.json:

    ```
    "PersonalizationEnabled": "true"
    ```

    Ta bort den här raden om du vill inaktivera anpassningar, eller ändra den till:

    ```
    "PersonalizationEnabled": "false"
    ```

    Läs mer om hur du ändrar filen navsettings.json i [Ändra navsettings.json filen direkt](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).

2. Skapa och hämta programsymboler.

    Detta steg är valfritt och krävs inte för att aktivera anpassningar. Det innebär dock att nya sidor som skapas av utvecklare kan anpassas.

    1. Först måste du skapa symboler genom att köra kommandot finsql.exe med `generatesymbolreference`. Finsql.exe-filen finns i mappen för utvecklingsmiljön för [!INCLUDE[server](includes/server.md)] och Dynamics NAV (CSIDE). Om du vill skapa symboler, öppna kommandotolken, gå till katalogen där filen lagras och kör kommandot:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Som exempel:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Mer information finns i [Köra C/SIDE och AL sida vid sida](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Konfigurera [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-instansen till att **aktivera inläsning av programsymbolens referenser när servern startas** (EnableSymbolLoadingAtServerStartup). Mer information finns i [Konfigurera Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>Så här inaktiverar du anpassningar för en profil

Du kan förhindra alla användare som tillhör en viss profil från att anpassa sidorna.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Profiler** och välj sedan relaterad länk.
2. Välj den profil i listan som du vill ändra.
3. Välj kryssrutan **Inaktivera anpassning** och välj sedan knappen **OK**.

## <a name="to-clear-user-personalizations"></a>Så här rensar du användaranpassning

Ta bort sidann för anpassningsändringar gör att sidan återställs till sin ursprungliga layout innan alla anpassningar gjordes. Det finns två sätt att ta bort de anpassningar som användare har gjort på sidor: med hjälp av sidan **Ta bort användaranpassning** och använda sidan **Anv.anpassningskort**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Du tar bort användaranpassningar genom att använda sidan ta bort användaranpassning

Sidan **Ta bort användaranpassning** låter dig ta bort anpassningen på per sida-basis, för varje enskild användare.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort användaranpassning** och välj sedan relaterad länk.

    Sidan visar en lista över alla sidor som har anpassats och användaren den tillhör.

    >[!NOTE]
    > Ett kryss i kolumnen **Äldre anpassning** anger att anpassningen har skett i en äldre version av [!INCLUDE[d365fin](includes/d365fin_md.md)], som hanterade anpassningen på ett annat sätt än som nu sker. Användare som försöker anpassa dessa sidor hindras från att göra detta såvida de inte väljer att låsa upp sidan. Mer information finns i [Anledningen till att anpassningen är låst för en sida](ui-personalization-locked.md).

2. Markera den transaktion som du vill radera och välj sedan åtgärden **Radera**.

    Användaren kommer att se ändringarna nästa gång de loggar in.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Du tar bort användaranpassningar genom att använda sidan användaranpassningskort

Sidan **Anv.anpassningskort** låter dig ta bort anpassningen på alla sidor för en specifik användare. Detta kräver skrivbehörighet för tabellen 2000000072 **Profil**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användaranpassning** och välj sedan relaterad länk.

    Sidan **användaranpassning** visar alla användare som eventuellt har anpassade sidor. Om du inte hittar en användare i listan, innebär det att de inte har några anpassade sidor.

2. Välj den användare från listan, välj åtgärden **Redigera**.

3. På fliken **Åtgärder**, välj **Ta bort anpassade sidor**.

    Användaren kommer att se ändringarna nästa gång de loggar in.

## <a name="see-also"></a>Se även
[Anpassa din arbetsyta](ui-personalization-user.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  
