---
title: "Hantera anpassning som administratör i Business Central | Microsoft Docs"
description: "Lär dig mer om att anpassa användargränssnittet så att det passar ditt sätt att arbeta."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 78eea4df6f25772063cef5770eb1dcb433bee012
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Hantera anpassning som administratör
<!--NAV in the Web client--> Användare kan anpassa sin arbetsyta efter eget behov. Som administratör kan du styra och hantera anpassning genom att inaktivera användare för att anpassa egna sidor och ta bort alla anpassningar på sidan som användare har gjort.

## <a name="disable-personalization-for-a-profile"></a>Inaktivera anpassningar för en profil
Du kan förhindra alla användare som tillhör en viss profil från att anpassa sidorna.
1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Profiler** och välj sedan relaterad länk.
2.  Välj den profil i listan som du vill ändra.
3. Välj kryssrutan **Inaktivera anpassning** och välj sedan knappen **OK**.

## <a name="clear-user-personalizations"></a>Rensa användaranpassning

Ta bort sidann för anpassningsändringar gör att sidan återställs till sin ursprungliga layout innan alla anpassningar gjordes. Det finns två sätt att ta bort de anpassningar som användare har gjort på sidor: med hjälp av fönstret **Ta bort användaranpassning** och använda fönstret **Anv.anpassningskort**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Ta bort användaranpassningar genom att använda sidan ta bort användaranpassning

Fönstret **Ta bort användaranpassning** låter dig ta bort anpassningen på per sida-basis, för varje enskild användare.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Ta bort användaranpassning** och välj sedan relaterad länk.

    Sidan visar en lista över alla sidor som har anpassats och användaren den tillhör.

    >[!NOTE]
    > Ett kryss i kolumnen **Äldre anpassning** anger att anpassningen har skett i en äldre version av [!INCLUDE[d365fin](includes/d365fin_md.md)], som hanterade anpassningen på ett annat sätt än som nu sker. Användare som försöker anpassa dessa sidor hindras från att göra detta såvida de inte väljer att låsa upp sidan. Mer information finns i [Anledningen till att anpassningen är låst för en sida](ui-personalization-locked.md).

2. Markera den transaktion som du vill radera och välj sedan åtgärden **Radera**.

    Användaren kommer att se ändringarna nästa gång de loggar in.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Ta bort användaranpassningar genom att använda sidan användaranpassningskort

Fönstret **Anv.anpassningskort** låter dig ta bort anpassningen på alla sidor för en specifik användare. Detta kräver skrivbehörighet för tabellen 2000000072 **Profil**.

1.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Användaranpassning** och välj sedan relaterad länk.

    Fönstret **användaranpassning** visar alla användare som eventuellt har anpassade sidor. Om du inte hittar en användare i listan, innebär det att de inte har några anpassade sidor.

2. Välj den användare från listan, välj åtgärden **Redigera**.

3.  På fliken **Åtgärder**, välj **Ta bort anpassade sidor**.

    Användaren kommer att se ändringarna nästa gång de loggar in.

## <a name="see-also"></a>Se även
[Anpassa din arbetsyta](ui-personalization-user.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

