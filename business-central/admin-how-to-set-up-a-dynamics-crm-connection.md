---
title: Anslut till Microsoft Dataverse (innehåller video)
description: Skapa en anslutning mellan Business Central och Dataverse. Företag skapar vanligtvis anslutningen för att integrera data med en annan Dynamics 365-affärsapp.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '7200, 7201'
ms.date: 02/28/2024
ms.service: dynamics-365-business-central
---
# Anslut till Microsoft Dataverse

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

I den här artikeln beskrivs hur du upprättar en anslutning mellan [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Vanligtvis skapar företag anslutningen för att integrera och synkronisera data med en annan Dynamics 365-affärsapp, till exempel [!INCLUDE[crm_md](includes/crm_md.md)].  

## Innan du börjar

Det finns lite information du bör ha tillhanda innan du skapar anslutningen:  

* Webbadressen (URL) till den [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljö du vill ansluta till. Om du använder den assisterade konfigurationen för **Installation av Dataverse-anslutning** för att skapa anslutningen hittar vi dina miljöer. Du kan också ange URL:en till en annan miljö i klientorganisationen.  
* Användarnamn och lösenord för ett konto som har administratörsbehörigheter i [!INCLUDE[prod_short](includes/prod_short.md)] och [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Om du har en lokal [!INCLUDE[prod_short](includes/prod_short.md)], 2020 års utgivningscykel 1, version 16.5, läs då artikeln [Vissa kända problem](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Du måste slutföra den beskrivna lösningen innan du kan skapa anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* De lokala valutor som respektive företag använder. [!INCLUDE [prod_short](includes/prod_short.md)]-företag kan ansluta till en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljö som har en basvaluta som är en annan än dess lokala valuta. Mer information om hur du hanterar inställningar med flera valutor finns i [Tillåt för olika valutor](#allow-for-different-currencies).

> [!IMPORTANT]
> Din [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljö får inte vara i administrationsläge. Administrationsläget gör att anslutningen misslyckas eftersom integreringsanvändarkontot för anslutningen inte har administratörsbehörighet. Mer information finns i [Administrationsläge](/power-platform/admin/admin-mode).

> [!Note]
> Här beskrivs proceduren för onlineversionen av [!INCLUDE[prod_short](includes/prod_short.md)].
> Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt och inte använder ett Microsoft Entra-konto för att ansluta till [!INCLUDE [cds_long_md](includes/cds_long_md.md)] måste du också ange användarnamn och lösenord för ett användarkonto för integreringen. Detta kontot kallas "integreringsanvändar"-kontot. Om du använder ett Microsoft Entra-konto krävs eller visas inte integrationens användarkonto. Integrationsanvändaren ställs in automatiskt och kräver ingen licens.

## Länka din Business Central och dina Dataverse-miljöer

Företag vill hålla sin data säker och säker inom sin integritetsgräns och särskilt när deras affärshanteringsprogram integreras med andra appar. Genom att länka [!INCLUDE [prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)] miljöer uppnår du inte bara dessa överväganden, utan ger också dina administratörer ett enklare sätt att skapa och underhålla dina integreringar med andra Dynamics 365-appar.

I [!INCLUDE [prod_short](includes/prod_short.md)] administrationscentret kan du länka din [!INCLUDE [prod_short](includes/prod_short.md)]-miljö till din [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljö. [!INCLUDE [prod_short](includes/prod_short.md)] kan använda informationen från länken för att göra det enklare och säkrare att integrera med andra Dynamics 365-appar, till exempel Sales och Field Service. Den länkade [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljöns URL är till exempel tillgänglig som standard på sidan **Dataverse anslutningsinställningar** och när du kör den assisterade konfigurationsguiden för **Dataverse-anslutningsinställningar**.

## Tillåt olika valutor

[!INCLUDE [prod_short](includes/prod_short.md)]-företag kan ansluta till en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljö som har en basvaluta som är en annan än dess lokala valuta.

> [!NOTE]
> Om du vill synkronisera flera valutor måste du använda en enkelriktad synkronisering, från [!INCLUDE [prod_short](includes/prod_short.md)] till [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

Mer information om basvalutan i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] finns i entiteten [Transaktionsvaluta (valuta)](/powerapps/developer/data-platform/transaction-currency-currency-entity). 

Om du vill veta mer om valutor i [!INCLUDE [prod_short](includes/prod_short.md)] går du till [Valutor i Business Central](finance-currencies.md).

För att möjliggöra olika valutor måste du kontrollera att du har angett följande inställningar innan du ansluter:

* Basinställningen för transaktionsvaluta i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] har den valutakod som anges på sidan **Valutor** i [!INCLUDE [prod_short](includes/prod_short.md)].
* Det finns minst en valutakurs angiven för valutan i [!INCLUDE [prod_short](includes/prod_short.md)] på sidan **Valutakurser**.

När du aktiverar anslutningen till [!INCLUDE [cds_long_md](includes/cds_long_md.md)] lägger [!INCLUDE [prod_short](includes/prod_short.md)] till sin lokala valuta i entiteten **Valuta** i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Den lokala valutan använder växelkursen från fältet **Valutafaktor** på sidan **Valutakurser**.

Eftersom valutasynkronisering är enkelriktad, från [!INCLUDE [prod_short](includes/prod_short.md)] till [!INCLUDE [cds_long_md](includes/cds_long_md.md)], konverteras och synkroniseras monetära belopp på följande sätt:

* Om i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-basvalutan konverteras belopp till den lokala [!INCLUDE [prod_short](includes/prod_short.md)]-valutan baserat på den senaste valutakursen som synkroniseras från [!INCLUDE [prod_short](includes/prod_short.md)].
* Om i lokal [!INCLUDE [prod_short](includes/prod_short.md)]-valuta synkroniseras belopp med lokal [!INCLUDE [prod_short](includes/prod_short.md)]-valuta i någon av övriga icke-basvalutor i [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

## Konfigurera en anslutning till [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

För alla autentiseringstyper förutom Microsoft 365-autentisering kan du ställa in anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på sidan **Dataverse-anslutningsinställningar**. För Microsoft 365-autentisering rekommenderar vi att du använder guiden för assisterad konfiguration **Dataverse-anslutningsinställningar**. Guiden gör det enklare att konfigurera anslutningen och specificera avancerade funktioner, till exempel ägarskapsmodell och initial synkronisering.  

> [!IMPORTANT]
> Under installationen av anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ombeds administratören att ge följande behörigheter till en registrerad Azure-tillämpning kallad [!INCLUDE[prod_short](includes/prod_short.md)]-integration för [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * Behörigheten **Öppna [!INCLUDE[cds_long_md](includes/cds_long_md.md)] som dig själv** krävs, varför [!INCLUDE[prod_short](includes/prod_short.md)] för administratörens räkning automatiskt kan skapa icke-interaktiva, icke-licensierade [!INCLUDE[prod_short](includes/prod_short.md)]-integrationsprogramanvändare, tilldela användaren säkerhetsroller samt distribuera [!INCLUDE[prod_short](includes/prod_short.md)]-integreringslösningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Den här behörigheten används endast en gång vid upprättandet av anslutning till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * **Ha fullständig åtkomst till Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** behörighet krävs så att automatiskt skapade [!INCLUDE[prod_short](includes/prod_short.md)] integrationsprogramanvändare kan komma åt [!INCLUDE[prod_short](includes/prod_short.md)] data som ska synkroniseras.  
> * **Logga in och läsa din profil** behörighet krävs för att verifiera användarloggning i själva verket har säkerhetsrollen systemadministratör tilldelad i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Genom att ge tillstånd till organisationen, är det administratören som omnämns det registrerade Azure-programmet som kallas [!INCLUDE[prod_short](includes/prod_short.md)] integration för [!INCLUDE[cds_long_md](includes/cds_long_md.md)] att synkronisera data med hjälp av automatiskt skapade [!INCLUDE[prod_short](includes/prod_short.md)] användarensreferenser för integrationsprogram.

### Så här använder du den assisterade guiden Konfiguration av anslutning till Dataverse

Guiden Konfiguration av anslutning till Dataverse kan göra det enklare att ansluta programmen, och kan till och med hjälpa dig att köra en första synkronisering. Om du väljer att köra inledande synkronisering kommer [!INCLUDE[prod_short](includes/prod_short.md)] att granska data i båda program rekommendationer för hur man tar sig an en inledande synkronisering. Rekommendationerna beskrivs i tabellen nedan.

|Rekommendation  |Beskrivning  |
|---------|---------|
|**Fullständig synkronisering**|Data finns bara i [!INCLUDE[prod_short](includes/prod_short.md)], eller bara i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Rekommendationen är att synkronisera alla data från tjänsten som har den till den andra tjänsten.|
|**Ingen synkronisering**|Data finns i båda programmen, och att köra en fullständig synkronisering skulle duplicera datan. Rekommendationen är att koppla poster.|
|**Beroendet inte uppfyllt**|Data finns i båda programmen, men det går inte att synkronisera raden eller tabellen eftersom dessa är beroende av en rad eller en tabell som har rekommendationen Ingen synkronisering. Om kunder exempelvis inte kan synkroniseras kan data för kontakter som är beroende av kunddatan heller inte synkroniseras.|

> [!IMPORTANT]
> Vanligtvis använder du bara fullständig synkronisering när du integrerar programmen för första gången, och endast ett program innehåller data. Fullständig synkronisering kan vara användbar i en demonstrationsmiljö eftersom den automatiskt skapar och kopplar poster i respektive program, vilket gör det möjligt att snabbare börja arbeta med synkroniserade data. Du bör dock bara köra fullständig synkronisering om du vill ha en rad i [!INCLUDE[prod_short](includes/prod_short.md)] för respektive rad i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] för registermappningarna. Annars kan resultatet bli dubblettposter.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Assisterad konfiguration** och väljer sedan relaterad länk.
2. Välj **Skapa en anslutning till Microsoft Dataverse** för att starta den assisterade konfigurationsguiden.
3. Fyll i fälten om det behövs.

> [!NOTE]
> Om du inte uppmanas att logga in med ditt administratörskonto beror detta förmodligen på att popup-fönster blockeras. Du kan logga in med popup-fönster från `https://login.microsoftonline.com`.

### Om du vill skapa eller hantera anslutningen manuellt

I följande procedur beskrivs hur du konfigurerar anslutningen manuellt på sidan **Konfiguration av anslutning till Dataverse**. Sidan **Konfiguration för Dataverse-anslutning** är platsen där du hanterar integreringsinställningar.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfiguration av inställningen av Dataverse** och väljer sedan relaterad länk.
2. Ange följande information om anslutningen från [!INCLUDE[prod_short](includes/prod_short.md)] till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Fält|Beskrivning|
    |-----|-----|
    |**Miljö-URL**|Om du äger miljöerna i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] kommer vi att hitta dem åt dig när du kör installationsguiden. Om du vill ansluta till en annan miljö i en annan klientorganisation kan du ange administratörsbehörighet för miljön, så hittar vi den. |
    |**Aktiv**|Starta använda integreringen Om du inte aktiverar anslutningen nu sparas anslutningsinställningarna, men användarna kan inte få åtkomst till data i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] från [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan gå tillbaka till sidan och aktivera anslutningen senare.  |

3. I fältet **Ägarskapsmodlel** väljer du om du vill att en grupptabell i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] ska äga nya transaktioner, eller om en eller flera specifika användare ska göra det. Om du väljer **Person** måste du ange varje enskild användare. Om du väljer **Team** visas den förvalda affärsenheten i fältet **Kopplad affärsenhet**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you're using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who don't have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account won't have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Kontrollera anslutningsinställningarna genom att välja **Anslutning** och sedan **Testa anslutning**.  

    > [!NOTE]  
    > Om datakrypteringen inte har aktiverats i [!INCLUDE[prod_short](includes/prod_short.md)] kommer du att tillfrågas om du vill aktivera den. Välj **Ja** och ange den obligatoriska informationen om du vill aktivera datakryptering. Annars väljer du **Nej**. Du kan aktivera datakryptering senare. Mer information finns i [kryptering av data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i Hjälp för utvecklare och administration.  
5. Om [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkroniseringen inte redan har ställts in får en fråga om du vill använda standardsynkroniseringskonfigurationen. Beroende på om du vill bokföra poster justerade i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och [!INCLUDE[prod_short](includes/prod_short.md)], välj **Ja** eller **Nej**.

<!--
## Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## Anpassa matchningsbaserad koppling

Från och med 2021 års utgivningscykel 2 kan en administratör ange kriterier i syfte att koppla poster baserade på matchningar. Du kan köra algoritmen för matchande poster från följande platser i [!INCLUDE [prod_short](includes/prod_short.md)]:

* Lista sidor som visar poster som är synkroniserade med [!INCLUDE [cds_long_md](includes/cds_long_md.md)], till exempel sidorna kunder och artiklar.  

    Markera flera poster och välj sedan åtgärden **relaterad**, välj **Dataverse**, välj **koppling** och sedan **Matchbaserad koppling**.

    När du inleder den matchande kopplingsmetoden från en huvuddatalista schemaläggs ett kopplingsprojekt direkt efter att du har anget kopplingskriteriet.  
* Sidan **Dataverse Fullständig synk.granskning**.  

    När hela synkroniseringsprocessen upptäcker att du har frikopplade poster i [!INCLUDE [prod_short](includes/prod_short.md)] och i [!INCLUDE [cds_long_md](includes/cds_long_md.md)], visas en **Välj kopplingskriterier**-länk för integrationstabellen.  

    Du kan starta processen **Kör fullständig synkronisering** från sidorna **Konfiguration av Dataverse-anslutning** och **Anslutningsinställningar för Dynamics 365**. Du kan också starta processen i den assisterade konfigurationen **Konfigurera en anslutning till Dataverse** när du är klar med inställningarna.  

    När du startar den matchningsbaserade kopplingsprocessen från sidan **Full Dataverse-sykronisering** schemaläggs ett kopplingsprojekt efter att du har slutfört konfigurationen.  
* Listan **integreringstabellens mappningslista** list.  

    Välj en mappning, välj åtgärden **koppling** och välj sedan **Matchningsbaserad koppling**.

    När du startar den matcningsbaserade kopplingsprocessen från en mappning för integrationstabellen kommer ett kopplingsprojekt att köras för alla icke-kopplade poster i mappningen. Du kan också välja att icke-kopplade poster i listan så att projektet bara körs för de posterna.

I alla tre fallen öppnas sidan **Välj kopplingsvillkor** så att du kan definiera relevanta kopplingskriterier. Anpassa kopplingarna med följande uppgifter på den här sidan:

* Välj de fält som ska användas för att matcha [!INCLUDE [prod_short](includes/prod_short.md)]-poster med [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-entiteter. Du kan ange huruvida matchningen är skiftlägeskänslig.  

* Ange om du vill synkronisera efter att du kopplat poster. Om posterna använder dubbelriktad mappning kan du också ange vad som ska hända om konflikter visas på sidan **Lös uppdateringskonflikter**.  

* Prioritera ordningen som posterna genomsöks i genom att ange en *matchningsprioritet* för relevanta mappningsfält. [!INCLUDE [prod_short](includes/prod_short.md)] söker efter en matchning i stigande ordning baserat på värdet i fältet **Matcha prioritet**. Ett tomt värde i fältet **Matchningsprioritet** är lika med prioritet 0, som är högsta prioritet. Fält med prioritet 0 beaktas först.  

* Ange om du vill skapa en ny entitetsinstansen i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] om det inte går att hitta någon icke unik ej kopplad matchning med hjälp av matchningsvillkoret. Om du vill aktivera funktionen väljer du åtgärden **Skapa ny om det inte går att hitta någon matchning**.  

### Visa resultatet av kopplingsprojektet

Om du vill visa resultatet av kopplings projektet öppnar du sidan **Registermappningar för integrering**, väljer lämplig mappning, väljer **kopplingsåtgärd** och väljer sedan åtgärden **Logg över integrationskopplingsprojekt**.  

Om det inte går att koppla poster kan du välja värdet i kolumnen **Misslyckade** om du vill öppna en lista över fel som beskriver orsaken.  

Kopplingen misslyckas vanligen av följande orsaker:

* Inga matchningsvillkor har definierats

    Kör den matchningsbaserade kopplingen igen, men tänk på att definiera kopplingskriterier.

* Det gick inte att hitta någon matchning för de fält som har angetts i matchningsvillkoret

    Upprepa kopplingen med hjälp av olika fält.

* Flera matchningar hittades för ett flertal poster, baserat på de fält som angets i matchande villkor  

    Upprepa kopplingen med hjälp av olika fält.

* En enskild matchning hittades, men motsvarande post är redan kopplad till en post i [!INCLUDE [prod_short](includes/prod_short.md)]  

    Upprepa kopplingarna med olika fält, eller undersök varför [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-entiteten är kopplad till posten i [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> För att hjälpa dig att få en överblick över kopplingens framsteg visar föltet **Kopplad till Dataverse** om en specifik post är kopplad till en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-entitet eller inte. Du kan använda fältet **Kopplad till Dataverse** om du vill filtrera postlistan som du synkroniserar.

## Uppgradera anslutningar från Business Central Online till använda certifikatbaserad autentisering

> [!NOTE]
> Det här avsnittet är endast relevant för innehavaradministration i [!INCLUDE[prod_short](includes/prod_short.md)] online som Microsoft har. Online innehavaradministratörer som körs av ISV och lokala installationer påverkas inte.

I april 2022 förklarar [!INCLUDE[cds_long_md](includes/cds_long_md.md)] autentiseringstypen Office365 som inaktuell (användarnamn/lösenord). Mer information finns i avsnittet [Avskrivning autentiseringstyp av Office 365](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). I mars 2022 förklarar dessutom [!INCLUDE[prod_short](includes/prod_short.md)] användningen av klienthemlighetsbaserad autentisering tjänst-till-tjänst som inaktuell för online-klientorganisationer. Du måste använda certifikatbaserad tjänst-till-tjänst-autentisering för anslutningar till [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. [!INCLUDE[prod_short](includes/prod_short.md)]-onlineklientorganisationer som är värdbaserade hos oberoende mjukvaruleverantörer (ISV) kan fortsätta att använda klienthemligheter för autentisering.

För att undvika störningar i integrationen _måste du uppgradera_ anslutningen så att den använder certifikatbaserad autentisering. Ãven om ändringen är planerad till mars 2022 rekommenderar vi starkt att du uppgraderar så snart som möjligt. Följande steg beskriver hur du uppgraderar till certifikatbaserad autentisering. 

### För att uppgradera din Business Central online-anslutning för att använda certifikatbaserad autentisering

1. Gör något av följande beroende på om du har integrerat med Dynamics 365 Sales:
   * Om du vill kan du öppna sidan **Microsoft Dynamics 365 anslutningsinställning**.
   * Om du vill kan du öppna sidan **Dataverse anslutningsinställning**.
2. Välj **anslutning** och sedan **Använd certifikatautentisering** för att uppgradera anslutningen till att använda certifikatbaserad autentisering.
3. Logga in med administratörsautentiseringsuppgifter för Dataverse. Inloggningen tar mindre än en minut.

> [!NOTE]
> Du måste upprepa dessa steg i varje [!INCLUDE[prod_short](includes/prod_short.md)]-miljö, inklusive både produktions- och miljöer i begränsat läge och i varje företag där du är ansluten till [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## Ansluta lokala versioner

Om du vill ansluta [!INCLUDE[prod_short](includes/prod_short.md)] lokalt till [!INCLUDE[cds_long_md](includes/cds_long_md.md)] måste du ange viss information på **Dataverse anslutningsinställningar**.

För att ansluta med ett Microsoft Entra-konto måste du registrera ett program i Microsoft Entra ID. Du måste tillhandahålla det program-ID, den nyckelvalvshemlighet och den omdirigerings-URL som ska användas. URL-adressen för omdirigering fylls i förväg och bör användas för de flesta installationer. Du måste ställa in installationen för att använda HTTPS. Mer information finns i [Konfigurera SSL för att skydda anslutningen till Business Central webbklienten](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Om du konfigurerar servern så att den får en annan startsida kan du alltid ändra URL-adressen. Klientens hemlighet kommer att sparas som en krypterad sträng i databasen. 

### Så här registrerar du ett program i Microsoft Entra ID för att ansluta från Business Central till Dataverse

Följande åtgärder förutsätter att du använder Microsoft Entra ID för att hantera identiteter och åtkomst. Mer information om hur du registrerar ett program i Microsoft Entra ID finns i [Snabbstart: Registrera ett program med Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). 

1. I Azure Portal, under **Hantera** i navigeringsrutan välj **autentisering**.  
2. Under **omdirigerings-URL**, lägger du till den omdirigerings-URL som föreslås på sidan **Inställningar för Dataverse-anslutning** i [!INCLUDE[prod_short](includes/prod_short.md)].
3. Under **Hantera**, välj **API-behörigheter**.
4. Under **konfigurerade behörigheter** väljer du **Lägg till en behörighet** och lägger sedan till delegerade behörigheter på fliken **Microsoft API:er** på följande sätt:
    * För Business Central lägger du till **Financials.ReadWrite.All** behörighet.
    * För Dynamics CRM lägg till behörigheter **user_impersonation**.  

    > [!NOTE]
    > Namnet på Dynamics CRM API kan ändras.

5. Under **Hantera**, välj **Certifikat och hemligheter** och skapa sedan en ny hemlighet för ditt program. Du kommer att använda hemligheten i [!INCLUDE[prod_short](includes/prod_short.md)] i fältet **klienthemlighet** på sidan **inställningar för Dataverse-anslutning**, eller lagra i en skyddad lagringsenhet och tillhandahålla den i en händelseprenumerant enligt beskrivningen ovan.
6. Välj **Översikt** och leta sedan reda på **App (klient-ID)**-värdet. Detta ID är klient-ID:t för ditt program. Du måste ange den på sidan **inställningar för Dataverse-anslutning** i fältet **klient-ID** eller lagra den på ett säkert lagringsutrymme och tillhandahålla den i en händelseprenumeration.
7. I [!INCLUDE[prod_short](includes/prod_short.md)], på sidan **inställningar av Dataverse-anslutning** i fältet **Miljö-URL** anger du URL för din [!INCLUDE[cds_long_md](includes/cds_long_md.md)] miljö.
8. För att aktivera anslutningen till [!INCLUDE[cds_long_md](includes/cds_long_md.md)], aktivera växlingen **Aktiverad**.
9. Logga in med ditt administratörskonto för Microsoft Entra ID (det här kontot måste ha en giltig licens för [!INCLUDE[cds_long_md](includes/cds_long_md.md)] och vara administratör i din [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljö). När du har loggat in kommer du att uppmanas att tillåta att ditt registrerade program loggar in på [!INCLUDE[cds_long_md](includes/cds_long_md.md)] å ditt företags vägnar. Du måste ange ett medgivande för att slutföra installationen.

   > [!NOTE]
   > Om du inte uppmanas att logga in med ditt administratörskonto beror det förmodligen på att popup-fönster blockeras. Du kan logga in med popup-fönster från `https://login.microsoftonline.com`.

### Koppla bort från [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Konfiguration av inställningen av Dataverse** och väljer sedan relaterad länk.
2. På sidan **Konfiguration av anslutning till Dataverse** stänger du av reglaget **Aktiverad**.  

## Se även

[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
