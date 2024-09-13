---
title: Skapa ett projektkort för ett projekt och ange aktiviteter
description: För ett nytt projekt kan du skapa ett projektkort med projektaktiviteterna och planeringsrader för att hantera hur och budgetar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-projects"></a>Skapa projekt

När du vill starta ett nytt projekt måste du skapa ett projektkort med inbyggda projektaktiviteter och projektplaneringsrader, strukturerade i två lager.  

Det första lagret består av projektaktiviteter. Du måste skapa minst en projektaktivitet per projekt eftersom all bokföring refererar till en projektaktivitet. Med åtminstone en projektaktivitet i ditt projekt kan du lägga upp projektplaneringsrader och bokföra förbrukningen i projektet.

Det andra lagret består av projektplaneringsrader som specificerar detaljerad förbrukning av resurser, artiklar och diverse redovisningskostnader.

Lagerstrukturen gör att du kan dela upp projekt i mindre aktiviteter och specificera budget, offerter och registrering mer i detalj. Dessutom att du får en inblick i hur ett projekt fortlöper. Du kan till exempel spåra om du uppfyller uppsatta milstolpar eller om du är i linje med mål för att uppfylla budget.

> [!TIP]
> Välj åtgärden **Nytt projekt** på Rollcentret **Projektchef** för att starta en assisterad inställningsguide som tar dig genom stegen för att skapa ett projekt med integrerade uppgifter och planeringsrader. Efterföljande procedur beskriver hur du utför stegen manuellt. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## <a name="to-create-a-project-card"></a>Fakturera en eller flera kunder för projektuppgifter

Ibland är den part som tar emot en service inte densamma som den part som betalar räkningen. Ibland kan du också behöva fakturera flera kunder för aktiviteter i projektet. På sidan **Projektkort** använder du fältet **Faktureringsmetod för aktivitet** för att ange om du fakturerar en kund eller flera kunder.

Om kunden som tar emot servicen också ska betala fakturan väljer du fälten **Fakturera till** och **Leverera till**, välj **Standard (kund)** och **Standard (adress för försäljning)**.

Om du fakturerar flera kunder kan du ange vilken kund som ska få tjänsten och vilken kund som ska fakturera för varje aktivitet i projektet. Du kan även ange följande information:

* Var arbetet sker genom att välja från en lista över leveransadress för kunden.
* Lägga till information om externa referenser för att förenkla kommunikationen med projektet.
* Skriv över projektets standard ekonomiska villkor.

## <a name="to-create-tasks-for-a-project"></a>Fakturera en kund för flera projektaktiviteter

Du kan förenkla faktureringsprocessen genom att skicka en faktura till en kund för flera projekt. Lägg till projektplaneringsrader från flera projekt till en försäljningsfaktura på en gång. Den här processen påminner om att skapa en försäljningsfaktura från en projektplaneringsrad och ange ett värde i fältet **Lägg till i förs.faktura nr.**.

Här är en översikt över processen.

1. Skapa en ny försäljningsfaktura och fyll i **Förs.kundnr.** . Om det behövs fyller du även i **Faktureringskundnr.** och fältet **Valutakod**.
2. På snabbfliken **Rader** klickar du på åtgärden **Hämta projektplaneringsrader**. På sidan **Hämta projektplaneringsrader** visas fakturerbara projektplaneringsrader från projekt för försäljningskund, faktureringskund och faktureringsvaluta där antalet som ska faktureras är större än noll. 
3. Välj de rader du vill lägga till på fakturan och välj sedan **OK**.

Upprepa dessa steg om du vill lägga till ytterligare en uppsättning projektplaneringsrader. Du kan också ta bort fakturan eller dess rader och börja om.

> [!NOTE]
> Det finns ett par begränsningar:
>
> * Åtgärden **Hämta projektplaneringsrader** är inte tillgänglig på försäljningsorder eller försäljningsofferter.
> * Du kan inte filtrera på **leveranskoden** eller **kontaktnr.** .

## <a name="invoice-one-or-more-customers-for-project-tasks"></a>Skapa ett projektkort

Du skapar ett projektkort och sedan skapar projektaktivitetsrader och projektplaneringsrader för det.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Projekt** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. För att basera projektet på information från ett annat projekt väljer du åtgärden **Kopiera projekt**, fyller i fälten efter behov och väljer sedan knappen **OK**.

> [!NOTE]  
> Om du använder tidrapporter i projektet måste du också ange en person som ansvarar. Denna person kan godkänna tidrapporter för anställdas aktiviteter som är kopplade till projektet. Mer information finns i [Skapa tidrapporter](projects-how-setup-time-sheets.md).

Om du vill kan du markera åtgärder i projekt som spärrade med fältet **spärrad**. följande tabell beskriver effekten av alternativen för detta fält.

|Alternativ  |Description  |
|---------|---------|
|Tom |Alla åtgärder tillåts.|
|Bokföra    |Du kan arbeta med planeringsrader, men projektet är spärrat för bokföring. Om du väljer det här alternativet innebär det att du inte kan bokföra någon förbrukning eller försäljning för projektet.|
|Alla  |Alla åtgärder är spärrade.|

## <a name="specify-a-default-location-for-project-items"></a>Skapa aktiviteter för ett projekt

En viktig del när du skapar ett projekt är att ange de olika aktiviteter som ingår i projektet. Du anger uppgifter genom att skapa en rad per uppgift på snabbfliken **Uppgifter** på sidan **Projektkort**. Varje projekt måste ha minst en aktivitet.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Projekt** och välj sedan relaterad länk.
2. Öppna projektkortet för ett relevant projekt.
3. På snabbfliken **Uppgifter** fyller du i fälten efter behov på en ny rad.
4. Om du vill dra in uppgifter och skapa en hierarki väljer du åtgärden **Uppgifter** och sedan väljer du åtgärden **Indrag för projektaktiviteter**.
5. Upprepa steg 3 och 4 för alla de aktiviteter som du behöver för projektet.
6. Om du vill ange projektaktiviteter med information om andra projektaktiviteter väljer du åtgärden **Kopiera projektaktiviteter från**, fyller i fälten efter behov och väljer sedan knappen **OK**.

## <a name="to-create-planning-lines-for-a-project"></a>Så här skapar du en planeringsrad för ett projekt

Du kan förfina dina nya projektaktiviteter på projektplaneringsrader. En planeringsrad kan används för att samla in den information som du vill spåra för ett projekt. Du kan t.ex. spåra de resurser som krävs av projektet eller vilka artiklar som behövs. Du har till exempel en uppgift för att få en kund att godkänna ett projekt. Du kan associera den aktiviteten med planeringsrader för objekt som att träffa kund och tilldela en resurs.  

En projektplaneringsrad kan ha en av följande typer.  

| Kontakttyp | Description |
| --- | --- |
| **Budget** |Anger uppskattad förbrukning och kostnader för projektet, vanligtvis i tids- och materialtypsprojekt. Du kan inte fakturera planeringsrader av den här typen. |
| **Fakturerbart** |Anger uppskattad fakturering till kunden, vanligtvis som ett fastprisprojekt. |
| **Både Budget och Fakturerbart** |Anger budgeterad förbrukning som motsvarar vad du vill fakturera. |

> [!NOTE]
> När du anger information på projektplaneringsrader fylls kostnadsinformationen i automatiskt. t. ex. baseras kostnaden, priset och rabatten för resurser och artiklar inledningsvis på informationen som definieras på resurs och artikel.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Projekt** och välj sedan relaterad länk.
2. Öppna ett relevant projektkort.
3. Markera ett projekt där fältet **Typ av projektaktivitet** innehåller **Bokföring** och klicka sedan på åtgärden **Projektplaneringsrader**.  
4. På sidan **Projektplaneringsrader**, på en ny rad, fyller du i fält efter behov.
5. Upprepa steg 3 och 4 för alla de planeringsrader som du behöver för projektaktiviteten.

## <a name="see-also"></a>Se även

[Projekthantering](projects-manage-projects.md)  
[Video: Hur du skapar du ett projekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
