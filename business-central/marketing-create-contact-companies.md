---
title: Skapa kontaktföretag | Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: aaeb98aa5e3c48a92be71546be33b1494a751cb9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "806946"
---
# <a name="creating-contacts"></a>Skapar kontakter
Ditt företag träffar regelbundet potentiella kunder som vanligtvis utvecklas till framtida affärsrelationer. När en ny kontakt skapas måste den här informationen registreras så att kommunikationen kan fortsätta.

Tilldela så mycket data som möjligt om ett visst företag ser du till att kommunikationen blir effektiv. Om du till exempel anger relevant branschgrupp ser du till att dessa specifika företag får all relevant kommunikation. Du kan också definiera vilken affärsrelation du har med en kontakt. En kontakt kan till exempel vara en potentiell kund, bank eller underleverantör.

> [!NOTE]
> I fältet **typ** på sidan **kontaktkort** kan du ange en kontakt som en person eller ett företag, vanligen beroende på om du känner till namnet på kontaktpersonen när den skapas. Funktionen är densamma för båda typerna, med undantag för vissa av de tilläggsinformationstyper som kan tilldelas. Du kan ändra värdet i fältet senare, eller du kan använda fälten på snabbfliken **Arv** på sidan **Marknadsföringsinställning** om du vill kontrollera vilka data som delas mellan en person och relaterat företag.

Du kan skapa en kontakt för varje ny person eller företag som du har förbindelse med, till exempel kund, leverantör, spekulant, bank, jurist, konsult och så vidare.

Du kan skapa en kontakt på två sätt:
 * Manuellt.
 * Från en befintlig kund, leverantör eller bankkonto.

## <a name="to-create-a-contact-manually"></a>Så här skapar du en kontakt manuellt
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fältet **Nr.** anger du ett nummer för kontakten.

    Om du har definierat en nummerserie för kontakter på sidan **Affärsstödsinställning** kan du i stället trycka på Retur för att infoga nästa tillgängliga kontaktnummer automatiskt.  
5. Fyll i återstående fält om det behövs. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Skapa en kontakt av en kund, en leverantör eller ett bankkonto så här
Om du har kunder, leverantörer och bankkonton som du vill skapa kontaktkort för, använd batch-jobben **skapa kontakter från** för att skapa kontakter baserat på befintliga uppgifter. När du skapar en kontakt på detta sätt, synkroniseras kontaktinformationen efteråt med den relaterade kunden, leverantören eller bankkontotinformationen. Mer information finns i [Så här synkroniserar du kontakter med kunder, leverantörer och bankkonton](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Innan du kan skapa kontakter baserat på befintliga data måste du ange en affärsrelationskod för kunder, leverantörer eller bankkonton på snabbfliken **Interaktioner** på sidan **Marknadsföringsinställningar**. Mer information finns i [Konfigurera kontakter](marketing-setup-contacts.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), gå till ett av följande beroende på varifrån du vill skapa kontakter välj sedan relaterad länk.
   * **Skapa kontakter från kunder**
   * **Skapa kontakter från leverantörer**
   * **Skapa kontakter från bankkonton**
2. På den begärda sidan som öppnas i avsnittet **Kund**, **Leverantör** eller **Bankkonto** kan du ställa in filter om du endast vill skapa kontakter från vissa kunder, leverantörer eller bankkonton.
3. Klicka på **OK** för att börja skapa kontakter.

Nästa kontaktnummer i nummerserien kopplas till de nya kontakterna. Affärsrelationerna som anges på sidan **Marknadsföringsinställning** tilldelas de nyligen skapade kontakterna.

> [!TIP]  
> Du kan även göra detta i motsatt riktning, dvs när du skapar en kund, leverantör eller bankkonto utifrån en kontakt. Mer information finns i [Att skapa en kontakt som en kund, leverantör eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisera kontakter med kunder, leverantörer och bankkonton
Om några av kontakterna också är kund-, leverantörs- och/eller bankkonton kan du synkronisera deras kontaktinformation med relaterade kund-, leverantörs- och bankkonton.

Följande fördelar finns när en kontakt synkroniseras med en kund, leverantör eller ett bankkonto.

* Du behöver bara uppdatera uppgifterna på ett ställe. Om du till exempel ändrar telefonnumret på kontakten uppdateras telefonnumret med samma ändring på kund-, leverantörs- eller bankkontot.
* Om du har angett nummerserie för kontakter när du skapar kund-, leverantörs- eller bankkontokort, skapas automatiskt ett kontaktkort för kunder, leverantörer eller bankkonton.
* Du kan skapa försäljningsofferter och försäljningsorder, inköpsofferter och inköpsorder från kontakten.
* Dina interaktioner kan registreras när du utför vissa åtgärder som att skriva ut order eller avropsorder, skapa försäljningsserviceorder, skicka e-post osv.
* Om du raderar en kontakt som är länkad till en kund, leverantör eller bank är det bara kontakten som tas bort från programmet. Kunden, leverantören eller bankkontot återstår.
* Om du raderar en kontakt som är länkad till en kund, leverantör eller ett bankkonto är det bara kontakten som återstår.

> [!NOTE]  
> Vissa detaljer, t.ex fakturering och bokföringsdetaljer, visas inte på kontaktkortet. Följaktligen kan du behöva lägga till dem manuellt på kund-, leverantörs- och bankkontokort, när du skapar kontakter som kunder, leverantörer eller bankkonton.

Synkronisering av gemensamma data mellan kontakter och relaterade kunder, leverantörer eller bankkonton måste aktiveras på tre sätt:

* När du länkar kontakterna till befintliga kunder, leverantörer eller bankkonton från kontaktkortet. Se [Länka en kontakt till en befintlig kund, leverantör eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).
* När du skapar kunder, leverantörer och bankkonton från kontakter. Se [Att skapa en kontakt från en kund, leverantör eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* När du skapar kontakter som kunder, leverantörer och bankkonton. Se [Skapa en kontakt som en kund, en leverantör eller ett bankkonto så här](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Länka en kontakt till en befintlig kund, leverantör eller bankkonto
Om du har en kontakt och antingen en kund, en leverantör eller ett bankkonto för samma företag, kan du länka de två enheterna så att allmänna data synkroniseras.

1. Öppna kontakten som du vill länka.
2. Välj åtgärden **Länka med befintlig** och välj sedan åtgärden **Kund**, **Leverantör** eller **Bank**.
3. På sidan som öppnas väljer du den kund, leverantör eller bankkonto att länka till.
4. I fältet **Nuvarande huvudfält** anger du vilka fält som ska gälla i händelse av en konflikt mellan fälten på kontakten och kund, leverantör eller konto. Om till exempel säljarkoden är olika på kontaktkortet och kundkortet kan du välja ett behålla den på kontaktkortet genom att välja **Kontakt**.
5. Välj knappen **OK**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Skapa en kontakt som en kund, en leverantör eller ett bankkonto så här
Om du har en kund, leverantör eller bankkonto för företaget som du vill skapa en kontakt för kan du använda funktionen **skapa som**. När du skapar en kontakt på detta sätt, synkroniseras kontaktinformationen efteråt med den relaterade kunden, leverantören eller bankkontotinformationen. Mer information finns i [Så här synkroniserar du kontakter med kunder, leverantörer och bankkonton](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Innan du kan skapa kunder, leverantörer eller bankkonton från kontakter måste du ange en affärsrelationskod för kunder, leverantörer eller bankkonton på snabbfliken **Interaktioner** på sidan **Marknadsföringsinställningar**. Mer information finns i [Konfigurera kontakter](marketing-setup-contacts.md).

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.
2. Välj kontakten du vill skapa som en kund, en leverantör eller ett bankkonto.
3. Välj åtgärden **Skapa som** och välj sedan antingen **Kund**, **Leverantör** eller **Bank**.
4. Välj knappen **OK**.

Kontaktinformationen överförs från kontaktkortet till en ny kund, leverantör eller bankkonto. Du kanske vill lägga till specifik information på varje kort, t.ex fakturering och betalningsinformation. Mer information finns i exempelvis [Registrera nya kunder](sales-how-register-new-customers.md).

## <a name="see-also"></a>Se även
[Hantera kontakter](marketing-contacts.md)  
[Ställa in kontakter](marketing-setup-contacts.md)  
[Arbeta med Business Central](ui-work-product.md)
