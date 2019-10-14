---
title: Exportera insamlingsposter för SEPA Autogiro | Microsoft Docs
description: Skapa en insamling för autogiro som innehåller information om kundens bankkonto och de berörda fakturorna och autogiromedgivandet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: c6a7231fa72e18a31a7971a333e9984aed7e5b8b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306346"
---
# <a name="create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Skapa insamlingsposter för SEPA Autogiro och exportera till en bankfil
För instruktioner till banken för att överföra betalningsbeloppet från kundens bankkonto till ditt företags konto, skapa en autogiroinsamling som innehåller information om kundens bankkonto, de berörda försäljningsfakturorna och medgivande för autogiro. Från direktdebitering-insamlingsposten som skapas kan du sedan exportera en XML-fil som du skickar eller överför till din elektroniska bank för bearbetning. Alla betalningar som inte kunde behandlas av banken meddelas till dig av din bank och du måste sedan manuellt avvisa de aktuella autogiroinsamlingsposterna.  

> [!NOTE]  
>  För att samla in betalningar med hjälp av SEPA Autogiro måste valutan på försäljningsfakturan vara EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Skapa en direktdebitering-insamling  

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Samlingar med autogiro** och välj sedan relaterad länk.  
2. På sidan **Samlingar med autogiro** på fliken **Start** i gruppen **Ny** väljer du **Skapa autogiroinsamling**.  
3. På sidan **Skapa samling med autogiro** fyller du i fälten enligt instruktionerna i följande tabell.  

    |Fält|Description|  
    |---------------------------------|---------------------------------------|  
    |**Från förfallodatum**|Ange tidigaste betalningsförfallodatumet på försäljningsfakturor som du vill skapa en direktdebitering-insamling för.|  
    |**Till förfallodatum**|Ange senaste betalningsförfallodatumet på försäljningsfakturor som du vill skapa en direktdebitering-insamling för.|  
    |**Partnertyp**|Anger om direktdebitering-insamlingen görs för kunder som är av typen **företag** eller **person**.|  
    |**Endast kunder med giltigt medgivande**|Ange om en autogiroinsamling skapas för kunder som har ett giltigt medgivande för autogiro. **Obs!**  En autogiroinsamling skapas även om fältet **Medgivande-ID för autogiro** inte fylls på försäljningsfakturan.|  
    |**Endast fakturor med giltigt medgivande**|Ange om en autogirering skapas för försäljningsfakturor endast om ett giltigt autogiromedgivande väljs i fältet **Medgivande-id för autogiro** på försäljningsfakturan.|  
    |**Bankkontonr.**|Ange vilka av företagets bankkonton som den insamlade betalningen ska överföras till från kundens bankkonto.|  
    |**Bankkontonamn**|Anger namnet på det bankkonto som du väljer i **Bankkontonr** fält. Detta fält fylls i automatiskt.|  

4. Välj knappen **OK**.  

     En autogiroinsamling läggs till på sidan **Autogiroinsamlingar** och en eller flera autogiroinsamlingsposter skapas.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Så här exporterar du direktdebeterings-insamlingposter till en bankfil  
1. På sidan **Samlingar med autogiro** i fönstret **Start** i gruppen **Process** väljer du **Transaktioner för samlingar med autogiro**.  
2. På sidan **Transaktioner för samlingar med autogiro**, markera den post som du vill exportera och sedan på fliken **Start** i gruppen **Process** väljer du **Skapa autogirofil**.  
3. Spara exportfilen på den plats från vilken du skickar eller överför den till din elektroniska bank.  

     På sidan **Transaktioner för samlingar med autogiro** kan fältet **Status för autogirosamling** ändras till fil. På sidan **SEPA Autogiromedgivanden** kan fältet **Debet antal** uppdateras fältet med ett antal.  

Om den exporterade filen inte kan behandlas, till exempel eftersom kunden är insolvent, kan du avvisa direktdebitering-insamlingsposten. Om den exporterade filen har bearbetats av banken, samlas automatiskt förfallna betalningar på de berörda försäljningsfakturorna från berörda kunder. I så fall kan du stänga samlingen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Avvisa en direktdebitering-insamlingspost  

* På sidan **Transaktioner för samlingar med autogiro**, markera den post som inte behandlades korrekt, och sedan på **Start** i gruppen **Process** och välj **Avvisa transaktionen**.  

     Värdet i fältet **Status** på sidan **Transaktioner för samlingar med autogiro** ändras till **Avvisad**.  

### <a name="to-close-a-direct-debit-collection"></a>Stänga en direktdebitering-insamling  
*  På sidan **Transaktioner för samlingar med autogiro**, markera den post som inte behandlades korrekt, och sedan på **Start** i gruppen **Process** och välj **Stäng samling**.  

     Relaterade direktdebitering-insamlingen är stängd.  

Du kan nu fortsätta med att bokföra inleveranser för de berörda försäljningsfakturorna. Du kan göra detta om du ofta bokför betalningsinleveranser, som på sidan **Betalningsregistrering** eller också kan du bokföra de relaterade betalningsinleveranser direkt från sidan **Transaktioner för samlingar med autogiro**. Mer information finns i [Bokför betalningsinleveranser för SEPA Autogiro](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Se även  
[Konfigurera SEPA autogiro](finance-how-to-set-up-sepa-direct-debit.md)  
[Så här bokför du betalningsinleveranser för SEPA Autogiro](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)  
