---
title: "Visa och redigera grundläggande inställningar i Financials | Microsoft Docs"
description: "Lär dig hur du ändrar några av de grundläggande inställningarna i Financials, till exempel, rollcenter, företag eller arbetsdatumet."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: f71b0e7d53138be0f89abe4e7935ab7c21437d8e
ms.contentlocale: sv-se
ms.lasthandoff: 05/28/2018

---
# <a name="changing-basic-settings"></a>Ändra grundinställningar
I fönstret **Mina inställningar** kan du visa och ändra grundläggande inställningar för [!INCLUDE[d365fin](includes/d365fin_md.md)]. De ändringar du gör påverkar bara din arbetsyta, inte arbetsytor för andra användare.  

## <a name="role-center"></a>Rollcenter
Rollcentret representerar startsidan, en startskärm som har utformats för den specifika rollens behov i en organisation. Beroende på din roll ger rollcentret en översikt över verksamheten, din avdelning eller dina personliga uppgifter. Du kan också navigera till ditt dagliga arbete och söka efter arbete som har tilldelats dig.

-   Längst upp låter navigeringen dig växla mellan kunder, leverantörer, artiklar och andra viktiga listor med information. På samma sätt kan du starta aktiviteter, såsom skapa en ny försäljningsfaktura direkt från Rollcentret.

-   I centret hottar du **Aktiviteter**. Aktiviteter visar aktuella data och kan klickas om du vill ha mer detaljerad information. Nyckelindikatorer kan ställas in att visa ett valt diagram för en visuell representation av till exempel kassaflöde eller intäkter och kostnader. Du kan också att upprätta en lista över favoritkunder på startsidan för konton som du arbetar med ofta eller behöver ge extra uppmärksamhet till.

### <a name="to-change-role-center"></a>Så här ändrar du rollcentret
Standardrollcentret är **Chef**, men du kan välja ett annat rollcenter som passar bättre till dina önskemål.
1. I det övre högra hörnet väljer du ikonen **inställningar** ![inställningar](media/ui-experience/settings_icon_small.png "ikonen för inställningar för rollcenter"), och välj **Mina inställningar**.
2. I fönstret **Mina inställningar** i fältet **Rollcenter** väljer du det rollcenter som du vill ange som standard. Välj till exempel **Revisor**.
3. Välj knappen **OK**.

## <a name="company"></a>Företag
Ett företag fungerar som en behållare för data i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det kan finnas åtskilliga företag i en databas, men endast ett kan väljas i taget.

Standardföretaget kallas CRONUS och innehåller endast demonstratiosdata.

> [!TIP]  
>   Om du vill visa ett annat namn för ditt företag i programmet (till exempel på startsidan för rollcenter) anger du fältet **Namn** på sidan **Företagsinformation** eller fältet **Visningsnamn** på sidan **Företag**.  

## <a name="work-date"></a>Arbetsdatum
Standardarbetsdatumet är vanligen dagens datum. För att utföra uppgifter som att slutföra transaktioner för ett datum som inte är aktuellt datum, kan det vara nödvändigt att tillfälligt ändra arbetsdatumet.

> [!TIP]  
>   Skriv **w** för att snabbt ange arbetsdatumet i datumfältet. Skriv **t** för att snabbt ange det aktuella datumet i datumfältet.

> [!IMPORTANT]  
>   Arbetsdatumet ändras endast till dess att du avslutar företaget eller datumet ändras. Om du öppnar ett annat företag eller öppnar företaget nästa dag, och fortfarande behöver använda ett annat arbetsdatum, måste du ange arbetsdatumet igen.

## <a name="region"></a>Region
Inställningen **Region** bestämmer hur datum, tid, tal och valutor visas eller formateras.   


## <a name="language"></a>Språk
Ändra displayspråk. Det här fältet visas bara om det finns flera språk att välja mellan. 

Startspråket bestäms antingen av administratören eller i webbläsaren när du registrerar dig för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det språk som du anger används för alla enheter som du loggar in från, till exempel en telefon eller surfplatta. 

## <a name="changing-when-i-receive-notifications"></a>Ändra när jag får meddelanden
Välj den här länken för att visa eller ändra meddelandena som du får om vissa evenemang eller stausändringar som t.ex. när du ska fakturera en kund som har en skuld som har förfallit, eller när det tillgängliga lagret är lägre än kvantiteten som du håller på att sälja. Mer information finns i [Smarta meddelanden](ui-smart-notifications.md).

## <a name="see-also"></a>Se även
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ändra vilka funktioner som visas](ui-experiences.md)  

