---
title: Behandla inkommande och utgående koncerninterna transaktioner | Microsoft Docs
description: Koncerninterna transaktioner som du tar emot från dina koncerninterna partner visas i den koncerninterna inkorgen där du behandlar dem manuellt eller automatiskt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: c7bf0c1c22d2f43220d9b101a1a54757add900e9
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/19/2019
ms.locfileid: "853287"
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Hantera koncerninterna in- och utkorgar
Alla koncerninterna transaktioner som du tar emot elektroniskt från dina koncerninterna partner visas i den koncerninterna inkorgen.  

## <a name="organizing-the-inbox"></a>Ordna inkorgen  
 Du kan använda filterfälten överst i inkorgen när du vill fastställa vilka transaktioner som ska visas på sidan. Du kan till exempel ange filter för transaktionskälla och konc.int. partnerkod om du endast vill visa de transaktioner som en viss partner har skapat i filtren **transaktionskälla** och **Kod för koncernintern partner**.  

### <a name="transaction-source"></a>Transaktionskälla  
Vad du kan göra med en transaktion beror på om den har:  

- skapats av en koncernintern partner  
- avvisats av den koncerninterna partnern och returnerats till dig  

Du kan använda fältet **Visa transaktionskälla** om du vill filtrera sidan **Koncerninterna inkorgstransaktioner** så att endast dessa typer av transaktioner visas. (Du kan även filtrera efter koncerninterna partner eller efter innehållet i fältet **Radåtgärd**.)  

#### <a name="created-by-intercompany-partner"></a>Skapats av en koncernintern partner  
 När du får en ny transaktion som har skapats av din partner kan du välja att:

- Acceptera transaktionen  
- Avvisa transaktionen (returnera den till partnern)  
- Avbryta transaktionen (ta bort transaktionen utan att returnera den till partnern)  

#### <a name="returned-from-intercompany-partner"></a>Returnerad från koncernintern partner  
 Om transaktionen har avvisats av den koncerninterna partnern är ditt enda alternativ att avbryta transaktionen i inkorgen. Du måste därefter skapa korrigeringsrader eller återföra journalen eller dokumentet i företaget.  

## <a name="recreating-inbox-entries"></a>Återskapa poster i inkorgen  
 Om du har accepterat en transaktion i inkorgen men därefter tagit bort dokumentet eller journalen i stället för att bokföra den kan du återskapa posten i inkorgen och acceptera den på nytt.  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a>Skaffa en översikt över koncerninterna transaktioner för en period  
 Du kan skapa en översikt över alla koncerninterna transaktioner som du har skickat och tagit emot under en period. I rapporten **Konc.int. transaktioner** visas alla koncerninterna redovisningstransaktioner, kundreskontratransaktioner och leverantörsreskontratransaktioner.

 > [!NOTE]  
 > Om den koncerninterna partnern finns i samma databas, överför transaktionerna utan behov av fil eller e-post. Visa fältet **Överföringstyp** på sidan **koncerninterna partner**. <br /><br />
I så fall kan du konfigurera systemet till att åsidosätta Inkorgen och Utkorgen genom att markera kryssrutan **automatiskt acceptera transaktioner** på sidan **koncerninterna partner** och markera kryssrutan **automatiskt skicka transaktioner** på sidan **koncerninterna inställningar**.

## <a name="to-import-intercompany-transactions-from-a-file"></a>Så här importerar du koncerninterna transaktioner från en fil:  
Om du har en koncernintern partner som inte finns i samma databas som ditt företag kan du ta emot koncerninterna transaktioner från den partnern i en XML-fil. Därefter måste du importera transaktionerna till inkorgen.  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Företagsinformation** och välj sedan relaterad länk.
2. Spara filen på den plats som du har angett i fältet **Konc.int. inkorgsinformation** på sidan **Företagsinformation**.  
3. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Koncerninterna inkorgstransaktioner** och välj sedan relaterad länk.
4. På sidan **koncerninterna inkorgstransaktioner** väljer du åtgärden **Importera transaktionsfil**.  
5. På sidan som visas markerar du XML-filen med transaktionerna och sedan väljer du **Öppna**.  

Transaktionerna importeras till inkorgen där du kan bearbeta dem.

## <a name="to-process-incoming-intercompany-transactions"></a>Så här hanterar du inkommande koncerninterna transaktioner:  
När koncerninterna partner skickar koncerninterna transaktioner hamnar de i den koncerninterna inkorgen. Du måste utvärdera varje transaktion i inkorgen och välja lämplig åtgärd.  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Koncerninterna inkorgstransaktioner** och välj sedan relaterad länk.  
2. På sidan **koncerninterna inkorgstransaktioner** markerar du en rad, och väljer sedan en åtgärd som **acceptera** för att bearbeta raden.
3. På sidan **Slutför konc.int. inkorgsåtg.** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj knappen **OK**.  

Rader som du har behandlats med åtgärden**acceptera** kommer dokument eller journalrader att skapas i företaget. Öppna varje dokument eller journal, gör nödvändiga ändringar och bokför.  

Rader som du har behandlats med åtgärden **returnera till partner** ska flyttas till utkorgen från där du kan sedan skicka dem till partnern.

För rader som du behandlade med åtgärden **Returnerad av partner** bokför du en korrigering av den ursprungliga transaktionen som du har bokfört i företaget.

## <a name="to-process-outgoing-intercompany-transactions"></a>Så här hanterar du utgående koncerninterna transaktioner  
När du bokför en koncernintern journal eller ett koncerninternt dokument, eller när du skickar en koncernintern orderbekräftelse, skickas transaktionerna till den koncerninterna utkorgen. Du måste öppna utkorgen och bearbeta dem för att de ska skickas till dina koncerninterna partner.  

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Koncerninterna utkorgstransaktioner** och välj sedan relaterad länk.  
2. På sidan **koncerninterna utkorgstransaktioner** markerar du en rad, och väljer sedan en åtgärd som **Returnera till inkorgen** för att bearbeta raden.

Rader som du har behandlats med åtgärden **skickas till en koncernintern partner** kommer att skickas till lämplig partners inkorg.

Rader som du har behandlat med åtgärden **returnera till inkorgen** kommer att flyttas till inkorgen där du kan acceptera dem för att skapa dokument- eller journalrader i företaget.  

För rader som du behandlade med åtgärden **Avbryt** bokför du en korrigering av den ursprungliga transaktionen som du har bokfört i företaget.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Så här  återskapar du koncerninterna inkorgstransaktioner  
Ibland kan du behöva återskapa en transaktion i inkorgen eller utkorgen. Om du till exempel har accepterat en transaktion i inkorgen men sedan tagit bort dokumentet eller journalen i stället för att bokföra den, kan du återskapa posten i inkorgen och acceptera den på nytt.  

Den här proceduren beskriver hur du återskapar inkorgstransaktioner, men det fungerar på samma sätt i utkorgen.

  1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Hanterade konc.int. inkorgstransaktioner** och välj sedan relaterad länk.  

  2.  På sidan **Hanterade konc.int. inkorgstransaktioner** markerar du raden med den transaktion som du vill återskapa i inkorgen och väljer sedan åtgärden **Återskapa inkorgstransaktion**.  

## <a name="see-also"></a>Se även
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
