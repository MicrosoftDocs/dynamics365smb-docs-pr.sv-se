---
title: Så här skapar du nummerserier | Microsoft Docs
description: Lära dig hur du anger nummerserier som tilldelar unika ID-koder till konton och dokument i Business Central.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 75a841fd2d6bf8321f15bb0a6fe88d41bf152308
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912652"
---
# <a name="create-number-series"></a>Skapa nummerserier
För varje företag som du lägger upp måste du tilldela unika ID-koder till exempelvis redovisningskonton, kund- och leverantörskonton, fakturor och dokument. Numrering är viktigt inte enbart för identifiering. Ett adekvat numreringssystem gör också företaget mer hanterbart och enkelt att analysera, och kan minska antalet fel som uppstår vid datainmatning.

> [!Important]
> Som standard är luckor inte tillåtna i nummerserier eftersom den exakta historiken över de ekonomiska transaktionerna måste vara tillgänglig för granskning, enligt lag, och därför måste följa en obruten sekvens utan borttagna nummer.<br /><br />
Om du vill tillåta luckor i vissa nummerserier ska du först samråda med revisorn eller redovisningschefen och se till att du följer de juridiska kraven i ditt land/din region. Mer information finns i [Luckor i nummerserier](ui-create-number-series.md#gaps-in-number-series).

> [!NOTE]  
>   Vi rekommenderar att du använder samma nummerserie som du ser på sidan **Nr-serielista** i demonstrationsföretaget CRONUS. Koder som *P-INV+* kanske inte passar direkt, men [!INCLUDE[d365fin](includes/d365fin_md.md)] har flera standardinställningar som hör ihop med dessa nummerseriekoder.

Du skapar ett numreringssystem genom att skapa en eller flera koder för varje typ av huvuddata eller dokument. Du kan till exempel skapa en kod för numrering av kunder, en annan för numrering av försäljningsfakturor och en annan för numrering av dokument i redovisningsjournaler. När du har skapat en kod måste du ställa in minst en nummerserierad. Nummerserieraden innehåller information som första och sista nummer i serien och startdatum. Du kan registrera flera nummerserierader per nummerseriekod, med olika startdatum på varje rad. Nummerserierna används löpande, med början på respektive startdatum.

Du ställer normalt in nummerserier till att automatiskt infoga nästa nummer på nya kort eller dokument som du skapar. Men kan du också skapa en nummerserie för att manuellt ange det nya numret. Du anger detta med kryssrytan **Manuell numrering.**

Om du vill använda mer än en nummerseriekod för en typ av huvuddata, till exempel om du vill använda olika nummerserier för olika kategorier med artiklar, kan du använda nummerseriesamband.

## <a name="gaps-in-number-series"></a>Luckor i nummerserier
Alla poster som du skapar i [!INCLUDE[d365fin](includes/d365fin_md.md)] är inte ekonomiska transaktioner som måste använda sekventiell numrering. Kundkort, försäljningsofferter och lageraktiviteter är exempel på poster som tilldelas ett nummer från en nummerserie, men som inte omfattas av finansiell granskning och/eller kan tas bort. För en sådan nummerserie kan du markera kryssrutan **Tillåt luckor i nummer** på sidan **Nr-serier rader**. Den här inställningen kan också ändras efter att nummerserien skapats. För mer information, se [Så här skapar du en ny nummerserie](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Fältet Nr. på Dokument och kort
På försäljnings-, inköps- och överföringsdokument och alla kort kan **Nr.** fyllas i automatiskt (från en nummerserie) eller manuellt, och kan även ställas in att vara osynligt.

Fältet **nr.** kan fyllas i på tre sätt:

1. Om endast en nummerserie finns för typen av dokument eller kort finns där kryssrutan **Förvalda nr.** är markerad och kryssrutan **Manuella nr.** inte är markerad, så fylls fältet automatiskt i med nästa nummer i serien, och fältet **Nr.** kommer inte att visas.

    > [!NOTE]  
    > Om nummerserien inte fungerar, till exempel eftersom antalet nummer har tagit slut, kommer fältet **Nr.** att visas och du kan manuellt ange ett nummer eller lösa problemet på sidan **Nummerserie**.

2. Om mer än en nummerserie finns för typen av dokument eller kort, och kryssrutan **Förvalda nr.** inte har markerats för den nummerserie som för tillfället tilldelats, så kommer fältet **Nr.** att visas, och du kan öppna sidan **Nummerserie** och välja den nummerserie som du vill använda. Nästa nummer i serien förs då in i fältet **Nr.** .

3. Om du inte har skapat en nummerserie för dokument- eller korttypen, eller om fältet **Manuella nr.** har valts för nummerserien, så kommer fältet **Nr.** att visas, och du måste ange en siffra manuellt. Du kan ange högst 20 tecken, både siffror och bokstäver.

När du öppnar ett nytt dokument eller kort som det finns en nummerserie för, öppnas tillhörande **Inställningar för nummerserie**-sida så att du kan ställa in en nummerserie för den typen av dokument eller kort innan du fortsätter med övriga datainmatningar.

> [!NOTE]  
> Om du behöver aktivera manuell numrering för till exempel nya artikelkort som har skapats med en datamigreringsprocess som döljer fältet **Nr.** som standard, gå då till sidan **Lagerinställningar** och välj sedan fältet **Artikelnr.** om du vill öppna och ange relaterade nummerserier som **Manuell numrering**.

## <a name="to-create-a-new-number-series"></a>Så här skapar du nummerserier
1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Nummerserie** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Välj åtgärden **Rader**.
5. På sidan **Nr-serier rader** fyller du i fälten för att definiera den faktiska användningen och innehållet i nummerserien som du skapade i steg 2.
6. Upprepa steg 5 för alla andra användningsområden för nummerserien som du behöver. Fältet **Startdatum** anges vilken nummerserierad som är aktiv.

## <a name="to-set-up-where-a-number-series-is-used"></a>Om du vill konfigurera var en nummerserie används
I följande procedur beskrivs hur du ställer in nummerserier för området Försäljning. Stegen är liknande för andra områden.
1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Försäljningsinställningar** och välj sedan relaterad länk.
2. På sidan **försäljning** klickar du på snabbfliken **nr-serier** och väljer önskade nummerserier för varje försäljningskort och dokument.

Det markerade numret kommer nu att användas för att fylla i fältet **nr.** på kortet eller dokumentet i fråga enligt de inställningar du har gjort på nummerserieraden.

## <a name="to-create-relationships-between-number-series"></a>Så här skapar du samband mellan nummerserier
Om du har definierat mer än en nummerseriekod för samma typ av allmän information eller transaktioner kan du skapa samband mellan koderna. Den här funktionen gör det enklare för dig att välja bland koderna när du använder ett nummer.

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Nummerserie** och välj sedan relaterad länk.
2. Markera raden med de nummerserier som du vill skapa relationer för och välj sedan **Relationer**.
3. I fältet **Seriekod** anger du koden för nummerserien som du vill koppla till serien du valde i steg 2.
4. Lägg till en rad för varje kod som du vill koppla till den valda nummerserien.
5. Stäng sidan.

När du hädanefter definierar något för vilket ett nummer krävs kan du använda sambanden som har skapats för att välja bland de kopplade nummerserierna.

## <a name="see-related-training-at-microsoft-learn"></a>Se Relaterad utbildning på [Microsoft Learn](/learn/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
