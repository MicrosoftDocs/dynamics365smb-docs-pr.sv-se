---
title: Flöde för användaråtkomst för Microsoft 365-licenser
description: Få en översikt över vad som händer när en användare kommer åt Business Central-data med hjälp av deras Microsoft 365-licens för första gången.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft-365-licenses" />Flöde för användaråtkomst för Microsoft 365-licenser

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Denna artikel beskriver vad som händer när en användare kommer åt Business Central-data med hjälp av deras Microsoft 365-licens för första gången. Med hjälp av det här flödet kan administratörer planera sina inställningar och konfigurera Business Central så att de överensstämmer med deras företags behov.

1. Först autentiseras användarens identitet 
2. Business Central kontrollerar att alla [minimikrav](admin-access-with-m365-license.md#minimum-requirements) uppfylls.
3. Business Central kontrollerar att användaren inte har en högre licens, till exempel en Business Central-licens eller en administrativ roll som en delegerad administratörsroll. 
4. Business Central kontrollerar om användaren har åtkomst till data som tillhör en miljö som har aktiverat åtkomst med Microsoft 365-licenser. 
5. Användarposten etableras i Business Central och tilldelar den användargrupp, profil och behörighetsgrupper som definierats på sidan för Microsoft 365-licenskonfiguration. Som standard tilldelas Teams-användarens användargrupp, medarbetarprofilen och endast den angivna inloggningsbehörigheten. Alla andra inställningar används även som standard, precis som licensierade användare av Business Central. 
6. Den fullständiga Business Central säkerhetsmodellen används för att avgöra om användaren ska kunna komma åt posten, sidan, i det angivna företaget och i den angivna miljön. 

Om alla åtgärder lyckas kan användaren nu visa dessa Business Central-data i Teams. Business Central-tjänsten säkerställer automatiskt skrivskyddad åtkomst och förenklar användargränssnittet. 

Användarkontot är nu registrerat i Business Central och kan hanteras som vilken företagsanvändare som helst.

> [!NOTE]
> Stegen kan variera beroende på vilken ytterligare säkerhetskonfiguration du har angett i Microsoft 365 eller Business Central.

## <a name="see-also" />Se även

[Business Central-åtkomst med Microsoft 365-licenser](admin-access-with-m365-license.md#minimum-requirements)  
[Ställ in åtkomst med Microsoft 365-licenser](admin-access-with-m365-license-setup.md)  
