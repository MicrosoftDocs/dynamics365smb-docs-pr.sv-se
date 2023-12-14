---
title: Felsök anslutning
description: I artikeln beskrivs hur du använder sidan felsök anslutning för att identifiera och lösa problem vid anslutning till Business Central Online.
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'connectivity, troubleshooting, connection problems'
ms.date: 11/24/2023
ms.author: jswymer
ROBOTS: NOINDEX
---

# Felsökning: anslutning för Business Central

> **GÄLLER:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Den här funktionen finns i förhandsgranskning. Funktionalitet och dokumentation kan ändras i senare versioner. Om du vill bidra till dokumentationen med utgångspunkt från dina egna resultat väljer du ![Redigera artikel i GitHub.](media/github-edit-pencil.png) **Redigera** och föreslå ändringar. Sedan kommer vi att ta en titt!

[!INCLUDE[prod_short](includes/prod_short.md)] Online innehåller **Felsökning anslutning** som du kan använda för att identifiera problem med anslutningen till online-tjänsten. Det finns flera saker som påverkar anslutningen till Business Central, till exempel brandväggsinställningar för konfiguration av nätverks- eller domännamntjänst. På sidan kan du köra en lista över kontroller som diagnostiserar vanliga problem med Business Central-anslutning. Du kan använda informationen för att försöka rätta till problemen själv eller för att skicka den till din support representant.

> [!NOTE]
> På sidan **felsöka anslutning** testas nätverkets prestanda eller pålitlighet, liksom anslutningens hastighet. Den verifierar endast anslutningen till olika resurser.

## Starta anslutningskontrollen 

1. Öppna en webbläsare.
2. I adressen anger du webbadressen som du använder för att öppna Business Central och lägg till `/connectivity` på slutet. 

    Om du till exempel använder `https://businesscentral.dynamics.com` skriver du:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

    Om URL: en innehåller klientorganisations-ID, `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB` skriver du t.ex.:

    ```http
    https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
    ```
 
3. På sidan **Felsöka anslutning** väljer du **Starta kontroll**.

    En serie kontroller körs och resultatet av varje kontroll visas:

    - ![Anslutningskontrollen har slutförts.](media/connectivity-check.png) visar att kontrollen har utförts.
    - ![Anslutningskontrollen misslyckades.](media/connectivity-failed.png) visar att kontrollen misslyckades. Granska meddelandet nedanför kontrollen om du vill ha mer information.
    - ![Anslutningskontrollen kördes inte.](media/connectivity-blocked.png) anger att kontrollen inte har utförts, oftast på grund av ett fel i en tidigare kontroll. Granska meddelandet nedanför kontrollen om du vill ha mer information.

4. Om du vill köra kontrollen igen, välj **Starta om kontroll**.

De kontroller som körs beskrivs i följande avsnitt, och några tips på hur du kan åtgärda problemen.

## Grundläggande internetanslutning

Kontrollerar att du har anslutning till Internet genom att kontrollera att du har åtkomst till en känd offentlig domän som www.bing.com.

|Problem|Vad du kan göra|
|-------|-------------|
|Din webbläsare stöder inte den här kontrollen|Öppna sidan i en webbläsare som stöds och försök igen. En lista över vilka webbläsare som stöds finns i [Minimikrav för att använda Business Central – webbläsare](product-requirements.md#browsers)|
|Det gick inte att skicka ping till servern på följande URL: {url}|Kontrollera dina brandvägginställningar.|

## CDN (Content Delivery Network) inläsning av resurser

[!INCLUDE[prod_short](includes/prod_short.md)] använder Azure Content Delivery Network (CDN) för att tillhandahålla resurser som krävs för att köra Business Central webbklienten. Den här kontrollen kontrollerar att de resurser som krävs är tillgängliga och kan nås genom att skicka ping till Business Central-instansen i CDN.

|Problem|Vad du kan göra|
|-------|-------------|
|Din webbläsare stöder inte den här kontrollen|Se kontrollen **Grundläggande internetanslutning**.|
|Det gick inte att skicka ping till servern på följande URL: {url}|Kontrollera dina brandvägginställningar.|

## Användarautentisering

Kontrollerar att den aktuella användaren har loggat in med ett giltigt Business Central-konto.

|Problem|Vad du kan göra|
|-------|-------------|
|Ingen användare är för närvarande autentiserad|Logga in på Business Central med giltigt användarnamn och lösenord.|

## Identifiering av Business Central-miljöer

Söker efter Business Central-miljöer som är tillgängliga för en autentiserad användare och verifierar sedan om användaren kan autentiseras i miljön.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Problem|Vad du kan göra|
|-------|-------------|
|Ingen autentiserad användare kan utföra den här kontrollen för|Se kontrollen **användarverifiering**.|
|Det gick inte att hämta tillgängliga miljöer för ditt konto.|Kontrollera listan över tillgängliga miljöer i administrationscentret för Business Central.|
|Ditt användarnamn eller lösenord är felaktigt, eller också har du inget giltigt konto.| Kontrollera att du har loggat in med rätt användarnamn och lösenord.|

## Anslutning för apptjänst

Kontrollerar att den autentiserade användaren kan ansluta till en identifierad miljö, vanligtvis från produktionsmiljön.

|Problem|Vad du kan göra|
|-------|-------------|
|Ingen autentiserad användare kan utföra den här kontrollen för|Se kontrollen **användarverifiering**.|
|Det gick inte att hämta tillgängliga miljöer för ditt konto.|Se **Identifiering av Business Central-miljöer**.|
|Ingen grupperad adress att utföra den här kontrollen för|Kontrollera listan över tillgängliga miljöer i administrationscentret för Business Central.|
|Versionsslutpunkten finns inte|Kontrollera listan över tillgängliga miljöer i administrationscentret för Business Central.|

## Webbserveranslutning

Kontrollerar att den autentiserade användaren kan upprätta anslutningar till webbservern.

|Problem|Vad du kan göra|
|-------|-------------|
|Ingen autentiserad användare kan utföra den här kontrollen för|Se kontrollen **användarverifiering**.|
|Det gick inte att hämta tillgängliga miljöer för ditt konto.|Se **Identifiering av Business Central-miljöer**.|
|Ingen grupperad adress att utföra den här kontrollen för|Kontrollera listan över tillgängliga miljöer i administrationscentret för Business Central.|
|Det gick inte att upprätta en anslutning till webbservern|Rensa cacheminnet och läs in sidan igen.|

## Status för tjänstens hälsotillstånd

Rapporterar hälsostatus för Business Central genom att söka efter deklarerade avbrott.

|Problem|Vad du kan göra|
|-------|-------------|
|Ingen autentiserad användare kan utföra den här kontrollen för|Se kontrollen **användarverifiering**.|
|Business Central är tillfälligt otillgänglig. Försök igen senare.|Försök igen senare.|

## Se även

[Resurser för hjälp och support](product-help-and-support.md)  
[Översikt över uppgifter för inställning av Business Central](setup.md)  
[Vanliga frågor om att använda Business Central](across-faq.yml)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Administrationscenter för Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
