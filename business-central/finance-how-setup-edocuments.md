---
title: Konfigurera e-dokument
description: Läs om hur du konfigurerar e-dokumentfunktioner.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
---

# <a name="set-up-e-documents"></a>Konfigurera e-dokument

> [!IMPORTANT]
> Kärnmodulen E-dokument är ett ramverk. Som standard finns det inget fält för **dokumentformat** eller **tjänstintegrering**. Den här informationen ingår i lokaliseringsappar eftersom de båda är specifika för lokala krav.

> [!NOTE]
> Från och med version 23.1 läggs ett standardformat för PEPPOL-dokument till som ett globalt format i fältet **Dokumentformat**.

Det första steget i konfigurationen av elektroniska dokument (e-dokument) är att konfigurera tjänsten E-dokument där du konfigurerar systemets fullständiga beteende när det gäller e-dokumentkommunikation.

## <a name="set-up-the-e-document-service"></a>Ställ in e-dokumenttjänsten

Följ dessa steg för att konfigurera e-dokumenttjänsten.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **E-dokumenttjänst** och väljer sedan relaterad länk.
2. Välj **Ny** och sedan på sidan **E-dokumenttjänst** på snabbfliken **Allmänt** konfigurera fälten enligt beskrivningen i följande tabell.

    | Fält | Description |
    |-------|-------------|
    | Kod | Välj inställningskoden för den elektroniska exporten. |
    | Description | Ange en kort beskrivning av konfigurationen av elektronisk export. |
    | Dokumentformat | <p>Exportformatet för konfigurationen av den elektroniska exporten.</p><p>Som standard finns det inga alternativ i det här fältet i utgivningscykel 1.</p> |
    | Tjänstintegration | Välj integrationskod för konfiguration av elektronisk export. I utgivningscykel 1 är det enda alternativet **Ingen integration**. |
    | Använd batchbearbetning | Ange om tjänsten använder batchbearbetning för export. |

4. Fyll i fälten enligt beskrivningen i följande tabell på snabbfliken **Importerade parametrar**.

    | Fält | Description |
    |-------|-------------|
    | Validera mottagande företag | Anger om informationen om mottagarföretaget måste valideras under importen. |
    | Lös måttenhet | Anger om måttenheten ska lösas under importen. |
    | Referens för sökobjekt | Anger om en artikel ska sökas utifrån artikelreferens under importen. |
    | Sök artikelns GTIN | Anger om en artikel ska sökas utifrån Global Trade Item Number (GTIN) artikelreferens under importen. |
    | Mappning av sökkonto | Anger om ett konto ska sökas i **Kontomappning** av den inkommande text under importen. |
    | Validera radrabatt | Anger om en radrabatt ska valideras under importen. |
    | Koppla fakturarabatt | Anger om en fakturarabatt ska tillämpas under importen. |
    | Verifiera summor | Anger om en fakturarabatt ska verifieras under importen. |
    | Uppdatera order | Anger om motsvarande inköpsorder måste uppdateras. |
    | Skapa journalrader | Anger om journalrader måste skapas i stället för inköpsdokument. Välj det här alternativet om du vill använda journaler som mål för dina fakturor. |
    | Namn på redovisningsjournalmall | Anger namnet på redovisningsjournalmallen som används när journalraden skapas. Detta fält är tillämpligt om du vill använda journaler som mål för dina fakturor. |
    | Redovisningsjournalnamn | Anger namnet på redovisningsjournal som används när journalraden skapas. Detta fält är tillämpligt om du vill använda journaler som mål för dina fakturor. |
    | Importera automatiskt | Ange om dokument ska importeras automatiskt från tjänsten. |
    | Batchens starttid | Ange starttiden för importjobben. |
    | Minuter mellan körningar | Anger antalet minuter mellan att importjobb körs. |

Om du har konfigurerat formatet **datautbytesdefinition** i din lokalisering kan du lägga till en rad för varje dokumenttyp du behöver. Du måste emellertid först välja alternativet **Dokumenttyp** för varje rad som du behöver. För varje datatyp väljer du det värde för **Importera oformaterad kod** eller **Exportera def.kod för datautbyte** som du vill använda.

Om du inte använder formatet **Datautbytesdefinition**, du kan konfigurera format genom raderna **Exportera mappning** och **Importera mappning**, där du kan hitta tabeller och fält att använda och konfigurera omvandlingsregler om tillämpligt.

## <a name="set-up-a-document-sending-profile"></a>Konfigurera en dokumentutskicksprofil

Du kan konfigurera en önskad metod för att skicka försäljningsdokument för respektive kund. På så sätt behöver du inte välja ett sändningsalternativ varje gång du väljer åtgärden **Bokför och skicka**. På sidan **Dokumentutskicksprofiler** konfigurerar du olika utskicksprofiler som du kan välja bland i fältet **Dokumentutskicksprofil** på ett kundkort. Du kan markera kryssrutan **Standard** om du vill ange att dokumentutskicksprofilen är standardprofilen för alla kunder förutom för kunder som har fältet **Dokumentutskicksprofil** ifyllt med en annan utskicksprofil.

Den här funktionen används för att konfigurera automatisering av elektronisk fakturering. När du väljer åtgärden **Bokför och skicka** i ett försäljningsdokument visar dialogrutan **Bekräftelse för bokför och utskick** den utskicksprofil som använts, antingen den profil som angetts för kunden eller standardprofilen för alla kunder.

Följ dessa steg för att ställa in en dokumentutskicksprofil.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Dokumentutskicksprofil** och väljer sedan relaterad länk.
2. På sidan **Dokumentutskicksprofiler** väljer du **Ny**.
3. Ange nödvändig information i fälten på snabbfliken **Allmänt**.
4. Konfigurera fälten enligt beskrivningen i följande tabell på snabbfliken **Utskicksalternativ**.

    | Fält | Description |
    |-------|-------------|
    | Elektroniskt dokument | Ange om dokumentet ska skickas som ett elektroniskt dokumentet som en kund kan importera till sitt system när du väljer **Bokför och skicka**. Om du vill använda det här alternativet måste du också ange fältet **Format** eller **Flödeskod för elektronisk dokumenttjänst**. Eller så kan filen sparas på hårddisken. |
    | Format | Ange vilket format som ska användas för att skicka ett e-dokument. Fältet krävs om du väljer **Genom dokumentväxlingstjänst** i fältet **Elektroniskt dokument**. |
    | Flödeskod för elektronisk dokumenttjänst | Ange det elektroniska serviceflöde som används för att skicka dokument. Fältet krävs om du väljer **Utökat serviceflöde för e-dokument** i fältet **Elektroniskt dokument**. |

    > [!NOTE]
    > Om du väljer select **Utökat serviceflöde för e-dokument** i fältet **Elektroniskt dokument** måste du redan ha konfigurerat arbetsflödet för dina e-dokument.

## <a name="set-up-the-workflow"></a>Konfigurera arbetsflödet

Följ de här stegen om du vill konfigurera arbetsflödet som används i e-dokumentfunktioner.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Arbetsflödesmallar** och väljer sedan relaterad länk.
2. Om du inte hittar sidan **Arbetsflödesmallar för e-dokument** eller **Arbetsflödesmallar**, välj **Återställ Microsoft-maller**. **Arbetsflödesmallar för e-dokument** bör då visas. Stäng sidan.
3. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Arbetsflöden** och väljer sedan relaterad länk.
4. Kör åtgärden **Nytt arbetsflöde från mall** för att välja en för e-dokumentprocessen. De tillgängliga mallarna är **Skicka till en tjänst** och **Skicka till flera tjänster**.
5. Välj **OK** för att slutföra konfigurationen av arbetsflödet.
6. I fältet **Då svar** väljer du **Skicka e-dokument med inställningarna** för att konfigurera arbetsflödessvaren.
7. Välj den e-dokumenttjänst som du skapade som ett alternativ, välj **OK** och aktivera sedan arbetsflödet.

> [!NOTE]
> Du kan skapa ett eget arbetsflöde för e-dokument utan att använda fördefinierade arbetsflödesmallar. Om du har fler tjänster kan du använda olika arbetsflöden.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Ställa in en lagringspolicy för e-dokument

E-dokument kan omfattas av olika lokala lagar som är relaterade till den period som e-dokumenten bevaras. Därför har vi lagt till en lagringspolicy för all viktig information som är relaterad till e-dokument. Administratörer kan definiera bevarandeprinciper som anger hur ofta Dynamics 365 Business Central tar bort inaktuella poster som är relaterade till e-dokument. Mer information om kvarhållningsprinciper i [Definiera kvarhållningsprincip](admin-data-retention-policies.md).

Så här konfigurerar du bevarandeprinciper för e-dokument.

1. På sidan **E-dokumenttjänster** kör du åtgärden **Bevarandeprincip**.
2. När åtgärden har slutförts väljer du någon av följande bevarandeprinciper att konfigurera:

    - E-dokumentlogg
    - Integrationslogg för e-dokument
    - Mappningslogg för e-dokument
    - Datalagring för e-dokument

## <a name="see-also"></a>Se även

[Hur man använder e-dokument i Business Central](finance-how-use-edocuments.md)  
[Hur man utökar e-dokument i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Ekonomihantering](finance.md)  
[Fakturera försäljning](sales-how-invoice-sales.md)  
[Registrera inköp med inköpsfakturor och order](purchasing-how-record-purchases.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
