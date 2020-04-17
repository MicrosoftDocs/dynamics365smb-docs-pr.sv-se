---
title: Samla in kundinställningsvärden | Microsoft Docs
description: Du använder frågeformuläret för konfiguration för att lättare kunna minska din implementeringsarbetsbörda, detta genom att effektivisera arbetet med att konfigurera det nya företaget. Du kan skapa frågeformuläret för konfiguration i Business Central och sedan leverera den sedan till kunden som en Excel- (.xlsx) eller XML-fil.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 125f8062db7404c0b873c6774c11906a0bfeef55
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187322"
---
# <a name="gather-customer-setup-values"></a>Samla in kundinställningsvärden
Du använder frågeformuläret för konfiguration för att lättare kunna minska din implementeringsarbetsbörda, detta genom att effektivisera arbetet med att konfigurera det nya företaget. Du kan skapa frågeformuläret för konfiguration i [!INCLUDE[d365fin](includes/d365fin_md.md)] och sedan leverera den till kunden som en .xls- eller XML-fil.  

Du kan ändra alla standardvärden i ett frågeformulär för att bättre matcha kundbehoven.  

> [!TIP]  
>  Läs mer om hur du definierar värdena i fälten för leveransplanering, [Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md).  

När kunden har slutfört frågeformuläret kan du importera filen till kundens nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag. Du och din kund validerar svaren i frågeformuläret innan du kopplar dem till företaget.

## <a name="to-create-a-configuration-questionnaire"></a>Så här skapar du ett konfigurationsfrågeformulär
Du kan använda ett frågeformulär för att bestämma omfattningen och behoven av konfigurationen. Du kan skapa ett nytt frågeformulär, eller ändra ett befintligt frågeformulär, genom att lägga till nya fråga eller frågeområden.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company informtion. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 Du kan bara skapa frågeformulär för tabeller av omställningstyp. Du kan till exempel använda verktyg för att ge information på följande sidor:  

-   Företagsinformation  
-   Anl.tillg.inställningar  
-   Redovisningsinställningar  
-   Lagerinställningar  
-   Monteringsinställningar
-   Produktionsinställningar  
-   Inköpsinställningar  
-   Marknadsföringsinställning  
-   Serviceinställningar  
-   Försäljningsinställningar  
-   Lagerstyrningsinställningar  

> [!NOTE]  
>  För att se en komplett lista över inställningsregister, välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställning** och välj sedan relaterad länk. Använd flyttningsfunktioner för att bestämma omfattningen för flyttning av transaktion data. Mer information finns i [Migrera kunddata](admin-migrate-customer-data.md).  

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Konfigurationsenkät** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**.   
3. På sidan **Konfigurationsenkät**, i fältet **Kod**, anger du... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Välj åtgärden **Frågeområden**. Sidan **Frågeområden** öppnas.  
4. Välj åtgärden **Ny**. Sidan **Konfig. frågeområden** öppnas.  
5. I fältet **Tabell-ID** väljer du ID på den tabell som du vill samla in information om. Fälten **Tabellnamn** fylls i automatiskt.  
6. Välj åtgärden **Uppdatera frågor**. Varje fält i tabellen läggs till det frågeformulär med ett frågetecken efter sin rubrik.

Du kan formulera om rubriken för att klargöra hur fråga ska besvaras. Om ett fält exempelvis kallas "Namn" kan du ändra det till att ange "Namn på <data being collected>." Du kan också ge vägledning i fältet **Referens**, inklusive en Webbadress till en sida med ytterligare information.  

Du kan även ta bort frågor som du inte vill inkludera i frågeformuläret.  

> [!NOTE]  
>  Fältet **Svarsalternativ** beskriver typen och formatet på svaret med data som är lämpliga. Fältet **Svar** innehåller användarinskickad information.  
>   
>  Vid behov, kan du också definiera standardsvar i fältet **Svar**. Dessa värden används som standard för anpassad installation. Personen som fyller i profilfrågeformuläret kan dock ändra och uppdatera svaret.  

## <a name="to-complete-the-configuration-questionnaire"></a>Så här slutför du konfigurationsfrågeformuläret
Du använder frågeformuläret för konfiguration för att strukturera och dokumentera en detaljerad diskussion om kundens specifika behov. Du kan också använda det för att samla inställningsdata från kunden för att konfigurera relevanta [!INCLUDE[d365fin](includes/d365fin_md.md)] inställningstabeller, t.ex redovisningen, lager och kunder.  

> [!NOTE]  
>  Du kan också skapa ett eget frågeformulär för konfiguration om så behövs.  

1. Öppna det företag som du vill slutföra frågeformuläret för.
2. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Konfigurationsenkät** och välj sedan relaterad länk.  
3. Välj frågeformuläret för företaget och välj sedan åtgärden **Exportera till Excel**, alternativt åtgärden **Exportera till XML**.
4. Låt kunden slutföra konfigurationsfrågeformuläret genom att ange svaren i Excel-arbetsboken. Det finns formulär för varje frågeområde som har skapats för frågeformuläret.   
5. Spara Excel-arbetsboken som *XML-data*. Välj åtgärden **Importera från XML** och välj .xml-filen med kundens svar.
6. Välj åtgärden **Frågeområden** för att inleda processen med att validera och tillämpa svaren i konfigurationsfrågeformuläret.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Så här kan du fylla i ett frågeformulär från konfigurationskalkylarket  
Följande process visar ett alternativt sätt att använda konfigurationsfrågeformulär. Vi förutsätter att konfigurationspaketet som du har fått innehåller frågeformulär.  

1. Öppna konfigurationskalkylarket när du har importerat ett konfigurationspaket.  
2. För varje tabell där det finns ett frågeområde väljer du åtgärden **Frågor**. Sidan med frågeformuläret öppnas.  
3. Svara på frågorna och välj sedan åtgärden **Koppla svar**.  
4. Välj **OK** för att stänga frågeformuläret.

## <a name="to-validate-the-configuration-questionnaire"></a>Så här validerar du konfigurationsfrågeformuläret
Det är viktigt att validera frågeformuläret för konfiguration innan du kopplar det mot [!INCLUDE[d365fin](includes/d365fin_md.md)]-formatet. Det är även en sätt att se till att dataformatering bevaras under import från Excel.  

En gemensam valideringsuppgift är att kontrollera att textsträngar inte anges i datumfälten. Denna granskningsprocess är nödvändig eftersom svarsformatet i frågeformuläret inte valideras automatiskt när du kör funktionen **Koppla svar**.  

> [!NOTE]  
>  Vanligtvis är validering av frågeformulär för konfiguration en manuell process. Men det finns kontroller för regionala formateringsinkonsekvenser. Dessutom kan det uppstå fel om strukturen på [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen inte motsvarar strukturen på flyttningsdatabasen.  

1. På sidan **Konfigurationsfrågeformulär** markerar du relevant frågeformulär och väljer sedan åtgärden **Frågeområden**.  
2. Öppna relevant frågeområde.  
3. För varje fråga, verifiera att värdet i fältet **Svar** motsvarar format som tillhandahålls i fältet **Svarsalternativ**. Kontrollera till exempel att adressen för ett företag är i textformat.  
4. Om du hittar fel, kan du utföra felsökning och göra korrigeringar i Excel, genom att exportera frågeformuläret och sedan importera det på nytt. Du kan även korrigera fel direkt i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du granskar svaren på sidan **Konfig. frågeområde**.  
5. Upprepa dessa steg för varje frågeområde.  

När du har slutfört din validering är din data klar att kopplas till databasen.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Så här kopplar du svar från konfigurationsfrågeformuläret
Efter att du har importerat och verifierat information från ett frågeformulär för konfiguration kan du överföra inställningsdatan till de motsvarande tabellerna i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  

1. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Konfigurationsenkät** och välj sedan relaterad länk. Sidan **Frågeformulär för inställningar** öppnas.  
2. Markera ett konfigurationsfrågeformulär i listan och välj sedan åtgärden **Redigera lista**.  
3. Du kan koppla svar på två sätt.  

- Om du vill koppla hela frågeformuläret väljer du åtgärden **Koppla svar**.  
- För att koppla svar enbart för ett visst **Frågeområde** väljer du åtgärden **Frågeområden**, väljer ett **Frågeområde** i listan och sedan åtgärden **Koppla svar**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Så här kontrollerar du att svar har kopplats korrekt  
1. Kontrollera inställningssidorna för olika huvudområden av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Välj ![glödlampikonen som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange namnet på inställningssidan, och välj sedan relaterad länk.  
2. Kontrollera att fältet har fyllts i med rätt data från de olika frågeområdena i frågeformuläret för konfiguration.  

Du har nu konfigurerat inställningen med kundens verksamhetsinformationen och regler.

## <a name="see-also"></a>Se även  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)
