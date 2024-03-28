---
title: Betalningsförslag för lev.
description: Använd batchjobbet Föreslå leverantörsbetalningar för att skapa betalningsrader för dina leverantörer baserat på förfallodatum och betalningsrabatter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 12/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="suggest-vendor-payments"></a>Betalningsförslag för lev.

På sidan **Betalningsjournal** kan du använda batch-jobbet **Föreslå leverantörsbetalning** för att föreslå betalningsrader. Baserat på dina inställningar, föreslår [!INCLUDE [prod_short](includes/prod_short.md)] rader:

- Betalningar som snart förfaller.
- Betalningar där en kassarabatt är tillgänglig.

För att dra full nytta av betalningsförslagen, måste du prioritera leverantörerna. Mer information om hur du prioriterar leverantörer finns i [Prioritera leverantörer](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Batch-jobbet exkluderar leverantörsreskontraposterna är **Stoppad** eller som redan har kopplats och som har ett värde i fältet **Koppla till ID**.  

> [!IMPORTANT]  
> Om du vill utnyttja kassarabatterna och har angett ett disponibelt belopp, används beloppet för:  
>
> * Prioritera förfallna leverantörstransaktioner först efter prioritet.
> * Förfallna leverantörstransaktioner som inte prioriterats.  
> * Öppna leverantörstransaktioner som är berättigade till kassarabatter. Transaktionerna är ordnade efter leverantörsnummer.  

## <a name="use-the-suggest-vendor-payments-action"></a>Använd åtgärden Betalningsförslag

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Betalningsjournaler** och väljer sedan relaterad länk.  
2. Öppna journalen och välj sedan åtgärden **Betalningsförslag för lev.**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Välj knappen **OK**.  

## <a name="insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Infoga förfallodatum som bokföringsdatum på betalningsjournalrader

När du använder **Betalningsförslag för lev.**-batchjobbet för att skapa betalningsrader för leverantörer, kan du fylla två specialfält så att de genererade raderna använder förfallodatumet för att beräkna bokföringsdatumet. Dessa fält är **Beräkna bokföringsdatum från dokumentets förfallodatum** och **Dokumentets förfallodatum är förskjutet**.  

> [!IMPORTANT]  
> Du kan inte använda fältet **Beräkna bokföringsdatum från dokumentets förfallodatum** tillsammans med fältet **Utnyttja kassarabatter** eller fältet **Summering per leverantör**. Om bokföringsdatumet baseras på förfallodatum, så kan vissa kassarabatter kanske inte beräknas korrekt eftersom bokföringsdatumet är efter kassarabattdatumet.  

Dessutom, om det beräknade bokföringsdatum inträffar tidigare flyttas bokföringsdatumet fram till arbetsdatumet, och en varning visas.  

Du kan även skapa betalningsrader manuellt genom att använda förfallodatum för att beräkna bokföringsdatum. När du har installerat leverantörsreskontratransaktioner kan du använda åtgärden **beräkna bokföringsdatum** för att uppdatera bokföringsdatumet på journalraden med förfallodatumet för relaterad inköpsfaktura. Mer information om den här manuella processen finns i [Koppla inköpstransaktioner manuellt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Om inköpsfakturan har förfallit kommer bokföringsdatum att anges till arbetsdatumet, och teckensnittet på raden ändras till röd färg.  

## <a name="see-also"></a>Se även

- [Hantera Leverantörsreskontra](payables-manage-payables.md)  
- [Göra betalningar](payables-make-payments.md)  
- [Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
- [Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
