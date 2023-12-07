---
title: Flera språk och lokala inställningar
description: Lär dig mer om hur språk och regionsinställningar påverkar din upplevelse i Business Central. Ändra språket för användargränssnittet under Mina inställningar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'language, locale, localization, culture, region, regional settings'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Byta språk och region

[!INCLUDE[prod_short](includes/prod_short.md)] finns på många marknader och språk runtom i världen. På de marknader där det finns [!INCLUDE[prod_short](includes/prod_short.md)] finns det regleringsfunktioner som hjälper företag med regleringar. [!INCLUDE[prod_short](includes/prod_short.md)] kan visas på olika språk. Du kan till och med ändra språket som används för att visa texter. Ändringen sker omedelbart när du har loggats ut och in igen automatiskt. Inställningen gäller för dig och inte de övriga i företaget.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Du använder exempelvis den kanadensiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)]. Det innebär att du kan visa användargränssnittet på engelska, tyska, franska eller ett annat språk, men det är fortfarande den kanadensiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)]. Det är inte detsamma som [!INCLUDE[prod_short](includes/prod_short.md)] i Tyskland, där funktionaliteten har anpassats till den marknadens krav.  

Om du vill ändra språket för användargränssnittet, går du till sidan **Mina inställningar**. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md#language). 

> [!NOTE]  
> Valet av språk kommer att återställas till din Microsoft 365-profilinställning om administratören synkroniserar användare från Microsoft 365 till [!INCLUDE[prod_short](includes/prod_short.md)].

Du kan inte ändra de texter som lagras som programdata. Exempel på den här typen av text är artikelnamnen i lagret och kundkommentarerna. Kort sagt är det här texttyper som inte översätts.  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] har bara stöd för en enda teckenuppsättning. Därför kanske en del tecken inte stöds i din miljö och det uppstår problem med att hämta data som har registrerats med en annan teckenuppsättning. Din miljö kan till exempel endast stödja engelska och ryska tecken. I sådant fall, om du anger data på något annat språk, kan det hända att dina data inte lagras som de ska. Kontakta systemadministratören om du vill ha information om vilka språk som stöds i din [!INCLUDE[prod_short](includes/prod_short.md)].  

## Ändra nationella inställningar

Region skiljer sig från både språk och juridiska krav på lokala marknader. Region bestämmer hur data visas, till exempel vad gäller decimalavgränsare, och hur text justeras till vänster eller höger. Region avgör även vissa systemelement i webbläsaren, till exempel åtgärden att skapa ett nytt objekt i en lista.  

Du kan ändra region i fliken som du använder för att arbeta i [!INCLUDE[prod_short](includes/prod_short.md)]. Ändringen gäller bara för dig och inte för de andra användarna i företaget.  Valet av region kommer att återställas till din Microsoft 365-profil om administratören synkroniserar användare från Microsoft 365 till [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]  
> När du ändrar region visas en lång lista över språk och region. Språk påverkas dock inte av val av region.  

Om du vill ändra region går du till sidan **Mina inställningar**. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).  

## Ändra nationella inställningar för kunder, kontakter och leverantörer

Vissa företag använder en extern tjänst som validerar adressuppgifter i landet eller regionen. Men när du behöver uppdatera adressinformation kanske det struktureras som de här tjänsterna använder inte alltid är det som passar för vissa situationer. Business Central ger dig ett mer flexibelt sätt att ange adressuppgifter.

På sidan **Redovisningsinställningar** , om du aktiverar växlingsknappen **Kräv lands-/regionkod för adress** ändrar till fältet **Lands-/regionkod** på adresser för kunder, kontakter eller leverantörer kommer att återställa värdena i andra adressfält.

## Programversion

På sidan **Hjälp och support** kan du se den version av [!INCLUDE[prod_short](includes/prod_short.md)] som ditt företag är baserat på. Om du vill basera ett företag på en annan version kan administratören skapa en ny produktionsmiljö. Mer information finns i [Skapa en ny produktionsmiljö](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) i innehållet för utvecklare och IT-proffs.  

## Språk för [!INCLUDE[prod_short](includes/prod_short.md)]-hjälpen

Hjälpinnehållet i standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)] publiceras till Microsoft Learn. Innehållet är tillgängligt på olika språk. Om du har tillgång till dokumentation inifrån [!INCLUDE[prod_short](includes/prod_short.md)], visas innehållet på ditt eget språk. Om en viss sida inte ännu är tillgänglig på ditt språk, visas den på engelska som standard.

### Hur ändrar jag språk på Microsoft Learn-webbplatsen?

Det är enkelt – bläddra längst ned på sidan och välj symbolen med en jordglob längst ned till vänster.

> [!NOTE]  
> Listan visar alla språk som stöds av Microsoft Learn-webbplatsen. [!INCLUDE[prod_short](includes/prod_short.md)] är tillgängligt i ett begränsat antal länder/regioner och [!INCLUDE [prod_short](includes/prod_short.md)] Hjälp-innehållet är inte tillgängligt på alla språk som Microsoft Learn-webbplatsen stöder.

## Se även

[Resurser för hjälp och support](product-help-and-support.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]