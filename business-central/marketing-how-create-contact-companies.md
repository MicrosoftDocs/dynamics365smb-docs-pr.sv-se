---
title: Skapa kontaktföretag | Microsoft Docs
description: Beskriver hur du skapar en kontakt för varje nytt företag eller potentiellt företag som du interagerar med eller har en relation med.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: fcd964cc1cea9fb256b58f3a73b061b241d92fe4
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309250"
---
# <a name="create-contacts"></a>Skapa kontakter
Du kan skapa en kontakt för varje nytt företag som du har förbindelse med, till exempel kund, leverantör, spekulant, bank, jurist, konsult och så vidare.

Det finns två sätt att skapa en kontakt: från noll eller från en befintlig kund, leverantör eller bankkonto.

## <a name="create-a-company-contact-from-scratch"></a>Skapa en företagskontakt från noll
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Skriv numret på den artikel som har beställts i fältet **Nr**.

    Om du har definierat en nummerserie för kontakter på sidan **Affärsstödsinställning** kan du i stället trycka på Retur så anges nästa tillgängliga kontaktnummer automatiskt.  
4. Ange **Typ** till **Företag**.
5. Fyll i övriga fält enligt behov.

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Skapa en företagskontakt från en kund, en leverantör eller ett bankkonto
Om du redan har lagt upp flera kunder, leverantörer eller bankkonton kan du skapa kontakter baserat på befintliga uppgifter. När du skapar en kontakt på detta sätt, synkroniseras kontaktinformationen med kunden, leverantören eller bankkontotinformationen.

> [!NOTE]  
>   Innan du kan skapa kontaktföretag på detta sätt måste du ange en affärsrelationskod för bankkonton, kunder eller leverantörer på sidan **Marknadsföringsinställningar**. Om du vill skapa kontakter från bankkonton måste du även ange nummerserien för bankkonton på sidan **Redovisningsinställningar**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), gå till ett av följande beroende på varifrån du vill skapa kontakter välj sedan relaterad länk.
   * **Skapa kontakter från kunder**
   * **Skapa kontakter från leverantörer**
   * **Skapa kontakter från bankkonton**
2. På batch-jobbsidan som öppnas i avsnittet **Kund**, **Leverantör** eller **Bankkonto** kan du ställa in filter om du endast vill skapa kontakter från vissa kunder, leverantörer eller bankkonton.
3. Klicka på **OK** för att börja skapa kontakter.

    Nästa kontaktnummer i nummerserien kopplas till de nya kontakterna. De nyskapade kontakterna tilldelas den affärsrelation för leverantörer som angetts på sidan **Affärsstödsinställning**.

> [!TIP]  
>   Du kan också skapa en kund, en leverantör eller ett bankkonto från en kontakt. Mer information finns i [Skapa en företagskontakt från kund, leverantör eller bankkonto från en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Se även
[Synkronisera kontakter med kunder, leverantörer och bankkonton](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Så här tilldelar du affärsrelationer till kontakter](marketing-business-relations.md#AssignBusRelContact)  
[Så här tilldelar du industrigrupper till en kontakt](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Tilldela utskicksgrupp till en kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Skapa kontaktpersoner](marketing-create-contact-persons.md)  
[Arbeta med Business Central](ui-work-product.md)
