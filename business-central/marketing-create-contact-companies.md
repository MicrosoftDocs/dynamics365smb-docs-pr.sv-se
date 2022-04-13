---
title: Skapa affärskontakter
description: Beskriver de uppgifter som är involverade i att skapa kontakter och definiera dina affärsrelationer på kontaktkortet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 07/08/2021
ms.author: edupont
ms.openlocfilehash: 6b82557463633959e62b4d2fed9484c8e2412b22
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520262"
---
# <a name="create-contacts"></a>Skapa kontakter

När du utvecklar en affärsrelation till någon på ett annat företag lägger du till denne som en kontakt i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan sedan lägga till information om dem eller deras företag som kan vara användbar för framtida kommunikation. På sidan **Kontaktkort** kan du skapa följande typer av kontakter:

* **Person** – Oftast är det när du har direkt kontakt med någon och har deras kontaktuppgifter.
* **Företag** – Till exempel om kontakten inte är en individ utan en entitet, t. ex. en underleverantör eller bank. 

Den information som är relevant för varje kontakttyp skiljer sig åt, så att de fält och åtgärder som är tillgängliga skiljer sig åt. Du kan till exempel bara tilldela arbetsansvar till en person och en industrigrupp till ett företag. 

Du kan också ändra värdet i fältet **Typ** vid ett senare tillfälle. Du kan också använda fälten på snabbfliken **Övertaget** på sidan **Marknadsföringsinställningar** för att ange vilka data som ska delas mellan en person och deras företag. Mer information finns i [Konfigurera kontakter](marketing-setup-contacts.md).

När en kontakt omvandlas till en kund blir kontaktpersonen eller kontaktföretaget namnet på kunden. Posten för kontakten behålls och du kan koppla kontakten till kunden så att informationen synkroniseras i framtiden.

> [!NOTE]
> Om du slår på [funktionsuppdateringen för konverteringsmallar](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees) kan du också skapa leverantörer eller anställda från affärskontakter.
>
> Men om du redan använder den inbyggda funktionen för att skapa kunder eller artiklar automatiskt, stöder den här funktionsuppdateringen inte anpassade fält och nyskapade kunder eller artiklar kommer inte att innehålla sådana data.

## <a name="to-create-a-contact-manually"></a>Så här skapar du en kontakt manuellt
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kontakter** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fältet **Nr.** anger du ett nummer för kontakten.

    Om du har definierat en nummerserie för kontakter på sidan **Marknadsföringsinställning** kan du i stället trycka på **Retur** för att infoga nästa tillgängliga kontaktnummer.  
5. Fyll i återstående fält om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Skapa en kontakt av en kund, en leverantör eller ett bankkonto så här
Om du har kunder, leverantörer och bankkonton som du vill skapa kontaktkort för, använder du batch-jobben **Skapa kontakter från** för att skapa kontakter av befintliga uppgifter. När du skapar en kontakt på detta sätt, synkroniseras kontaktinformationen efteråt med den relaterade kunden, leverantören eller bankkontotinformationen. Mer information finns i [Så här synkroniserar du kontakter med kunder, leverantörer och bankkonton](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Innan du kan skapa kontakter baserat på befintliga data måste du ange en affärsrelationskod för kunder, leverantörer eller bankkonton på snabbfliken **Interaktioner** på sidan **Marknadsföringsinställningar**. Mer information finns i [Ställa in kontakter](marketing-setup-contacts.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange ett av följande, beroende på varifrån du vill skapa kontakter och välj sedan relaterad länk.
   * **Skapa kontakter från kunder**
   * **Skapa kontakter från leverantörer**
   * **Skapa kontakter från bankkonton**
2. På den begärda sidan som öppnas i avsnittet **Kund**, **Leverantör** eller **Bankkonto** kan du ställa in filter om du endast vill skapa kontakter från vissa kunder, leverantörer eller bankkonton.
3. Klicka på **OK** för att börja skapa kontakter.

Nästa kontaktnummer i nummerserien kopplas till de nya kontakterna. Affärsrelationerna som anges på sidan **Marknadsföringsinställning** tilldelas de nyligen skapade kontakterna.

> [!TIP]  
> Du kan även göra detta i motsatt riktning, dvs när du skapar en kund, leverantör eller bankkonto utifrån en kontakt. Mer information finns i [Att skapa en kontakt som en kund, leverantör eller bankkonto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Skapa en kund, leverantör, medarbetare eller ett bankkonto från en kontakt
Om du har en kund, leverantör, medarbetare eller ett bankkonto för företaget som du vill skapa en kontakt för kan du använda åtgärden **Skapa som**. När du skapar en kontakt på detta sätt synkroniseras kontaktinformationen efteråt med den relaterade kunden, leverantören, medarbetaren eller bankkontoinformationen. Mer information finns i [Så här synkroniserar du kontakter med kunder, leverantörer och bankkonton](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Innan du kan skapa kunder, leverantörer, medarbetare eller bankkonton från kontakter måste du ange en affärsrelationskod på sidan **Marknadsföringsinställningar** under snabbfliken **Interaktioner**. Mer information finns i [Konfigurera kontakter](marketing-setup-contacts.md).

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kontakter** och väljer sedan relaterad länk.
2. Välj kontakten du vill skapa som en kund, leverantör, medarbetare eller ett bankkonto.
3. Välj åtgärden **Skapa som** och välj sedan antingen **Kund**, **Leverantör**, **Bank** eller **Medarbetare**.
4. Välj **OK**.

Kontaktinformationen överförs från kontaktkortet till en ny kund, leverantör, medarbetare eller ett nytt bankkontokort. Du kanske vill lägga till specifik information på varje kort, t.ex fakturering och betalningsinformation. Mer information finns i exempelvis [Registrera nya kunder](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Länka en kontakt till en befintlig kund, leverantör, medarbetare eller ett befintligt bankkonto
Om du har en kontakt och antingen en kund, en leverantör, en medarbetare eller ett bankkonto för samma företag, kan du länka de två enheterna så att data synkroniseras.

1. Öppna kontakten som du vill länka.
2. Välj åtgärden **Länka med befintlig** och sedan åtgärden **Kund**, **Leverantär**, **Bank** eller **Medarbetare**.
3. På sidan som öppnas väljer du den kund, leverantör, medarbetare eller det bankkonto som ska länkas till.
4. I fältet **Nuvarande huvudfält** anger du vilka fält som ska prioriteras i händelse av en konflikt mellan fält som är gemensamma för kontakten och kunden, leverantören, medarbetaren eller bankkontot. Om till exempel säljarkoden är olika för kontakten och kunden kan du välja ett behålla den på kontaktkortet genom att välja **Kontakt**.
5. Välj **OK**.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>För att ta bort en länk mellan en kontakt och en befintlig kund, leverantör, medarbetare eller ett befintligt bankkonto

Om du felaktigt har kopplat en kontakt och en kund, leverantör, medarbetare eller ett bankkonto tar du bort länken mellan entiteterna så att data inte längre synkroniseras.

1. Öppna kontakten som har fel länk.  
2. Välj åtgärden **Affärsrelationer**.  
3. På sidan som öppnas väljer du den kund, leverantör, medarbetare eller det bankkonto från vilken/vilket länken ska tas bort.  
4. Välj åtgärden **Radera**.  

> [!NOTE]  
> Använd inte fönstret **Affärsrelationer** för att ändra befintliga relationer. Ta i stället bort relationen och använd sedan åtgärden **Länka med befintlig**. Mer information finns i avsnittet [Länka en kontakt till en befintlig kund, leverantör eller befintligt bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Synkronisera kontakter med kunder, leverantörer, medarbetare och bankkonton
Om några av kontakterna också är kunder, leverantörs. medarbetare eller bankkonton kan du synkronisera dem med data från kontakten och dra nytta av följande förmåner:

* Du behöver bara uppdatera uppgifterna på ett ställe. Om du till exempel ändrar telefonnumret på kontakten uppdateras telefonnumret automatiskt för kunden, leverantören, medarbetaren eller bankkontot.
* Om du har angett nummerserie för kontakter när du skapar kund-, leverantörs-, medarbetar- eller bankkontokort, skapas automatiskt en kontakt.
* Du kan skapa försäljningsofferter och order, samt inköpsofferter och order från kontakten.
* Du kan registrera dina interaktioner, som att skriva ut order eller avropsorder, skapa försäljningsserviceorder, skicka e-post osv.
* Om du raderar en kontakt som är länkad till en kund, leverantör, medarbetare eller ett bankkonto är det bara kontakten som tas bort. Kunden, leverantören, medarbetaren eller bankkontot återstår.
* Om du raderar en kontakt, leverantör, medarbetare eller ett bankkonto som är länkat till en kontakt, återstår kontakten.

> [!NOTE]  
> Vissa detaljer, t.ex fakturering och bokföringsdetaljer, är inte tillgängliga för kontakter. När du skapar kontakter som kunder, leverantörer, medarbetare eller bankkonton kanske du vill lägga till dem manuellt.

Det finns tre sätt att aktivera datasynkronisering mellan kontakter och kunder, leverantörer, medarbetare eller bankkonton:

* När du skapar kontakter från kunder, leverantörer, medarbetare eller bankkonton. Se [Att skapa en kontakt från en kund, leverantör eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* När du skapar kunder, leverantörer, medarbetare eller bankkonton från kontakter. Se [Att skapa en kund, leverantör eller ett bankkonto från en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* När du länkar kontakterna till befintliga kunder, leverantörer, medarbetare eller bankkonton från kontaktkortet. Se [Länka en kontakt till en befintlig kund, leverantör eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Visar vilken kund, leverantör, medarbetare eller vilket bankkonto en kontakt tillhör
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Kontakter** och väljer sedan relaterad länk.
2. Markera raden för en kontakt, välj åtgärden **Relaterad information** och välj sedan åtgärden **Kund/Leverantör/Bankkonto/Medarbetare**.

## <a name="see-also"></a>Se även
[Hantera kontakter](marketing-contacts.md)  
[Ställa in kontakter](marketing-setup-contacts.md)  
[Arbeta med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]