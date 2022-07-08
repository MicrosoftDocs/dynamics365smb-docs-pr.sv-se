---
title: Kassaflödesprognoser genom att använda kontouppställningar
description: Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 242c3e65401f188068c6e1fbea20212d4a3a7653
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076155"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Genomgång: Utföra kassaflödesprognoser genom att använda kontouppställningar

Den här genomgången beskriver hur du kan använda kontouppställningar för att göra kassaflödesprognoser. Kontouppställningar utför beräkningar som inte kan göras direkt i kontoplaner för kassaflöden. I kontouppställningar kan du skapa delsummor för kassainflöden och utbetalningar. Dessa delsummor kan inkluderas i nya totaler som kan användas vid kassaflödesprognoser.  

## <a name="about-this-walkthrough"></a>Om den här genomgången

I den här genomgången tas följande aktiviteter upp:  

- Lägga upp ett nytt namn för kassaflödeskontouppställningen.  
- Skapa kontouppställningsrader.  
- Lägga upp en ny kolumnlayout.  
- Koppla en kolumnlayout till en kontouppställning.  
- Visa och skriva ut kassaflödesprognosen.  

### <a name="prerequisites"></a>Förutsättningar

För att kunna utföra den här genomgången behöver du:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Kalkylarksraderna för kassaflöde är bokförda  

## <a name="roles"></a>Roller

Den här genomgången innehåller arbetsuppgifter som utförs av följande användarroll:  

- Controller  

## <a name="story"></a>Situation

Ken är controller på CRONUS som varje månad gör kassaflödesprognoser. Han tar med ekonomi, försäljning, inköp och anläggningstillgångar i prognosen, och sedan visar han den till Sara som är ekonomichef.  

## <a name="setting-up-a-new-account-schedule-name"></a>Lägga upp ett nytt kontouppställningsnamn

En kontouppställning består av ett kontouppställningsnamn för kassaflöde med en serie rader och en kolumnlayout.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Så här skapar du ett nytt kontouppställningsnamn  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **kontouppställningar** och väljer sedan relaterad länk.  
2. På sidan **Kontouppställningsnamn** väljer du åtgärden **Ny** för att skapa ett nytt kontouppställningsnamn för kassaflöde.  
3. I fältet **Namn** anger du **Prognos**.  
4. I fältet **Beskrivning**, ange **Kassaflödesprognos**.  
5. Lämna fälten **Standard kolumnlayout** och **Analysvynamn** tomma.  

## <a name="setting-up-account-schedule-lines"></a>Skapa kontouppställningsrader

När ett kontouppställningsnamn har upprättats, definierar Ken varje rad som visas i kontouppställningen för kassaflödet. Ken definierar rader som kan visas i rapporter förutom rader som bara används vid beräkning.  

### <a name="to-set-up-account-schedule-lines"></a>Så här skapar du kontouppställningsrader  

1. På sidan **Kontouppställningsnamn** väljer du det nya kontouppställningsnamnet **Prognos** som du har skapat och väljer sedan åtgärden **Redigera kontouppställning**.  
2. På sidan **Kontouppställning** anger du varje rad exakt som i följande tabell.  

    > [!TIP]  
    >  Med hjälp av funktionen **Infoga kassaflödeskonton** kan du snabbt välja kassaflödeskonton från kontoplanen för kassaflöde och kopiera dem till kontouppställningsrader.  

    | Rad-nr | Beskrivning              | Summeringstyp            | Summeringsintervall | Radtyp   | Beloppstyp | Visa |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Öppna försäljningsorder        | Transaktionskonton för kassaflöde | 20       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Uthyrning                  | Transaktionskonton för kassaflöde | 30       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Finansiella tillgångar         | Transaktionskonton för kassaflöde | 40       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Avyttring av anläggningstillgångar    | Transaktionskonton för kassaflöde | 50       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Privata investeringar      | Transaktionskonton för kassaflöde | 60       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Diverse inleveranser   | Transaktionskonton för kassaflöde | 70       |Nettoförändring | Nettobelopp  | Ja  |
    | R10     | Öppna serviceorder      | Transaktionskonton för kassaflöde | 80       |Nettoförändring | Nettobelopp  | Ja  |
    | R20     | Summa inbetalningar      | Formel                  | R10      |Nettoförändring | Nettobelopp  | Ja  |
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

## <a name="setting-up-a-new-column-layout"></a>Skapa en ny kolumnlayout

Innan Ken kan skriva ut kassaflödesprognosen, måste han att skapa kolumnlayouten för den numeriska informationen. I kolumnerna definierar han den information som han vill använda från raderna.

- Den första kolumnen har numret *C10* med rubriken **Amount** och innehåller nettoförändringen.  
- Den andra kolumnen har numret *C20* och rubriken **Saldo på datum** och innehåller transaktionerna för perioden.  
- Den tredje kolumnen har numret *C30* och rubriken **Hela året** och innehåller nettoförändringen i saldona för hela räkenskapsåret.  
- Slutligen anger han att kolumnlayouten ska vara standardkolumnlayout för kontouppställningen **Prognos**.  

## <a name="to-set-up-a-new-column-layout"></a>Så här lägger du upp en ny kolumnlayout

1. I fönstret **Kontouppställningsnamn** väljer du det nya kontouppställningsnamnet för **Prognos** som du har skapat. På fliken **Start**, i gruppen **Bearbeta**, väljer du **Redigera inställning för kolumnlayout**.

    > [!TIP]
    > Du hittar samma åtgärd på sidan **Kontouppställning** om du fortfarande redigerar kontouppställningen **Prognos** där.

2. Skapa en ny kolumnlayout med namnet **Kassaflöde**.

3. Välj OK.

4. Fyll i raderna exakt så som det visas i följande tabell.

    |Kolumnnr|Kolumnrubrik|Kolumntyp|Transaktionstyp|Beloppstyp|Visa|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Belopp|Nettoförändring|Transaktioner|Nettobelopp|Alltid|  
    |C20|Belopp till datum|Saldo t.o.m. datum|Transaktioner|Nettobelopp|Alltid|  
    |C30|Hela räkenskapsåret|Hela räkenskapsåret|Transaktioner|Nettobelopp|Alltid|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Koppla kolumnlayouten till kontouppställningsnamnet

Nu kan Ken koppla kolumnlayouten till kontouppställningsnamnet.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Så här kopplar du kolumnlayouten till kontouppställningsnamnet  

1. På sidan **Kontouppställning** där du arbetar med kontouppställningen **Prognos** väljer du åtgärden **Redigera kolumnlayout**.  
2. I fältet **Namn på kolumnlayout** väljer du kolumnlayouten **Kassaflöde** som standardkolumnlayout.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Så här visar och skriver du ut kassaflödesprognosen

1. På sidan **Kontouppställningsnamn** väljer du åtgärden **Översikt** för att visa kassaflödesprognosen.  
2. På sidan **Kontouppställning översikt** kan du ange ett belopp och sedan visa transaktionerna i kassaflödesprognosen som utgör beloppet. Dessutom kan du visa formeln som används för att beräkna beloppet. Du kan också filtrera beloppen efter datum och dimension.  
3. Välj åtgärden **Skriv ut** när du vill skriva ut kassaflödesprognosen.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relaterad utbildning på [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/)

## <a name="see-also"></a>Se även

[Arbeta med kontouppställningar](bi-how-work-account-schedule.md)  
[Analysera kassaflödet i företaget](finance-analyze-cash-flow.md)  
[Genomgång av affärsprocesser](walkthrough-business-process-walkthroughs.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]