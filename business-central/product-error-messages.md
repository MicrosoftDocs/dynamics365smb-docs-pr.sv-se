---
title: Varningar och felmeddelanden
description: Lär dig hur du felsöker och hittar lösningar på felmeddelanden när du arbetar i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-temeplate
---
# <a name="warnings-and-error-messages"></a>Varningar och felmeddelanden

Under din arbetsdag kan du se meddelanden i [!INCLUDE [prod_short](includes/prod_short.md)] om att något gick fel eller att det inte var möjligt att bokföra någonting t. ex. I många fall gör meddelandet det enkelt att lösa ärendet eller att återställa de ändringar som du har gjort. I andra fall kanske du inte har den information som du behöver för att få en avblockering. I den här artikeln finns tips om hur du gör framsteg.  

## <a name="in-product-user-assistance"></a>Användarhjälp i produkten

Standardversionen av [!INCLUDE [prod_short](includes/prod_short.md)] innehåller beskrivningar av de flesta fält, kolumner och åtgärder som du kan komma åt när du väljer namnet. I kombination med undervisningstips för viktiga sidor, beskrivande rubriker och instruktionstext är dessa beskrivningar eller bildtexter vår aktuella implementering av *inbäddat användarstöd*, som är en viktig princip i dagens programvarudesign.  

Om du har en fråga om ett fält eller något annat element i användargränssnittet, väljer du namnet och en kort beskrivning. Välj länken **Fråga Copilot** om det inte räcker. Du kan också använda Hjälp fönstret i produkt för att hitta svar på dina frågor.  

Mer information finns i [Dynamics 365 Business Central användarhjälpsmodell](/dynamics365/business-central/dev-itpro/user-assistance) i administrationsinnehållet för [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="help-and-support-page"></a>Hjälp- och supportsida

I [!INCLUDE[prod_short](includes/prod_short.md)] ger hjälpmenyalternativet (frågetecken i övre högra hörnet) dig tillgång till sidan **Hjälp och support** där du hittar länkar till resurser som kan hjälpa dig att hitta svaren på dina frågor. Mer information finns i [Resurser för Hjälp och support](product-help-and-support.md).  

## <a name="help-others"></a>Hjälpa andra

Om du är administratör eller superanvändare kan du hjälpa andra genom att söka efter felmeddelanden på sidan **Felmeddelanderegister** eller i administrationscentret. I många fall handlar varningen eller felmeddelandet om installation eller avsaknad av behörighet och liknande problem som superanvändaren eller administratören kan hjälpa till med. I andra fall kanske du måste inspektera sidorna för att identifiera orsaken. Mer information finns i avsnittet [Söka efter teknisk information](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) i administrationsinnehållet för [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="share-error-details-for-faster-assistance"></a>Dela felinformation för snabbare hjälp

Utnyttja expertisen hos kollegor eller ämnesexperter för att övervinna hinder och minimera stilleståndstiden. När du blockeras av ett fel kan du enkelt dela felinformationen när du får hjälp.

Informationen omfattar felmeddelande, felkod och annan information som är användbar när du felsöker ett fel. Genom att dela felinformationen kan du effektivt kommunicera det specifika problemet du står inför, vilket hjälper dina kollegor att hjälpa dig.  

Du kan kopiera detaljer genom att välja **ikonen Dela** i infogade valideringsdialogrutor eller menyn **Dela information** i feldialogrutor.  

Förutom att kopiera felinformation kan du också välja att dela information via Microsoft Teams genom att välja **Dela information till Teams** för att göra följande:

* Kopiera felinformationen.
* Öppna fönstret **Dela till Teams** där du kan klistra in felinformationen du kopierade och ange vem du vill be om hjälp. [!INCLUDE [prod_short](includes/prod_short.md)] lägger till en länk till sidan där du upplevde felet för att underlätta felsökningen.

Du kan också välja att dela information via e-post genom att välja **Dela information via e-post** för att göra följande:

* Kopiera felinformationen.
* Öppna standardredigeringsprogram för e-post där du kan klistra in felinformationen du kopierade och ange vem du vill be om hjälp. [!INCLUDE [prod_short](includes/prod_short.md)] lägger till en länk till sidan där du upplevde.

## <a name="help-yourself"></a>Hjälp dig själv

Felmeddelanden innehåller information och åtgärder som gör det lättare att förstå, gå till och lösa fel som kommer från plattformen.

Felmeddelandena som [!INCLUDE [prod_short](includes/prod_short.md)] plattformen genererar innehåller fullständig teknisk information, inklusive fältnamn, i avsnittet **Detaljerat felmeddelande**. Välj ikonen **Kopiera information** vid infogade valideringsfel eller i ett felmeddelande för att komma åt den tekniska informationen.

Åtgärder i felmeddelanden tar dig direkt till sidan där ett fält orsakar felet. Du behöver inte ta dig tid att hitta sidan eller fältet själv. För att lösa felet, välj bara åtgärden i felmeddelandet och [!INCLUDE [prod_short](includes/prod_short.md)] tar dig till lämplig plats.

Följande video visar hur du använder åtgärdsbara felmeddelanden för att häva blockeringen.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2sM]

### <a name="tip-for-developers"></a>Tips för utvecklare

Om du är utvecklare och anropar metoden [TestField](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-testfield-joker-joker-errorinfo-method) men inte skickar |`ErrorInfo`-objekt, [!INCLUDE [prod_short](includes/prod_short.md)] automatiskt länken till en sida där en användare kan åtgärda problemet. [!INCLUDE [prod_short](includes/prod_short.md)] hämtar först uppslags- eller detaljsidan för posten och söker sedan efter kortsidan eller uppslagssidan och lägger till en navigeringslänk på kortsidan. [!INCLUDE [prod_short](includes/prod_short.md)] lägger inte till en länk i följande situationer:

* Om felet finns på sidan som är öppen.
* Om användaren inte har behörighet att ändra den underliggande posten.

## <a name="see-also"></a>Se även

[Resurser för hjälp och support](product-help-and-support.md)  
[Vanliga frågor och svar](across-faq.yml)  
[Vanliga frågor om Berätta](ui-search-faq.md)  
[Vanliga frågor och svar om sökning och filtrering](ui-search-filter-faq.yml)  
[Vanliga frågor om Kopiera och klistra in](faq-copy-paste.yml)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
