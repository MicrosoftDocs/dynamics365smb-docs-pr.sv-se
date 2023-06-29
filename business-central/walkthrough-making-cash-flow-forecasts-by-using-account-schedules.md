---
title: Utför kassaflödesprognoser med hjälp av ekonomiska rapporter
description: Den här genomgången beskriver hur du kan använda ekonomiska rapporter för att göra kassaflödesprognoser i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: edupont
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports"></a><a name="walkthrough-making-cash-flow-forecasts-using-financial-reports"></a>Genomgång: Utföra kassaflödesprognoser med hjälp av ekonomiska rapporter

Den här genomgången beskriver hur du kan använda ekonomiska rapporter för att göra kassaflödesprognoser. Ekonomiska rapporter utför beräkningar som inte kan göras direkt i diagram för kassaflödeskonton. I ekonomiska rapporter kan du skapa delsummor för kassainflöden och utbetalningar. Dessa delsummor kan inkluderas i nya totaler som kan användas för att göra kassaflödesprognoser.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Om den här genomgången

I den här genomgången tas följande aktiviteter upp:  

- Lägga upp ett nytt namn för ekonomisk rapport för kassaflöde.  
- Skapa rader i ekonomisk rapport.  
- Skapa en ny kolumndefinition.  
- Tilldela en kolumndefinition till en ekonomisk rapport.  
- Visa och skriva ut kassaflödesprognosen.  

### <a name="prerequisites"></a><a name="prerequisites"></a>Förutsättningar

För att kunna utföra den här genomgången behöver du:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Ett kassaflödeskalkylblad med registrerade rader  

## <a name="roles"></a><a name="roles"></a>Roller

Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroll:  

- Controller  

## <a name="story"></a><a name="story"></a>Situation

Ken är controller på CRONUS som varje månad gör kassaflödesprognoser. Ken tar med ekonomi, försäljning, inköp och anläggningstillgångar i prognosen och presenterar den för Sara som är ekonomichef.  

## <a name="setting-up-a-new-financial-report-name"></a><a name="setting-up-a-new-financial-report-name"></a>Lägga upp ett nytt namn för ekonomisk rapport

Namnet på den ekonomiska rapporten är det namn som du ger kassaflödesprognosen, som innehåller en serie definierade rader och en kolumndefinition.  

### <a name="set-up-a-new-financial-report-name"></a><a name="set-up-a-new-financial-report-name"></a>Lägga upp ett nytt namn för ekonomisk rapport

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Ekonomisak rapporter** och väljer sedan relaterad länk.  
2. På sidan **Ekonomiska rapporter** väljer du **Nytt** för att skapa ett nytt namn på ekonomisk rapport för kassaflöde.  
3. I fältet **Namn** anger du **Prognos**.  
4. I fältet **Beskrivning**, ange **Kassaflödesprognos**.  
5. Lämna fälten **Raddefinition** och **Kolumndefinition** tomma.

## <a name="setting-up-row-definition-lines"></a><a name="setting-up-row-definition-lines"></a>Ställa in raddefinitionsrader

När ett namn på en ekonomisk rapport ställs in definierar Ken varje rad i den ekonomiska rapporten för kassaflöde. Ken definierar rader så att de visas i rapporter förutom rader som bara används vid beräkning.  

### <a name="set-up-row-definition-lines"></a><a name="set-up-row-definition-lines"></a>Ställa in raddefinitionsrader

1. På sidan **Ekonomiska rapporter** väljer du den nya ekonomiska rapporten **Prognos** som du skapat och väljer sedan åtgärden **Redigera raddefinition**.  
2. På sidan **Raddefinition** anger du varje rad exakt som i följande tabell.  

    > [!TIP]  
    > Använd funktionen **Infoga CF-konton** för att snabbt markera, i diagrammet för kassaflödeskontot, de kassaflödeskonton du vill använda och kopierar dem till raddefinitionsrader.  

    | Radnr | Description              | Summeringstyp            | Summeringsintervall | Radtyp   | Beloppstyp | Visa |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Kundreskontra              | Transaktionskonton för kassaflöde | 10       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Öppna försäljningsorder        | Transaktionskonton för kassaflöde | 20       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Uthyrning                  | Transaktionskonton för kassaflöde | 30       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Finansiella tillgångar         | Transaktionskonton för kassaflöde | 40       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Avyttring av anläggningstillgångar    | Transaktionskonton för kassaflöde | 50       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Privata investeringar      | Transaktionskonton för kassaflöde | 60       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Diverse inleveranser   | Transaktionskonton för kassaflöde | 70       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Öppna serviceorder      | Transaktionskonton för kassaflöde | 80       |Nettoförändring | Nettobelopp  | Ja  |
    | R20     | Summa inbetalningar      | Formel                  | R10      |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Leverantörsreskontra                 | Transaktionskonton för kassaflöde | 1010     |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Öppna inköpsorder     | Transaktionskonton för kassaflöde | 1020     |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Personalkostnader          | Transaktionskonton för kassaflöde | 1030     |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Löpande kostnader            | Transaktionskonton för kassaflöde | 1040     |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Finanskostnader            | Transaktionskonton för kassaflöde | 1050     |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Investeringar              | Transaktionskonton för kassaflöde | 1070     |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Privat konsumtion     | Transaktionskonton för kassaflöde | 1090     |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Förfallen moms                  | Transaktionskonton för kassaflöde | 1100     |Nettoförändring | Nettobelopp  | Ja  |
    | R30     | Övriga utgifter           | Transaktionskonton för kassaflöde | 1110     |Nettoförändring | Nettobelopp  | Ja  |
    | R40     | Summa kontantutbetalningar | Formel                  | R30      |Nettoförändring | Nettobelopp  | Ja  |
    | R50     | Överskott                  | Formel                  | R20+R40  |Nettoförändring | Nettobelopp  | Ja  |
    | R60     | Kassaflödesmedel          | Transaktionskonton för kassaflöde | 2100     |Nettoförändring | Nettobelopp  | Ja  |
    | R70     | Summa kassaflöde          | Formel                  | R50+R60  |Nettoförändring | Nettobelopp  | Ja  |

    > [!NOTE]
    > Radnumret R10 används för att överföra kontosummorna för kundreskontra. Radnumret R20 används för att beräkna summan av alla inbetalningsjournaler. Radnumret R30 används för att överföra kontosummorna för leverantörsreskontra. Radnumret R40 används för att beräkna summan av alla kontantutbetalningar. Radnumret R50 används för att överföra summan av alla kontantöverskott. Radnumret R60 används för att överföra likvida medel. Radnumret R70 används för att beräkna kassaflödesprognosen.

## <a name="setting-up-a-new-column-definition"></a><a name="setting-up-a-new-column-definition"></a>Skapa en ny kolumndefinition

Innan Ken kan skriva ut kassaflödesprognosen, måste han att skapa kolumndefinitionen för den numeriska informationen. I kolumnerna definierar Ken den information som han vill använda från raderna.

- Den första kolumnen har numret *C10* med rubriken **Amount** och innehåller nettoförändringen.  
- Den andra kolumnen har numret *C20* och rubriken **Saldo på datum** och innehåller transaktionerna för perioden.  
- Den tredje kolumnen har numret *C30* och rubriken **Hela året** och innehåller nettoförändringen i saldona för hela räkenskapsåret.  
- Slutligen anger Ken att kolumndefinitionen ska vara standardalternativet för den ekonomiska rapporten **Prognos**.  

### <a name="set-up-a-new-column-definition"></a><a name="set-up-a-new-column-definition"></a>Lägga upp en ny kolumndefinition

1. På sidan **Ekonomiska rapporter** väljer det nya namnet för rapporten **Prognos** som du skapat. På fliken **Start**, i gruppen **Bearbeta**, väljer du **Redigera kolumndefinition**.

2. Skapa en ny kolumndefinition med namnet **Kassaflöde**.

3. Välj **OK**.

4. Fyll i raderna exakt så som det visas i följande tabell.

    |Kolumnnr|Kolumnrubrik|Kolumntyp|Transaktionstyp|Beloppstyp|Visa|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |K10|Momsbelopp|Nettoförändring|Transaktioner|Nettobelopp|Alltid|  
    |C20|Belopp till datum|Saldo t.o.m. datum|Transaktioner|Nettobelopp|Alltid|  
    |C30|Hela räkenskapsåret|Hela räkenskapsåret|Transaktioner|Nettobelopp|Alltid|

## <a name="assigning-the-column-definition-to-the-financial-report-name"></a><a name="assigning-the-column-definition-to-the-financial-report-name"></a>Tilldela en kolumndefinition till namnet på den ekonomiska rapporten

Nu kan Ken koppla kolumndefinitionen till namnet på den ekonomiska rapporten.  

### <a name="assign-the-column-definition-to-the-financial-report-name"></a><a name="assign-the-column-definition-to-the-financial-report-name"></a>Tilldela en kolumndefinition till namnet på den ekonomiska rapporten

1. På sidan **Ekonomiska rapporter** väljer du den ekonomiska rapporten **Prognos** och väljer sedan åtgärden **Redigera kolumndefinition**.  
2. I fältet **Namn** väljer du kolumndefinitionen **Kassaflöde** som standardkolumndefinition.  

## <a name="view-and-print-the-cash-flow-forecast"></a><a name="view-and-print-the-cash-flow-forecast"></a>Visa och skriv ut kassaflödesprognosen

1. På sidan **Ekonomiska rapporter** väljer du den ekonomiska rapporten **Prognos** för att visa kassaflödesprognosen.  
2. På sidan **Ekonomisk rapport** kan du ange ett belopp och sedan visa transaktionerna i kassaflödesprognosen som utgör beloppet. Dessutom kan du visa formeln som används för att beräkna beloppet. Du kan också filtrera beloppen efter datum och dimension.  
3. Välj åtgärden **Skriv ut** när du vill skriva ut kassaflödesprognosen.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/forecast-cash-flow-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Arbeta med ekonomiska rapporter](bi-how-work-account-schedule.md)  
[Analysera kassaflödet i företaget](finance-analyze-cash-flow.md)  
[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
