---
title: Hantera användare och roller
description: Lär dig hantera användarprofiler och rollcenter i Business Central. Med profiler kan administratörer centralt definiera och hantera vad användare kan se och göra.
author: SorenGP
ms.topic: conceptual
ms.search.keywords: profiles, users
ms.search.form: 9171
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: a44338ca10dee37bba6d78ec1c73cb7b156bd2b3
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079278"
---
# <a name="manage-user-profiles"></a>Hantera användarprofiler

Alla användare av [!INCLUDE[prod_short](includes/prod_short.md)] tilldelas en profil som motsvarar affärsrollen, den avdelning de arbetar i eller någon annan kategorisering. Med hjälp av profiler kan administratörer definiera och hantera centralt olika typer av användare som kan se och arbeta i användargränssnittet så att de kan utföra affärsuppgifter på ett effektivt sätt.

> [!NOTE]
> En typisk företagsanvändning är en roll. En profil har därför namnet *profil (roll)* i användargränssnittet.

Som administratör skapar och hanterar du profiler på sidan **profiler (roller)**. Varje profil har ett kort där du hanterar olika inställningar för den relaterade rollen, till exempel rollnamn, användarinställningar och vilket rollcenter profilen använder. Mer information om användarinställningar och rollcenter finns i [ändra grundläggande inställningar](ui-change-basic-settings.md).

Innan du kan administrera användarprofiler måste användarna skapas och läggas till via administrationscentret för Microsoft 365. Sedan kan du tilldela behörigheter till varje användare eller användargrupp för att definiera vilka funktioner de får visa och/eller redigera. Mer information finns i [Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md).

## <a name="page-customization"></a>Sidanpassning
Du kan anpassa sidlayouter för en profil så att alla användare som tilldelats profilen kan se de anpassade sidorna. Som administratör anpassar du sidorna med samma funktion som användarna gör när de anpassar. Mer information finns i [Anpassa sidor för profiler](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Så här skapar du en profil:

Om du inte kan kopiera en befintlig profil kan du skapa en ny manuellt.

1. Välj ![Sök efter sida eller rapport.](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport") anger du **Profiler (roller)** och väljer sedan relaterad länk.  
2. På sidan **Profiler (roller)** väljer du åtgärden **Ny**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Om du vill att en viss profil bara ska vara tillgänglig för mycket specifika användare kan du ställa in fältet **Beskrivning** till `Navigation menu only.`. På så sätt undantas profilen från listan över tillgängliga roller i **Mina inställningar**.

## <a name="to-copy-a-profile"></a>Så här kopierar du en profil
Du kan spara tid genom att skapa en ny profil genom att kopiera en befintlig. Kopiera en som innehåller liknande inställningar som du vill skapa.

> [!NOTE]
> När du kopierar en profil kopieras också alla relevanta anpassningar av sidorna, både skapade av användaren och de som har härletts från tillägg.

1. I sidan **Profiler (roller)**, markera raden för den profil som du vill kopiera och välj sedan åtgärden **Kopiera profil**.
2. Fyll i fälten **profil-ID** och **visningsnamn** och klicka sedan på **OK**.
3. På sidan **profiler (roller)** öppnar du det nyss skapade profilkortet och redigerar sedan andra fält om det behövs.

## <a name="to-edit-a-profile"></a>Så här redigerar du en profil
Du kan redigera en profil genom att ändra fälten på sidan **Profil (roll)**. Ändringarna visas dock inte för användare som tilldelats profilen förrän de loggar ut och in igen.

> [!Caution]
> Byt inte namn på en profil när användare som tilldelats profilen är inloggade eftersom användare kan uppleva att produkten låses och måste startas om.

## <a name="to-assign-a-profile-to-a-user"></a>Så här tilldelar du en profil till en användare:
Användare kan tilldela sig själva en roll (som representerar en profil) genom att välja fältet **Roll** på sidan **Mina inställningar**. Som administratör kan du göra samma sak via sidan **Profiler (roller)**.

1. På sidan **Profiler (roller)**, markera den profil som du vill tilldela och välj sedan åtgärden **Anv. anpassningslista**.
2. På sidan **Användaranpassningar**, markera den användare som du vill tilldela profilen till och välj sedan åtgärden **Redigera**.
3. I fältet **Profil-ID** välj relevant profil.

> [!NOTE]
> Om du tilldelar en annan profil till en användare bevaras all anpassning som görs av användaren med den tidigare profilen.

## <a name="to-define-user-settings-for-a-profile"></a>Så här definierar du användarinställningar för en profil
På sidan **Mina inställningar** kan användare definiera grundläggande funktioner för sitt konto, till exempel rollcenter, språk och meddelanden. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).

Som administratör kan du definiera dessa inställningar för en profil och på så sätt tillämpa inställningarna för alla användare av den relaterade rollen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Profiler (roller)** och väljer sedan relaterad länk.
2. Markera raden för den profil som du vill ändra användarinställningar för och välj åtgärden **Lista över användaranpassningar**.
3. På sidan **användaranpassningar** öppnar du kortet för den användare vars inställningar du vill ändra.
4. På sidan **användaranpassningskort** redigerar du fälten efter behov.

## <a name="to-activate-a-profile"></a>Så här aktiverar du en profil
När en profil skapas kan du markera olika kryssrutor som definierar om, var och hur profilen och dess information ska vara tillgänglig för användarna.

* Markera följande kryssrutor på sidan **Profiler (roller)**:
    - **Aktiverad** för att ange om den relaterade rollen visas på sidan **tillgängliga roller** för användare att välja bland.  
    - **Använd som standardprofil** för att ange den profil som gäller för användare som inte har tilldelats en viss roll.
    - **Inaktivera anpassningar** för att ange om användare av den relaterade rollen kan anpassa sina arbetsytor.
    - **Visa i rollutforskaren** om du vill ange om åtgärder till affärsfunktioner som ingår i profilen ska visas i den utökade vyn av rollutforskaren, en översikt över funktioner. Mer information finns i [Söka efter sidor med rollutforskaren](ui-role-explorer.md).

## <a name="to-export-profiles"></a>För att exportera profiler
Du kan exportera profiler från [!INCLUDE[prod_short](includes/prod_short.md)], t. ex. återanvända dem i en annan innehavare. Profilerna exporteras till en zip-fil som innehåller .al-filer som kan återanvändas för att utveckla tillägg. Mer information finns i [Använda klienten för att skapa profiler och sidanpassningar](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* På sidan **Profiler (roller)**, välj åtgärden **Exportera profiler**.

En zip-fil med .al-filerna för alla profiler exporteras.

## <a name="to-import-profiles"></a>För att importera profiler
Du kan importera profiler som har exporterats från [!INCLUDE[prod_short](includes/prod_short.md)]. Stegen är mer eller mindre motsatsen till de olika stegen för att exportera profiler. Mer information finns i [För att exportera profiler](admin-users-profiles-roles.md#to-export-profiles).

1. På sidan **Profiler (roller)**, välj åtgärden **Importera profiler**.
2. Följ stegen i guiden **Importera profiler**.

    Om du bara vill importera valda profiler markerar du kryssrutan **Markerad** för att ange vilka du vill importera.
3. Välj knappen **Importera markerade**.

En zip-fil med .al-filerna för valda profiler importeras.

## <a name="to-delete-a-profile"></a>Så här tar du bort en profil
Du kan ta bort en profil genom att klicka på åtgärden **Ta bort** på sidan **Profiler (roller)**. Följande begränsningar gäller emellertid:

- Du kan inte ta bort en profil som är tilldelad till en användare eller användargrupp.
- Du kan inte ta bort profiler som härstammar från tillägg. Tillägget måste först avinstalleras.
- Du kan bara ta bort en profil i taget.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Ta bort alla anpassningar som användaren har gjort
Du kan ta bort alla ändringar som användaren gjort på sidor som utgör arbetsytan. Detta kan t. ex. vara användbart om en anställd har ändrat roll och inte längre behöver anpassningarna. Ta bort användares anpassningar ändrar tillbaka sidlayouten till det som definieras av profilen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Användaranpassning** och väljer sedan relaterad länk.

    Sidan **Användaranpassningar** visar alla användare som har gjort anpassningar.

2. Öppna kortet för en användare vars anpassningar du vill ta bort.
3. På sidan **Användaranpassningskort**, välj åtgärden **Ta bort anpassade sidor** och acceptera sedan meddelandet som visas.

Användaren kommer att se ändringarna nästa gång de loggar in.

Du kan också ta bort alla sidanpassningar för en profil. Mer information finns i [Så här tar du bort alla anpassningar för en profil](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Så här tar du bort anpassningar för specifika sidor
Du kan ta bort anpassningar som en eller flera användare har gjort på vissa sidor som utgör arbetsytan. Detta kan t. ex. vara användbart om en ändrad affärsprocedur innebär att en anpassning inte längre får användas av användarna. Ta bort användares anpassningar ändrar tillbaka sidlayouten till det som definieras av profilen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Anpassningar av användarsidan** och väljer sedan relaterad länk.

    Sidan **Anpassningar av användarsidan** visar alla sidor som har anpassats och användaren som de tillhör.

    > [!Note]
    > Ett kryss i fätet **Äldre anpassning** anger att anpassningen har skett i en äldre version av [!INCLUDE[prod_short](includes/prod_short.md)], som hanterade anpassningen på ett annat sätt. Användare som försöker anpassa dessa sidor hindras från att göra detta såvida de inte väljer att låsa upp sidan. Mer information finns i [Anledningen till att anpassningen är låst för en sida](ui-personalization-locked.md).

2. Markera raden för den sidanpassning som du vill radera och välj sedan åtgärden **Radera**.

Användaren kommer att se ändringarna nästa gång de loggar in.  

Du kan också ta bort individuella sidanpassningar för en profil. Mer information finns i [Så här tar du bort alla anpassningar för en viss sida för en profil](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Hantera användarsessioner

Som administratör av [!INCLUDE[prod_short](includes/prod_short.md)] online kan du hantera användarsessioner i administrationscentret. Mer information finns i [Hantera sessioner](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions) i administrationsinnehållet.  

För [!INCLUDE[prod_short](includes/prod_short.md)] lokal kan du t. ex. hantera sessioner med SQL Server Management Studio. Mer information finns i den [tekniska dokumentationen för SQL Server](/sql/sql-server).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/users-security-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Tilldela behörigheter till användare och grupper](ui-define-granular-permissions.md)  
[Anpassa sidor för profiler](ui-personalization-manage.md)  
[Anpassa din arbetsyta](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]