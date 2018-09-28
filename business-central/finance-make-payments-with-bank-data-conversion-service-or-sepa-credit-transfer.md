---
title: "Gör betalningar med tjänsten för bankdatakonvertering eller SEPA Kreditöverföring | Microsoft Docs"
description: "Behandla betalningar till dina leverantörer genom att exportera en fil tillsammans med betalningsinformation från på journalraderna."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 99277cb2daf37fbce4548cf637e8967fa6688dbc
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a>Göra betalningar med tjänsten för bankdatakonvertering eller SEPA-kreditöverföring
I fönstret **Betalningsjournal** kan du behandla betalningar till dina leverantörer genom att exportera en fil tillsammans med betalningsinformation från på journalraderna. Du kan sedan överföra filen till den elektroniska banken där relaterade pengaöverföringar bearbetas. [!INCLUDE[d365fin](includes/d365fin_md.md)] stödjer SEPA kreditöverföringar-format, men andra format för elektroniska betalningar i ditt land/din region kan finnas.   

 Om du vill aktivera SEPA-kreditöverföringar måste du först lägga upp ett bankkonto, en leverantör och redovisningsjournalen som utbetalningsjournalen baseras på. Sedan förbereder du betalningar till leverantörer genom att automatiskt fylla i fönstret **Betalningsjournal** med förfallna betalningar med angivna bokföringsdatum.  

> [!NOTE]  
>  När du har verifierat att betalningarna har behandlats korrekt av banken kan du fortsätta att bokföra utbetalningsjournalraderna.  

 I följande tabell beskrivs en serie uppgifter, med länkar till de avsnitt där de beskrivs.   

|**Om du vill**|**Gå till**|  
|------------|-------------|  
|Aktivera funktionen för bankdatakonvertering om du vill få en eventuell bankutdragsfil konverterad till ett format som du kan importera eller få dina exporterad betalningfiler konverterade till det format som din bank kräver.|[Ställa in konverteringstjänsten för bankdata](bank-how-setup-bank-statement-service.md)|  
|Skapa ett bankkonto, en leverantör och en utbetalningsjournal för SEPA-kreditöverföring.|[Konfigurera SEPA-kreditöverföring](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Fyll i betalningsjournalen med rader för förfallna betalningar till leverantörer, med alternativet att infoga bokföringsdatum som baseras på förfallodatumet för de relaterade inköpsdokumenten.|[Hantera Leverantörsreskontra](payables-manage-payables.md)|  
|Exportera utbetalningsjournalraderna till en fil i formatet SEPA Krediteringsöverföring.|[Exportera betalningar till en bankfil](payables-how-export-payments-bank-file.md)|  
|Bokför betalningarna när den elektroniska betalningen har behandlats utan problem av banken.|[Arbeta med redovisningsjournaler](ui-work-general-journals.md)|  

## <a name="see-also"></a>Se även  
[Ställa in konverteringstjänsten för bankdata](bank-how-setup-bank-statement-service.md)  
[Konfigurera SEPA-kreditöverföring](finance-how-to-set-up-sepa-credit-transfer.md)  
[Hantera Leverantörsreskontra](payables-manage-payables.md)   
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Samla in betalningar med SEPA-autogiro](finance-collect-payments-with-sepa-direct-debit.md)   

