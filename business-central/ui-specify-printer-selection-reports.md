---
title: Ställa in skrivare
description: Lär dig mer om hur du konfigurerar skrivare som du kan använda för rapporter och dokument samt vilken utskriftsfunktion som är tillgänglig för dig i Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing, email printing, cloud printing, Universal Print
ms.search.form: 8900, 9018, 9022
ms.date: 06/24/2021
ms.author: jswymer
ms.openlocfilehash: 317e90976aed760f55fc7122483377e8df11c906
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8335165"
---
# <a name="set-up-printers"></a>Ställa in skrivare

Att skriva ut dokument och rapporter från [!INCLUDE[prod_short](includes/prod_short.md)] är en viktig uppgift för företagsanvändare. Användare vill vanligtvis skicka utskriftsjobb direkt till en av organisationens skrivare&mdash;oavsett vilken [!INCLUDE[prod_short](includes/prod_short.md)] klient eller app som de använder. Eftersom [!INCLUDE[prod_short](includes/prod_short.md)] online är en molntjänst kan den inte direkt nå lokala skrivare som är anslutna till användarnas enheter, men kan ansluta till molnbaserade skrivare.

För att stödja dina utskriftsbehov [!INCLUDE[prod_short](includes/prod_short.md)] finns följande funktioner:

|Funktion|Beskrivning|Webbklient| Mobilapp|App för Teams|
|-------|-----------|----------|-----------|--------------|
|Universell utskrift|Universell utskrift är en lösning för skrivarhantering som finns tillgänglig som en molntjänst från Microsoft. Med den här funktionen kan du ställa in skrivarna i Universell utskrift och sedan registrera dem för användning i [!INCLUDE[prod_short](includes/prod_short.md)]. För den här funktionen krävs en Universell utskrift-prenumeration och tillägget **Universell utskrift-integrering**|![arbetar online.](media/check.png)|![arbetar online.](media/check.png)|![arbetar online](media/check.png)|
|E-postutskrift|Med den här funktionen kan du konfigurera skrivare som har stöd för e-post. [!INCLUDE[prod_short](includes/prod_short.md)] skickar sedan utskriftsjobben till en skrivare med hjälp av skrivarens e-postadress. För den här funktionen krävs e-postaktive rad skrivare och tillägget **Skicka till e-postskrivare**.|![arbetar online.](media/check.png)|![arbetar online](media/check.png)|![arbetar online](media/check.png)|
|Webbläsarutskrift|Utskriftsjobb hanteras av utskriftsfunktionen i användarens webbläsare. Om en molnskrivare inte har installerats eller konfigurerats, eller om en installerad skrivare havererar, kommer utskriften att ske via webbläsarens standardalternativ för utskrift. Fältet **Skrivare** på sida för rapportförfrågan visas *(hanteras av webbläsaren)*.|![arbetar online](media/check.png)|||

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] stöder också anpassade skrivartillägg som lägger till ännu fler utskriftsfunktioner. Om du har installerat anpassade skrivartillägg kan det till exempel vara utskrifts funktioner som inte beskrivs i den här artikeln. 

## <a name="set-up-universal-print"></a>Ställ in Universell utskrift

Universell utskrift är en Microsoft 365-prenumerationstjänst som körs helt på Microsoft Azure. Med den här funktionen får du centraliserad utskriftshantering via Universell utskrift-portalen. [!INCLUDE[prod_short](includes/prod_short.md)] gör skrivarinställningar i Universell utskrift tillgängliga för klientanvändare via tillägget **Universell utskrift-integrering**.

![Inställning av Universell utskrift.](media/Universal-Print-arch.png)

Den fullständiga installationen kräver att du arbetar både i Microsoft Azure med [Azure-portal](https://portal.azure.com) och i [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="supported-printers"></a>Skrivare som stöds

[!INCLUDE[prod_short](includes/prod_short.md)] stöder samma skrivare som Universell utskrift, som kan vara antingen Universell utskrift-kompatibla eller icke-kompatibla skrivare. Icke-kompatibla skrivare kan inte kommunicera direkt med Universell utskrift, så de kräver extra anslutningsprogram vara, som tillhandahålls av Universell utskrift. Vissa äldre skrivare kanske inte stöds. 

<!-- TODO If not installed, go to AppSource -->

### <a name="prerequisites"></a>Förutsättningar

**För [!INCLUDE[prod_short](includes/prod_short.md)]**

- [!INCLUDE[prod_short](includes/prod_short.md)] utgivningscykel 1 år 2021 eller senare
- Tillägget för **Universell utskrift-integrering** är installerat

    Tillägget publiceras och installeras som standard som en del av [!INCLUDE[prod_short](includes/prod_short.md)] online och lokalt.  Du kan kontrollera om den är installerad på sidan **Tilläggshantering**. Mer information finns i [Installera och avinstallera tillägg i Business Central](ui-extensions-install-uninstall.md).
- [!INCLUDE[prod_short](includes/prod_short.md)] lokalt:
  - Azure Active Directory (AD) eller NavUserPassword-autentisering konfigureras.
  - Ett program för Business Central har registrerats i din Azure AD klientorganisation och [!INCLUDE[prod_short](includes/prod_short.md)]

      Precis som andra Azure-tjänster som arbetar med [!INCLUDE[prod_short](includes/prod_short.md)], Universell utskrift kräver en appregistrering för [!INCLUDE[prod_short](includes/prod_short.md)] i Azure Active Directory (Azure AD). Programregistreringen tillhandahåller autentisering och autentiseringstjänster mellan [!INCLUDE[prod_short](includes/prod_short.md)] och Universell utskrift.

      Din distribution kanske redan använder en appregistrering för andra Azure-tjänster som Power BI. Om så är fallet ska du använda den befintliga appregistreringen även för Universell utskrift, i stället för att lägga till en ny. Det enda du behöver göra i det här fallet är att ändra appregistreringen så att den innehåller relevanta utskriftsbehörigheter för Microsoft Graph API.

      Om du vill registrera en app som en uppsättning med lämpliga behörigheter följer du de steg som beskrivs i [Registrera ett program i Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

**För Universell utskrift**

- En Universell utskrift-prenumeration/licens för organisationen.

    Mer information finns i [licens för Universell utskrift](/universal-print/fundamentals/universal-print-license).

- Du har rollerna **Utskriftshantering** och **Global administratör** i Azure.

    För att kunna hantera Universell utskrift måste ditt konto ha rollerna **Utskriftshantering** and **Global administratör** i Azure AD. Dessa roller behövs bara för att hantera Universell utskrift. De krävs inte av användarna för att de ska kunna använda skrivarna i [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="set-up-universal-print-and-add-printers-in-microsoft-azure"></a>Konfigurera Universell utskrift och lägg till skrivare i Microsoft Azure

Innan du kan börja hantera Universell utskrift-skrivare i Business Central finns det flera uppgifter du måste gå igenom för att Universell utskrift ska kunna köras i Azure med de skrivare du vill använda.

För detaljerade instruktioner om hur du installerar, se [Komma igång: Ställ in Universell utskrift](/universal-print/fundamentals/universal-print-getting-started) i Universell utskrift-dokumentation. Här följer en översikt över de steg du måste utföra. De flesta av dessa steg är gjorda på Azure-portalen.

1. Tilldela Universell utskrift-licenser till dig själv och andra användare.

    Hur du tilldelar licensen beror på om du integrerar med Business Central online eller lokal.

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] online tilldelar du licenser genom att använda Microsoft 365-administrationscentret.

      Mer information finns i [Hjälp för Microsoft administrationscenter – tilldela licenser till användare](/microsoft-365/admin/manage/assign-licenses-to-users).

    - Med [!INCLUDE[prod_short](includes/prod_short.md)] lokala fördelar tilldelar du licenser i din Azure-klient med hjälp av Azure-portalen.

      Mer information finns i [Azure Directory – Tilldela eller ta bort licenser i Azure Active Directory-portalen](/azure/active-directory/fundamentals/license-users-groups).

2. Installera anslutningsprogrammet för Universell utskrift för att registrera skrivare som inte kan kommunicera direkt med Universell utskrift.

    De flesta skrivare på marknaden kan inte kommunicera med Universell utskrift direkt. Du måste installera anslutningsprogrammet för Universell utskrift för dessa skrivare. Mer information finns i [Installera anslutningsprogrammet för Universell utskrift](/universal-print/fundamentals/universal-print-connector-installation).

3. Registrera dina skrivare i Universell utskrift.

    Att registrera en skrivare gör Universell utskrift medveten om skrivaren.

    - Följ instruktionerna från skrivartillverkaren för skrivare som kan kommunicera direkt med Universell utskrift.

    - För andra skrivare registrerar du skrivarna med hjälp av anslutningsprogrammet för Universell utskrift. 

      Mer information finns i [Skrivarregistrering](/universal-print/fundamentals/universal-print-connector-printer-registration).

4. Ändra skrivaregenskaper (valfritt)

    När en skrivare har registrerats kan du visa och ändra skrivaregenskaperna, som standardinställningar.

    Mer information finns i [Hantera skrivarinställningar med hjälp av den universella utskriftsportalen](/universal-print/portal/configure-printer-settings).

5. Dela skrivarna.

    Alla skrivare som du vill använda i [!INCLUDE[prod_short](includes/prod_short.md)] måste delas ut i Universell utskrift.

    <!--For more information, see [Share a Printer](/universal-print/fundamentals/universal-print-printer-permissions#share-a-printer). -->

    Mer information finns i [Dela en skrivare](/universal-print/portal/share-printers).

6. Ge användarna behörighet till de delade skrivarna.

    <!--For more information, see [Printer Permissions](/universal-print/fundamentals/universal-print-printer-permissions#printer-permissions).-->

    Mer information finns i [Skrivarbehörigheter](/universal-print/portal/share-printers#configure-user-permissions-for-a-printer-share).


7. Aktivera dokumentkonvertering.

    Med Universell utskrift återges innehåll som ska skrivas ut i XPS-format. Vissa äldre skrivare på marknaden stöder inte rendering av XPS-innehåll&mdash;i många fall endast PDF-format. Utskrift till dessa skrivare misslyckas om inte Universell utskrift är inställt för att konvertera dokument till det skrivarstödda formatet.

    Mer information finns i [Översikt över dokumentkonvertering](/universal-print/portal/document-conversion).

Nu kan du lägga till skrivarna till [!INCLUDE[prod_short](includes/prod_short.md)], konfigurerar standardskrivare för rapporter och skriva ut.  

### <a name="add-universal-printer-printers-to-business-central"></a>Lägga till Universell skrivare till Business Central

När du har skapat och delat ut skrivare i Universell skrivare kan du börja använda dem i Business Central. Det finns två sätt att lägga till skrivare på Universell skrivare. Du kan lägga till alla skrivarna på en gång eller individuellt, en i taget.

Lägga till skrivare individuellt vill du installera samma Universell skrivare i Business Central mer än en gång. För varje skrivare som har lagts till kan du ändra utskriftsinställningarna, t.ex. papperskassett, storlek och orientering. På så sätt kan du lägga upp skrivare för olika rapporter och dokument som har särskilda krav på utdata.
  
<!-- To Do Adding printers individually lets you duplicate printers with custom , like different paper trays and paper size and orientation.  To add printers individually, you'll need to know printer's share name in Universal Print. -->

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utskriftshantering** och väljer sedan relaterad länk.
2. Välj **Universell utskrift** och välj sedan något av följande alternativ:

    - **Lägg till alla skrivare för Universell utskrift** som inte redan har lagts till. Du kan använda det här alternativet även om det redan finns skrivare som har lagts till. 

    - **Lägga till en skrivare för Universell utskrift** om du vill lägga till en viss skrivare.  
3. Följ instruktionerna på skärmen.

    - Om du väljer **Lägg till alla skrivare för Universell utskrift**, sedan startar inställningen av **Lägg till skrivare för Universell utskrift**. <!--This setup leads you through the process of verifying your Azure AD setup (for on-premises), checking your Universal Print license, and then finally adding the printers.-->

    - Om du väljer **Lägg till alla skrivare för Universell utskrift**, sedan visas sidan av **Skrivare för Universell utskrift**. Fyll i fältet **Namn**, välj **...** bredvid fältet **Utskriftsresurs i Universell utskrift** för att välja skrivare i Universell utskrift. Fyll i återstående fält om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
  
    Med de här åtgärderna kan du verifiera inställningen för Azure AD (lokalt) kontrollera att du har Universell utskrift-licens och lägg sedan till skrivarna.

    > [!NOTE]
    > För lokalt, om det är första gången som du ansluter till Universell utskrift visas sidan TJÄNSTEBEHÖRIGHETER FÖR AZURE ACTIVE DIRECTORY och du uppmuntras att ge tillstånd till Azure-tjänster. Du behöver bara ge samtycke en gång.

När du har lagt till en skrivare kan du visa och ändra dess inställningar från **Skrivarhanteringen**. Markera bara skrivaren och välj sedan **Redigera skrivarinställningar**. 

<!--
### Troubleshooting

#### You don't see the a printer in the 

The printer is not shared in Universal Print.

### You get an error when tryong to add all or a single printer

You have'nt been assigned a Uincersla Print license.

There was an error fetching printers shared to you. You don't have access to the data. Make sure your account has been assigned a Universal Print license and you have the required permissions.
or 
You don't seem to have access to Universal Print. Make sure you have a Universal Print subscription, and that your account has been assigned a Universal Print license.

## Could not upload the document to print job 50.

There is a technical problem withe the printer. Unsupported document-format: application/pdf. Supported formats: Attribute document-format-supported: SimpleIppValue-Type:MimeMediaType-Value:application/oxps

## You don't have access to the printer

- You have not been assigned a Up license
- You have not been given access to the printer in UP.
- (On-prem) The app registration has been broken
-->
## <a name="set-up-email-print"></a>Konfigurera e-postutskrift

### <a name="prerequisites"></a>Förutsättningar

- [!INCLUDE[prod_short](includes/prod_short.md)] utgivningscykel 1 år 2020 eller senare
- Tillägget **Skicka till e-postskrivare** är installerat

    Detta tillägg instalelras dessutom som standard. Information om hur du installerar tillägg finns i 
- E-postfunktionen har konfigurerats.

   Mer information finns i [Konfigurera e-post](admin-how-setup-email.md).

### <a name="add-an-email-printer"></a>Lägg till en e-postskrivare

På sidan **Utskriftshantering** kan du se vilka skrivare som är inställda. Sidan ger dig också åtkomst till sidan **Inställningar** för varje skrivare att redigera en befintlig installation eller ställa in en ny skrivare.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utskriftshantering** och väljer sedan relaterad länk.
2. Välj **E-posta utskrift** och välj sedan **Lägg till en e-postskrivare**.
3. På sidan **Inställningar av e-postskrivare** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du måste manuellt välja rätt pappersstorlek för en skrivare eftersom det varken finns någon lokal skrivare eller några användarinställningar som kan lagras.
    >
    > Tänk på att tillägget för e-postskrivare som standard är inställt på pappersformatet **A4**, vilket exempelvis inte lämpar sig för Nordamerika.

### <a name="privacy-notice"></a>Sekretesspolicy

Om du använder tillägget för e-postskrivare skickas alla eller vissa utskriftsjobb till den e-postadress konfigureras för skrivaren. Vi rekommenderar starkt att ett unikt e-transaktion-ID kopplas till en skrivarenhet endast med de officiella tjänster som tillhandahålls av maskinvarutillverkaren, till exempel HP ePrint, KonicaMinolta EveryonePrint eller Epson Email Print.

Du måste vidta alla nödvändiga sekretessåtgärder, inklusive att se till lösningen för e-postutskrift har korrekt konfigurerade behörigheter, sekretessinställningar och lagringsmetoder. Det är ditt ansvar att skapa en korrekt, verifierad och fungerande e-postadress. Mer information finns i [Microsofts sekretesspolicy](https://privacy.microsoft.com/privacystatement).


## <a name="set-up-default-printers"></a><a name="default"></a>Ställa in standardskrivare

Det finns ett par sätt att installera skrivare som ska användas som standard för utskriftsjobb. En standardskrivare är användbar om du arbetar med olika rapporter som kräver olika skrivare på grund av sin placering i företaget eller deras utskriftskapacitet.

### <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Ange en skrivare som standardskrivare för alla utskriftsjobb

På sidan **Skrivarhantering** kan du ställa in en skrivare som standardskrivare för alla utskriftsjobb. Du kan ange skrivaren som standard för dig eller för alla användare.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Utskriftshantering** och väljer sedan relaterad länk.

    > [!TIP]
    > Du kan också öppna sidan **Utskriftshantering** från sidan **Skrivarval** genom att välja **Utskriftshantering**.  
2. På sidan **Utskriftshantering** välj en skrivare från listan, välj **Hantera**, välj sedan **Ange som standardskrivare** eller **Använd som standardskrivare för alla användare**.

> [!NOTE]
> Om du anger en standard skrivare från **skrivarhanteringen** läggs en post till i **skrivarvalet**.

### <a name="set-a-default-printer-for-specific-reports"></a>Ange standardskrivaren för specifika rapporter

På sidan **Skrivarval** låt oss ange skrivaren som en rapport ska använda som standard. Standard skrivare är inställda på användarkontots grunder. Du kan ange en standardskrivare för bara dig själv, en annan användare eller alla användare.

> [!IMPORTANT]
> För [!INCLUDE[prod_short](includes/prod_short.md)] lokal, kan sidan **Val av skrivare** kan endast användas för molnskrivare definierade av skrivartillägg, som e-postutskrift och skrivare för Universell utskrift. Det kan inte användas för lokala skrivare.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Utskriftsval** och väljer sedan relaterad länk. Du kan också välja sidan **Skrivarhantering** och sedan välja åtgärden **Skrivarhantering**.
2. Välj åtgärden **Ny** om du vill lägga till ett Skrivarhantering för en specifik rapport.
3. Fyll i fälten om det behövs.

Den angivna rapporten är nu konfigurerad för att skriva ut på den valda skrivaren som standard.

> [!NOTE]
> När du skriver ut rapporten i fråga kan du välja en annan med hjälp av fältet **Skriv ut** på sidan för begäran.

> [!NOTE]
> Om du inte anger en rapport för en viss skrivare på sidan **Skrivarhantering** kommer den att skrivas ut till företagets standardskrivare enligt definitionen på sidan **Skrivarhantering**.

Du eller administratören kan också använda sidan **Skrivarhantering** för att definiera andra utskriftsvariationer för användare och rapporter. I följande tabell beskrivs kombinationen av värdena för att ange olika utskriftsinställningar för en rapport.

|Till                                                 |Ange följande värden                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Skriv ut en rapport till en viss skrivare för alla användare |Ange värden i fälten **Rapport-ID** och **Skrivarnamn** och lämna fältet **Användar-ID** tomt.|
|Skriv ut alla rapporter till en viss skrivare för en specifik användare|Ange värden i fälten **Användar-ID** och **Skrivarnamn** och lämna fältet **Rapport-ID** tomt. Denna post gör samma sak som åtgärden **Ange som standardskrivare** på sidan **Utskriftshantering**.|
|Ange standardskrivaren för alla rapporter för alla användare|Ange ett värde i fälten **Skrivarnamn** och lämna fälten **Användar-ID** och **Rapport-ID** tomma. Denna post gör samma sak som åtgärden **Ange som standardskrivare för alla användare** på sidan **Utskriftshantering**.|
|Skriv ut en viss rapport till användarens standardskrivare|Ange ett värde i fältet **Rapport-ID** och lämna fälten **Skrivarnamn** och **Användar-ID** tomma.|
|Skriv ut en specifik rapport till en viss skrivare för en viss användare|Ange värden i samtliga tre fält.|

> [!NOTE]
> Mer specifika skrivarval har företräde framför mer allmänna skrivarval. Ett skrivarval som exempelvis har värden i fälten **Användar-ID**, **Rapport-ID** och **Skrivarnamn** har företräde framför ett skrivarval som innehåller tomma poster i fälten **Användar-ID** och **Rapport-ID**.

### <a name="choosing-the-printer-when-running-a-report"></a>Välja skrivare när en rapport körs
I stället för att använda standardskrivaren när du kör en rapport kan du åsidosätta inställningen från begärandesidan. Välj helt enkelt den skrivare som du vill använda för detta anrop i rapporten i listrutan **Skrivare**.

### <a name="sizing-print-jobs"></a>Ändra storlek på utskriftsjobb

Molnutskrift är utformat för dokument av rimligt storlek. De flesta molntjänster, inklusive PrintNode och HP ePrint, har en gräns på 10 MB per jobb. Om du behöver skriva ut större rapporter måste du kanske dela upp dem i flera utskrifter.

## <a name="see-also"></a>Se även

[Skriva ut en rapport](ui-work-report.md#PrintReport)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kör batchjobb](ui-how-run-batch-jobs.md)  
[Skicka dokument via e-post](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
