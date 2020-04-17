---
title: Flera språk och lokalisering | Microsoft Docs
description: Lär dig mer om hur språk och nationella inställningar påverkar din upplevelse i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2d98f433acbe5905d9807bf7e7ded8708ed22d3b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189027"
---
# <a name="changing-language-and-locale"></a>Byta språk och plats

[!INCLUDE[d365fin](includes/d365fin_md.md)] fungerar på flera olika marknader och på de språk som dessa marknader kräver. Detta är ett resultat av stöd för flera språk vid körning i kombination med stöd för juridiska krav på marknaderna som stöds. Detta innebär att en [!INCLUDE[d365fin](includes/d365fin_md.md)] kan användas på flera olika språk. Du kan ändra det språk som används för att visa texter och ändringen sker direkt, när du automatiskt har loggats ut och in igen. Inställningen gäller för dig och inte de övriga i företaget.  

Om du till exempel använder en kanadensisk version av [!INCLUDE[d365fin](includes/d365fin_md.md)], visas användargränssnittet på engelska och franska, men det är fortfarande den kanadensiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] i alla andra avseenden. Den är inte likadan som exempelvis [!INCLUDE[d365fin](includes/d365fin_md.md)] i Storbritannien.  

Om du vill ändra språket för användargränssnittet, går du till sidan **Mina inställningar**. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md#language).  

Det ingår inte i funktionen Multilanguage att ändra språk för de texter som lagras som programdata. Detta är i stället ett fråga om utformning. Exempel på den här typen av text är artikelnamnen i lagret och kundkommentarerna. Kort sagt är det här texttyper som inte har översatts.  

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] har bara stöd för en enda teckenuppsättning. Därför kanske en del tecken inte stöds i din klientorganisation och det uppstår problem med att hämta data som har registrerats med en annan teckenuppsättning. Din klientorganisation kanske enbart stöder engelska och ryska tecken, och om du registrerar data på ett annat språk kanske de inte lagras på rätt sätt. Kontakta systemadministratören om du vill ha information om vilka språk som stöds i din [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="changing-the-locale"></a>Ändra språkvariant
Språkvarianter skiljer sig från både språk och juridiska krav på lokala marknader. Språkvarianter bestämmer hur data visas när det gäller kommateckenavgränsare, justering till vänster eller till höger och vissa andra inställningar. Dessa inställningar avgör vissa systemelement i webbläsaren, till exempel åtgärden att skapa ett nytt objekt i en lista.  

Du kan ändra språkvariant i fliken som du använder för att arbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)]. ändringen gäller bara för dig och inte för de andra användarna i företaget.  

> [!IMPORTANT]  
>  När du ändrar språkvariant visas en lång lista över språk och språkvarianter. Däremot används bara språkvarianterna i den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Om du vill ändra språkvariant går du till sidan **Mina inställningar**. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).  

## <a name="application-version"></a>Programversion

På sidan **Hjälp och support** kan du se den version av [!INCLUDE [prodshort](includes/prodshort.md)] som ditt företag är baserat på. Om du vill basera ett företag på en annan version kan administratören skapa en ny produktionsmiljö. Mer information finns i [Skapa en ny produktionsmiljö](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) i innehållet för utvecklare och IT-proffs.  

## <a name="languages-of-the-d365fin-help"></a>Språk för [!INCLUDE[d365fin](includes/d365fin_md.md)]-hjälpen
Innehållet i hjälpen för grundläggande funktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] publicerar på webbplatsen Microsoft Docs och finns på flera olika språk. Om du har tillgång till dokument inifrån [!INCLUDE[d365fin](includes/d365fin_md.md)], visas innehållet på ditt eget språk. Om en viss sida inte ännu är tillgänglig på ditt språk, visas den på engelska.

### <a name="how-do-i-change-the-language"></a>Hur ändrar jag språket?
Det är enkelt - bläddra längst ned på sidan och välj symbolen med en jordglob längst ned till vänster.

> [!NOTE]  
> Listan visar alla språk som stöds av webbplatsen Microsoft Docs. [!INCLUDE[d365fin](includes/d365fin_md.md)] finns i ett begränsat antal länder/regioner, men hjälpinnehållet är tillgänglig på flera språk. Hjälpinnehållet är inte tillgängligt för alla språk som stöds av webbplatsen Microsoft Docs.

## <a name="see-also"></a>Se även

[Resurser för hjälp och support](product-help-and-support.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Komma igång](product-get-started.md)  
