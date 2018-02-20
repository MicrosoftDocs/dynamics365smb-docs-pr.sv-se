---
title: "Så här använder du fördelningsnycklar i redovisningsjournaler | Microsoft Docs"
description: "Lär dig hur du kan använda fördelningsnycklar i journaler."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6ee3e0f325623666eb720e3cc2656cfd1f6332eb
ms.contentlocale: sv-se
ms.lasthandoff: 01/30/2018

---
# <a name="use-allocation-keys-in-general-journals"></a>Så här använder du fördelningsnycklar i redovisningsjournaler
Du kan fördela en transaktion i en redovisningsjournal på flera olika konton när du bokför journalen. Fördelningen kan göras efter kvantitet, procentuellt eller med ett belopp.

## <a name="to-set-up-allocation-keys"></a>Så här skapar du fördelningsnycklar
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Återkommande redov.journal** och välj sedan relaterad länk.
2. Välj fältet **Journalnamn** för att öppna fönstret **redovisningsjournaler**.
3. Du kan antingen ändra fördelningar på en befintlig journal i listan eller skapa en ny journal med fördelningar.
   * För att skapa en y journal väljer du åtgärden **Ny** och går vidare till nästa steg för att skapa en ny journal.
   * Välj journalen och gå till steg 7 för att ändra fördelningar av en befintlig journal.    
4. I fältet **Namn** anger du ett namn för journalens som t.ex. RENSNING. I fältet **beskrivning** anger du en beskrivning som t.ex. Rensning av utläggsjournal.
5. Stäng fönstret när du är klar. En ny, tom återkommande journal öppnas.
6. Fyll i fälten på raden.
7. Välj åtgärden **Fördelningar**.
8. Lägg till en rad för varje fördelning. Du måste fylla i fältet **Fördelning %**, **Fördelningskvantitet** eller **Belopp**. Du måste också fylla i fältet **Nr** och, om du fördelar transaktionen bland globala dimensioner, fälten för globala dimensioner.
9. Om du anger ett värde i procent på en rad beräknas beloppet i fältet **Belopp** automatiskt. Dessa belopp har motsatt tecken mot det totala beloppet i fältet **Belopp** i den återkommande journalen.
10. Välj **OK** för att återgå till fönstret **Återkommande redov.journal** fönstret, när du har angett fördelningsraderna. Fältet **Fördelat belopp (USD)** är ifyllt och matchar fältet **Belopp**.
11. Bokför journalen.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>För att ändra en fördelningsnyckel som redan har angetts.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Återkommande redov.journal** och välj sedan relaterad länk.
2. Välj journalen med fördelningen i fältet **Återkommande redov.journal**.
3. Välj raden med fördelningen och välj sedan åtgärden **fördelningar**.
4. Fyll i de relevanta fälten och välj sedan knappen **OK**.

## <a name="see-also"></a>Se även
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Bokför dokument och journaler](ui-post-documents-journals.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

