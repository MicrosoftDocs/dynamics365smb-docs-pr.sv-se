---
title: Hantera momsrapportering till skattemyndigheten | Microsoft Docs
description: "Lär dig hur du förbereder en rapport över moms från försäljning under en period och skickar rapporten till en skattemyndighet."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, tax, report, EC sales list, statement
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 9b0db56fc08881a94b1f80bafed32d7bcbc24fd8
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---

# <a name="how-to-report-vat-to-tax-authorities"></a>Så här: rapportera moms till skattemyndigheterna
Europeiska gemenskapens (EG) försäljningrappport listar de momsbelopp (VAT) som du har samlat in för försäljning inom EU, så att du kan skicka till en skattemyndighets webb.

> [!NOTE]  
>   I Storbritannien måste alla företag som säljer mer än ett visst värde årligen till kunder i EU-länder lämna in en elektronisk version av deras försäljning i Europeiska gemenskapen (EG) rapport i XML-format via webbplatserna Her Majesty's Revenue och Customs (HMRC).

EG-försäljningslisterapporten fungerar bara för länder inom EU. Det är till exempel exklusive moms på försäljning till länder som Kina och USA.

Om du vill rapportera moms till en skattemyndighet elektroniskt, måste du ansluta [!INCLUDE[d365fin](includes/d365fin_md.md)] till den skattemyndighetens webbplats. Detta kräver att du upprättar ett konto med skattemyndigheten. Om du har ett konto kan du aktivera en service-anslutning som finns i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Till exempel i Storbritannien Använd **GovTalk** service-anslutning.

Rapporten innehåller en rad för varje typ av transaktion med kunden och visar det totala beloppet för alla typer av transaktioner. Det finns tre olika typer av transacitons som kan ta med i rapporten:  
  
* B2B varor  
* B2B-tjänster  
* B2B triangulerade varor  
  
B2B varor och tjänster som anger om du köpt en vara eller tjänst, och är kontrollerade av inställningen **EU-tjänst** i momsbokföringen. B2B triangulerade varor anger om du bedriver handel med en 3:e part och är kontrollerad av inställningen **EU trepartshandel** för försäljningsdokument, till exempel försäljningsorder, fakturor, kreditnotor och så vidare.  
  
När du skickar rapporten, övervakar [!INCLUDE[d365fin](includes/d365fin_md.md)] tjänsten och håller reda på dina meddelanden. Fältet **Status** indikerar var rapporten finns i processen. Till exempel när myndigheterna bearbetar rapporten, ändras rapportens status till **lyckades**. Om fel hittas i rapporten som du har skickat in till skattemyndigheten visar status för rapporten **misslyckad**. Du kan visa fel under **fel och varningar**, rätta till dem och sedan skicka rapporten igen. Om du vill visa en lista över alla EG-försäljningslisterapporter, går du till sidan **EG försäljningsrapporter**.  
  
> [!NOTE]  
>   Om du använder en annan metod för att skicka rapporten, till exempel genom att exportera XML-data och överföra den till en skattemyndighetens webbplats, kan du välja **Välj som levererad** för att stänga perioden. När du markerar en momsrapport som släppt, går den inte längre att redigera. Om du måste ändra rapporten, när du har markerat den som släppt, måste du först öppna den på nytt. 
  
När skattemyndigheten granskar rapporten, skickar de ett e-postmeddelande till kontaktpersonen för ditt företag. I [!INCLUDE[d365fin](includes/d365fin_md.md)] anges kontaktpersonen på sidan **företagsinformation**. Kontrollera att du väljer en kontaktperson i tabellen innan du skickar rapporten.

<!--> [!NOTE]  
>   EG-försäljningslisterapporten kan innehålla upp till 1000 rader. Om du har fler rader måste du skicka en ny rapport. -->

## <a name="to-connect-to-your-tax-authoritys-web-service"></a>Ansluta till webbtjänsten för lokal skattemyndighet
[!INCLUDE[d365fin](includes/d365fin_md.md)] ger tjänstanslutningar som ansluter till skattemyndighetens webbplatser. Till exempel i Storbritannien måste du aktivera **GovTalk** service-anslutning.  

1. I fältet **Sök efter sidor och rapporter** anger du **Tjänstanslutningar**, och väljer sedan länken. <!-- remember to get the updated text for this-->  
2. Fyll i relevanta fält.  

## <a name="to-set-up-the-ec-sales-list-report"></a>Så här skapar du EG-försäljningsrapporten
1. I fältet **Sök efter sidor och rapporter** anger du **Konfigurera momsrapport**, och väljer sedan relaterad länk.  
2. Om du vill låta användarna ändra och skicka om rapporten, väljer du kryssrutan **ändra skickade rapporter**.  
3. Ange nummerserien som ska användas för EG-försäljningslisterapporter.  

## <a name="to-prepare-and-submit-the-ec-sales-list-report"></a>Förbereda och skicka EG-försäljningslisterapporter
1. I fältet **Sök efter sidor och rapporter** anger du **EC-försäljningslista**, och väljer sedan relaterad länk.  
2. Välj **Ny** och fyll sedan i relevanta fält.  
3. Om du vill generera innehållet i rapporten, väljer du åtgärden **Föreslå rader**.  

    > [!NOTE]  
>   Du kan granska transaktionerna i raden innan du skickar rapporten. Välj raden och välj sedan åtgärden **Visa momstransaktioner**.  
4. När du förbereder rapporten för att skicka den, välj åtgärden **Frisläpp**.  
5. Om du vill skicka rapporten, väljer du åtgärden **skicka**.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerar att rapporten har ställts in korrekt. Om valideringen misslyckas visas felen i **Fel och varningar** så att du kan göra lämpliga ändringar.

## <a name="viewing-communications-with-your-tax-authority"></a>Visa kommunikationen med skattemyndigheten.
I vissa länder skickar du meddelanden till skattemyndigheten när du skickar rapporter. Du kan visa första och det sista meddelandet som du skickat eller tagit emot genom att välja åtgärderna **hämta skickat meddelande** och **hämta svarsmeddelandet**.  

## <a name="configuring-your-own-vat-reports"></a>Skapa egna momsrapporter.
Du kan använda den EG-försäljningslisterapport men du kan också skapa egna rapporter. Detta innebär att du skapar några kodmoduler. Kontakta en Microsoft Partner om du behöver hjälp med.  
    
I följande tabell beskrivs de kodmoduler som måste skapas för rapporten.

| Kodmodul | Vad du måste göra |
|----|-----|
|Föreslå rader| Hämta information från tabellen momstransaktioner och visa dem i rader i momsrapporten.|
|Innehåll | Kontrollera formatet för rapporten. Till exempel om det är XML- eller JSON. Formaten som ska användas beror på kraven i din skattemyndighets webbtjänsten. |
|Överföring | Styra hur och när du skickar rapporten utifrån hänsyn till skattemyndigheterna. |
|Svarshanterare | Hantera returen från skattemyndigheten. Det kan till exempel skicka ett e-postmeddelande till företagets kontaktperson. |
|Annullera | Skicka en annullering av en momsrapport som har skickats tidigare till skattemyndigheterna. |

> [!NOTE]  
>   När du skapar kodmoduler för rapporten måste du ta hänsyn till värdet i fältet **momsrapportversion**. Det här fältet måste motsvara versionen av rapporten som är, eller var, krävd av skattemyndigheten. Du kan till exempel ange **2017** i kryssrutan för att ange att rapporten överensstämmer med de krav som gällde det året. Kontakta skattemyndigheterna för att få den senaste versionen.  

## <a name="see-also"></a>Se även
[Ställa in moms](finance-setup-vat.md)  
[Ställa in försäljning](sales-setup-sales.md)  
[Så här fakturerar du försäljning](sales-setup-sales.md)  

