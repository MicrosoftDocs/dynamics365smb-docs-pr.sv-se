---
title: "Så här skapar du arbetsflöden | Microsoft Docs"
description: "Du kan skapa arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cab6546e152ad91c1b3264fa8bd10c0fd668636d
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-workflows"></a>Skapa arbetsflöden
Du kan skapa arbetsflöden som kopplar affärsprocessuppgifter som ska utföras av olika användare. Systemuppgifter, till exempel automatisk bokföring, kan inkluderas som ett steg i arbetsflöden, före eller efter användaruppgifter. Begära och bevilja godkännande för att skapa eller bokföra nya poster är vanliga arbetsflödessteg.  

I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar med svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden.  

När du skapar arbetsflöden kan du kopiera stegen från befintliga arbetsflöden eller från arbetsflödesmallar. Arbetsflödesmallar representerar icke-redigerbara arbetsflöden som finns i den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Koden för arbetsflödesmallar som läggas till av Microsoft har prefixet ”MS-”, till exempel "MS-PIW”. Mer information finns i [Skapa arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).  

Om ditt företagsscenario kräver arbetsflödehändelser eller svar som inte stöds måste en Microsoft-partner implementera dem genom att anpassa applikationskoden.  
  
> [!NOTE]  
>  Alla meddelanden om arbetsflödessteg skickas via en jobbkö. Se till att jobbkön i din installation är konfigurerad för att hantera arbetsflödemeddelanden och att kryssrutan **Starta automatiskt från NAS** är markerad. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-workflow"></a>Skapa ett arbetsflöde  
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**. Fönstret **arbetsflöde** öppnas.  
3. Ange högst 20 tecken för att identifiera arbetsflödet i fältet **Kod**.  
4. Så här skapar du arbetsflödet från en arbetsflödesmall **Arbetsflöden**, välj åtgärden **Så här skapar du arbetsflödet från en arbetsflödesmall**. Mer information finns i [Skapa arbetsflöden genom att använda arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md).  
5. Beskriv arbetsflödet i fältet **Beskrivning**.  
6. I fältet **kategorin** ange kategorin som arbetsflödet tillhör.  
7. I fältet **När händelse** ange den händelse som måste uppstå för att starta arbetsflödessteget.  

    När du väljer fältet öppnas fönstret **Arbetsflödeshändelse** där du kan välja mellan alla arbetsflödeshändelser som finns  
8. I fältet **Tillstånd** skriver du ett eller flera villkor som måste uppfyllas innan händelsen i fältet **När händelse** kan uppstå.  

    När du väljer fältet öppnas fönstret **Händelseförhållanden** där du väljer från en lista med filterfält som är relevanta som villkor för händelsen i fråga. Du kan lägga till nya filterfält som du vill använda som händelsevillkor. Du ställer in händelsevillkorfilter så som du ställer in filter på rapportsidor.  

    Om arbetsflödeshändelsen är ändringen av ett visst fält i en post, då öppnas fönstret **Händelsevillkor** med alternativ för att markera fältet och typen av ändring.  

    1.  Så här anger du en fältändring för händelsen: i fönstret **Händelsevillkor**, i fältet **Fält**, markerar du det fält som ska ändras.  
    2.  Välj antingen **Minskad**, **Ökad**eller **Ändrad** i fältet **Operatör**.  
9. I fältet **Sedan svar** anger du svaret som ska följa när arbetsflödeshändelsen inträffar.  

     När du väljer fältet öppnas fönstret **Arbetsflödessvar** där du kan välja mellan alla arbetsflödessvar som finns och ange svarsalternativ för det valda svaret.  
10. På snabbfliken **Alternativ för valt arbetsflödessvar** anger du alternativ för arbetsflödessvaret genom att välja värden i de olika fälten som visas, enligt följande:  

    1.  Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skicka ett meddelande.  

        |Fält|Description|  
        |----------------------------------|---------------------------------------|  
        |**Mottagarens användar-ID**|Ange den användare som meddelande ska skickas till. Obs! Alternativet är bara tillgängligt för arbetsflödesvar med en platshållare för en specifik användare. För arbetsflödesvar utan platshållare för användare definieras meddelandemottagaren vanligtvis av inställningen av godkännandeanvändare.|  
        |**Målsida för länk**|Ange en annan sida i [!INCLUDE[d365fin](includes/d365fin_md.md)] som länken i meddelandet öppnar i stället för standardsidan.|  
        |**Anpassad länk**|Ange URL-adressen till en länk som läggs till i meddelandet utöver länken till sidan i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    2.  Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skapa en godkännandebegäran.  

        |Fält|Description|  
        |----------------------------------|---------------------------------------|  
        |**Formel för förfallodatum**|Ange hur många dagar det är kvar tills godkännandebegäran måste lösas från datumet då det skickades.|  
        |**Delegera efter**|Ange om och när en godkännandebegäran delegeras automatiskt till den relevanta ersättaren. Du kan välja att automatiskt delegera en, två eller fem dagar efter datumet när godkännandet begärdes.|  
        |**Godkännartyp**|Ange vem godkännaren är, enligt inställningarna av godkännandeanvändare och arbetsflödesanvändare.<br /><br /> Följande alternativ finns:<br /><br /> -   **Säljare/Inköpare** anger att användaren som ställs in i fältet **Säljare/inköpare kod** i fönstret **Användarinställningar för godkännande** fastställer godkännaren. Godkännandebegäranposter skapas sedan enligt värdet i fältet **Gränstyp för godkännare**.<br />     Mer information finns i [Konfigurera godkännandeanvändare](across-how-to-set-up-workflow-users.md).|  
        |**Visa bekräftelsemeddelande**|Ange om ett bekräftelsemeddelande visas för användarna när de har begärt ett godkännande.|  
        |**Gränstyp för godkännare**|Ange hur godkännares godkännandegränser påverkas när godkännandebegärandeposter skapas för dem. En kvalificerad godkännare är en godkännare vars godkännandegräns är högre än värdet på begäran.<br /><br /> Följande alternativ finns:<br /><br /> 1. **Godkännarkedja** anger att godkännandebegärandeposter skapas för alla begärandens godkännare upp till och med den första kvalificerade godkännaren.<br />2. **Direkt godkännare** anger att en godkännandebegärandepost skapas endast för begärandens omedelbara godkännare, oberoende av godkännarens godkännandegräns.<br />3. **Första kvalificerade godkännare** anger att en godkännandebegärandepost skapas endast för begärandens första kvalificerade godkännare.<br />|  
    3.  Fyll i fälten som beskrivs i följande tabell för att ange alternativ för arbetsflödesvar som omfattar att skapa journalrader.  

        |Fält|Description|  
        |----------------------------------|---------------------------------------|  
        |**Namn på redovisningsjournalmall**|Ange namnet på redovisningsjournalmallen som de angivna journalraderna skapas i.|  
        |**Redovisningsjournalnamn**|Ange namnet på redovisningsjournalbatchen som de angivna journalraderna skapas i.|  

11. Välj knapparna **Öka indrag** och **Minska indrag** för att göra ett indrag för händelsenamnet i fältet **När** för att definiera stegets position i arbetsflödet.  
    1.  Ange att steget är nästa i arbetsflödesföljden genom att göra ett indrag för händelsenamnet i det föregående steget.  
    2.  Ange att steget är ett av flera alternativa steg som kan startas beroende på dess villkor genom att placera händelsenamnet med samma indrag som de andra alternativa stegen. Ordna sådana valfria efter prioritet genom att placera det viktigaste steget först.  

    > [!NOTE]  
    >  Du kan endast ändra indrag för ett steg som inte har ett efterföljande steg.  

12. Upprepa steg 7 till 11 för att lägga till fler arbetsflödessteg, antingen före eller efter steget som du precis har skapat.  
13. Markera kryssrutan **Aktiverad** för att ange att arbetsflödet ska starta så snart som händelsen i det första steget av typen **Insteg** inträffar. Mer information finns i [Använda arbetsflöden](across-use-workflows.md).  

> [!NOTE]  
>  Aktivera inte ett arbetsflöde förrän du vet att arbetsflödet är avslutat och att relevanta arbetsflödessteg kan startas.  

> [!TIP]  
>  För att visa relationer mellan tabeller som används i arbetsflöden, välj ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten") och ange **arbetsflöde – tabellrelationer**.  

## <a name="see-also"></a>Se även  
[Skapa arbetsflöden från arbetsflödesmallar](across-how-to-create-workflows-from-workflow-templates.md)   
[Konfigurera användare för godkännande](across-how-to-set-up-approval-users.md)   
[Konfigurera meddelanden för arbetsflödet](across-setting-up-workflow-notifications.md)   
[Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)   
[Ta bort arbetsflöden](across-how-to-delete-workflows.md)   
[Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
[Konfigurera arbetsflöden](across-set-up-workflows.md)   
[Använda arbetsflöden](across-use-workflows.md)   
[Arbetsflöde](across-workflow.md)      


