---
title: Kom igång med en Business Central förhandsversion för Copilot
description: I artikeln beskrivs hur du skaffar en Business Central-miljö med den nya AI-funktionen för att skapa textförslag för artikel-/produktbeskrivningar.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# <a name="get-started-with-a-business-central-preview-version-for-copilot"></a><a name="get-started-with-a-business-central-preview-version-for-copilot"></a><a name="get-started-with-a-business-central-preview-version-for-copilot"></a>Kom igång med en Business Central förhandsversion för Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Du kan försöka använda AI-baserad text för marknadsföring av text med en Copilot, oavsett om du är en befintlig Business Central-kund eller en potentiell kund, det vill säga någon som är intresserad av att utforska Business Central och testa den nya funktionen. För att komma igång måste du ha tillgång till en version av Business Central Online som stöder den nya funktionen. Slutför det avsnitt nedan som gäller dig.

## <a name="your-organization-already-uses-business-central"></a><a name="your-organization-already-uses-business-central"></a><a name="your-organization-already-uses-business-central"></a>Organisationen använder redan Business Central

Som befintlig kund eller partner behöver du en administratör som har tillgång till Business Central administrationscenter för att konfigurera en miljö som kör den förhandsversion som innehåller Copilot. När miljön är igång kan användarna prova den nya funktionen.

Om du är miljöadministratör utför du följande steg:

1. Logga in på administrationscenter för Business Central.
2. Välj **Miljöer** > **Ny**.
3. I fönstret **Skapa miljö** anger du ett namn för den nya miljön i fältet **Miljönamn**.
4. Ange **Miljötyp** till **Begränsat läge** eller **Produktion**.
5. Ange **land** för valfritt land/region i listan, men tänk på att den AI-genererade marknadsföringstexten från Copilot endast är på engelska.
6. I rutan **Version** väljer du en version 22 eller senare från listan.

   <!--
   > [!IMPORTANT]
   > You must use **22.0.54157.54311 (Preview - Copilot edition)** to experience Copilot.
   -->
7. Välj **skapa**.  

Om du vill ha mer information om hur du skapar miljöer går du till [Skapa en miljö](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Om begränsade miljöer i förhandsversion som kör **22.0.54157.54311 (förhandsversion – Copilot-version)** bör du vara medveten om att dessa miljöer endast är tillgängliga till 1 maj 2023. Efter det här datumet måste du konfigurera en ny miljö, eller uppgradera alla andra miljöer till version 22.0 eller senare om du vill fortsätta att försöka förhandsgranska AI-baserad text.

## <a name="your-organization-doesnt-use-business-central"></a><a name="your-organization-doesnt-use-business-central"></a><a name="your-organization-doesnt-use-business-central"></a>Organisationen använder inte Business Central

Om du inte är en Business Central-kund kan du registrera dig för en kostnadsfri utvärderingsversion för att testa de nya AI-funktionerna. Det är enkelt att registrera sig för utvärderingsversionen. Du vägleds genom några steg där du måste ange en del information, t.ex. e-postadress, telefonnummer och namn. Slutför följande steg om du vill skaffa utvärderingsversionen:

1. Gå till [den här provwebbplatsen](https://go.microsoft.com/fwlink/?linkid=2227167) för att komma igång med registreringsprocessen.
2. Följ instruktionerna på skärmen.

   Du ombeds ange information som din e-postadress, ditt namn och ditt telefonnummer. Den exakta upplevelsen kan variera beroende på vilken information du anger. <!--But here are a couple important points to be aware of as you run through the sign-up process:--> För e-postadress använder du din e-postadress på jobbet eller i skolan. Vi upprättar din utvärderingsversion på ditt företagskonto. Du kan inte använda e-postadresser som tillhandahålls av e-posttjänster för konsumenter eller telekommunikationsleverantörer, som till exempel outlook.com, hotmail.com, gmail.com och andra.
   
   <!-- When you get to the option for **Country or region** be sure to set this **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  -->
3. När du kommer till steget **bekräftelseinformation** kan du börja utvärderingen.

   - Om du vill gå direkt till Business Central, välj **Hoppa över och gå till Dynamics 365 Business Central** > **Kom igång**.
   - Du kan också bjuda in andra i organisationen till den kostnads fria utvärderingsperioden. Ange bara e-postadresserna till varje person och välj sedan **Skicka inbjudningar**. Välj **Kom igång** för att gå till Business Central.  

   Du kommer att omdirigeras till din utvärderingsversion på [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). Det kan ta flera minuter innan utvärderingsversionen börjar bli klar första gången du loggar in.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. När du har loggat in visas startsidan för Business Central, som kallas rollcentret, som ser ut ungefär så här:

   [![Visar rollcenter för Business Central och checklista för Copilot](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. För att få en guidad introduktion till att skapa AI-baserad marknadsföringstext för artikel med Copilot, under **Din checklista** längst upp på sidan, välj **Skapa med Copilot** > **Starta visningen**. Följ bara instruktionerna på skärmen.

   > [!TIP]
   > Om du inte ser **Dina checklistor**, välj knappen **Visa demopresentationer** först.

## <a name="next-steps"></a><a name="next-steps"></a><a name="next-steps"></a>Nästa steg

AI-funktionerna som tillhandahålls av en Copilot måste aktiveras innan du eller någon annan kan använda en Copilot. För att aktivera AI-funktionerna måste en administratör samtycka till villkoren i [förhandsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) och [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839) för organisationens räkning.

> [!NOTE]
> Om du använder en utvärderingsversion är du administratör. Om du har bjudit in andra personer i organisationen till utvärderingsversionen under registreringen kan de inte använda Copilot förrän du godkänner villkoren.

Det finns två sätt att godkänna som en administratör:

- Det enklaste sättet är att använda Copilot. Första gången du använder Copilot som administratör uppmanas du att granska villkoren och sedan godkänna eller avböja dem. Om du vill veta hur du använder en Copilot går du till [Lägg till marknadsföringstext till artiklar](item-marketing-text.md).  

- Det andra är att använda sidan **Status för sekretessmeddelanden** i Business Central och godkänn integrering av **Azure OpenAI** för alla användare. Mer information finns i [godkänna allmänna villkor](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Översikt över marknadsföringstext för AI-baserad artikel med Copilot](ai-overview.md)  
[Konfigurera marknadsföringstext för AI-baserad artikel med Copilot som en administratör](enable-ai.md)  
[Skapa marknadsföringstext för artiklar som använder Copilot](item-marketing-text.md)  
[Marknadsföringstext för AI-baserad artikel (förhandsversion) med vanliga frågor och svar om Copilot](ai-faq.md)  
