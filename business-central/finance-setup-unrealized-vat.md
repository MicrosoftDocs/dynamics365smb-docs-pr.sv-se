---
title: Ställa in icke-realiserad moms
description: Om du använder kontantbaserad redovisning kan ange du hur du vill hantera orealiserad moms för försäljning och inköp.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'cash, VAT, unrealized, cash-based'
ms.search.form: '118, 472, 473'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Ställa in orealiserad moms för kontantbaserad redovisning

Om du använder kontantbaserade redovisningsmetoder kan du skapa [!INCLUDE[prod_short](includes/prod_short.md)] för att hantera orealiserad moms.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Använda redovisningskonton för orealiserad moms

Du kan ange att momsbelopp ska beräknas och bokföras på ett temporärt redovisningskonto när en faktura bokförs, för att sedan bokföras på rätt redovisningskonto och inkluderas i momsrapporter när den faktiska betalningen av fakturan bokförs. Innan du kan göra detta måste du slutföra [bokföringsinställningarna för moms](finance-setup-vat.md).

Om du vill använda konton för orealiserad moms, gör du så här:

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **inställningar för redovisning**.
2. På sidan **Redovisningsinställningar**, välj kryssrutan **Orealiserad moms**.
3. Välj ikonen **Sök efter sida eller rapport** ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") och ange **Bokföringsinställning för moms**.
4. På sidan **Bokföringsinställningar för moms** väljer du moms och väljer sedan åtgärden **redigera**.
5. I fältet **Orealiserad momstyp** väljer du ett alternativ för att ange hur du ska fördela betalningar till fakturabeloppet (exklusive moms) och själva momsbeloppet, samt hur momsbeloppen överförs från kontot för orealiserad moms till konto för (realiserad) moms. Alternativen beskrivs i tabellen nedan.

| Alternativ | Beskrivning |
| --- | --- |
| Tomt | Välj det här alternativet om du inte vill använda funktionen för orealiserad moms. |
| Procent | Betalningar täcker både moms och fakturabelopp i proportion till betalningens procent av det återstående fakturabeloppet. Det betalda momsbeloppet överförs från kontot för orealiserad moms till realiserade momskontot. |
| Första | Betalningar täcker först momsbeloppet och sedan fakturabeloppet. I det här fallet kommer det belopp som överförs från kontot för orealiserad moms att vara lika med betalningsbeloppet tills den totala momsen har betalts. |
| Sista | Betalningar täcker först fakturabeloppet och sedan momsen. I det här fallet kommer inget belopp att överföras från kontot för orealiserad moms till momskontot förrän fakturans totala belopp, exklusive moms, har betalts. |
| Först (hela beloppet) | Betalningar täcker först momsen (som i alternativet _Först_), men inget belopp överförs till momskontot förrän hela momsbeloppet har betalats. |
| Sist (hela beloppet) | Betalningar täcker först fakturabeloppet (som i alternativet _Sist_), men inget belopp överförs till momskontot förrän hela momsbeloppet har betalats. |

6. I fältet **Oreal. utgående moms** anger du kontot för orealiserad utgående moms.

    > [!NOTE]  
    > Momsbeloppet kommer att bokföras till kontot för orealiserad moms där det kvarstår tills betalningen till leverantören bokförts. Beloppet överförs sedan till kontot för utgående moms.
7. Ange redovisningskontot för orealiserad ingående moms i fältet **Oreal. ingående moms**.

> [!NOTE]  
> Momsbeloppet kommer att bokföras till kontot för orealiserad moms där det kvarstår tills betalningen till leverantören bokförts. Beloppet överförs sedan till kontot för ingående moms.

## <a name="see-also"></a>Se även
[Konfigurera beräknings- och bokföringsmetoder för moms](finance-setup-vat.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
