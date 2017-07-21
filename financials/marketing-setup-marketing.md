---
title: "Ställ in Marknadsföring och Kontakthanteringsinformation | Microsoft Docs"
description: "Du kan ställa in marknadsföring och kontakthantering i Financials för att optimera relationer med potentiella kunder eller kunder och förbättra kampanjer och erbjudanden."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1bac6c541a07f5da6c42fa076627e174249f708b
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="setting-up-relationship-management"></a>Ställa in Kundhantering
Innan du sätter igång med att arbeta med kontakter och marknadsföringsräntor, är det några beslut och steg som du måste vidta för att ange hur marknadsföringsområdet hanterar vissa aspekter av kontakterna. Du kan till exempel bestämma om du ska synkronisera kontaktkort med kund-, leverantörs- och bankkontokort, hur nummerserier definieras eller vilken standardhälsningsfras som ska användas när ni skriver till kontakterna.

Att hantera kontakter och ha en strategi för att identifiera, attrahera och behålla kunder optimerar din verksamhet och ökar kundnöjdheten. Med ett bra kontakthanteringssystem blir det också enklare att skapa och upprätthålla relationer med kunderna. Kommunikation är nyckeln till dessa relationer. Att kunna skräddarsy kommunikationen med potentiella och befintliga kunder, leverantörer och affärspartners utifrån deras behov är nödvändigt för att ett företag ska lyckas. Ett första steg är att lägga upp en strategi och definiera hur företaget ska använda kontaktinformationen. Den här information används av många olika grupper i företaget, så ett ändamålsenligt system gör det enklare för alla att bli mer effektiva.

Du kan skapa marknadsförings- och kontakthantering från fönstret **Marknadsföringsinställningar**. För att öppna fönstret **Marknadsföringsinställning** väljer du ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "ikonen Sök efter sida eller rapport"), ange **Marknadsföringsinställning** och välj sedan relaterad länk.

## <a name="automatically-copying-specific-information-from-the-contact-companies-to-the-contact-persons"></a>Automatisk kopiering av särskild information från kontaktföretag till kontaktpersoner
Vissa uppgifter om kontaktföretag är helt identiska med uppgifter om kontaktpersoner som arbetar i dessa företag, till exempel adresser. I avsnittet **Arv** i fönstret **Marknadsföringsinställningar** kan du ange att programmet automatiskt kopierar särskilda fält från kontaktföretagkort till kontaktpersonkort, varje gång du skapar en kontaktperson för ett kontaktföretag. Du kan t.ex välja att kopiera säljarkod, adressdetaljer (adress ,adress 2, postnr, ort och län), kommunikationsdetaljer (faxnummer, telefonsvarare och telefonnummer) mm.

När du ändrar i något av dessa fält på kontaktföretagskortet ändras motsvarande fält automatiskt på kontaktpersonskortet (om du inte har ändrat fälten på detta manuellt).

Mer information finns i [Så här skapar du kontaktpersoner](marketing-how-create-contact-persons.md).

## <a name="using-predefined-defaults-on-new-contacts"></a>Använd fördefinierade standardinställningar på nya kontakter
Du kan ange att särskild språkkod, distriktskod, säljarkod och lands-/regionkod automatiskt ska tilldelas av programmet som standard på varje ny kontakt som du skapar. Du kan också ange standardförsäljningscykelkod som automatiskt ska tilldelas varje ny affärsmöjlighet som du skapar.

Värden i övertagna fält ersätter de standardvärden som du har angett. Om du exempelvis har angett engelska som standardspråk men företagets språk är tyska, tilldelas tyska automatiskt som språkkod för de kontaktpersoner som är registrerade på det företaget.

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Automatiskt registrerade interaktioner
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan automatiskt återges som interaktioner (till exempel order, fakturor, inleveranser och så vidare) liksom e-post, telefonsamtal och meddelanden.

Mer information finns i [automatiskt registrera interaktioner med kontakter](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more"></a>Synkronisera kontakter med kunder och fler
För att synkronisera kontaktkort med kund-, leverantörs- och bankkontokort måste du välja affärsrelationskod för kunderna, leverantörerna och bankkontona. Du kan exempelvis bara koppla kontakter till befintliga kunder om du har valt en affärsrelationskod för kunder i fönstret **Marknadsföringsinställningar**.

Mer information finns i [Så här synkroniserar du kontakter med kunder, leverantörer och bankkonton](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Tilldela en nummerserie för kontakter och affärsmöjligheter
Du kan ange nummerserier för kontakter, kampanjemöjligheterer, segment och affärsmöjligheter. Om du har angett nummerserie för kontakter, kan du när du skapar en kontakt trycka på  RETUR i fältet Nr på kontaktkortet. på kontaktkortet så skriver programmet in nästa lediga kontaktnummer automatiskt.

Mer information om nummerserier finns i [Skapa nummerserier](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Söka efter dubbelkontakter, när kontakter skapas
Du kan välja automatisk sökning efter kopior varje gång du skapar kontaktföretag eller söka manuellt när du har skapat kontakter. Du kan också välja automatisk uppdatering av söksträngar varje gång du ändrar uppgifter om kontakter eller skapar kontakter. Du kan bestämma procentuell överensstämmelse för sökningar, det vill säga hur många procents överensstämmelse det måste vara mellan två kontakter för att de ska anses vara kopior.

## <a name="setting-up-email-logging"></a>Ställa in e-postloggning
Du kan utbyta e-post med kontakter, kunder, leverantörer och så vidare. Du kan skicka och ta emot e-post från programmet eller Outlook. Innan du kan utbyta meddelanden på detta sätt och låta e-post lagras och placeras i kö måste du definiera vissa parametrar, till exempel hur ofta det ska kontrolleras om e-post väntar på att behandlas och namnet på profilen för e-postloggning.

## <a name="see-also"></a>Se även
[Hantera kontakter](marketing-contacts.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

