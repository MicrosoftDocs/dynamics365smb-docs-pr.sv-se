---
title: Chatt med Copilot (förhandsversion)
description: Läs mer om hur du använder chatt med Copilot för att hitta data och få hjälp i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/18/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# <a name="chat-with-copilot-preview"></a>Chatt med Copilot (förhandsversion)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

I den här artikeln beskrivs hur du chattar med Copilot för att få svar om dina företagsdata och hjälp med uppgifter och ämnen relaterade till Business Central.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-chat-with-copilot"></a>Om chatt med Copilot

Microsoft Copilot är den AI-drivna assistenten som hjälper till att gnista kreativitet, öka produktiviteten och eliminera tråkiga uppgifter. Du kan chatta med Copilot i Business Central för att svara på frågor och hitta affärsdata genom att uttrycka vad du letar efter på naturligt språk. Du kan använda chatten för att:

- Hitta affärsdata för företaget du arbetar med i Business Central. Använd chatt för att söka efter (och öppna) data om entiteter/poster som är relaterade till affärsprocesser, till exempel kunder, leverantörer, försäljningsorder och artiklar med mera. Fråga till exempel Copilot: "Visa den senaste försäljningsordern för Adatum."
- Förklara ett koncept eller få vägledning om hur du utför en uppgift. Fråga till exempel "Hjälp mig förstå dimensioner" eller "Hur bokför jag en försäljningsorder".
- Förstå syftet med och den typiska användningen av enskilda fält. När du väljer **Fråga Copilot** i en knappbeskrivning för ett fält öppnas chatten med en Förklara-prompt för fältnamnet och Copilot ger information om det. Copilot länkar till artiklarna som den hänvisade till, så det är enkelt att verifiera beskrivningen.

  De svar som Copilot ger baseras enbart på den officiella Dynamics 365 Business Central dokumentationen, som finns tillgänglig på Microsoft Learn på [Dynamics 365 Business Central dokumentationen](/dynamics365/business-central/).

Chatta med Copilot kringgår behovet av att navigera i användargränssnittet eller produkthjälpen, vilket kan spara tid och öka produktiviteten.
  
> [Titta på video](https://go.microsoft.com/fwlink/?linkid=2250609)

## <a name="prerequisites"></a>Förutsättningar

- Möjligheten att chatta med Copilot är aktiverad. Denna uppgift utförs av en administratör. [Läs mer om hur du konfigurerar Copilot- och AI-funktioner](enable-ai.md).
- Visningsspråket i Business Central är inställt på något av följande engelska språk: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Läs mer om hur du ändrar språk](ui-change-basic-settings.md#language).
- Din Business Central-miljö finns i alla länder/regioner utom Kanada (den här funktionen är ännu inte tillgänglig i Kanada).

## <a name="get-started-using-chat-with-copilot"></a>Kom igång med chatt med Copilot

1. I det övre högra hörnet av skärmen väljer du ikonen ![Visar ikonen för chatt med Copilot](media/chat-copilot-icon.png) **Copilot** ![Visar bildtext nummer 1](media/callout-number-1.svg).

   Fönstret **Copilot** visas till höger enligt bilden nedan:

    ![Visar ikonen för chatt med Copilot-fönstret med bildtexter](media/chat-with-copilot-pane.svg)

1. I rutan **Ställ en fråga** längst ned ![Visar bildtext nummer 2](media/callout-number-2.svg) anger du din fråga och väljer sedan pilspetsen eller trycker på <kbd>Retur</kbd> för att få ett svar.

   Texten du anger, som ofta kallas en *prompt* när det gäller Copilot, kan vara i form av en fråga, ett uttalande eller ett kommando.

   > [!TIP]
   > Copilot innehåller ett par funktioner som kan hjälpa dig att skriva frågor:
   > - Kom igång med att formulera en fråga genom att välja en av snabbguiderna&mdash;**Sök**, **Förklara** eller **Guide**&mdash;som finns överst i fönstret ![Visar bildtext nummer 3](media/callout-number-3.svg) eller från ![ikonen Visar frågeguiden](media/prompt-guide-icon.png) **Visar prompter** ovanför rutan **Ställ en fråga** ![Visar bildtext nummer 4](media/callout-number-4.svg). Frågeguider är fördefinierade korta fraser som inleder en fråga eller prompt. Förutom att spara tid är de utformade för att vägleda Copilot-svar mot en kategori med svar. De hjälper dig också att förstå hur du formulerar frågor för att få de bästa svaren.
   > - Välj promptförslagen ovanför knappen **Visa prompter** ![Visar bildtext nummer 5](media/callout-number-5.svg) om du automatiskt vill ställa en fördefinierad fråga för att få insikt i hur frågorna och svaren fungerar. Promptförslag är bara tillgängliga när du använder CRONUS demonstrationsföretaget.

1. Granska svaren som visas i Copilot-rutan ![Visar bildtext nummer 6](media/callout-number-6.svg).

   Beroende på din fråga kan svaret innehålla text, länkar till poster eller sidor i Business Central och länkar till Business Central-hjälpartiklar om Microsoft Learn.

1. Ställ en annan fråga för att förfina svaret.

   Chatt kommer ihåg sammanhanget, vilket innebär att du inte behöver upprepa viktiga punkter från den ursprungliga frågan.

## <a name="clear-chat-to-start-over"></a>Ta bort chatten och börja om

Om du vill växla till ett annat samtalsämne med Copilot väljer du ikonen ![Visar ikonen Rensa chatt](media/clear-chat-icon.png) **Starta en ny ikon för Copilot-chattsession** längst ned i Copilot-rutan ovanför frågerutan. Den här åtgärden rensar minnet i Copilot från dina senaste meddelanden. Att börja om är ofta användbart efter en lång konversation med många meddelanden, och det kan hjälpa Copilot att leverera mer exakta svar.

Chatten rensas också om du stänger eller loggar ut från Business Central.

## <a name="get-the-most-out-of-your-questions"></a><a name="tips"></a>Få ut mesta möjliga av dina frågor

I det här avsnittet kan du förbättra svaren du får från Copilot.

- Ställ tydliga och specifika frågor.
- Var kortfattad och undvik långa meningar eller flera meningar.
- Ställ en fråga i taget. <!--Avoid asking about multiple questions in one message.-->
- Använd naturligt språk och uttryck frågorna på ett vänligt och konversationsmässigt sätt.
- Använd nyckelord, fraser och termer som du vet används i Business Central, antingen i appen eller dokumentationen.
- Om det första svaret inte helt svarar på dina frågor, ställ uppföljningsfrågor eller omformulera den sista frågan.
- Om du ställer en fråga om ett annat ämne än föregående fråga rensar du den aktuella chattsessionen för att börja om.

## <a name="example-prompts"></a>Exempel på prompter

Dina frågor till Copilot varierar naturligtvis beroende på din roll, nuvarande uppgift, de processer som din organisation följer och hur du uttrycker dig i ord. Följande är exempel som visar olika sätt att ställa frågor i chattfönstret som kan inspirera dig att skriva egna frågor baserade på din egen unika situation.

Prompt: `Find the Item with Description 'ATHENS Desk'`

I det här exemplet ger du tydliga instruktioner för Copilot att hitta en enskild post. Du kan till exempel antyda att posten finns i listan Artikel. Du anger att fältet "Beskrivning" måste vara en specifik text som du har skrivit med citattecken och med korrekta versaler. Copilot svarar vanligtvis exakt när han får några exakta tips, men du kan också använda ett mer avslappnat språk som i nästa exempel.

Prompt: `give me the latest invoice for adatum`

I det här exemplet ber du Copilot att hitta en post, men frågan är mindre exakt och kan resultera i ett mindre exakt svar. Copilot kan ofta förstå, eller gissa, att fakturan du letar efter inte är en inköpsfaktura utan en försäljningsfaktura från listan Bokförd försäljningsfaktura. Copilot skulle också behöva matcha `adatum` med `Adatum Corporation`, det vill säga det fullständiga och exakta namnet på det försäljningskundnamn som är kopplat till fakturan.

Prompt: `Show me customer ledger entries for Adatum from about three weeks ago`

I det här exemplet ber du copilot att lösa ett vanligt datumpussel som vanligtvis kräver att du öppnar en kalender som referens eller använder avancerade datumintervallfilter. Copilot kan vanligtvis förstå vanliga uttryck och affärstermer.

Prompt: `How does I save my filterrings to do them later?`

I det här exemplet ber du Copilot om vägledning om hur du utför en uppgift i Business Central. Copilot kan vanligtvis förstå avsikten med din fråga, även om det finns några grammatiska fel, stavfel eller förkortningar.

Prompt: `Provide feedback on answers`

Du kan betygsätta svaren du får från Copilot genom att använda gilla-knappen (tummen upp) för bra betyg eller ogilla-knappen (tummen ned) för ett dåligt betyg. När du väljer knappen ogilla kan du välja en anledning, inklusive felaktig, olämplig eller annan. Denna information kan hjälpa oss att förbättra förslagen.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
## <a name="see-also"></a>Se även

[Felsöka Copilot- och AI-funktioner](ai-copilot-troubleshooting.md)  
[Konfigurera Copilot- och AI-funktioner](enable-ai.md)  
[Vanliga frågor och svar om Ansvarsfull AI för chatt med Copilot](faqs-chat-with-copilot.md)  
[Resurser för hjälp i Business Central](product-help-and-support.md)  