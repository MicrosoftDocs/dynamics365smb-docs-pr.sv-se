---
title: Använda e-dokument vid försäljning och inköp
description: Lär dig hur du använder e-dokumentfunktioner som är relaterade till försäljnings- och inköpsfakturor.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
---

# <a name="use-e-documents-in-sales-and-purchases"></a>Använda e-dokument vid försäljning och inköp

Du kan använda konfigurerade elektroniska dokument (e-dokument) med försäljnings- och inköpsdokument.

Du kan använda följande dokument med funktionen för för e-dokument:  

- Försäljning: 
    - Försäljningsfakturor
    - Försäljningsorder
    - Försäljningskreditnotor
    - Servicefakturor
    - Servicekreditnotor
    - Räntefakturor
    - Påminnelser
- Inköp: 
    - Inköpsfakturor
    - Inköpsorder (skapa endast nytt dokument)
    - Inköpskreditnotor
    - Redovisningsjournaler

> [!NOTE]
> För närvarande kan en inköpsorder endast användas när du skapar dokumentet från leverantörens e-dokument. Du kan dock inte uppdatera det befintliga dokumentet med rader som du har fått från leverantören.  

## <a name="e-documents-in-sales"></a>E-dokument inom försäljning

Om du vill skapa och skicka en e-faktura till en kund måste du skapa och bokföra försäljningsfakturan. Mer information om standardprocessen finns i [Fakturaförsäljning](sales-how-invoice-sales.md).

När du har bokfört försäljningsdokumentet öppnar du sidan **Bokförd försäljningsfaktura** för att komma åt den relaterade **e-dokumentsidan**.

### <a name="view-e-documents"></a>Se e-dokument

Så här visar du befintliga e-dokument.

1. På sidan **Bokförd försäljningsfaktura**, välj **E-dokument** \> **Öppna E-dokument**.
2. I huvudet på sidan **E-dokument** kan du visa grundläggande information om den bokförda fakturan.
3. Fältet **Post** visar dokumentnumret för den bokförda försäljningsfakturan. Välj länken för att öppna dokumentet.
4. I fältet **Status för elektroniskt dokument** kan du visa dokumentets realtidsstatus och dess placering i processpipelinen. Om dokumentet bokförs är statusen **Bearbetat**.

### <a name="e-document-statuses-and-logs"></a>E-dokumentstatusar och loggar

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

## <a name="e-documents-in-purchases"></a>E-dokument vid köp

Inleveransen av elektroniska inköpsfakturor Dynamics 365 Business Central kan göras som ett batchjobb eller manuellt.

### <a name="run-the-batch-job"></a>Kör batch-jobbet

> [!NOTE]
> Det här batchjobbet används för automatisk insamling av dina inkommande fakturor. Det kan bara fungera i ett land eller en region där funktionen finns.

Varje gång en jobbkö körs och den externa tjänsten har inkommande fakturor som har skickats från din leverantör, samlar systemet in och importerar dessa fakturor. Följ dessa steg för att slutföra processen.

1. När batch-jobbet har körts visas de nyligen importerade fakturorna på sidan **E-dokument** tillsammans med grundläggande detaljinformation.
2. Om du vill visa mer information öppnar du ett särskilt e-dokument.
3. Om det inte fanns några fel eller problem i e-dokumentet och det mappas, visar fältet **Post** dokumentnumret på inköpsfakturan som systemet skapade automatiskt. Välj länken för att öppna dokumentet. Det här systemskapade dokumentet är inte det bokförda dokumentet.
4. Om du vill gå direkt till inköpsdokumentet markerar du fältet **Post**. När du har öppnat sidan **Inköpsfaktura** kontrollerar du dokumentet. Sedan, om allt är korrekt, bokför dokumentet.
5. När du bokför inköpsdokumentet uppdateras fältet **Post** i **e-dokumentet** från **Faktura** till **Inköpsfaktura** och numret på det bokförda inköpsdokumentet är tillgängligt. Du kan välja numret för att öppna den bokförda inköpsfakturan.

Detaljer om loggar är desamma som i försäljningsprocessen för e-dokument.

Eftersom fel i försäljningsprocessen oftast beror på tjänstens tillgänglighet kan det inkommande dokumentet ha flera orsaker. Den vanligaste orsaken till ett fel är att systemet inte kan känna igen raderna på e-dokumentet som du har fått från leverantören. Därför kan den inte ange rader på inköpsfakturan.

Det finns två vanliga fel:

- Om du vill använda den här specifika raden från leverantörsfakturan som bokfördes direkt på redovisningskontot måste du ha konfigurerat värdet **Mappningstext** korrekt. För att kringgå det här felet om du vill använda huvudkonton, välj **Mappa text till konto** för att skapa en specifik mappningsvärde **Mappningstext** med värde **Debetkontonr.** som du vill använda.
- Om du vill spåra inventeringen och använda rader från din leverantörsfaktura för att fylla i artiklar på dina dokumentrader, måste du ha konfigurerat korrekt **Artikelreferensnummer.** värde. Om du vill kringgå det här felet mappar du den externa artikeln med dina artikelnummer med hjälp av artikelreferenslistan. Mer information finns i [Använd artikelreferenser](inventory-how-use-item-cross-refs.md).

När du har åtgärdat felen och varningarna kan du manuellt ange när systemet ska skapa en inköpsfaktura baserat på dina inställningar genom att välja **Skapa dokument**.

### <a name="manually-import-invoices"></a>Manuellt importera fakturor

Så här importerar du externa e-dokument manuellt.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **E-dokumenttjänst** och väljer sedan relaterad länk.
2. På sidan **E-dokumenttjänst** väljer du den aktiva tjänsten. 
3. Välj **Inleverera** och överför e-dokumentfilen som du fick från leverantören.
4. Om ett felmeddelande visas öppnar du e-dokumentet för att åtgärda problemet.
5. När du har åtgärdat problem, i **Importera manuellt**, välj **Skapa dokument**.
6. När dokumentet har skapats i Business Central kan du visa det precis som om du använder ett batch-jobb.

## <a name="overview-of-e-document-statuses"></a>Översikt över status för e-dokument

Om du vill få en bättre överblick över alla e-dokument i företaget kan du välja det rollcenter för **Revisor** där det finns e-dokumentstatus. Där kan du hitta e-dokumentaktiviteter som har följande status:

- **Utgående e-dokument:**

    - Bearbetade
    - Pågår
    - Fel

- **Inkommande e-dokument:**

    - Bearbetade
    - Pågår
    - Fel

## <a name="see-also"></a>Se även

[Hur man ställer in e-dokument i Business Central](finance-how-setup-edocuments.md)  
[Hur man utökar e-dokument i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Ekonomihantering](finance.md)  
[Fakturera försäljning](sales-how-invoice-sales.md)  
[Registrera inköp med inköpsfakturor och order](purchasing-how-record-purchases.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
