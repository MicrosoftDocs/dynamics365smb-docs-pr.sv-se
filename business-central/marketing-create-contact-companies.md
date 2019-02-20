---
title: "Skapa kontaktföretag | Microsoft Docs"
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: sv-se
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Skapa kontaktföretag
Ditt företag träffar regelbundet potentiella kunder som vanligtvis utvecklas till framtida affärsrelationer. När en ny kontakt skapas måste den här informationen registreras så att kommunikationen kan fortsätta.

Genom att ange så mycket data som möjligt om ett visst företag ser du till att kommunikationen blir effektiv. Om du till exempel anger relevant branschgrupp ser du till att dessa specifika företag får all relevant kommunikation.

Du kan också definiera vilken affärsrelation du har med en kontakt. En kontakt kan till exempel vara en potentiell kund, bank eller underleverantör.

## <a name="creatinge-contact-companies"></a>Skapa kontaktföretag
Du kan skapa en kontakt för varje nytt företag som du har förbindelse med, till exempel kund, leverantör, spekulant, bank, jurist, konsult och så vidare.

Det finns två sätt att skapa en kontakt: från noll eller från en befintlig kund, leverantör eller bankkonto.

Innan du skapar en kontakt kan du kontrollera inställningarna på sidan **Affärsstödsinställning**. Mer information finns i [Ställa in e-postmeddelanden](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Skapa en företagskontakt från noll
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Skriv numret på den artikel som har beställts i fältet **Nr**.

    Om du har definierat en nummerserie för kontakter på sidan **Affärsstödsinställning** kan du i stället trycka på Retur så anges nästa tillgängliga kontaktnummer automatiskt.  
4. Ange **Typ** till **Företag**.
5. Fyll i övriga fält enligt behov.

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Skapa en företagskontakt från en kund, en leverantör eller ett bankkonto
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

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisera kontakter med kunder, leverantörer och bankkonton
Om några av kontakterna också är kund-, leverantörs- och/eller bankkonton kan du synkronisera deras kontaktinformation med relaterade kund-, leverantörs- och bankkonton. Synkroniseringen gör information som är gemensam mellan kontakter och kunder, leverantörer eller bankkonton densamma.  

Innan du kan synkronisera kontakterna med kund-, leverantörs- och/eller bankkonton måste du ange en affärsrelationskod för dessa på sidan **Marknadsföringsinställningar**. Mer information finns i [Ställa in e-postmeddelanden](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Olika sätt att synkronisera kontakter med kunder, leverantörer och bankkonton
Du kan synkronisera kontakterna med kunder, leverantörer eller bankkonton på tre olika sätt:

* Länka kontakterna till befintliga kunder, leverantörer eller bankkonton från kontaktkortet. Mer information finns i [Länka kontakter med kunder, leverantörer och bankkonton](marketing-how-link-contact.md).
* Skapa kunder, leverantörer och bankkonton från kontakten. Mer information finns i [Skapa en företagskontakt från kund, leverantör eller bankkonto från en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Skapa kontakter från kunder, leverantörer eller bankkonton. Mer information finns i [Skapa en företagskontakt från kund, leverantör eller bankkonto](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Konsekvenser för synkroniseringen
När kontaken har synkroniserats med kund-, leverantörs- eller bankkontot:

* Du behöver bara uppdatera uppgifterna på ett ställe. Om du till exempel ändrar telefonnumret på kontakten uppdateras telefonnumret med samma ändring på kund-, leverantörs- eller bankkontot.
* Om du har angett nummerserie för kontakter när du skapar kund-, leverantörs- eller bankkontokort, skapas automatiskt ett kontaktkort för kunder, leverantörer eller bankkonton.
* Du kan skapa förs.offerter och försäljningsorder, inköpsofferter och inköpsorder från kontakten.
* Dina interaktioner kan registreras när du utför vissa åtgärder som att skriva ut order eller avropsorder, skapa försäljningsserviceorder, skicka e-post osv.
* Om du raderar en kontakt som är länkad till en kund, leverantör eller bank är det bara kontakten som tas bort från programmet. Kunden, leverantören eller bankkontot återstår.
* Om du raderar en kontakt som är länkad till en kund, leverantör eller ett bankkonto är det bara kontakten som återstår.

> [!NOTE]  
>   Vissa detaljer, t.ex fakturering och bokföringsdetaljer, visas inte på kontaktkortet. Följaktligen kan du behöva lägga till dem manuellt på kund-, leverantörs- och bankkontokort, när du skapar kontakter som kunder, leverantörer eller bankkonton.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Koppla kontakter till kunder, leverantörer och bankkonton
Om du har kontakten och antingen en kund, en leverantör eller ett bankkonto för samma företag, kan du länka de två enheterna. När du länkar de tillgängliga enheterna aktiverar synkronisering av data som är gemensam så att den är samma på båda platser.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Länka en kontakt till en befintlig kund, leverantör eller bankkonto
1. Öppna kontakten som du vill länka.
2. Välj åtgärden **Länka med befintlig** och välj sedan **Kund**, **Leverantör** eller **Bank**.
3. Välj den kund, leverantör eller bankkonto att länka till.

   I **Nuvarande huvudfält** anger du vilka fält som ska gälla i händelse av en konflikt mellan fälten på kontakten och kund, leverantör eller konto. Om till exempel säljarkoden är annorlunda i kontakten än kunden kan du bestämma genom att välja **Kontakt** för att använda informationen i kontakten.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Skapa en kund, leverantör eller bankkonto från en kontakt
   Du vill kanske registrera några av dina befintliga kontakter som kunder, leverantörer eller bankkonton. Skapa en kund, en leverantör eller ett bankkonto från en kontakt låter dig använda befintliga data. När du skapar en kund, leverantör eller ett bankkonto på detta sätt, synkroniseras den med kontakten. Synkroniseringen gör information som är gemensam mellan kontakter och kunder, leverantörer eller bankkonton densamma.

   Innan du kan registrera kontakterna på detta sätt måste du ange en affärsrelationskod för bankkonton, kunder eller leverantörer på sidan **Marknadsföringsinställningar**. Om du vill registrera kontakter som bankkonton måste du även ange nummerserien för bankkonton på sidan **Redovisningsinställningar**.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Skapa en kontakt som en kund, en leverantör eller ett bankkonto så här
   1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.
   2. Välj kontakten du vill skapa som en kund, en leverantör eller ett bankkonto.
   3. Välj åtgärden **Skapa som** och välj sedan antingen **Kund**, **Leverantör** eller **Bank**.
   4. Bekräfta det följande meddelandet.

   Kontaktinformationen överförs från kortet **Kontakt** kortet **Bankkonto**, **Kund** eller **Leverantörens**. Du kanske vill lägga till specifik information på varje kort, t.ex fakturering och betalningsinformation.

## <a name="setting-up-business-relations-on-contact-companies"></a>Ställa in affärsrelationer på kontaktföretag
Affärsrelationer används för att visa vilket affärsförhållande du har till kontakterna, till exempel spekulant, bank, konsult eller serviceleverantör.

Att använda affärsrelationer på kontakter är en två-stegsprocess. Först definierar du affärsrelationskoden. Du måste bara utföra den här steget en gång för varje affärsrelation. När du har en affärsrelation kan du börja koppla koden till kontaktföretag.

> [!NOTE]  
>   Om du tänker synkronisera kontakterna med leverantörer, kunder eller bankkonton i andra delar av programmet vill du kanske skapa en affärsrelation för dem.

### <a name="to-define-a-business-relation-code"></a>Definiera en affärsrelationskod
Affärsrelationkoden definierar en kategori eller en typ av affärsrelation, till exempel BANK eller LAG. Du kan ha flera affärsrelationskoder. För att definiera affärsrelationen använder du sidan **affärsrelationer**.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Affärsrelationer** och välj sedan relaterad länk.
2. Välj åtgärden **Ny** och fyll i en kod och en beskrivning. Koden kan bestå av högst 11 tecken, både siffror och bokstäver.

### <a name="AssignBusRelContact"></a> Så här tilldelar du affärsrelationer till kontakter
Du kan inte tilldela affärsrelationer till en kontaktperson, endast företag.

1. Öppna kontakten .
2. Välj åtgärden **företag** och sedan **affärsrelationer**.

    Sidan **Kontakt affärsrelationer** öppnas.
3. I fältet **Affärsrelationskod**, markera den affärsrelation du vill tilldela.

Upprepa stegen för varje affärsrelation du vill tilldela. Affärsrelationer kan också tilldelas i Kontaktlista på samma sätt.

Antalet affärsrelationer som du har tilldelat kontakter anges automatiskt i fältet **Antal affärsrelationer** på avsnittet **Segmentering** på **Kontakt**-sidan.

När du har tilldelat kontakterna affärsrelationer kan du använda dessa uppgifter för urval av kontakter till segmenten. Mer information finns i [Så här lägger du till kontakter i segment](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se även
[Skapa kontaktpersoner](marketing-create-contact-persons.md)   
[Arbeta med Business Central](ui-work-product.md)

