---
title: "Skapa Företag | Microsoft Docs"
description: "Beskriver hur du skapar kontaktföretag i Financials "
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bd8dfb8abc9387ad6b9c500f25feb181878b6cfe
ms.contentlocale: sv-se
ms.lasthandoff: 05/04/2017


---
# <a name="create-contact-companies"></a>Skapa kontaktföretag
Du kan skapa en kontakt för varje nytt företag som du har förbindelse med, till exempel kund, leverantör, spekulant, bank, jurist, konsult och så vidare.

Det finns två sätt att skapa en kontakt: från noll eller från en befintlig kund, leverantör eller bankkonto.

Innan du skapar en kontakt kan du kontrollera inställningarna i fönstret **Affärsstödsinställning**. Mer information finns i [Ställa in e-postmeddelanden](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Skapa en företagskontakt från noll
1. I det övre högra hörnet väljer du ikonen **Sök efter sidan eller rapporten** ![Sök efter sidan eller rapporten](media/ui-search/search_small.png "Sök efter sidan eller rapporten"), ange **Kontakter**, och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Skriv numret på den artikel som har beställts i fältet **Nr** .

    Om du har definierat en nummerserie för kontakter i fönstret **Affärsstödsinställning** kan du i stället trycka på Retur så anges nästa tillgängliga kontaktnummer automatiskt.  
4. Ange **Typ** till **Företag**.
5. Fyll i övriga fält enligt behov.

## <a name="create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Skapa en företagskontakt från en kund, en leverantör eller ett bankkonto
Om du redan har lagt upp flera kunder, leverantörer eller bankkonton kan du skapa kontakter baserat på befintliga uppgifter. När du skapar en kontakt på detta sätt, synkroniseras kontaktinformationen med kunden, leverantören eller bankkontotinformationen.

**Obs!** Innan du kan skapa kontaktföretag på detta sätt måste du ange en affärsrelationskod för bankkonton, kunder eller leverantörer i fönstret **Marknadsföringsinställningar**. Om du vill skapa kontakter från bankkonton måste du även ange nummerserien för bankkonton i fönstret **Redovisningsinställningar**.

1. I det övre högra hörnet väljer du ikonen **Sök efter sida eller rapport** ![Sök efter sida eller rapport](media/ui-search/search_small.png "ikonen Sök efter sida eller rapport") anger ett av följande beroende på från var du vill skapa kontaker och väljer sedan relaterad länk.
   * **Skapa kontakter från kunder**
   * **Skapa kontakter från leverantörer**
   * **Skapa kontakter från bankkonton**
2. I batch-jobbfönstret som öppnas i avsnittet **Kund**, **Leverantör** eller **Bankkonto** kan du ställa in filter om du endast vill skapa kontakter från vissa kunder, leverantörer eller bankkonton.
3. Klicka på **OK** för att börja skapa kontakter.

    Nästa kontaktnummer i nummerserien kopplas till de nya kontakterna. De nyskapade kontakterna tilldelas den affärsrelation för leverantörer som angetts i fönstret **Affärsstödsinställning**.

**Tips** Du kan också skapa en kund, en leverantör eller ett bankkonto från en kontakt. Mer information finns i [Skapa en företagskontakt från kund, leverantör eller bankkonto från en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Se även
[Synkronisera kontakter med kunder, leverantörer och bankkonton](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Så här tilldelar du affärsrelationer till kontakter](marketing-business-relations.md#AssignBusRelContact)  
[Så här tilldelar du industrigrupper till en kontakt](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Tilldela utskicksgrupp till en kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Så här skapar du kontaktpersoner](marketing-create-contact-persons.md)  
[Arbeta med Financials](ui-work-product.md)

