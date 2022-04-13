---
title: Ställ in projekt, priser och projektbokföringsmallar
description: Beskriver hur du ställer in jobb för allmän information och ställer in priser för projektartiklar, resurser och redovisningskonton och projektbokföringsmallar.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.search.form: 211, 463, 1012
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e150dfec7471ad755ce6e0f69a224a36f24fc6f3
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514914"
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Ställ in projekt, priser och projektbokföringsmallar

Som projektledare kan du skapa jobb som definierar alla projekt som du hanterar i [!INCLUDE[prod_short](includes/prod_short.md)]. På sidan **Projektinställningar** måste du ange hur du vill använda vissa projektfunktioner.

För varje jobb, anger du de individuella de projektkorten med information om priser för projektartiklar, projektresurser och projektredovisningskonton och du måste skapa projektbokföringsmallar.

## <a name="to-set-general-information-for-jobs"></a>Så här anger du allmän information för projekt
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projektinställningar** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Fältet **Tillämpa användningslänk som standard** indikerar om projekttransaktioner är länkade till projektplaneringsrader som standard. Välj fältet om du vill använda den här inställningen för alla nya projekt som du skapar. Du kan aktivera eller inaktivera spårning av projektförbrukning för ett visst projekt genom att ändra värdet i fältet **Använd förbrukningslänk** på det enskilda projektkortet. Konsekvenserna beskrivs i följande avsnitt.

### <a name="to-set-up-job-usage-tracking"></a>Så här anger du projektförbrukningsspårning

När du arbetar på ett projekt kan det hända att du vill veta hur förbrukningen spåras mot din plan. Det gör du enkelt genom att skapa en koppling mellan dina projektplaneringsrader och den faktiska förbrukningen. Detta gör att du kan spåra dina kostnader och enkelt visa hur mycket som återstår att göra. Som standard är projektplaneringsradtypen *Budget*, men radtypen **Både Budget och Fakturerbart** har liknande effekter.

När du har ställt in användningsspårning genom att välja fältet **Använd förbrukningslänk** kan du granska informationen på projektplaneringsraden. Du kan ange antal av resursen, artikeln eller redovisningskontot och sedan ange vilket antal som du vill överföra till projektjournalen. Fältet **Återstående antal** på projektplaneringsraden talar om vad som återstår att överföra och bokföra till projektjournalen.

>[!NOTE]
> Om **Använd förbrukningslänk** har valts för det enskilda projektet och fältet **Radtyp** på projektjournalraden eller inköpsraden är *Fakturerbar*, skapas nya projektplaneringsrader av radtypen *Budget* när du bokför projektjournal eller inköpsdokument.  
> Mer information finns i [Registrera förbrukning för projekt](projects-how-record-job-usage.md) och [Hantera projektleveranser](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Om fältet **Radtyp** på projektjournalraden eller inköpsraden är tomt skapas inga projektplaneringsrader när du bokför projekt journalen eller inköpsdokumentet.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>För att skapa priser för resurser, artiklar och redovisningskonton för jobb
> [!NOTE]
> I 2020 års utgivningscykel 2 släppte vi nya processer för att ställa in och hantera priser och rabatter. Om du är en ny kund använder du den nya upplevelsen. Om du är en befintlig kund vilar din användning av den nya versionen på om administratören har aktiverat funktionsuppdateringen **Ny försäljningsprisupplevelse** i **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).

Du kan skap priser för resurser, artiklar och redovisningskonton relaterade till ett jobb. 

#### <a name="current-experience"></a>[Aktuell upplevelse](#tab/current-experience)
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj jobbet och sedan åtgärden **Resurs**, **Artikel** eller **Redovisningskonto**.
3. På sidorna fyller du i **Priser för jobbresurser**, **Priser för jobbartiklar** eller **Priser för jobbredovisningskonto** efter behov.

I följande tabell visas hur informationen i de valfria fälten används på projektplaneringsrader och -journaler när resurs-, artikel- eller redovisningskontot väljs för jobbet.

|Kolumn1  |Kolumn2  |
|---------|---------|
|**Projektresurser**|Fälten **Projektuppgiftsnr.**, **Arbetstyp**, **Valutakod**, **Radrabatt %** och **Styckkostnadsfaktor**. Värdet i fältet **Enhetspris** för resursen kommer att användas i projektjournalerna och projektets planeringsrader när den här resursen, en resurs tilldelad till resursgruppen eller valfri resurs anges. Notera att detta pris alltid kommer att åsidosätta eventuella priser som har angetts på den befintliga sidan **Resurspris/Resursgruppriser**.|
|**Projektartiklar**|Fälten **Projektaktivitetsnr**, **Valutakod** och **Radrabatt %**. Värdet i fältet **Enhetspris** för artikeln kommer att användas i projektplaneringsraderna och projektjournalerna när den här artikeln anges. Obs! Detta pris kommer alltid att åsidosätta det vanliga kundpriset ("bästa pris"-mekanismen) för artiklar. Du bör inte skapa några artikelpriser för projektet om du vill använda mekanismerna för vanliga kundpriser.|
|**Redovisningskonton**|Den valfria informationen i fälten **Projektaktivitetsnr.**, **Valutakod**, **Radrabatt %**, **Styckkostnadsfaktor** och **Styckkostnad** kommer att användas i projektplaneringsrader och projektjournaler när detta redovisningskonto anges och läggs till i ett projekt. Värdet i fältet **Enhetspris** för projektkostnaden för redovisningskontot kommer att användas i projekplaneringstjournalerna och projektjournalerna när detta redovisningskonto anges.|

#### <a name="new-experience"></a>[Ny upplevelse](#tab/new-experience)
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj relevant projekt och sedan åtgärden **Försäljningsprislistor**.

---

## <a name="to-set-up-job-posting-groups"></a>Så här lägger du upp projektbokföringsmallar
En aspekt av att planera projektet är att bestämma vilka bokföringskonton som ska användas för projektvärdering. Om du vill kunna bokföra projekt måste du lägga upp bokföringskonton för varje projektbokföringsmall. En bokföringsmall representerar en länk mellan projektet och hur det ska hanteras i redovisningen. När du skapar ett projekt anger du en bokföringsmall och, som standard, kopplar du varje aktivitet som du skapar för projektet till den här bokföringsmallen. Men medan du skapar aktiviteter kan du välja att åsidosätta standarden och välja en annan, mer lämplig, bokföringsmall.  

> [!NOTE]  
>   Nödvändiga konton i kontoplanen måste registreras innan du registrerar bokföringsmallar. Mer information finns i [Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md).  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **projektbokföringsmallar** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i kontofälten enligt instruktionerna i följande tabell.  

| Kontofält | Beskrivning |
| --- | --- |
| **Kod** |En kod för bokföringsmallen. Du kan ange upp till 10 tecken inklusive blanksteg. |
| **Konto för PIA-kostnader** |PIA-kontot för den beräknade kostnaden för projektets PIA, vilket är ett konto för anläggningstillgångar i balansräkningen. |
| **Konto för upplupna PIA-kostnader** |Ett konto för kostnadsvärde eller kostnadsförsäljningsmetod för beräkningen av PIA, vilket är ett skuldkonto för upplupna kostnader i balansräkningen. Bokföring kommer att ske på detta konto när det krävs att förbrukningskostnader som har bokförts på resultatkontot ökas i PIA-justeringsprocessen. |
| **Konto för kopplade projektkostnader** |Ett balanskonto för PIA-kostnadskontot, som är ett motkonto för ett negativt kostnadskonto. |
| **Konto för kopplade artikelkostnader** |Ett balanskonto för PIA-kostnadskontot, som är ett motkonto för ett negativt kostnadskonto. |
| **Konto för kopplade resurskostnader** |Ett balanskonto för PIA-kostnadskontot, som är ett motkonto för ett negativt kostnadskonto. |
| **Konto för kopplade kostnader** |Ett balanskonto för PIA-kostnadskontot, som är ett motkonto för ett negativt kostnadskonto. |
| **Konto för projektkostnadsjustering** |Balanskontot för kontot för upplupna PIA-kostnader, som är ett kostnadskonto. |
| **Konto för redovisningskostnader (budget)** |Försäljningskontot som ska användas för redovisningskostnader i projektaktiviteter med den här bokföringsmallen. Om fältet lämnas tomt kommer det redovisningskonto som har angetts på projektplaneringsraden att användas. |
| **Konto för upplupen PIA-försäljning** |PIA-kontot för det beräknade försäljningsvärdet för PIA, vilket är ett konto för upplupen intäkt i balansräkningen. Bokföring kommer att ske på detta konto när den bokförda intäkten måste ökas i PIA-justeringsprocessen. |
| **Konto för fakturerad PIA-försäljning** |Kontot för värdet för fakturerad PIA-försäljning som inte kan bokföras. Det är ett konto för förutbetald intäkt i balansräkningen. |
| **Konto för kopplad projektförsäljning** |Balanskontot för kontot för fakturerad PIA-försäljning, vilket är ett motkonto för inkomst. |
| **Konto för projektförsäljningsjustering** |Balanskontot för PIA-projektförsäljningskontot, som är ett inkomstkonto. |
| **Konto för bokförda kostnader** |Det kostnadskonto som innehåller bokförda kostnader för projektet. Kontot är vanligtvis ett debetkonto för kostnader. |
| **Konto för bokförd försäljning** |Inkomstkontot som innehåller den bokförda inkomsten för projektet. Kontot är vanligtvis ett kreditkonto för inkomst. |

## <a name="see-also"></a>Se även

[Ange projekthantering](projects-setup-projects.md)  
[Video: Hur du skapar du ett projekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Hantera projekt](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
