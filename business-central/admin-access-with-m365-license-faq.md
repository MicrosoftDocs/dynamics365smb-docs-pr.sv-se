---
title: Vanliga frågor rom åtkomst med Microsoft 365-licenser
description: Få svar på vanliga frågor om åtkomst till Business Central med Microsoft 365 licenser.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 11/22/2022
ms.custom: bap-template
---
# Vanliga frågor rom åtkomst med Microsoft 365-licenser

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Användare kan komma åt Business Central -data i Microsoft Teams med deras Microsoft 365 licens. I denna artikel besvaras vanliga frågor från administratörer, konsulter och andra. Utvecklare bör läsa vanliga frågor och svar om utvecklare. Gå till vanliga frågor och svar Business Central med Microsoft Teams, gå till [vanliga frågor och svar om Teams](teams-faq.md).

## [Behörigheter](#tab/permissions) 

### Kan jag konfigurera olika startbehörigheter för olika användargrupper proaktivt?

Inte just nu. Med Business Central kan du bara konfigurera en gruppbehörigheter som tilldelas alla Microsoft 365 användare när de loggar in på Business Central för första gången.

### Kan jag konfigurera behörigheter, profiler och inställningar för enskilda användare i proaktivt innan de loggar in?

Ja. Du kan åstadkomma detta genom säkerhetsgrupper. Genom att använda en säkerhetsgrupp i en miljö definierar du den totala uppsättningen användare som har åtkomst till den miljön. Den här säkerhets gruppen kan omfatta användare med Business Central-licens och användare med Microsoft 365-licens. När du sedan uppdaterar användare från Microsoft 365 i **användare** listan kommer Microsoft 365 användarposter skapas. Du kan sedan tilldela användargrupper, behörigheter, profiler och andra inställningar innan de loggat in.

### Kan jag när en användare har loggat in ändra de objekt som de har tillgång till?

Ja. När en användare har loggat in för första gången och användarposten har etablerats, hanterar administratörer dessa användare på samma sätt som andra Business Central-användare. De kan till exempel lägga till eller ta bort behörigheter för olika objekt. Om du ändrar behörighetsgrupperna som tilldelats Microsoft 365 licensen på sidan licens konfiguration kommer ändringen endast att påverka nästa användare som loggar in för första gången.

### Hur förhindrar jag åtkomst till känsliga tabeller?

Business Central erbjuder en kraftfull och flexibel behörighetsmodell där administratörer kan definiera behörighetsuppsättningar som ger åtkomst till specifika objekt, affärsprocesser eller hela roller. Om du vill förhindra åtkomst till känsliga tabeller kan du skapa anpassade behörighetsgrupper som utesluter behörighet för känsliga objekt. Mer information om exkluderingsbehörigheter finns i [Skapa en behörighetsuppsättning](ui-define-granular-permissions.md).  

### I stället för att anpassa licenskonfigurationen kan jag anpassa en användargrupp?

Ja. Att lägga till behörighetsgrupper till Microsoft Teams Interna användares användargrupp i Business Central har samma nettoeffekt som att lägga till behörighetsuppsättningar till Microsoft 365-licensen så länge som Microsoft 365-licensen fortsätter mappa till denna användargrupp. Den här metoden har extra fördelen att behörighetsgrupper alltid synkroniseras med gruppmedlemmar när du ändrar användargruppen.

### När en Business Central användare delar en post i Teams, tilldelar de nya behörigheter?

Nr. Den här åtgärden är inte samma sak som att dela en länk till ett SharePoint-dokument där personen som delar dokumentet kan välja att ge andra behörighet åt andra. I Business Central kan endast administratörer konfigurera och tilldela behörigheter. När dokumentet jämförs med att dela SharePoint-dokument är det detsamma som att välja alternativet "dela till personer med befintlig åtkomst".

### Stöder den här funktionen säkerhet på radnivå.

Ja. Även om en person som har åtkomst till en post i Teams med tillhörande Microsoft 365-licens kan ha rätt behörigheter för tabell-och sid objekt, kommer behörighet på radnivå att tillämpas om den har implementerats för tabellen.  

### Om jag konfigurerar behörigheter som innehåller skrivbehörighet kan användare skriva in Teams?

Om du konfigurerar Business Central för att tilldela en behörighetsgrupp som innehåller behörigheterna infoga, ändra eller ta bort till ett eller flera objekt, kan användare med den behörighets gruppen fortfarande inte skriva i Teams när de bara har en Microsoft 365-licens. Business Central-tjänsten använder skrivskyddad åtkomst oavsett vilken behörighet som du tilldelar Infoga, ändra och ta bort.  

Även om Business Central har denna skyddsnivå rekommenderar vi ändå att du undviker behörighetsgrupper med skrivbehörighet. Om du gör detta kan du förhindra att problemen blir mer underordnade när användare byter roll eller skaffar nya licenser.  

## [Inställning och konfiguration](#tab/setup)

### Varför är inställningen för att aktivera åtkomst inte tillgängligt för min miljö?

Det går bara att aktivera åtkomst med Microsoft 365 licenser för Business Central-miljöer i plattform version 21.1 eller senare. När miljön uppgraderas till denna minimala version blir inställningen automatiskt tillgänglig. Om du vill kontrollera versionen av din miljö går du till miljö informationssidan för företags nätverket i Business Central administrationscenter. Du kan till exempel logga in på miljön och gå till **Hjälp och support** från menyn **Hjälp**.

### Kan jag komma åt Business Central lokalt med Microsoft 365-licenser?

Nej det stöds inte. Business Central visar ett felmeddelande när användare försöker komma åt Business Central lokala poster i Teams.

### Vad är medarbetarprofilen?

Profil **Medarbetare** visas i listan **Profiler (roller)** infördes med uppdatering 21.1. Det är den standardprofil som tilldelas till användare som har åtkomst till Business Central med deras Microsoft 365-licens. Den här profilen är avsedd för personer i en organisation som inte har en specifik roll i Business Central och som bara behöver visa data som delats med dem.

### Vad är användargruppen Teams-användare?

Gruppen **Microsoft Teams Intern använder** visas på sidan **Användargrupp** introducerades med uppdatering 21.1. Denna grupp är standardanvändargruppen som tilldelas till användare som har åtkomst till Business Central med deras Microsoft 365-licens. Användargruppens avsedda för personer inom samma organisation där Business Central är värd som samarbetar i Microsoft Teams.  

### Visas användare som bara har en Microsoft 365-licens i listan användare i Business Central?

Ja. Om du använder säkerhets grupper i miljöer visas dessa användare i listan användare när du har använt åtgärden Microsoft 365 uppdatera användare från listan **användare** . Om du inte tillämpar säkerhets grupper visas användarposterna i listan användare efter första gången de ansluter till en Business Central-post.

### Fungerar den här funktionen för inbäddning av ISV-lösningar?

Ja. Användare med endast en Microsoft 365-licens kan också komma åt poster i miljöer som körs i domänen *. bc.dynamics.com.

## [Licenser](#tab/license)

### Kan en kund använda den här funktionen om de inte har Business Central?

Åtkomst till Business Central med en Microsoft 365-licens är avsedd för organisationer som redan prenumererar på Business Central och använder en eller flera Business Central-miljöer med licensierade företagsanvändare. Den innehåller inga nya funktioner eller rättigheter att använda till Microsoft 365 kunder som inte har en Business Central-plan.

### Hur kan det här hjälpavsnittet hantera abonnemangs kostnader i min organisation?

För att maximera produktiviteten och effektivisera sina åtgärder köper SMB ofta Dynamics 365 Business Central tillsammans med Microsoft 365. I så fall får de flesta användare en Microsoft 365-licens, men endast vissa roller eller personer får en Business Central-licens. Business Central ger licensieringsmöjligheter så att kunder endast betalar för det som de behöver:

- Användare som vill ha fullständig åtkomst till Business Central tilldelas normalt en Business Central Essentials- eller Business Central Premium-licens. 
- Användare som kräver begränsad skriv åtkomst tilldelas vanligtvis en Business Central-licens för teammedlemmar.
- Alla andra anställda i organisationen som bara behöver läsa affärsdata som delas med dem ibland kan göra det om de har en Microsoft 365-licens. De behöver inte tilldelas en licens för en teammedlem. Andra licensalternativ är tillgängliga. Om du vill ha mer information kan du hämta och läsa [Dynamics 365 licensguiden](https://go.microsoft.com/fwlink/?LinkId=866544).

### Är denna 100 % utan kostnad?
 
Nr. Åtkomst till Business Central-data i Microsoft Teams kräver att varje användare har antingen en Business Central-licens eller Microsoft 365-licens från listan med planer som stöds.

### Fungerar det med Microsoft 365 testversioner och utvärderingsversion av Business Central?

Ja. Om en användare tilldelas en Microsoft 365-licens från en testversion av en plan som stöds, kan de också komma åt Business Central-poster i Teams. Det är då möjligt för kunder att prova Microsofts produktivitets- och affärsprogram som arbetar tillsammans och gör det möjligt för partner säljare och konsulter att på ett enkelt sätt visa denna funktion. Partner kan till exempel tillhandahålla sina egna Azure AD klientorganisationer från [https://aka.ms/CDX](https://aka.ms/CDX) som innehåller Microsoft 365 testversioner och utvärderingsversion av Business Central.

### Listan över licenser i Business Central visar en Microsoft 365-licens. Vad är detta?

På sidan **Licenskonfiguration** i Business Central visar de olika typerna av licenser som kan ge åtkomst till Business Central-tjänsten. I version 21 lade Microsoft till Microsoft 365 i den här listan som ett nytt sätt att komma åt Business Central. Listan över licenser innebär inte att organisationen har köpt prenumerationer på någon av dessa licenser eller att organisationen har aktiverat åtkomst genom dessa licenser.

### Behöver jag skaffa en ny licenstyp Microsoft 365 för att funktionen ska fungera?  

Microsoft har inte skapat några nya licenser eller planer för att sätta på den här funktionen. Denna funktion är helt beroende av befintliga Microsoft 365 planer och licenser. Om du redan prenumererar på en av de scheman som stöds Microsoft 365 har du redan denna nya användningsrättighet. Om du inte prenumererar på Microsoft 365 idag kan du registrera dig för Microsoft 365 Business Premium eller liknande planer här. 

### Hur tar jag reda på vilka användare som bara har en Microsoft 365-licens?

Det finns flera sätt. I Microsoft 365 administrationscenter, gå till listan **aktiva användare** och se kolumnen **licenser**. I Business Central, gå till listan **Användare** välj någon av användarna och visa Faktabox **Licenser**.  

### Hur filtrerar jag listan Användare i Business Central för att se användare som bara har en Microsoft 365-licens?

Det går inte att använda en filter- eller listvy för att utföra den här aktiviteten. Du kan emellertid välja en användare i listan och visa faktaboxen för licenser som bara ska inkluderas Microsoft 365 om användaren endast har en Microsoft 365-licens.

### Vad om användare som har både en Microsoft 365-licens och en Business Central-licens?

När flera licenser tilldelas till en användare ger den högre licens användningsrättigheterna över mindre licensanvändningsrättigheter vid åtkomst till Business Central. I det här fallet ger Business Central-licensen användaren rätt till fler användarrättigheter. Det innebär att användare kan läsa och skriva Business Central-poster i Teams och tillgång till Business Central webbklienten i webbläsaren, på samma sätt som alla andra företag som innehar Business Central-licens. Om specifika behörighetsuppsättningar har konfigurerats för Microsoft 365 licensen får användaren de konfigurerade behörighetsuppsättningarna kombinerade med behörighetsuppsättningarna från Business Central-licensen eller som redan har tilldelats användaren.

### Är licensieringen relaterad till Business Central teammedlemslicensen?

Det finns ingen relation mellan de olika licenserna för Business Central teammedlemlicenser och åtkomst till Business Central Microsoft Teams med Microsoft 365 licenser. Även om Microsoft Teams den tillhörande dokumentationen avser personer i ett *teammedlemmar* är det en kollektiv term för en grupp Microsoft Teams användare. Det refererar inte till Business Central-licenser.

### Tvingar Business Central alla begränsningar?

Ja, alla plattformsbegränsningar och minimi krav, inklusive licenskrav, tillämpas av Business Central-plattformen. Med hjälp av detta rikt linjer kan användare felsöka sina inställningar och förhindra missbruk. Om till exempel en användare som bara har en Microsoft 365 licens försöker få åtkomst till Business Central webbklienten i webbläsaren, kommer åtkomst att nekas och ett guide felmeddelande kommer att visas. 

## [Förbrukning](#tab/usage)
 
### Kan jag komma åt poster för Teams för iOS och Teams för Android? 

Det går för närvarande inte att komma åt Business Central data på Teams mobil med hjälp av en Microsoft 365-licens. Microsoft arbetar snart med att aktivera den här funktionen. 

### Hur ändrar användarna sina personliga inställningar i mina inställningar? 

När en användare har åtkomst till Business Central för första gången med bara deras Microsoft 365 licens, anges automatiskt användarinställningar som språk, tidszon och nationella inställningar baserat på deras inställningar för operativ system eller webbläsare. Administratörer kan ändra dessa inställningar från Business Central för varje användare. 

### Vad bestämmer valet av språk när du loggar in för första gången? 

Språket som du upplever Business Central med ställs in baserat på olika faktorer, inklusive Teams-klienten genom vilken du fick tillgång till Business Central första gången. För team skriv bord, Teams för iOS och Teams för Android används operativsystemets språk. Webbläsarspråk tillämpas på webbgrupper. I alla fall beaktas inte Teams språket. 

### Varför kan jag inte aktivera vissa av de färgade länkarna i flikar och kort information?

Länkar på Business Central-sidor visas ofta som fetstilta hyperlänkar som kan aktive ras på andra ställen eller med andra åtgärder. På en teknisk nivå är dessa länkar vanligen implementerade som fält värden utan titel som utlöser viss kod och där valet av format ofta visar tillståndet. När användarna ansluter till Business Central sidor med sina Microsoft 365 licenser formateras länkarna som om de är åtgärdsbara. Men de kan inte aktiveras eftersom den här licensen inte erbjuder användnings rättigheter för att köra åtgärder.  

### Varför kan jag inte aktivera åtgärder för sidaviseringar?

Sammanhangsbaserade meddelanden som visas på sidor åtföljs ofta av länkar som går att vidta. När användare ansluter till Business Central sidor med tillhörande Microsoft 365-licens, visas dessa länkar, men de kan inte aktiveras eftersom licensen inte erbjuder användningsrättigheter för att köra åtgärder. På en teknisk nivå är dessa länkar implementerade som åtgärder.

### Kan Microsoft 365-användare ta bort flikar?

Ja. Vem som helst i chatten eller kanalen kan ta bort flikar som har skapats av andra. När du tar bort en flik tas eller påverkar inte data i Business Central, men fliken tas bort för alla användare i chatten eller kanalen.

### Om det inte går att filtrera visas fortfarande en filtrerad lista som har skapats av andra?

Användare som använder Business Central med sin Microsoft 365-licens har inte behörighet att filtrera med hjälp av filter rutan eller att använda listvyer. Om en annan användare har skapat en flik som innehåller en filtrerad listsida Microsoft 365 visas även de filter som används på fliken.

---

## Se även

[Översikt över Business Central-åtkomst med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Ställ in åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  