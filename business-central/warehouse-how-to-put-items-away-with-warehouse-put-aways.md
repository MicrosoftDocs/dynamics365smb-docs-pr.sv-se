---
title: 'Så här: Införa artiklar med dist.lager artikelinförsel | Microsoft Docs'
description: När lagerstället kräver både inleverans- och artikelinförselbearbetning för distributionslagret använder du funktionen för distributionslagerartikelinförseldokumenten för att styra hur artiklar införs.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f9c1e144e5574e04d1d5baec039d3f358839631e
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881660"
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Föra in artiklar med lagerartikelinförsel
När lagerstället kräver både inleverans- och artikelinförselbearbetning för distributionslagret använder du funktionen för distributionslagerartikelinförseldokumenten för att styra hur artiklar införs.  

När du bokför en lagerinleverans uppdateras källdokumenten automatiskt, t.ex. inköpsorder, ankommande överföring eller försäljningsreturorder, varefter inlevererat antal bokförs i artikelregistret och raderna om de inlevererade artiklarna skickas till artikelinförselfunktionen i lagret. Om du använder intern artikelinförsel och plockning kan den interna artikelinförseln också skapa rader för artikelinförsel.  

Beroende på hur lagret har ställts in görs raderna antingen tillgängliga för artikelinförselkalkylarket eller så används de för att skapa instruktioner för artikelinförsel direkt. Mer information finns i [Planera artikelinförsel i kalkylark](warehouse-how-to-plan-put-aways-in-worksheets.md).  

Förutom standardsätten att skapa artikelinförslar i distributionslagret, som beskrivs i det här avsnittet, kan du skapa en artikelinförsel från den relaterade bokförda distributionslagerinleveransen. Detta är användbart om har tagit bort artikelinförselrader, eller om du använder dirigerad artikelinförsel och plockning och har bestämt dig för att inte använda artikelinförselkalkylarket, kan du skapa eller på nytt skapa artikelinförselanvisningar för bokförda inleveransrader.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>Så här för du in artiklar utan dirigerad artikelinförsel och plockning  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelinförslar** och välj sedan relaterad länk.  
2.  Öppna dist.lager artikelinförsel som är klara att hantera.  

    Du kan sortera Artikelinförselrader efter flera villkor, till exempel efter artikel, hyllnummer eller förfallodatum, och på så sätt optimera artikelinförselprocessen.  
3.  På varje rad Anger du hur stort antal som ska införas i fältet **Ant. att hantera**.  
4.  När du är klar och alla artiklarna har förts in klickar du på åtgärden **Registrera artikelinförsel** för att registrera artikelinförseln och göra artiklarna tillgängliga för plockning.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>Så här för du in artiklar med dirigerad artikelinförsel och plockning  
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Artikelinförslar** och välj sedan relaterad länk.
    Om instruktioner för artikelinförseln skapats visas en lagerartikelinförsel.  
2.  Öppna Dist.lager artikelinförsel som du vill arbeta med.  
3.  Om distributionslagret kräver det anger du ditt användar-ID på snabbfliken **Allmänt** när du börjar arbeta med en särskild artikelinförsel.  
4.  Utför åtgärderna "Ta" och "Placera" som indikeras i fältet **Åtgärdstyp** på raderna.  

    Observera att varje inleveransrad har omvandlats till minst två rader i lagerartikelinförseln:  

    -   Den första raden, med **Ta** i fältet **Åtgärdstyp**, anger var artiklarna finns i inleveransområdet. Du kan inte ändra zon- och lagerplatsfältet på den här raden.  
    -   Nästa rad, med **Plats för** i **Åtgärdstyp** fältet, anger var du måste placera artiklarna i lagret. Om distributionslagret har fått ett stort antal artiklar på en enda inleveransrad, kanske de måste föras in på flera lagerplatser, så det finns en Plats rad för varje lagerplats.  

        Om raderna för Ta och Placera för varje inleveransrad inte visas direkt efter varandra och det är så du vill att de ska visas, kan du sortera raderna genom att välja **Artikel** i fältet **Sorteringsmetod** på snabbfliken **Allmänt**.  

        Om lagrets fysiska struktur återspeglar lagerplatsernas ordning kan du använda sorteringsmetoden **Lagerplatsordning** för att förbereda en artikelinförsel, som minimerar antalet steg i lagerprocessen.  

5.  När du har placerat alla artiklarna på lagerplatser enligt anvisningarna, välj åtgärden **Registrera artikelinförsel**.  

Vid lagerställen som är inställt på dirigerad artikelinförsel och plockning, följande inställningar är nödvändig för den process som beskrivs ovan:  

- En artikelinförselmall skapas. Mer information finns i [Skapa artikelinförselsmallar](warehouse-how-to-set-up-put-away-templates.md).  
- vikten, volymen och särskilda lagerkrav för artikeln eller lagerställeenheten definieras. Mer information finns i Bruttovikt.  
- lagerplatsernas kapacitet, typ och prioritet. Mer information finns i Lagerplatsordning.  

Lagerplatsordningen beaktas när fler än en lagerplats matchar villkoren i artikelinförselmallen. Om både villkoren i artikelinförselmallen och lagerplatsordningen är samma för fler än en lagerplats väljs den lagerplats som har högst nummer.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Att skapa en artikelinförsel från en bokförd inleveransen  
 Om du använder både bearbetning av artikelinförsel och inleverans för lagerstället, måste du ta bort artikelinförselrader. Om du använder dirigerad artikelinförsel och plockning och har bestämt dig för att inte använda artikelinförselkalkylarket, kan du  skapa eller på nytt skapa artikelinförselanvisningar för bokförda inleveransrader.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Bokförda dist.lager inleveranser** och välj sedan relaterad länk.  
2.  Välj en bokförd inleverans som kan behöva föras in.  
3.  Välj åtgärden **Kort**.  

    Om fältet **Dokumentstatus** är tomt har inleveransen inte förts in alls. Annars visar det här fältet att Inleverans är delartikelinförsel eller färdig artikelinförsel.  

4.  Om inleveransen har införts delvis eller inte alls väljer du åtgärden **Skapa artikelinförsel**.  
5.  Fyll i sidan för begäran om batch-jobbet för att skapa artikelinförseln och klicka på **OK**.   

## <a name="see-also"></a>Se även  
[Lagerstyrning](warehouse-manage-warehouse.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)     
[Monteringshantering](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyrning](design-details-warehouse-management.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
