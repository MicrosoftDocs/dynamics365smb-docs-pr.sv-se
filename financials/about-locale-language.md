---
title: "Flera språk och lokalisering | Microsoft Docs"
description: "Lär dig mer om hur språk och språkvarianter påverkar din upplevelse i Dynamics 365."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 94a7a3e1da9f2ac3145f18102f86386cfc980ea5
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="language-and-locale"></a>Språk och språkvarianter
[!INCLUDE[d365fin](includes/d365fin_md.md)] fungerar på flera olika marknader och på de språk som dessa marknader kräver. Detta är ett resultat av stöd för flera språk vid körning i kombination med stöd för juridiska krav på marknaderna som stöds. Detta innebär att en [!INCLUDE[d365fin](includes/d365fin_md.md)] kan användas på flera olika språk. Du kan ändra det språk som används för att visa texter och ändringen sker direkt, när du automatiskt har loggats ut och in igen. Inställningen gäller för dig och inte de övriga i företaget.  

Om du till exempel är kanadensisk visas användargränssnittet på engelska och franska, men det är fortfarande den kanadensiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)] i alla andra avseenden. Den är inte likadan som exempelvis [!INCLUDE[d365fin](includes/d365fin_md.md)] i Storbritannien.  

> [!NOTE]  
>  Ändring av språk stöds för närvarande inte i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Det ingår inte i funktionen Multilanguage att ändra språk för de texter som lagras som programdata. Detta är i stället ett fråga om utformning. Exempel på den här typen av text är artikelnamnen i lagret och kundkommentarerna. Kort sagt är det här texttyper som inte har översatts.  

> [!NOTE]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] har bara stöd för en enda teckenuppsättning. Därför kanske en del tecken inte stöds i din klientorganisation och det uppstår problem med att hämta data som har registrerats med en annan teckenuppsättning. Din klientorganisation kanske enbart stöder engelska och ryska tecken, och om du registrerar data på ett annat språk kanske de inte lagras på rätt sätt. Kontakta systemadministratören om du vill ha information om vilka språk som stöds i din [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="changing-the-locale"></a>Ändra språkvariant
Språkvarianter skiljer sig från både språk och juridiska krav på lokala marknader. Språkvarianter bestämmer hur data visas när det gäller kommateckenavgränsare, justering till vänster eller till höger och vissa andra inställningar. Dessa inställningar avgör vissa systemelement i webbläsaren, till exempel åtgärden att skapa ett nytt objekt i en lista.  

Du kan ändra språkvariant i fliken som du använder för att arbeta i [!INCLUDE[d365fin](includes/d365fin_md.md)]. ändringen gäller bara för dig och inte för de andra användarna i företaget.  

> [!IMPORTANT]  
>  När du ändrar språkvariant visas en lång lista över språk och språkvarianter. Däremot används bara språkvarianterna i den aktuella versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Om du vill ändra språkvariant går du till fönstret **Mina inställningar**. Mer information finns i [Ändra grundläggande inställningar](ui-change-basic-settings.md).  

## <a name="see-also"></a>Se även  
[Språk för Docs](about-languages.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

