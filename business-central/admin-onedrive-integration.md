---
title: Hantera OneDrive-integrering med Business Central
description: Lär dig mer om vad du kan göra för att hantera en integration mellan Business Central och OneDrive för företag.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 06/13/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="managing-onedrive-integration-with-business-central"></a>Hantera OneDrive-integrering med Business Central

Den här artikeln innehåller en översikt över vad en administratör kan göra som administratör för att styra OneDrive för företag-integrationen med [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] online-kunder kan dra nytta av automatisk integration, utan ytterligare inställningar som krävs för att använda funktionerna för att öppna och dela i OneDrive. Med guiden för assisterad konfiguration **OneDrive-konfiguration** kan du ge användare åtkomst till ännu fler OneDrive-funktioner, som att öppna Excel-filer i OneDrive&mdash;eller till och med stänga av alla funktioner.  

## <a name="configure-onedrive-for-integration-with-business-central"></a>Konfigurera OneDrive för integrering med Business Central

I det här avsnittet beskrivs krav som måste uppfyllas i OneDrive för företag för att konfigurera integrationen med Business Central och den uppgift som du kan utföra för att hantera integrationen.

### <a name="minimum-requirements"></a>Minsta krav

* Varje användare måste ha en licens för [!INCLUDE[prod_short](includes/prod_short.md)] och OneDrive  som en del av en Microsoft 365-plan.
* OneDrive måste ställas in för varje användare.

### <a name="managing-privacy"></a>Hantera sekretess

> [!IMPORTANT]
> Om du har valt att distribuera Business Central och OneDrive till olika länder eller regioner kan det hända att de filer som skapas av Business Central och placeras i OneDrive kan korsa datahemvistgränser. Se till att bekräfta organisationens principer och myndighetsefterföljandekrav för datahemvist innan du aktiverar anslutningen till OneDrive.

Administratörer och slutanvändare styr innehållet som lagras i OneDrive, och dessa data ägs uteslutande av din organisation. Mer information finns i [så här skyddar SharePoint och OneDrive data i molnet](/sharepoint/safeguarding-your-data). Du kan också besöka vår [Sekretesspolicy för Microsoft](https://privacy.microsoft.com/en-us/privacystatement), som förklarar vilka data Microsoft behandlar, hur Microsoft behandlar den och för vilka ändamål.

Genom att aktivera den här tjänstanslutningen godkänner du:

(a) dela data från Dynamics 365 Business Central med tjänstleverantören, som kommer att använda dem enligt dennes villkor och sekretesspolicy, (b) tjänstleverantörens efterlevnadskrav kan skilja sig från Dynamics 365 Business Central och (c) Microsoft kan dela din kontaktinformation med den här tjänstleverantören om det behövs för att leverantören ska kunna driva och felsöka tjänsten.

## <a name="configure-business-central"></a>Konfigurera Business Central

Med Business Central online konfigureras kopplingen mellan Business Central och OneDrive automatiskt, och OneDrive-funktionerna är tillgängliga för användarna som standard. Om du vill stänga av vissa eller samtliga av funktionerna kan du använda guiden för assisterad konfiguration **OneDrive-konfiguration** i Business Central-klienten.

Att konfigurera Business Central lokalt är annorlunda eftersom anslutningen mellan Business Central och OneDrive inte har konfigurerats åt dig. Du måste du göra manuellt. Mer information finns i [Konfigurera OneDrive-integration med Business Central lokalt](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a>Om flera miljöer

OneDrive-integrationen konfigureras per miljö, vilket innebär att dina inställningar gäller för alla företag i den miljön. Om organisationen har mer än en miljö måste du konfigurera OneDrive-integrationen för varje.

### <a name="prerequisites"></a>Förutsättningar

- Indirekt, ändra och ta bort (imd) behörighet i tabellen **Dokumentservicescenario** som minimum

### <a name="configure-onedrive-using-onedrive-setup"></a>Konfigurera OneDrive med OneDrive-konfiguration

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger **OneDrive-konfiguration** och välj sedan relaterad länk. 
2. Första gången du kör assisterad konfiguration kan du se **Din integritet**. Läs informationen på sidan och om du godkänner villkoren väljer du **Godkänn** för att fortsätta.
3. På sidan **Konfigurera OneDrive filhantering** har du följande alternativ att välja bland:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Välj **Nästa**>**Klart**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a>Växla till ny OneDrive-integration efter uppgradering

Den assisterade konfigurationen **OneDrive-konfiguration** introducerades i utgivningscykel 2 år 2022, version 21.0. Tidigare använde OneDrive-integrationen **SharePoint-anslutningskonfigurationen**, som är inaktuell och kommer att tas bort i utgivningscykel 2 år 2023, version 23.0. När du har uppgraderat till version 21 fungerar OneDrive fortfarande som tidigare. Men vi rekommenderar att du växlar till den nya OneDrive-integrationen. Om du gör detta byte nu blir det enklare när **SharePoint-anslutningskonfigurationen** tas bort. Dessutom kan du använda guiden för assisterad konfiguration **OneDrive-konfiguration** för att hantera de OneDrive-funktioner som är tillgängliga för användarna. Den assisterade konfigurationen **OneDrive-konfiguration** gör övergången från den äldre SharePoint-konfigurationen enkel och smidig.

Du byter genom att helt enkelt öppna och köra den assisterade konfigurationen **OneDrive-konfiguration** direkt eller genom att öppna sidan **SharePoint-anslutningskonfiguration** och välja **Gå till ny OneDrive-konfiguration** i meddelandet längst upp på sidan. Följ konfigurationsguiden på det sätt som beskrivs i föregående avsnitt.

## <a name="restoring-onedrive-and-"></a>Återställa OneDrive och [!INCLUDE[prod_short](includes/prod_short.md)]

Som en del av en katastrofåterställning kan administratörer behöva återställa en [!INCLUDE[prod_short](includes/prod_short.md)] online-miljö till en säkerhetskopia från en tidpunkt som redan har passerat och synkronisera OneDrive-lagringen till samma tidpunkt. OneDrive tillhandahåller olika återställningsverktyg, t.ex. att återställa en användares OneDrive till en tidigare tidpunkt, återställa en tidigare version av en enskild fil eller återställa borttagna filer. Mer information finns i följande artiklar:

* För [!INCLUDE[prod_short](includes/prod_short.md)], se [återställa en miljö i administrationscentret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* För OneDrive, se [återställa dina OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="governance"></a>Styrelse

Administrationscentret för SharePoint ger omfattande kontroll över principer som styr användningen av OneDrive organisationen. Globala administratörer eller användare med rollen SharePoint administratör kan konfigurera principer som avgör vem som har åtkomst till OneDrive, varifrån data finns, livscykeln för innehåll och mycket mer. Följande länkar ger information om ofta använda funktioner och inställningar som kan förbättra integrationen med [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Hantera delningsinställningar](/sharepoint/turn-external-sharing-on-or-off)
* [Använda informationshinder med SharePoint](/sharepoint/information-barriers)
* [Lär dig mer om att förhindra dataförlust](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Ange standard lagringsutrymme för OneDrive användare](/onedrive/set-default-storage-space)
* [Lägga till och ta bort administratörer för en användaresOneDrive](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Inaktivera OneDrive skapande av vissa användare](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Flera geografiska funktioner i OneDrive och SharePoint online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Vissa funktioner kan vara tillgängliga endast för vissa uppställningar.

## <a name="see-also"></a>Se även

[Business Central och OneDrive för företag-integration](across-onedrive-overview.md)  
[Öppna Business Central-filer i OneDrive](across-share-onedrive.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
