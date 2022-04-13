---
title: Använda tillägget AMC Banking 365 Fundamentals
description: Lär dig byta data enkelt med bankerna genom att omvandla data till det format de kräver.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 06/23/2021
ms.author: bholtorf
ms.openlocfilehash: ec7ba151f94a7209e81f8e695b3053885d0fcc24
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510538"
---
# <a name="use-the-amc-banking-365-fundamentals-extension"></a>Använda AMC Banking 365 Fundamentals tillägget 
Med tillägget AMC Banking 365 Fundamentals blir det enklare och mer exakt att skicka data till dina banker. Tillägget ansluter [!INCLUDE[prod_short](includes/prod_short.md)] till AMC Banking 365 Fundamentals för Microsoft Dynamics 365 Business Central-tjänsten, som kan omvandla bankdata från [!INCLUDE[prod_short](includes/prod_short.md)] till de format som krävs av över 600 banker runt om i världen. Det gör det till exempel enklare att överföra betalningar och krediter till leverantörer genom att registrera betalningarna i [!INCLUDE[prod_short](includes/prod_short.md)] och sedan överföra dem till din bank. Formaten kan också göra bankavstämningsprocesser smidigare. Mer information finns i [AMC Banking för Microsoft Dynamics 365 Business Central](https://www.amcbanking.com/bc-fundamentals/)

> [!Note]
> AMC Banking har skapat ytterligare tillägg som fungerar med [!INCLUDE[prod_short](includes/prod_short.md)]. I det här avsnittet beskrivs endast Fundamental-tillägget.

> [!NOTE]
> I den generiska versionen av [!INCLUDE[prod_short](includes/prod_short.md)], ställs en global tjänstleverantör in och ansluts för att konvertera bankdata till valfritt filformat som din bank kräver. I Nordamerikanska versioner kan samma service användas för att skicka betalningsfiler som EFT (Elektronisk överföring), t.ex. det ACH-nätverk som ofta används, men med en något annorlunda metod.

## <a name="use-our-demonstration-account"></a>Använda vårt demonstrationskonto
[!INCLUDE[prod_short](includes/prod_short.md)] har ett demonstrationskonto som du kan använda för att testa tillägget AMC Banking 365 Fundamentals. Vi tillhandahåller standardinställningar för anslutning till AMC Banking och anger vilka bankkonton som data hämtas från i [!INCLUDE[prod_short](includes/prod_short.md)], plus några datautbytesdefinitioner. Du kan visa anslutningsinställningarna på sidan **Konfiguration av AMC Banking**. För bankkonton använder tillägget värden i fälten **Banknamn**, **Nr-serie för kredittrans.med.**, **Format för bankutdragsimport** och **Format för betalningsexport** på bankkontokort.

Vi tillhandahåller inställningarna, men om du vill testa tillägget måste du köra guiden för assisterad konfiguration för att använda dem. Om du vill köra guiden väljer du på sidan **Konfiguration av AMC Banking** åtgärden **Assisterad konfiguration**.

> [!Note]
> Det finns vissa begränsningar för demokontot. När du t. ex. konverterar betalningar kommer inte beloppet i den konverterade filen att matcha det faktiska beloppet. I stället är beloppet alltid fem enheter av den valuta som du använder för betalningar.  

## <a name="setting-up-the-extension"></a>Konfigurera tillägget
Att komma igång med tillägget består bara av några enkla steg, och en guide för assisterad konfiguration kommer att upprätta anslutningen och slå på tillägget. Guiden kommer att göra sådant som att installera datautbytesdefinitioner för bankutdrag, inställningar för export/import och initiera den nummerserie som används för kreditöverföringsmeddelanden.  

### <a name="to-set-up-the-required-permission-sets"></a>Ange de behörighetsuppsättningar som krävs
Innan användarna kan använda det här tillägget måste administratören kopiera följande behörighetsuppsättningar, redigera dem och sedan tilldela de nya behörighetsuppsättningarna till användare i stället för de ursprungliga:

* **D365 Basic**
* **D365 Team Member**
* **D365 Read**
* **IntelligentCloudBC**

Mer information finns i avsnittet [Kopiera en behörighetsuppsättning](ui-define-granular-permissions.md#to-copy-a-permission-set).

För varje ny behörighetsuppsättningar beviljar du bara **Läs**-behörighet för **AMC Banking-inställningar (20101)**. Mer information finns i avsnittet [Skapa eller ändra behörigheter manuellt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-connect-the-extension-to-amc-banking"></a>Ansluta tillägget till AMC Banking
1. Hämta en modul och en tjänstplan för AMC Banking. Om du vill göra det går du till sidan [AMC-licens](https://license.amcbanking.com/register).
2. I [!INCLUDE[prod_short](includes/prod_short.md)] välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **AMC Banking inställningar** och väljer sedan relaterad länk.  
3. På sidan **Konfiguration av AMC Banking** väljer du åtgärden **Assisterad konfiguration**.
4. Följ instruktionerna i assisterad konfiguration.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Koppla bankkonton till tillägget
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bankkonton** och väljer sedan relaterad länk.
2. Öppna kortet för det bankkonto som du vill koppla till tjänsten.
3. I fältet **Banknamn** väljer du det format som din bank kräver.  

   Formaten är filtrerade så att endast de som är relevanta för det land/den region som har angetts för bankkontot visas.
4. I fältet **Nr-serie för kredittrans.med.** väljer du nummerserien som ska användas för meddelanden som medföljer betalningar.
5. I fälten **Format för bankutdragsimport** och **Format för betalningsexport** väljer du de datautbytesdefinitioner som din bank kräver.

## <a name="use-the-extension"></a>Använda tillägget 
När du använder det här tillägget kan du bara exportera data på **Utbetalningsjournaler** och sedan överföra dem till din banks webbtjänst. Mer information finns i [Göra betalningar med bankdatakonvertering eller SEPA-kreditöverföring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!Note]
> Du måste fylla i fälten **SWIFT-kod** och **IBAN** för varje bankkonto.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Exportera data och skicka dem till din bank
> [!CAUTION]  
>  När du exporterar data med hjälp av tillägget AMC Banking 365 Fundamentals kommer vissa av dina affärsdata att bli exponerade för tjänstleverantören. Serviceleverantören, AMC Consult A/S, är ansvarig för sekretessen för dessa data. Mer information finns i [Sekretesspolicy för AMC](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Betalningsjournaler** och väljer sedan relaterad länk.
2. Skapa de journalrader som du vill exportera.  

   > [!Note]
   > Kom ihåg att välja **Elektronisk betalning** i fältet **Bankbetalningstyp** för varje rad.
3. Välj åtgärden **Exportera**.

### <a name="to-import-and-apply-the-converted-file"></a>Importera och använda den konverterade filen
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **betalningsavstämningsjournal** och väljer sedan relaterad länk.
2. Välj åtgärden **Importera banktransaktion** och välj sedan den konverterade filen.  

   [!INCLUDE[prod_short](includes/prod_short.md)] skapar en ny betalningsavstämningsjournal som innehåller data som finns i filen. Mer information finns i [Koppla betalningar automatiskt och stäm av bankkonton](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Se även
[Anpassa [!INCLUDE[prod_short](includes/prod_short.md)] med tillägg](ui-extensions.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]