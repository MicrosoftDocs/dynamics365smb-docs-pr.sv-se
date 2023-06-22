---
title: Fakturera din bokningar i Business Central
description: I det här avsnittet beskrivs hur du kan utföra massfakturering från Microsoft Bookings i Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'invoicing, bookings'
ms.search.form: '1638, 6702, 6704'
ms.date: 05/20/2022
ms.author: edupont
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-includeprodshortincludesprodshortmd" />Bulkfakturera för Microsoft Bookings i [!INCLUDE[prod_short](includes/prod_short.md)]

Om företaget använder appen Bookings i Microsoft 365 kan du göra bulkfakturering för avtalade tider. SIdan **Ofakturerade bokningar** i [!INCLUDE[prod_short](includes/prod_short.md)] innehåller en lista över företagets slutförda bokningar. Du kan snabbt markera avtalade tider som du vill fakturera och skapa fakturor för utkast för tjänsterna på den här sidan.  

## <a name="connect-to-bookings" />Anslut till Bookings

För att ansluta ditt [!INCLUDE[prod_short](includes/prod_short.md)] med Bookings, måste du ange ditt Bookings-företag, vad som ska synkroniseras med Bookings, hur ofta du vill synkronisera och vilka mallar du vill använda. Du kan ställa in informationen på sidan **Inställningar av Bookings-synkning** som du kan starta från sidan **Inställningar för Exchange-synkning** som du hittar genom [söka](ui-search.md).  

Till exempel om du vill synkronisera kunder mellan Bookings och [!INCLUDE[prod_short](includes/prod_short.md)], måste du ange standardmallen för att lägga till nya kunder i [!INCLUDE[prod_short](includes/prod_short.md)] baserat på kunder i ditt Bookings-företag.  

> [!NOTE]
> Appen Bokningar är utformad för att boka möten för enskilda kunder, snarare än företag. Synkronisering med [!INCLUDE[prod_short](includes/prod_short.md)] kan därför endast synkronisera kundkontakter med en typ av *Person*. En e-postadress krävs också för att synkronisera kontakten.  

På liknande sätt, om du till exempel vill synkronisera kunder mellan Bookings och [!INCLUDE[prod_short](includes/prod_short.md)], måste du ange standardmallen för att lägga till nya serviceartiklar i [!INCLUDE[prod_short](includes/prod_short.md)] baserat på kunder i ditt Bookings-företag.  

> [!NOTE]
> Endast objekt av typen *Service* synkroniseras mellan Bookings och [!INCLUDE[prod_short](includes/prod_short.md)]. Den mall som du har skapat på sidan **Konfigurationsmallar** så att den kan användas för artikelsynkroniseringen måste ange typen som *Service*.

## <a name="invoice-appointments" />Fakturera möten

När det är dags att skicka fakturor för slutförda bokningar kan du gå till sidan **Ofakturerade bokningar**. Beroende på hur ofta informationen är synkroniserad, är listan lång eller kort. Du kan skapa fakturor för alla bokningar i listan eller en bokning i taget. Du kan markera en eller flera poster i listan och fakturera sådana.  

Stöd för faktureringsmöten från Bookings är enklare än det fullständiga arbetsflödet för att arbeta med offerter, försäljningsorder och försäljningsfakturor. Mer information finns i [Så här fakturerar du försäljningsaktiviteter](sales-how-invoice-sales.md). Du kan välja att sälja tjänsterna med hjälp av [!INCLUDE[prod_short](includes/prod_short.md)] eller använda Bookings, beroende på dina behov.  

> [!NOTE]
> I maj 2022 upptäckte vi ett problem i integrationen med bokningar. För närvarande synkroniseras från Bokningar till [!INCLUDE [prod_short](includes/prod_short.md)] kräver att du manuellt kopplar fakturorna till kunder i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="see-also" />Se även

[Ekonomi](finance.md)  
[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
