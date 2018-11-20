---
title: "Ställ in SEPA Autogiro | Microsoft Docs"
description: "Lär dig hur du ställer in SEPA-autogirering i Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0ba40eb247c1edb2b4d8c7437bf60790545799ee
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-direct-debit"></a>Konfigurera SEPA Autogiro
Från fönstret **Samlingar med autogiro** kan du exportera instruktioner till din Internetbank för autogirobetalning från kundens bankkonto till ditt bankkonto. [!INCLUDE[d365fin](includes/d365fin_md.md)] stödjer SEPA Autogiro-format, men andra format för elektroniska betalningar i ditt land/din region kan finnas.  

Om du vill aktivera export av bankfilformat som inte stöds från början i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du konfigurera en datautbytesdefinition med ramverket för datautbyte. Mer information finns i [Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Innan du kan bearbeta kundbetalningar på elektronisk väg genom att exportera instruktioner om autogiro i formatet SEPA-autogiro måste du utföra följande inställningssteg:  

* Ställ in exportformat för bankfilen som används av din bank för att utföra en autogiroinsamling från kundens bankkonto till ditt bankkonto.  
* Ställ in kundens betalningsmetod.  
* Ställ in medgivande för autogiro att återspegla ditt avtal med kunden för att samla in sina betalningar under en viss avtalsperiod.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Så här ställer du in ditt bankkonto för SEPA-autogiro  
1. I rutan **Sök**, ange **Bankkonton** och välj sedan relaterad länk.  
2. Öppna det bankkonto som du vill använda för autogiro.  
3. På snabbfliken **Överföring**, i fältet **Exp.format för SEPA-autogiro**, välj alternativet för SEPA-autogiro.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Ange kundens betalningsmetod för SEPA-autogiro  
1. I rutan **Sök**, ange **Betalningssätt** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Så här anger du betalningssätt. Fyll i de specifika fälten för autogiro enligt beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Autogiro**|Ange om betalningsmetoden används för SEPA-autogiroinsamling.|  
    |**Betalningsvillkorskod för autogiro**|Ange betalningsvillkor, till exempel Betala inte, som visas på försäljningsfakturor som betalas med SEPA-autogiro för att visa kunden att betalningen kommer att samlas in automatiskt. Du kan även lämna fältet tomt.|  

    > [!NOTE]  
    >  Ange inte ett värde i fältet **Motkonto.**  

4. Välj **OK** för att stänga fönstret **Betalningssätt**.  
5. I rutan **Sök**, ange **Kunder** och välj sedan relaterad länk.  
6. Öppna kortet för den kund som du vill ställa in för SEPA-autogiroinsamling.  
7. Välj **Betalningssätt**-fältet och välj sedan koden för betalningssätt som du angav i steg 3.  
8. Upprepa steg 6 till och med 7 för alla kunder som du vill ställa in för SEPA-autogiroinsamling.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Så här ställer du in medgivande för autogiro som representerar kundavtalet  
1. I rutan **Sök**, ange **Kunder** och välj sedan relaterad länk.  
2. Öppna kortet för den kund som du vill ställa in för SEPA-autogiro.  
3. Välj åtgärden **bankkonton**.  
4. I **Kund bankkontolista**-fönstret väljer du det kundbankkonto som använder autogiro och väljer sedan, på fliken **Hem** i gruppen **Process**, **Medgivande av autogiro**.  
5. I fönstret **SEPA Autogiromedgivanden** fyller du i fälten enligt instruktionerna i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Kund bankkontokod**|Anger det bankkonto som direktdebiteringsbetalningar samlas in från. Detta fält fylls i automatiskt.|  
    |**Giltig från**|Ange det datum när medgivande för autogiro startar.|  
    |**Giltig till**|Ange det datum när medgivande för autogiro upphör.|  
    |**Signeringsdatum**|Ange det datum när kunden signerade medgivande för autogiro.|  
    |**Typ av betalning**|Ange om avtalet omfattar flera (**återkommande**) eller en enda (**Enstaka**) autogiroinsamling.|  
    |**Förväntat antal debet**|Ange hur många autogiroinsamlingar som du förväntar dig att göra. Det här fältet gäller bara om du har valt **Återkommande** i fältet **Typ av betalning**.|  
    |**Antal debet**|Anger hur många autogiroinsamlingar som har gjorts med hjälp av medgivande av autogiro. Fältet uppdateras automatiskt.|  
    |**Spärrad**|Anger att autogiroinsamlingar inte kan göras med hjälp av medgivande av autogiro.|  

6.  Upprepa steg 1 till och med 5 för alla kunder som du vill ställa in för SEPA-autogiro.  

 Medgivande för autogiro infogas automatiskt i fältet **Medgivande-ID för autogiro** när du skapar en försäljningsfaktura för den kund som du valde i steg 2. Mer information finns i [Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Se även  
[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)  
[Så här konfigurerar du dataintegrationsdefinitioner](across-how-to-set-up-data-exchange-definitions.md)
[Så här skapar du återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md)
[Elektroniskt datautbyte](across-data-exchange.md)

