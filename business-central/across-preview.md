---
title: "Hämta förhandsgranskningen för nya marknader"
description: "Lär dig hur du får tillgång till förhandsgranskningar för Business Central."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: preview, trial, sandbox
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 50d1429a58b878766c76ed97f65936db78191ee0
ms.contentlocale: sv-se
ms.lasthandoff: 09/28/2018

---
# <a name="access-to-the-included365finlongincludesd365finlongmdmd-preview"></a>Åtkomst till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-förhandsgranskningen
Från och med våren 2018 kommer [!INCLUDE[d365fin](includes/d365fin_md.md)] att bli tillgängligt i nya länder. För att säkerställa att [!INCLUDE[d365fin](includes/d365fin_md.md)] är den bästa lösningen för dessa kunder erbjuder vi en förhandsgranskning av tjänsten före lanseringen i vår. Förhandsgranskningen för Danmark blev tillgänglig i januari 2018, och ytterligare marknader följer snart.  

## <a name="getting-started-with-previews-and-sandboxes"></a>Komma igång med förhandsgranskning och begränsat läge
Förhandsgranskningar och begränsade lägen gör det enkelt att komma igång med [!INCLUDE[d365fin](includes/d365fin_md.md)]. End förhandsgranskningsinstans innehåller funktioner som går utöver vad som är tillgängligt i den aktuella versionen. Förhandsgranskningen ger partners och kunder möjlighet att testa och ge feedback om funktioner som vi överväger att släppa. Även om förhandsgranskningar främst är avsedda för partners, får även kunder gärna använda dem under en begränsad tid. Den aktuella förhandsvisningen av [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller de flesta funktioner som finns i Dynamics NAV 2018, vilket som regel kräver lite hjälp från en partner att konfigurera.

För att skapa en förhandsgranskning går du till [denna sida](https://go.microsoft.com/fwlink/?linkid=866045) och anger din e-postadress för arbete. Mer information om [!INCLUDE[d365fin](includes/d365fin_md.md)] och de funktioner det erbjuder finns i dokumentationen på den här webbplatsen.

Du kan se ett begränsat läge som en produktionsfri miljö som du kan använda utöver din produktions- eller förhandsgranskningsinstans av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ett begränsat läge låter dig skapa och testa tillägg och utveckla nya funktioner i syfte att anpassa tjänsten utan att påverka data och inställningar för produktions- eller förhandsgranskningsinstanser. Just nu kan alla kunder med en produktions- eller förhandsgranskningsversion använda ett begränsat läge.

Mer information om hur du kommer igång med ett begränsat läge finns nedan.

## <a name="creating-a-sandbox-environment"></a>Skapa en miljö för begränsat läge
Du måste ha en prenumeration på [!INCLUDE[d365fin](includes/d365fin_md.md)] för att arbeta i begränsat läge. Det kan bara finnas ett begränsat läge per prenumeration.

### <a name="advanced-functionality-available-in-a-sandbox-environment"></a>Avancerade funktioner i miljöer med begränsat läge
Miljöer med begränsat läge innehåller en klientintern designerfunktion som gör det möjligt att utforma sidor med hjälp av ett dra-och-släpp-gränssnitt samt att skapa tillägg i själva klienten genom att lägga till och ordna om fält.

Mer information finns i [Använda designern](https://docs.microsoft.com/en-us/dynamics-nav/developer/devenv-inclient-designer).

### <a name="to-create-a-sandbox-environment"></a>Skapa miljö för begränsat läge.
1.  Logga in i din produktions- eller förhandsvisningsinstans av [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Miljö för begränsat läge** och välj sedan relaterad länk.
3.  Välj **Skapa**. En flik öppnas där du kan avsluta konfigureringen av ditt begränsade läge.

    > [!Note]
    > Om en popup-blockerare aktiverats i din webbläsare, ändra då så att den tillåter URL-adresser tillåts från adressen *.businesscentral.dynamics.com*.  

4.  En välkomstsida visas när det begränsade läget är klart.  
5.  Om du vill läsa om scenarier som du kan testa i ett begränsat läge, till exempel hur du utvecklar tillägg, väljer du länk **Mer information**. Klicka annars på **Stäng** för att fortsätta till rollcentret för din begränsade [!INCLUDE[d365fin](includes/d365fin_md.md)]-instans.  
6.  Högst upp i Rollcentret visas ett meddelande för att informera dig om att begränsat läge råder. Du kan också se miljötypen i namnlisten på klienten.

    > [!Note]
    > Det begränsade läget innehåller demonstrationsdata för det fiktiva företaget CRONUS. Inga data kopieras till eller på annat sätt överförs från produktionsmiljön.  

7.  Du kan när som helst återgå till sidan för begränsat läge och återställa det begränsade läget.

    > [!Note]
    > Återställning av ett begränsat läge tar bort det helt och hållet, och skapar sedan om et igen med standarddemonstrationsdata.  

8.  Använd menyn Dynamics 365 eller Dynamics-startsidan om du vill växla mellan din produktionsmiljö och begränsat läge.

    > [!Note]
    > En administratör eller en annan användare kan begränsa eller till och med blockera åtkomst till sandlådan via standardsäkerhetsfunktionerna i [!INCLUDE[d365fin](includes/d365fin_md.md)], exempelvis användarkort, användargrupper och behörighetsgrupper.  

### <a name="building-new-solutions-and-intellectual-property"></a>Skapa nya lösningar och immateriella rättigheter
[!INCLUDE[d365fin](includes/d365fin_md.md)] har en uppsättning utvecklingsverktyg och en modern plattform att bygga vidare på så att du kan skapa egna tilläggsprogram inbäddade lösningar för att ansluta eller utöka [!INCLUDE[d365fin](includes/d365fin_md.md)].

[!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller verktyg som du kan använda för att implementera egna tillägg och bädda in funktioner i syfte att lägga till nya, branschspecifika slutpunkt-till-slutpunkt-lösningar eller integrera tredjepartslösningar. Till exempel kan du använda en API för att skapa ett anslutet program i syfte att utbyta data mellan [!INCLUDE[d365fin](includes/d365fin_md.md)] och din löneapp. Ansluta appar har också användning av tillägg i syfte att skapa sidor som ska användas för installation, konfiguration eller app-specifika funktioner. Mer information finns i [Utveckla appar för [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://aka.ms/getstartedwithapps).

## <a name="see-also"></a>Se även
[Komma igång](product-get-started.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

