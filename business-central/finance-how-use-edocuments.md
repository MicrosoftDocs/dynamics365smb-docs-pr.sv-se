---
title: Använd e-dokument inom försäljning
description: Lär dig hur du använder e-dokumentfunktioner som är relaterade till försäljning.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 03/29/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Använda e-dokument i försäljningsprocessen

Du kan använda konfigurerade elektroniska dokument (e-dokument) med försäljningsdokument.

Du kan använda följande försäljningsdokument med funktionen för e-dokument:  

- Försäljningsfakturor
- Försäljningsorder
- Försäljningskreditnotor
- Servicefakturor
- Servicekreditnotor
- Räntefakturor
- Påminnelser

## E-dokument inom försäljning  

Om du vill skapa och skicka en e-faktura till en kund måste du skapa och bokföra försäljningsfakturan. Mer information om standardprocessen finns i [Fakturaförsäljning](sales-how-invoice-sales.md).

När du har bokfört försäljningsdokumentet öppnar du sidan **Bokförd försäljningsfaktura** för att komma åt den relaterade **e-dokumentsidan**.

### Se e-dokument   

Så här visar du befintliga e-dokument.

1. På sidan **Bokförd försäljningsfaktura**, välj **E-dokument** \> **Öppna E-dokument**.
2. I huvudet på sidan **E-dokument** kan du visa grundläggande information om den bokförda fakturan.
3. Fältet **Post** visar dokumentnumret för den bokförda försäljningsfakturan. Välj länken för att öppna dokumentet.
4. I fältet **Status för elektroniskt dokument** kan du visa dokumentets realtidsstatus och dess placering i processpipelinen. Om dokumentet bokförs är statusen **Bearbetat**.

### E-dokumentstatusar och loggar 

Mer information om servicestatusnivån för ditt e-dokument finns på snabbfliken **Servicestatus för e-dokument**. På raderna visar systemet en eller flera tjänster som dokumentet använt. I det vanligaste scenariot använder varje dokument bara en tjänst. Ett dokument kan dock använda flera tjänster.

- Kontrollera fältet **E-dokument servicekod** för att fastställa vilken tjänst som användes.
- Kontrollera fältet **Status för e-dokument** för att fastställa aktuell servicestatus för det här dokumentet.
- Om du vill ha mer information väljer du fältet **Loggar** för tjänsten på sidan **E-dokumentloggar**. En kronologisk översikt över dokumentets olika status visas.
- Kontrollera fälten **Löpnr.** och **Skapad den** och annan information på sidan **E-dokumentloggar**. I fältet **E-dokumentstatus** är den första statusen **Exporterad**, vilket anger att e-dokumentfilen har skapats. Nästa status är **Skickat**, vilket anger att dokumentet har skickats till tjänstleverantören, om en sådan har konfigurerats.

Om du vill ha mer information väljer du den post som har statusen **Exporterad** och kör sedan någon av följande åtgärder:

- **Öppna mappningsloggar** – Få en översikt över alla exporterade fält från källtabellerna i fältet **Ursprungligt värde**. Om du använde omvandlingsregler i exportprocessen kan du också hämta det slutliga värdet i fältet **Nytt värde**.
- **Exportera fil** – Exportera XML-filen för manuell granskning.

Om du vill visa kommunikationen mellan dig själv och tjänsten som du skickar dokumentet till använder du fältet **Kommunikationsloggar**. Öppna sidan **Kommunikationsloggar för e-dokument** om du vill visa information om meddelandet om begäran och orsaker till tjänsten.

Om det finns ett problem med tjänsteleverantören och dokumentet inte kan skickas, leta efter följande indikatorer på sidan **E-dokument**:

- I fältet **Status för elektroniskt dokument** i huvudet visas **Felstatus**.
- Fältet **E-dokumentstatus** på snabbfliken **Status för e-dokumenttjänst** visas statusen **Sändningsfel**.
- Snabbfliken **Fel och varningar** innehåller ett eller flera meddelanden som anger orsaken till problemet.

När problemet har åtgärdats kör du åtgärderna **Skicka dokument** manuellt. Om du behöver olika åtgärder, till exempel **Återskapat dokument**, **Avbryt dokument** eller **Hämta godkännande**, kan du köra dem.

## Översikt över status för e-dokument

Om du vill få en bättre överblick över alla e-dokument i företaget kan du välja det rollcenter för **Revisor** där det finns e-dokumentstatus. Där kan du hitta e-dokumentaktiviteter som har följande status:

- **Utgående e-dokument:**

    - Bearbetade
    - Pågår
    - Fel


## Se även

[Hur man ställer in e-dokument i Business Central](finance-how-setup-edocuments.md)  
[Hur man utökar e-dokument i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Ekonomihantering](finance.md)  
[Fakturera försäljning](sales-how-invoice-sales.md)  
[Registrera inköp med inköpsfakturor och order](purchasing-how-record-purchases.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
