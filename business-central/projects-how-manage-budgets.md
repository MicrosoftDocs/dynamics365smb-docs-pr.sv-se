---
title: Ställ in och hantera en budget för ett projekt
description: Beskriver hur du planerar resurser och prognos och styr kostnader för ett projekt genom att skapa en budget för varje projekt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'project budget, forecast'
ms.search.form: '1002, 1007'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="manage-project-budgets"></a>Hantera projektbudgetar

Du kan lägga upp en budget för varje projekt. Budgeten används för att planera de resurser du tilldelar ett projekt. Budgeten kan antingen vara allmän med få poster eller innehålla fler poster som är indelade i aktivitetsnivåer. Du kan sedan jämföra budgeterade belopp med den faktiska förbrukningen enligt registreringen i projektjournalen. Genom att övervaka skillnader mellan faktisk förbrukning och budgeterad användning kan du kontrollera pågående projekt och förbättra kvaliteten hos framtida projekt genom att minska risken för att kostnader underskattas.

Efterföljande procedur beskriver hur du beräknar budgeterade kostnader under planering. Mer information om registrering av budgeterade jämfört med faktiska projektpriser och -kostnader finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).  

## <a name="to-estimate-the-budgeted-costs-for-a-project"></a><a name="JobBudgetCosts"></a>Att ange budgeterade kostnader för ett projekt
När en kund vill veta priset på ett projekt som kommer att faktureras baserat på förbrukning, måste du fastställa de budgeterade kostnaderna för projektet. Du använder sidan **Projektaktivitetsrader** om du vill göra detta.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Öppna ett relevant projekt.
3. Markera en projektrad av typen Bokföring och välj sedan åtgärden **Projektplaneringsrader**.
4. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Se följande information för fältet **Radtyp**.  

| Typ av rad | Beskrivning |
| --- | --- |
| **Både Budget och Fakturerbart** |Kostnads- och prisbelopp som har angetts på planeringsraderna är de budgeterade kostnaderna för denna specifika planeringsrad. Prisbeloppet faktureras. |
| **Budget** |Kunden debiteras inte för användning. Förbrukningen överförs inte till en faktura, men den kommer fortfarande att användas i PIA-beräkningen. |
| **Fakturerbart** |Kunden debiteras för användning. Förbrukningen överförs till fakturan baserat på det antal som finns angivet i fältet Antal att överföra till faktura. |

> [!NOTE]  
> Fältet **Planerat leveransdatum** för planeringsraden innehåller datumet då förbrukning som relateras till planeringsraden förväntas slutföras. Det är också datumet då planeringsraden kan överföras till en försäljningsfaktura och bokföras. <br /><br /> I underliggande projektaktiviteten på sidan **projektkortet** innehåller **startdatum** och **slutdatum** värdet för fältet **planerat leveransdatum** på tidigaste och senaste projektets planeringsrader på relaterad sida för **projektplaneringsrader**.

> [!NOTE]  
>   När du fyller i fältet **Antal** kommer all information om totalt pris och total kostnad att beräknas och fyllas i för planeringsraden. De kan redigeras när det passar dig.

På sidan **Projektkort** kan du nu se en översikt över de totala budgeterade kostnaderna, budgeterat pris, fakturerbar kostnad och fakturerbart pris för varje aktivitet.

Mer information om registrering av budgeterade jämfört med faktiska projektpriser och -kostnader finns i [Så här registrerar du förbrukning för projekt](projects-how-record-job-usage.md).

## <a name="see-also"></a>Se även

[Projekthantering](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
