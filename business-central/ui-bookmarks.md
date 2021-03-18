---
title: Förse en länk med ett bokmärke på en sida eller rapport i ditt rollcenter | Microsoft Docs
description: Lär dig hur du lägger till en länk från ditt rollcenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5e85c6200f9fafa800e2e44978a5efb10ececefb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376693"
---
# <a name="bookmark-a-page-or-report-on-your-role-center"></a>Förse en sida eller rapport med ett bokmärke på ditt rollcenter
Med hjälp av bokmärkesikonen kan du lägga till en åtgärd som öppnar en sida eller rapport från navigeringsmenyn i rollcentret. På så sätt kan du snabbt nå ditt favoritinnehåll eller dina affärsuppgifter. Du lägger till bokmärket från målsidan eller rapport vilket innebär skärmen som du vill att länken i rollcentret ska öppnas på.

Ikonen för bokmärket visas i det övre högra hörnet på en sida och även i fönstret **Berätta** där du kan förse flera sidor eller rapporter med ett effektivt bokmärke. Om det redan finns ett bokmärke för sidan är ikonen mörk ruta och beskrivningen visar "bokmärke".

## <a name="to-bookmark-the-target-page"></a>Så här förser du målsidan med bokmärke
1. Öppna en sida som du vill ha en länk för i ditt rollcenter.
2. Välj ikonen ![bokmärke](media/ui_bookmark_icon.png "Bokmärke").

Ett åtgärd med namn efter sidan läggs nu till på navigeringsmenyn i rollcentret.

## <a name="to-bookmark-the-target-report"></a>Så här förser du målrapporten med bokmärke
1. Öppna en sida för rapportförfrågan som du vill ha en länk för i ditt rollcenter.
2. Välj ikonen ![bokmärke](media/ui_bookmark_icon.png "Bokmärke").

Ett åtgärd med namn efter rapporten läggs nu till på navigeringsmenyn i rollcentret.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window"></a>Så här lägger du till ett bokmärke från en sida eller rapport från fönstret berätta
1. Öppna fönstret **Berätta** och ange till exempel, **försäljningsorder**.
2. Hovra över sökresultatet för sidan eller rapporten **försäljningsorder** och välj sedan ikonen ![bokmärke](media/ui_bookmark_icon.png "Bokmärke").

Ett åtgärd med namn efter sidan eller rapporten läggs nu till på navigeringsmenyn i rollcentret.


## <a name="frequently-asked-questions"></a>Vanliga frågor och svar  

- **Kan jag omorganisera mina bokmärken?**  
Ja. Du kan anpassa rollcentret och flytta åtgärder till en mer optimal sekvens eller flytta dem till befintliga grupper eller undergrupper.  
Lär dig hur du [anpassar arbetsytan](ui-personalization-user.md).

- **Hur tar jag bort ett bokmärke?**  
Välj ikonen bokmärke på målsidan eller rapporten igen för att ta bort den åtgärd som berörs från ditt rollcenter. Du kan också anpassa ditt rollcenter och temporärt dölja åtgärder utan att ta bort dem helt.

- **Var hittar jag mina bokmärken?**  
När du lägger till ett bokmärke på en sida eller rapport läggs den nya åtgärden till på den översta navigeringsmenyn i den aktuella startskärmen (rollcenter). Om du råkar ut för många åtgärder kanske du måste aktivera knappen **mer** för att visa alla dem eftersom den nya åtgärden alltid läggs till i slutet av dessa åtgärder.
<!-- Should we add a screenshot here? -->

- **Jag har ingen ikon för bokmärken. Är något fel?**  
Möjligheten att förse en sida eller rapport med är en av många anpassningsfunktioner för användare i Business Central. Om ikonen för bokmärket inte visas är det troligt att administratören har inaktiverat anpassningar.

- **Varför kan jag inte använda sidmärke för vissa sidor eller rapporter?**  
Alla sidor och rapporter kan inte förses med bokmärken. När en sida eller rapport körs i en viss särskild kontext som styrs av affärs programmet, visas inte bokmärksikonen. Sidor som inte kan hittas i fönstret **berätta** startas från någon annan stans visar inte en bokmärkesikon. På samma sätt visas inte en bokmärkesikon i rapportbegäransidor som endast används för att hämta filter utan att köra rapporten.

Se teknisk information om [RunRequestPage](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) och [FilterPageBuilder](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **När jag avmarkerar min anpassning tas även mina bokmärken bort?**  
Ja. Bokmärkena finns på navigeringsmenyn. Om du rensar ändringar i navigeringsmenyn från en sida, eller avmarkerar all anpassning i rollcentret, kommer alla nya åtgärder att tas bort permanent.

- **Varför fortsätter ikonen för bokmärket att ange att den fortfarande inte har bokmärke?**  
När du lägger till ett bokmärke läggs den nya åtgärden till på navigeringsmenyn i rollcentret och efterföljande besök på sidan eller rapporten visar en mörk ikon i bokmärket. Om du anpassar ditt rollcenter och strukturerar om dina åtgärder genom att flytta dem till grupper, kommer bokmärkesikonen inte längre att vara mörk och du kan lägga till ett annat bokmärke till samma sida eller rapport. På så sätt kan du lägga till flera åtgärder på samma sida eller rapport och kategorisera dem i olika grupper.

- **Varför visas en annan rapport i min länk till en rapport?**  
En del rapporter kan ersättas av andra rapporter efter att ha tillämpat ett tillägg på Business Central. När ersättning inträffar uppdateras inte texten för den nya åtgärden och namnet på den ursprungliga rapporten visas, men det går att navigera till den nyare rapporten. Om du vill korrigera texten för den nya åtgärden kan du ta bort den nya åtgärden och lägga till den igen.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Är bokmärket tillgängligt för XMLport?**  
Nr Det går för tillfället inte att lägga till åtgärder för att öppna XMLport-data från användargränssnittet.

- **Kommer mina bokmärken att översättas när jag ändrar språk i Business Central?**  
När du lägger till en ny åtgärd kommer all översatt text som var tillgänglig vid tidpunkten att användas när du lägger till ett bokmärke. Om ny översatt text läggs till senare kommer den nya åtgärden inte att inkludera de nyare översättningarna.


## <a name="see-also"></a>Se även
[Anpassa din arbetsyta](ui-personalization-user.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]