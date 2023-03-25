---
author: edupont04
ms.topic: include
ms.date: 05/09/2022
ms.author: edupont
---
Det kan hända att du ser andra användare i listan **Användare** än bara de från ditt eget företag. När en utsedd administratör från en återförsäljarpartner loggar in på en [!INCLUDE [prod_short](prod_short.md)]-miljö på uppdrag av sin kund, skapas han/hon automatiskt som en användare i [!INCLUDE [prod_short](prod_short.md)]. På så sätt loggas de åtgärder som utförs av en utsedd administratör i [!INCLUDE [prod_short](prod_short.md)], t.ex. publicering av dokument, och kopplas till dennes användar-ID.  

Med *detaljerade administratörsprivilegier (GDAP)* visas användaren i listan **Användare** och kan tilldelas alla behörigheter. De visas inte med namn och annan personlig information, utan med företagsnamnet och ett unikt ID. Både interna och externa administratörer kan se dessa användare i listan **Användare** och de har full insyn i vad dessa användare gör i till exempel [ändringsloggen](../across-log-changes.md). Men de kan inte se användarnas verkliga namn. GDAP-användare listas med användarnamn i följande format: `User123456@partnerdomain.com`. De kan ha ett användarnamn som motsvarar partnerns företagsnamn och e-postadressen är inte personens faktiska e-postadress. På så sätt avslöjar inte GDAP-användarkonton personlig information. Om du behöver ta reda på vilken person som ligger bakom en sådan pseudonym måste du kontakta det företag som den här användaren arbetar med.  
