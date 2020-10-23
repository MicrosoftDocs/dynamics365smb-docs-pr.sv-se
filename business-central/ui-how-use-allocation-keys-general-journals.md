---
title: Så här använder du fördelningsnycklar i redovisningsjournaler | Microsoft Docs
description: Lär dig hur du kan använda fördelningsnycklar i journaler.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: af18a94f5cf6b24b0da24821499e3866487207be
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918544"
---
# <a name="use-allocation-keys-in-general-journals"></a>Så här använder du fördelningsnycklar i redovisningsjournaler
Du kan fördela en transaktion i en redovisningsjournal på flera olika konton när du bokför journalen. Fördelningen kan göras efter kvantitet, procentuellt eller med ett belopp.

## <a name="to-set-up-allocation-keys"></a>Så här skapar du fördelningsnycklar
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Återkommande redovisningsjournal** och välj sedan tillhörande länk.
2. Välj fältet **Journalnamn** för att öppna sidan **redovisningsjournaler**.
3. Du kan antingen ändra fördelningar på en befintlig journal i listan eller skapa en ny journal med fördelningar.
   * För att skapa en y journal väljer du åtgärden **Ny** och går vidare till nästa steg för att skapa en ny journal.
   * Välj journalen och gå till steg 7 för att ändra fördelningar av en befintlig journal.    
4. I fältet **Namn** anger du ett namn för journalens som t.ex. RENSNING. I fältet **beskrivning** anger du en beskrivning som t.ex. Rensning av utläggsjournal.
5. Stäng sidan när du är klar. En ny, tom återkommande journal öppnas.
6. Fyll i fälten på raden.
7. Välj åtgärden **Fördelningar**.
8. Lägg till en rad för varje fördelning. Du måste fylla i fältet **Fördelning %**, **Fördelningskvantitet** eller **Belopp**. Du måste också fylla i fältet **Nr** och, om du fördelar transaktionen bland globala dimensioner, fälten för globala dimensioner.
9. Om du anger ett värde i procent på en rad beräknas beloppet i fältet **Belopp** automatiskt. Dessa belopp har motsatt tecken mot det totala beloppet i fältet **Belopp** i den återkommande journalen.
10. Välj **OK** för att återgå till sidan **Återkommande redov.journal** fönstret, när du har angett fördelningsraderna. Fältet **Fördelat belopp (USD)** är ifyllt och matchar fältet **Belopp**.
11. Bokför journalen.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>För att ändra en fördelningsnyckel som redan har ställts in
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Återkommande redovisningsjournal** och välj sedan tillhörande länk.
2. Välj journalen med fördelningen på sidan **Återkommande redov.journal**.
3. Välj raden med fördelningen och välj sedan åtgärden **fördelningar**.
4. Fyll i de relevanta fälten och välj sedan knappen **OK**.

## <a name="see-also"></a>Se även
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Bokför dokument och journaler](ui-post-documents-journals.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
