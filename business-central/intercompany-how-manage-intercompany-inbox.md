---
title: Hantera koncerninterna in- och utkorgar
description: Koncerninterna transaktioner som du tar emot från dina koncerninterna partner visas i den koncerninterna inkorgen där du behandlar dem manuellt eller automatiskt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.search.form: 600, 605, 618, 650, 651, 648, 649, 617, 614, 642, 643, 640, 641, 613, 616, 646, 647, 644, 645, 615, 619, 612, 638, 639, 636, 637, 611
ms.date: 03/09/2022
ms.author: edupont
ms.openlocfilehash: 868f07b2b56ccaefb4c56e26be72c27b941d950c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522124"
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a>Hantera koncerninterna in- och utkorgar
Alla koncerninterna transaktioner som du tar emot elektroniskt från dina koncerninterna partner visas i den koncerninterna inkorgen.  

Beroende på hur koncerninterna aspekter har ställts in för ditt företag replikeras emellertid vissa transaktioner automatiskt till aktuella koncerninterna partners. Från och med 2022 års utgivningscykel 1 kan du också ställa in företaget för automatiskt skapande av mottagna koncerninterna transaktioner från koncerninterna partner, bokförda via den koncerninterna redovisningsjournalen. Mer information finns i [Fylla i och bokföra en koncernintern journal](intercompany-how-work-documents-journals.md#to-fill-in-and-post-an-intercompany-journal).  

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
I så fall kan du konfigurera systemet till att åsidosätta Inkorgen och Utkorgen genom att markera kryssrutan **automatiskt acceptera transaktioner** på sidan **koncerninterna partner** och markera kryssrutan **automatiskt skicka transaktioner** på sidan **koncerninterna inställningar**. Inkommande koncerninterna transaktioner kan endast accepteras automatiskt om Schemaläggaren är aktiverad. Mer information finns i [Konfigurera Business Central Server – Inställningar för Schemaläggaren](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Task).

## <a name="to-import-intercompany-transactions-from-a-file"></a>Så här importerar du koncerninterna transaktioner från en fil:

[!INCLUDE [onprem_only_md](includes/onprem_only_md.md)]

Om du har en koncernintern partner som inte finns i samma databas som ditt företag kan du ta emot koncerninterna transaktioner från den partnern i en XML-fil. Därefter måste du importera transaktionerna till inkorgen.  

1. Spara filen på den plats som du har angett i fältet **Koncerninterna detaljer för inkorg** när du konfigurerar koncerninterna aspekter.  
2. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **koncerninterna inkorgstransaktioner** och väljer sedan relaterad länk.
3. På sidan **koncerninterna inkorgstransaktioner** väljer du åtgärden **Importera transaktionsfil**.  
4. På sidan som visas markerar du XML-filen med transaktionerna och sedan väljer du **Öppna**.  

Transaktionerna importeras till inkorgen där du kan bearbeta dem.

## <a name="to-process-incoming-intercompany-transactions"></a>Så här hanterar du inkommande koncerninterna transaktioner:  
När koncerninterna partner skickar koncerninterna transaktioner hamnar de i den koncerninterna inkorgen. Du måste utvärdera varje transaktion i inkorgen och välja lämplig åtgärd.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **koncerninterna inkorgstransaktioner** och väljer sedan relaterad länk.  
2. På sidan **koncerninterna inkorgstransaktioner** markerar du en rad, och väljer sedan en åtgärd som **acceptera** för att bearbeta raden.
3. På sidan **Slutför konc.int. inkorgsåtg.** fyller du i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj knappen **OK**.  

Rader som du har behandlats med åtgärden **acceptera** kommer dokument eller journalrader att skapas i företaget. Öppna varje dokument eller journal, gör nödvändiga ändringar och bokför.  

Rader som du har behandlats med åtgärden **returnera till partner** ska flyttas till utkorgen från där du kan sedan skicka dem till partnern.

För rader som du behandlade med åtgärden **Returnerad av partner** bokför du en korrigering av den ursprungliga transaktionen som du har bokfört i företaget.

## <a name="to-process-outgoing-intercompany-transactions"></a>Så här hanterar du utgående koncerninterna transaktioner  
När du bokför en koncernintern journal eller ett koncerninternt dokument, eller när du skickar en koncernintern orderbekräftelse, skickas transaktionerna till den koncerninterna utkorgen. Du måste öppna utkorgen och bearbeta dem för att de ska skickas till dina koncerninterna partner.  

1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **koncerninterna utkorgstransaktioner** och väljer sedan relaterad länk.  
2. På sidan **koncerninterna utkorgstransaktioner** markerar du en rad, och väljer sedan en åtgärd som **Returnera till inkorgen** för att bearbeta raden.

Rader som du har behandlats med åtgärden **skickas till en koncernintern partner** kommer att skickas till lämplig partners inkorg.

Rader som du har behandlat med åtgärden **returnera till inkorgen** kommer att flyttas till inkorgen där du kan acceptera dem för att skapa dokument- eller journalrader i företaget.  

För rader som du behandlade med åtgärden **Avbryt** bokför du en korrigering av den ursprungliga transaktionen som du har bokfört i företaget.  

## <a name="to-recreate-intercompany-inbox-transactions"></a>Så här återskapar du koncerninterna inkorgstransaktioner  
Ibland kan du behöva återskapa en transaktion i inkorgen eller utkorgen. Om du till exempel har accepterat en transaktion i inkorgen men sedan tagit bort dokumentet eller journalen i stället för att bokföra den, kan du återskapa posten i inkorgen och acceptera den på nytt.  

Den här proceduren beskriver hur du återskapar inkorgstransaktioner, men det fungerar på samma sätt i utkorgen.

  1.  Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Hanterade konc.int. inkorgstransaktioner** och väljer sedan relaterad länk.  

  2.  På sidan **Hanterade konc.int. inkorgstransaktioner** markerar du raden med den transaktion som du vill återskapa i inkorgen och väljer sedan åtgärden **Återskapa inkorgstransaktion**.  

## <a name="see-also"></a>Se även
[Hantera koncerninterna transaktioner](intercompany-manage.md)  
[Ekonomi](finance.md)  
[Ställa in Finance](finance-setup-finance.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
