---
title: Komma igång med kopplingen för Shopify
description: Första stegen när du konfigurerar anslutningen mellan Business Central och Shopify
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# Kom igång med Shopify-kopplingen

Anslut din Shopify butik (eller butiker) med [!INCLUDE [prod_short](../includes/prod_short.md)] och maximera företagets produktivitet. Hantera och visa insikter från ditt företag och din Shopify butik som en enhet.

Om du vill använda Shopify med [!INCLUDE [prod_short](../includes/prod_short.md)] är det ett par saker du måste göra först. Den här artikeln används för att integrera Shopify-butiken med [!INCLUDE [prod_short](../includes/prod_short.md)].

## Förutsättningar för Shopify

Du måste ha följande:

- Ett Shopify-konto
- En onlinebutik med Shopify

Mer information om hur du skapar Shopify testversioner och rekommenderade inställningar finns i [ skapa och ställa in Shopify konto](shopify-account.md).

## Förutsättningar för Business Central

- Kontrollera att **[Shopify anslutning](https://go.microsoft.com/fwlink/?linkid=2196238)**-appen för har installerats.

  Appen är förinstallerad för alla nya registreringar och utvärderingsversioner. Läs mer om att installera appar från AppSource på [Installera och avinstallera tillägg](../ui-extensions-install-uninstall.md#install). Följ instruktionerna nedan om du inte har [!INCLUDE[prod_short](../includes/prod_short.md)].

- Kontrollera att användaren har rätt behörighet. Shopify Anslutningen täcks av **Shopify – Admin (SHPFY – ADMIN)** behörighetsuppsättningen. Mer information om [Skapa användare enligt licenser](../ui-how-users-permissions.md) och [Att komponera behörighetsuppsättningar](../ui-define-granular-permissions.md).

## Installera Dynamics 365 Business Central-appen till din Shopify onlinebutik

För befintliga instanser av [!INCLUDE[prod_short](../includes/prod_short.md)] är det här steget valfritt och kan hoppas över.

1. Leta upp [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) appen på [Shopify AppStore](https://apps.shopify.com/)
2. Välj knappen **Lägg till app**. Logga in på ditt Shopify-konto om du uppmanas. Välj onlinebutik om du har fler än en.
3. När du har granskat sekretess och behörighet väljer du knappen **Installera app**.

   Du kan söka efter och öppna den installerade **Dynamics 365 Business Central** appen i avsnittet **Appar** på sidan **Shopify admin**.
4. Välj **Registrera dig nu** om du vill starta [!INCLUDE[prod_short](../includes/prod_short.md)] utvärderingsversion eller **Logga in** om du redan har [!INCLUDE[prod_short](../includes/prod_short.md)]. Du kommer att omdirigeras till sidan [Business Central](https://businesscentral.dynamics.com).
5. Gör nästa steg i [!INCLUDE[prod_short](../includes/prod_short.md)].

## Ansluta Business Central till onlinebutiken på Shopify

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](../media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Shopify-butik** och välj relaterad länk.
2. Välj åtgärden **Ny**.  
3. I fältet **Kod** anger du den kod som gör det lätt att hitta i [!INCLUDE[prod_short](../includes/prod_short.md)]. Ett namn kan t.ex. återspegla det som en fabrik säljer, t.ex. "möbler" eller "kaffe", eller det land eller den region där det används.
4. I fältet **Shopify URL** anger du webbadressen till den onlinebutik som du vill ansluta till. Använd följande format: `https://{shop}.myshopify.com/`.
5. Aktivera reglaget **Aktiverad**, granska och godkänn villkoren.
6. Om du uppmanas att logga in på ditt Shopify-konto. Granska sekretess och behörighet och välj knappen **Installera app**.

Upprepa steg 2–6 för alla onlinebutiker som du vill ansluta.

### Kända problem

- Webbläsaren blockerar popup-fönstret. När du aktiverar **Aktiverad** [!INCLUDE [prod_short](../includes/prod_short.md)] öppnas sidan **Väntar på ett svar. Stäng inte sidan** medan den väntar på åtkomsttoken från Shopify. Om den sidan är stängd eller blockerad kan du inte ansluta till Shopify. Läs mer på [begäran om åtkomsttoken](troubleshoot.md#request-the-access-token)
- Det kan vara en bra idé att ha Shopify-administration öppen i samma webbläsare som [!INCLUDE [prod_short](../includes/prod_short.md)]
- [Fel: Oauth error invalid_request: Det gick inte att hitta Shopify API-programmet med api_key](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Fel: Oauth-fel invalid_request: Ditt konto har inte behörighet att bevilja den begärda åtkomsten för den här appen.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [Det går inte att ansluta från sandbox](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)

## Nästa steg

Nu är din onlinebutik ansluten till [!INCLUDE[prod_short](../includes/prod_short.md)]. I nästa steg ska du definiera vad som ska synkroniseras och hur.

- [Synkronisera artiklar](synchronize-items.md)
- [Synkronisera kunder](synchronize-customers.md)
- [Synkronisera order](synchronize-orders.md)

## Teststrategier

Det finns olika metoder för att testa en integration och varje metod har sina tekniker och nackdelar.

Du kan ansluta [!INCLUDE[prod_short](../includes/prod_short.md)] och Shopify-konton så ofta du vill.  Shopify-anslutningen påverkar endast miljön eller är mer exakt, det företag där den är aktiverad. Du kan ansluta till samma  Shopify  onlinebutik från flera olika miljöer eller företag. Du kan inaktivera anslutningsprogram och aktivera på nytt.

Det är lätt att köra synkroniseringstester igen. Med anslutningsprogram kan du ta bort importerade data, till exempel produkter, kunder och order, och sedan importera dem igen. Bara [Återställ synkronisering](troubleshoot.md#reset-sync).

### Shopify begränsat läge och Business Central begränsat läge

Det är förmodligen det säkraste sättet att testa integrationen. I stället för att använda ett  Shopify  begränsat läge kan du också använda provprenumerationen eller Utvecklingsbutik. I [!INCLUDE[prod_short](../includes/prod_short.md)] kan du också använda ett testföretag i en produktionsmiljö.

Om du vill lära dig mer om [!INCLUDE[prod_short](../includes/prod_short.md)] begränsat läge går du till [Skapa en ny miljö](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### Shopify begränsat läge och Business Central produktion

Det här är *inte* en rekommenderad konfiguration för testning eftersom Shopify anslutningsprogram kan skapa eller ändra artiklar och kunder. Du kan också skapa försäljningsdokument som order och fakturor. Det kan vara svårt att ångra dessa dokument.
 
Om du måste använda den här konfigurationen rekommenderar vi att du granskar och troligen inaktiverar följande inställningar:

* **Skapa automatiskt okända objekt** för att inte skapa objekt
* **Shopify kan uppdatera objekt** så att de inte uppdaterar mappade objekt
* **Skapa okänd kund automatiskt** så att kunder och kontakter inte kan skapas
* **Shopify kan uppdatera kunder** så att de inte uppdaterar befintliga kunder
* **Skapa automatiskt försäljningsorder** för att inte skapa försäljningsorder och försäljningsfakturor

Mer information finns i [Återställa en miljö](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### Shopify produktion och Business Central begränsat läge

Det kan vara en god idé att säkerhetskopiera data. Du kan till exempel exportera dina produkter och kunder. Mer information finns i [Använda CSV-filer för att säkerhetskopiera butiksinformation](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Inaktivera växlingen **Tillåt datasynkronisering till Shopify** så att [!INCLUDE[prod_short](../includes/prod_short.md)] inte skriver till Shopify. I detta fall kan du importera produkter, bilder, kunder och order från Shopify. Du kan dock inte skicka artiklar, priser, lagernivåer, kunder, uppfyllelseinformation till Shopify.

Om du behåller växlingen **Tillåt datasynkronisering till Shopify** aktiverad är ytterligare skyddsåtgärder följande:

*   Välj **utkast** i fältet **status för skapa produkt** för att säkerställa att exporterade produkter inte är tillgängliga för köpare. Du kan kontrollera hur produkten ser ut i onlinebutiken, synkronisera priser, alternativ och lagernivåer. Kontrollera att du använder filtren på sidan **Lägg till objekt till Shopify** för att begränsa antalet exporterade objekt.
* Inaktivera växlingen **Exportera kund till Shopify** så att du inte skickar kunderna till Shopify.

## Se även

[Genomgång: ställa in och använda Shopify anslutningsprogram](walkthrough-setting-up-and-using-shopify.md)  

