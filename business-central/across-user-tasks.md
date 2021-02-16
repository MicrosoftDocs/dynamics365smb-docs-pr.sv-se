---
title: Tilldela och hantera uppgifter
description: Lär dig hur du tilldelar uppgifter till användare i Business Central – till exempel din revisor – samt hur du hämtar och slutför uppgifter.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dd8b774f8dea2762df177ae141730cce8285480e
ms.sourcegitcommit: 1c9eec7554305603d688bf85ce3986d0b1f72ede
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/26/2021
ms.locfileid: "5068388"
---
# <a name="define-user-tasks"></a>Definiera användarens uppgifter

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du skapa uppgifter som påminner dig om arbetet som ska utföras. Du kan skapa uppgifter åt dig själv, men du kan också tilldela uppgifter till andra eller tilldela en uppgift för någon annan i organisationen.  

## <a name="managing-user-tasks"></a>Hantera användaruppgifter

Sidan **användaruppgifter** visar alla uppgifter och du kan enkelt skapa och tilldela nya uppgifter. När du skapar en uppgift kan du ange start- och förfallodatum och du kan lägga till en länk till sidan eller rapporten i [!INCLUDE[prod_short](includes/prod_short.md)] där användaren måste göra arbetet.  

Du kan till exempel skapa en uppgift för dig själv eller en medarbetare för att visa alla bokförda försäljningsfakturor. Om så är fallet kan du länka uppgiften till sidan 143, **Bokförda försäljningsfakturor**. På följande skärmbild skapar någon en uppgift för MeganB för att granska de bokförda försäljningsfakturorna.  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Exempel på en användaruppgift":::

> [!TIP]  
> Använd sökfunktionen i fältet **Sida** och använd fältet **Sök** för att hitta sidan du vill ha.  
>
> Du kan länka till vilken sida som helst, men du kan inte länka till enskilda poster, så gör beskrivningen så utförlig som möjligt, t.ex. "Ta en titt på kundnr 10 000 och kontrollera att de inte har förfallna betalningar.".

### <a name="picking-up-user-tasks"></a>Plocka upp användaruppgifter

I chef, bokföringsansvarig och rollcenter för redovisare visar en panel pågående uppgifter som har tilldelats den användaren. Om du vill välja en uppgift, väljer du den bara från listan över väntande användaruppgifter. I menyfliken öppnar länken **Gå till uppgiftsobjekt** sidan där du kan utföra arbetet.  

När du har slutfört en uppgift bara markerar du den som slutförd.  

### <a name="deleting-user-tasks"></a>Ta bort användaruppgifter

Om du vill ta bort flera eller vissa användaruppgifter kan du använda rapporten **ta bort aktiviteter för användare**. På formuläret för begäran lägger du till filter för att ta reda på vilka uppgifter som måste tas bort.  

## <a name="see-also"></a>Se även

[Sök efter sida eller rapport](ui-search.md)  
[Revisorupplevelse i [!INCLUDE[prod_short](includes/prod_short.md)]](finance-accounting.md)  
