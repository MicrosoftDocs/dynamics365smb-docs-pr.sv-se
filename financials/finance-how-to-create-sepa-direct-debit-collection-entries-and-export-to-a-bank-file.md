---
title: "Insamling för SEPA Autogiro | Microsoft Docs"
description: "Skapa insamling av autogiro och exportera till en XML som du skickar eller laddar upp till din elektroniska bank för bearbetning."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct-debit, collection, payment, sepa
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: ff6fc3af28273545781fc96b811f3c164eaa6fd8
ms.contentlocale: sv-se
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Så här skapar du insamlingsposter för SEPA Autogiro och exporterar till en bankfil
För instruktioner till banken för att överföra betalningsbeloppet från kundens bankkonto till ditt företags konto, skapa en autogiroinsamling som innehåller information om kundens bankkonto, de berörda försäljningsfakturorna och medgivande för autogiro. Från direktdebitering-insamlingsposten som skapas kan du sedan exportera en XML-fil som du skickar eller överför till din elektroniska bank för bearbetning. Alla betalningar som inte kunde behandlas av banken meddelas till dig av din bank och du måste sedan manuellt avvisa de aktuella autogiroinsamlingsposterna.  

> [!NOTE]  
>  För att samla in betalningar med hjälp av SEPA Autogiro måste valutan på försäljningsfakturan vara EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Skapa en direktdebitering-insamling  
1. Välj ikonen ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "ikonen Sök efter sidan eller rapporten"), ange **Autogiroinsamlingar**, och välj sedan relaterad länk.  
2. I fönstret **Samlingar med autogiro** i fönstret **Start** i gruppen **Ny** väljer du **Skapa autogiroinsamling**.  
3. I fönstret **Skapa samling med autogiro** fyller du i fälten enligt instruktionerna i följande tabell.  

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

     En autogiroinsamling läggs till i fönstret **Autogiroinsamlingar** och en eller flera autogiroinsamlingsposter skapas.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Så här exporterar du direktdebeterings-insamlingposter till en bankfil  
1. I fönstret **Samlingar med autogiro** i fönstret **Start** i gruppen **Process** väljer du **Transaktioner för samlingar med autogiro**.  
2. Fönstret **Transaktioner för samlingar med autogiro**-fönster, markera den post som du vill exportera och sedan på fliken **Start** i gruppen **Process** väljer du **Skapa autogirofil**.  
3. Spara exportfilen på den plats från vilken du skickar eller överför den till din elektroniska bank.  

     I fönstret **Transaktioner för samlingar med autogiro** kan fältet **Status för autogirosamling** ändras till fil. I fönstret **SEPA Autogiromedgivanden** kan fältet **Debet antal** uppdateras fältet med ett antal.  

Om den exporterade filen inte kan behandlas, till exempel eftersom kunden är insolvent, kan du avvisa direktdebitering-insamlingsposten. Om den exporterade filen har bearbetats av banken, samlas automatiskt förfallna betalningar på de berörda försäljningsfakturorna från berörda kunder. I så fall kan du stänga samlingen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Avvisa en direktdebitering-insamlingspost  
* I fönstret **Transaktioner för samlingar med autogiro**-fönster, markera den post som inte behandlades korrekt, och sedan på **Start** i gruppen **Process** och välj **Avvisa transaktionen**.  

     Värdet **Status** i **Transaktioner för samlingar med autogiro** ändras till **Avvisad**.  

### <a name="to-close-a-direct-debit-collection"></a>Stänga en direktdebitering-insamling  
* I fönstret **Transaktioner för samlingar med autogiro**-fönster, markera den post som inte behandlades korrekt, och sedan på **Start** i gruppen **Process** och välj **Stäng samling**.  

     Relaterade direktdebitering-insamlingen är stängd.  

Du kan nu fortsätta med att bokföra inleveranser för de berörda försäljningsfakturorna. Du kan göra detta om du ofta bokför betalningsinleveranser, som i fönstret **Betalningsregistrering** eller du kan bokföra de relaterade betalningsinleveranser direkt från **Transaktioner för samlingar med autogiro**. Mer information finns i [så här: Bokför betalningsinleveranser för SEPA Autogiro](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Se även  
[Så här: Konfigurera SEPA Autogiro](finance-how-to-set-up-sepa-direct-debit.md)   
[Så här bokför du betalningsinleveranser för SEPA Autogiro](finance-how-to-post-sepa-direct-debit-payment-receipts.md)   
[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)   

