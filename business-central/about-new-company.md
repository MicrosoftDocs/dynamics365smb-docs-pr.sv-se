---
title: Skapa nya företag med en assisterad konfiguration
description: 'Det är enkelt att skapa ett nytt, tomt företag i Business Central. En assisterad konfiguration hjälper dig genom stegen och du kan importera dina affärsdata.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/08/2024
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.service: dynamics-365-business-central
---
# Skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] tillhör behållaren för affärsdata en affärsenhet eller juridisk person som kallas ett *företag*. När du registrerar dig för [!INCLUDE[prod_short](includes/prod_short.md)] får du ett demonstrationsföretag och ett tomt företag, *Mitt företag*. Att växla mellan företag är enkelt: gå bara till **Mina inställningar** och flytta till det andra företaget. Men du kan också skapa nya företag i [!INCLUDE[prod_short](includes/prod_short.md)] beroende på dina affärsbehov.  

> [!NOTE]
> För att skapa ett nytt företag måste du vara tilldelad behörighetsuppsättning **Super**.

När du skapar ett nytt företag får du hjälp med de grundläggande inställningarna av en assisterad konfiguration. Du kan sedan importera relevanta data från ditt gamla system eller från något annat företag i [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Välj rätt mall

Om du bestämmer dig för att lägga till ett företag till din [!INCLUDE[prod_short](includes/prod_short.md)] kan du använda den assisterade inställningsguiden **Skapa nytt företag** för att komma igång. Guiden för assisterad konfiguration är tillgänglig från sidan **Företag** och från sökfunktionen i fältet **Företag** på sidan **Mina inställningar**.  

I guiden för assisterad konfiguration finns två mallar och ett tomt alternativ:

- **Utvärdering – exempeldata**  
    Detta skapar ett företag som liknar demonstrationsföretaget med exempeldata och inställningsdata. Denna typ av företag är tillgänglig för dig utan att du behöver växla till en 30-dagars provperiod som de andra typerna gör.  
- **Produktion – endast inställningsdata**  
    Detta skapar ett företag som liknar **Mitt företag** med inställningsdata, men utan exempeldata. Du kan använda detta företag under en 30 dagar lång testperiod.  
- **Skapa ny – Inga data**  
    Detta skapar ett tomt företag utan inställningsdata. Du kan använda detta företag under en 30 dagar lång testperiod.  

Om du vill komma igång snabbt med ett nytt företag väljer du **Produktion – endast inställningsdata** och importerar sedan dina egna affärsdata, till exempel kunder, artiklar och leverantörer. Välj mallen **Nytt** om du vill ställa in allt från början. Om så är fallet kan du använda den assisterade konfigurationen **Företagsinställningar** som hjälper dig att komma igång med grundläggande inställningsdata.  

> [!NOTE]  
> När du skapar ett nytt företag tar detnågra minuter innan du kan öppna det i [!INCLUDE[prod_short](includes/prod_short.md)]. Inställningsstatus på sidan **Företag** visas när det nya företaget är redo för dig. Sedan kan du växla till det nya företaget med hjälp av **Mina inställningar**.  

Du kan skapa valfritt antal nya företag under en utvärderingsversion på 30 dagar, men de kan bara användas under utvärderingsperioden. Kontakta din [!INCLUDE[prod_short](includes/prod_short.md)]-partner för mer information. Se även artikeln med [Vanliga frågor och svar för Dynamics 365 Business Central](trial-faq.md).  

Administratören kan läsa mer om försök och prenumerationer [här](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## Kopiera ett företag

På sidan **Företag** kan du använda åtgärden **Kopiera** för att skapa ett andra företag baserat på innehållet i ett befintligt företag. Detta är användbart om du t. ex. vill testa ett företag utan att störa produktionsdata.

> [!Important]
> Använd inte kopieringsåtgärden för att göra en säkerhetskopia av ett företag. För att göra en säkerhetskopia av ett företag börjar du genom att exportera databasen som en .bacpac-fil. Mer information finns i [Exportera databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjälpen för utvecklare och administration.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

[!INCLUDE [dataverse-copy-company](includes/dataverse-copy-company.md)]

## Konfigurera företagsnavet

När du loggar in på ett nytt företag körs guiden **företagsinställningar** automatiskt och hjälper dig att komma igång. Du kommer att ombedas om information om företaget, till exempel adress, bankuppgifter och lagervärderingsprincip. Vi ber om denna information eftersom den används som grund för många områden i [!INCLUDE[prod_short](includes/prod_short.md)] som du sedan inte måste konfigurera manuellt senare.  

Till exempel inkluderar [!INCLUDE [prod_short](includes/prod_short.md)] din företagsadress på fakturor och andra dokument samt dina bankuppgifter i betalningar. Värderingsprincipen används för att beräkna priser och lagervärdet.  

När du har grundläggande inställningar på plats kan du ställa in återstående huvudområden. Sedan är du redo att lägga till affärsdata som t.ex. kunder och leverantörer. Mer information finns i [Konfigurera [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## Företag och miljöer

[!INCLUDE [company_environment](includes/company_environment.md)]

Mer information finns i [byta till ett annat företag eller annan miljö](ui-organization-switch.md). Mer information om miljöer finns i [Förstå infrastrukturen i Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (endast på engelska).  

## Ändra ett företags namn

När ett företag har skapats kan du inte ändra namnet. Du kan emellertid ändra dess **Visningsnamn**, d.v.s. den text som ska visas för företaget i hela programmet.  

> [!TIP]
> Du kan byta namn på ett företag om du använder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.

## Lägga till Contoso Coffee

Appen Contoso Coffee tillhandahåller demonstrationsdata som hjälper dig att utforska de avancerade funktionerna i [!INCLUDE [prod_short](includes/prod_short.md)]. Hitta appen i AppSource och installera den i ett tomt företag, till exempel ett företag i en sandbox-miljö. Mer information finns i [Introduktion till demonstrationsdata för Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).  

## Se även

[Anpassa Business Central](ui-customizing-overview.md)  
[Ställa in [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importera affärsdata från andra ekonomisystem](across-import-data-configuration-packages.md)  
[Ändra grundinställningar](ui-change-basic-settings.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Förstå infrastrukturen i Business Central online (endast engelska)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
