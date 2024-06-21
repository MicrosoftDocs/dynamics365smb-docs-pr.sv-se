---
title: Dela kontakter mellan Business Central och Outlook
description: Denna tjänst har djupgående integrering med Microsoft 365 så att du kan dela kontakter mellan Outlook och Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Synkronisera kontakter i Business Central med kontakter i Microsoft Outlook

Du kan ställa in synkronisering av kontakter så att kontakterna i [!INCLUDE[prod_short](includes/prod_short.md)] har samma information som dina kontakter i Microsoft Outlook. Om du t.ex. är säljare kan du arbeta i Outlook och [!INCLUDE[prod_short](includes/prod_short.md)] på samma gång. Om kontakterna är desamma på båda platser, är ditt arbete enklare.  

Som standard sparas de kontakter som du synkroniserar i en **Business Central**-mapp i favoriter i mappfönstret i Outlook. Business Central-mappen kan göra det enklare att identifiera vilka kontakter som ska synkroniseras. Du kan ange att filter endast ska synkronisera vissa kontakter från [!INCLUDE[prod_short](includes/prod_short.md)] till Outlook. När du har ställt in synkroniseringen kan du synkronisera manuellt eller automatisera den så att den synkroniseras enligt ett schema.  

## Förutsättningar

- Din användarprofil i [!INCLUDE[prod_short](includes/prod_short.md)] måste ange ditt e-postkonto för Microsoft 365.

  Du kan kontrollera denna inställning i avsnittet **Microsoft 365-autentisering** i din användarprofil i listan **Användare**.
- Med [!INCLUDE[prod_short](includes/prod_short.md)] har du ställt in synkronisering av kontakter enligt beskrivningen i [Konfigurera synkronisering av kontakter med Outlook för Business Central lokalt](admin-contact-sync-setup-onprem.md)

## Konfigurera synkronisering

Du kan ange hur du vill synkronisera kontakter med Outlook på sidan **Konfigurering av Exchange-synkronisering** i [!INCLUDE[prod_short](includes/prod_short.md)]. 

Sedan på sidan **Konfigurering av Exchange-synkronisering** kan du verifiera att anslutningen till Exchange fungerar och sedan skapa synkroniseringen av kontakter. Från sidan **Konfigurering av Exchange-synkronisering** kan du öppna sidan **Inställningar för kontaktsynkning** och starta synkroniseringen. Du kan även definiera ett filter för att ange vilka kontakter som ska synkroniseras. Du kan till exempel filtrera på namn, typ, företag och så vidare. Du kan också ändra standardnamnet på mappen i Outlook som kontakterna kommer att synkroniseras till.  

Var och en av dina medarbetare kan också ställa in sin egna Exchange-synkronisering och registrera egna filter på vilka kontakter som ska synkroniseras.  

När du har ställt in synkroniseringen kan du synkronisera ändringar av kontakten manuellt eller automatisera den genom att lägga upp en jobbkötransaktion. Mer information om Automation finns i nästa avsnitt i den här artikeln.

### Automatisk synkronisering

Du kan skapa en jobbkötransaktion som ska synkronisera kontakter enligt ett schema som du definierar. Mer information finns i [Använda jobbköer för att schemalägga uppgifter](admin-job-queues-schedule-tasks.md). 

I följande tabell visas inställningarna på sidan **Transaktionskort för jobbkö** som används för att synkronisera kontakter:

|Fält|Inställning för synkronisering av kontakter|
|-----|-----|
|Objekttyp som ska köras|Kodmodul|
|Objekt-ID som ska köras|6700|

## Synkronisera kontakter

Om du vill arbeta med kontakter i [!INCLUDE[prod_short](includes/prod_short.md)], och du sedan tycker att det är lätt att starta synkroniseringen manuellt när det passar dig från listan **kontakter**. Du kan synkronisera kontakter på två sätt:

* **Synka med Microsoft 365**

  Synkronisera alla ändringar från [!INCLUDE[prod_short](includes/prod_short.md)] till Microsoft 365 sedan senaste synkronisering, baserat på senaste ändringsdatum. Inga nya kontakter från Microsoft 365 synkroniseras till [!INCLUDE[prod_short](includes/prod_short.md)]. Detta är vanligtvis snabbare än att göra en fullständig synkronisering. 

* **Full synkronisering med Microsoft 365**

  Synkronisera alla kontakter i båda riktningar oavsett senast synkroniserad och senast ändrades.  

I båda fallen synkroniseras bara kontakter från Outlook om de har alla nödvändiga fält ifyllda. De obligatoriska fälten för synkronisering till Microsoft 365 är **Namn**, **E-postadress** och kontakten måste vara av typen **Person**. [!INCLUDE[prod_short](includes/prod_short.md)] är källa för kontaktinformation i [!INCLUDE[prod_short](includes/prod_short.md)] kommer att sparas om det finns dubbletter.  

> [!NOTE]
> Om du tar bort en kontakt i Outlook, men behåller den [!INCLUDE[prod_short](includes/prod_short.md)], kommer kontakten att återskapas i Outlook nästa gång du synkroniserar. 

## Se även

[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Ekonomi](finance.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Använda kontakter (personer) i Outlook på Internet](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]