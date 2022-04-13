---
title: 'Felsökning: komma åt kamera och plats'
description: I den här artikeln beskrivs felsökning av åtkomst till kamera och platsinformation i Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.openlocfilehash: 5c5693b05d8590e569e0fb1b80993e35550c5ed5
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8518815"
---
# <a name="troubleshooting-accessing-camera-and-location"></a>Felsökning: komma åt kamera och plats

Det kan uppstå problem när du försöker komma åt kamera och platsinformation för en enhet [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan hitta möjliga orsaker till det här problemet och hur du kan undvika dem i listan nedan.

## <a name="device-must-have-camera-and-location-capabilities"></a>Enheten måste ha kamera och platsfunktioner

För att du ska kunna komma åt kameran eller en användares plats från en enhet måste enheten ha en fysisk kamera eller möjlighet att hämta platsinformation.

Om enheten har funktioner för kamera och plats, men det fortfarande uppstår problem, kan vissa drivrutiner behöva uppdateras eller installeras om. Även om du är osäker, rekommenderar vi alltid att du uppdaterar enhetens operativsystem, drivrutiner och webbläsare till den senaste versionen för bästa möjliga upplevelse.

## <a name="access-permissions-not-enabled"></a>Åtkomstbehörighet är inte aktiverad

Du måste aktivera allmän åtkomst till kamera och plats från enhetens sekretessinställningar och uttryckligen ge behörighet till [!INCLUDE[prod_short](includes/prod_short.md)] för åtkomst till dem. Om du till exempel vill visa eller ändra behörigheter för en enhet som körs på Windows går du till **Inställningar**, väljer **Sekretess** och sedan **Appbehörigheter**. 

För mobila enheter måste du ge den mobila appen åtkomstbehörighet för kamera och plats till [!INCLUDE[prod_short](includes/prod_short.md)] mobilapp. Om du vill göra det för en iOS-enhet går du till **inställningar**, väljer **sekretess** och sedan **kamera** eller **plats**. För Android enheter går du till **Inställningar**, välj **Appar och meddelanden**, **Avancerat**, **Behörighetshanteraren** och **Kamera** eller **Plats**.

Om du använder [!INCLUDE[prod_short](includes/prod_short.md)] i en webbläsare måste du också ge [!INCLUDE[prod_short](includes/prod_short.md)] webbplatsbehörighet att komma åt kameran eller platsinformationen. Om du vill visa eller ändra webbplatsbehörighet i Microsoft Edge webbläsaren, gå till **Inställningar**, välj **Webbplatsbehörigheter** och **Kamera** eller **Plats**. Observera att detta kan vara annorlunda i andra webbläsare.

Som standard dyker enheten eller webbläsaren upp en begäran om åtkomst till dessa funktioner när användaren aktiverar dem för första gången.

> [!NOTE]  
> Vissa äldre webbläsare ger inte tillgång till kameran och platsen. Kameran är till exempel inte tillgänglig i Internet Explorer eller den äldre Edge-webbläsaren.

## <a name="web-client-connection-not-secure"></a>Webbklient anslutning inte säker

Kamera- och platsfunktionerna är endast tillgängliga vid åtkomst till webbklienten via säkra SSL-anslutningar via SSL med hjälp av `https://` URI-schemat. 

Det enda undantaget anknyter till `http://localhost` används i utvecklings- och testsyfte.


## <a name="work-with-virtualization-technologies"></a>Arbeta med virtualiseringsteknik

När du ansluter till [!INCLUDE[prod_short](includes/prod_short.md)] via fjärrskrivbord eller en annan virtualisering kanske inte åtkomsten till kameran eller platsen är tillgänglig. Använd i så fall det fysiska systemet i stället.

## <a name="antivirus-software"></a>Antivirusprogram
Vissa antivirusprogram blockerar som standardåtkomst till kameran och platsen. Kom ihåg att kontrollera inställningarna för antivirusprogrammet.

## <a name="see-also"></a>Se även
[Implementera kameran i AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[Implementera platsen i AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]