---
title: Kräva in utestående saldon
description: Lära dig hur du kan påminna kunder om utestående betalningar. Skicka ett kundkontoutdrag, skicka ut en betalningspåminnelse eller skicka en räntefaktura.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 02/09/2022
ms.author: edupont
ms.openlocfilehash: fe9dc2ed31244bbca601d90397dc813085817eb1
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144963"
---
# <a name="collect-outstanding-balances"></a>Kräva in utestående saldon

Betalningshanteringen består i att kontrollera om kunderna betalar i tid. Om kunderna har förfallna betalningar, kan du börja med att skicka **kundkontoutdragsrapporten** som betalningspåminnelse. Alternativt kan du skicka betalningspåminnelser.

Du kan använda betalningspåminnelser för att påminna kunder om förfallna belopp. Du kan även använda betalningspåminnelser för att beräkna ränta eller avgifter och inkludera dem i betalningspåminnelsen. Använd räntefakturor om du vill debitera kunder för ränta eller avgifter utan att påminna dem om förfallna belopp.

## <a name="statements"></a>Rapporter

Från kundkortet kan du skapa en rapport med den kundens transaktioner med dig. Sedan skickar du kunden till den genererade PDF-filen. Du kan också använda rapporten **Kundkontoutdrag** för att skicka kunderna en översikt över deras affärer med dig. Kundkontoutdraget kan skickas till Excel för vidare behandling.  

### <a name="to-send-the-customer-statement-report"></a>Om du vill skicka kundkontoutdragsrapporten.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 10.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kundkontoutdrag** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I **Utdataalternativ** väljer du hur rapporten ska skickas till kunden.

> [!NOTE]
> Om du använder flera valutor, skrivs kundkontoutdragsrapporten alltid ut i kundens valuta. Det sista datumet i en rapportperiod används även som meddelandedatumet och åldersfördelningdatumet, om åldern inkluderas.

## <a name="reminders"></a>Påminnelser

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## <a name="finance-charges"></a>Räntefakturor

Om en kund inte har betalat på förfallodatumet kan du låta beräkna dröjsmålsränta automatiskt och lägga på den på de förfallna beloppen på kundens konto. Du kan informera kunder om debiterade dröjsmålsräntor genom att skicka räntefakturor.  

> [!NOTE]  
> Du använder räntefakturor för att beräkna dröjsmålsränta och informera dina kunder om dröjsmålsräntor utan att påminna dem om förfallna betalningar. Ett alternativ är att du i stället beräknar ränta på förfallna betalningar när du skapar betalningspåminnelser.  

Innan du kan skapa räntefakturor måste du ange villkoren. Mer information finns i [Konfigurera räntevillkor](finance-setup-finance-charges.md).  

Du kan manuellt skapa en räntefaktura för en enskild kund och fylla i raderna automatiskt. Som Alternativt kan du använda funktionsjobbet **Skapa räntefakturor** för att skapa räntefakturor för alla eller valda kunder med förfallna betalningar.  

När du skapat räntefakturorna kan du ändra dem. Texten som visas i början och i slutet av räntefakturan bestäms av räntevillkoren och visas i kolumnen **Beskrivning** på raderna. Om ett beräknat belopp har infogats automatiskt i den inledande eller avslutande texten justeras inte texten om du tar bort rader. Då måste du använda funktionen **Uppdatera räntefakturatext**.  

När du har skapat räntefakturor och gjort eventuella ändringar kan du antingen skriva ut testrapporter eller skicka ut räntefakturorna, vanligtvis som e-post.

### <a name="to-create-a-finance-charge-memo-manually"></a>Så här skapar du en räntefaktura manuellt

En räntefaktura påminner om en vanlig faktura. Du kan fylla i ett huvud manuellt och ange att raderna ska fyllas i automatiskt, eller så kan du välja att automatiskt skapa räntefakturor för alla kunder.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 2.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Räntefakturor** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov.  
3. Välj åtgärden **Föreslå räntefakturarader**.
4. På sidan **Föreslå räntefakturaraderna** anger du ett filter på snabbfliken **Kundreskontratransaktion** om du bara vill skapa räntefakturor för särskilda transaktioner.

    > [!NOTE]
    > Även om de visas får filtren **Betalning** och **Kreditnot** som **Dokumenttyp** ingen effekt eftersom funktionen **Föreslå räntefakturaraderna** endast hanterar positiva belopp.
5.  Klicka på **OK** för att starta batchjobbet.  

### <a name="to-update-finance-charge-memo-texts"></a>Så här uppdaterar du räntefakturatexter  
I vissa fall kan det hända att du behöver ändra den inledande och avslutande text som angetts för räntevillkoren. Om du gör detta när du har skapat, men ännu inte skickat ut, räntefakturor kan du uppdatera fakturorna med den ändrade texten.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Räntefaktura** och väljer sedan relaterad länk.  
2. Öppna den räntefaktura som du vill ändra texten och välj sedan åtgärden **Uppdatera räntefakturatext**.
3. På sidan **Uppdatera räntefakturatext** kan du definiera ett filter om du vill uppdatera flera fakturor.
4. Klicka på **OK** om du vill uppdatera de inledande och avslutande texterna.  

### <a name="to-issue-finance-charge-memos"></a>Att utfärda räntefakturor
När du har skapat räntefakturor och gjort eventuella ändringar kan du antingen skriva ut testrapporter eller skicka ut räntefakturorna.

När en betalningspåminnelse skickas ut, bokförs transaktionerna enligt vad du angett på sidan **Räntevillkor**. Denna specifikation bestämmer om ränta och/eller extraavgifter ska bokföras på kundkontot och i redovisningen. Inställningen på sidan **Kundbokföringsmallar** bestämmer vilka konton som bokförs.

För varje kundreskontratransaktion på räntefakturan skapas en transaktion på sidan **Bet.påminnelse/räntetrans.**.

Om kryssrutorna **Bokför ränta** eller **Bokför avgift** är markerade på sidan **Räntevillkor** skapas även följande transaktioner:

- En transaktion på sidan **Leverantörsreskontratransaktion**.
- En kundfordringar-transaktion på relevant redovisningskonto
- En "ränte-" och/eller en "avgifts"-transaktion på relevant redovisningskonto

Dessutom kan utskickandet av räntefaktura resultera i momstransaktioner.

1. Välj den ![Glödlampa som öppnar funktionen Berätta 4.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Räntefakturor** och väljer sedan relaterad länk.
2. Välj relevant faktura och välj sedan åtgärden **Utskick**.
3. På sidan **Utskick räntefakturor** fyller du i fälten efter behov.
4. Välj **OK**.

Räntefakturan är avsedd att skickas ut till en angiven e-postadress som en bifogad PDF-fil.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>För att annullera utfärdad räntefaktura.
Om räntefakturor utfärdades felaktigt kan du avbryta dem innan de skickas ut. Det kan du göra antingen av en eller som en batch.
1. På sidan **Utfärdade räntefakturor**, välj en eller flera rader för utfärdade räntefakturor som du vill avbryta och välj sedan åtgärden **Avbryt**.
2. På sidan **Annullera utfärdade räntefakturor** fyller du i fälten efter behov och väljer sedan knappen **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Så här visar du betalningspåminnelse- och räntetransaktioner  
När du skickar ut en betalningspåminnelse skapas en betalningspåminnelsetransaktion på sidan **Bet.påminnelse/räntetrans.** för alla betalningspåminnelserader som innehåller en kundreskontratransaktion. Om du vill kan du visa en översikt över de betalningspåminnelsetransaktioner som skapats för en viss kund.    
1. Välj den ![Glödlampa som öppnar funktionen Berätta 5.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kunder** och väljer sedan relaterad länk.  
2. Öppna det relevanta kundkortet och välj sedan åtgärden **Transaktioner**.
3. På sidan **Kundreskontratransaktioner** markerar du raden med den transaktion som du vill visa betalningspåminnelsetransaktionerna för och väljer sedan åtgärden **Bet.påminnelse-/räntetrans.**.

## <a name="multiple-interest-rates"></a>Flera räntesatser

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Mer information finns i [Ställa in flera räntesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Konfigurera påminnelsevillkor och nivåer](finance-setup-reminders.md)  
[Konfigurera räntevillkor](finance-setup-finance-charges.md)  
[Hantera kundreskontra](receivables-manage-receivables.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]