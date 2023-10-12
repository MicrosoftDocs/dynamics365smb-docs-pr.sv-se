---
title: Skapa ett leverantörskort för att registrera en ny leverantör (innehåller video)
description: Lär dig hur du skapar ett leverantörskort för registrering av en ny leverantör eller leverantör och hur du sparar leverantörskort som en mall.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: '26, 27, 34, 461, 786, 1379, 1385, 1386, 1628'
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="register-new-vendors"></a>Registrera nya leverantörer

Leverantörer erbjuder produkter som du säljer. Varje leverantör som du har köpt av måste registreras som ett leverantörskort.

Innan du kan registrera nya leverantörer, måste du lägga upp olika inköpskoder som du kan välja mellan, när du fyller i leverantörskort. När alla nödvändiga basdata har skapats kan du lägga till unika egenskaper för en leverantör, till exempel genom att prioritera leverantören i betalningssyfte och upprätta en lista över artiklar som leverantören och andra leverantörer kan tillhandahålla. En annan grupp av inställningsuppgifter för leverantörer är att lägga in dina avtal om inköpspris, rabatter och betalning. Läs mer i [Ställa in inköp](purchasing-setup-purchasing.md).

Leverantörskort innehåller den information som behövs för att köpa produkter från varje leverantör. Mer information finns i [Registrera inköp](purchasing-how-record-purchases.md) och [Så här registrerar du nya artiklar](inventory-how-register-new-items.md).
<br /><br />  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Lägga till nya leverantörer

Du kan lägga till nya leverantörer manuellt, genom att fylla i sidan för **leverantörskortet** eller använda mallar som innehåller fördefinierad information. Du kan t.ex. skapa mallar för olika typer av leverantörsprofiler. När du använder mallar sparar du tid när du lägger till nya leverantörer och ser till att informationen är korrekt varje gång.

> [!NOTE]  
> Om leverantörsmallar finns för olika leverantörstyper, när du börjar skapa ett nytt leverantörskort kommer du att se en sida där du kan välja rätt mall. Om endast en leverantörsmall finns, då använder nya leverantörskort alltid den mallen.

När du har skapat en mall kan du använda åtgärden **tillämpa mall** för att tillämpa den på en eller flera valda leverantörer. Om du vill skapa en mall fyller du i den information som du vill använda på **leverantörskort** och sparar den som en mall. Mer information finns i [För att spara sidan Leverantörskort som en mall](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Det kan vara användbart att anpassa sidan för **leverantörsmall** när du skapar en mall. Du kanske till exempel vill lägga till ett fält som inte redan visas på sidan. Mer information finns i avsnittet [Anpassa din arbetsyta](/dynamics365/business-central/ui-personalization-user#start-personalizing-by-using-the-personalization-mode).

Du kan också skapa en leverantör från en kontakt. Mer information finns i avsnittet [Skapa en kund, leverantör, anställd eller bankkonto från en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

Remittera till-adresser används när du skriver ut checkar för att betala leverantörerna, och leverantörer kan ha flera remittera till-adresser för betalningar. En leverantör kan till exempel leverera en artikel från ett dotterbolag, men vill erhålla betalning vid sitt huvudkontor. Med [!INCLUDE [prod_short](includes/prod_short.md)] kan du skapa flera postadresser för varje leverantör, och du kan välja rätt plats att skicka betalningar till per faktura.

Du anger remittera till-adresser på leverantörskortsidorna och på snabbfliken Leverans & betalningar på inköpsorder och fakturor. När du skapar utbetalningsjournalrader med hjälp av åtgärderna Betala leverantör eller Skapa betalning på sidan Leverantörslista eller sidan Leverantörskort, eller åtgärden Koppla transaktioner i en utbetalningsjournal, tilldelas remittera till-koden på leverantörsreskontratransaktionen. Du kan skriva över det här värdet.

### <a name="to-create-a-new-vendor"></a>Skapa en ny leverantör

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Om du inte vet vilken faktureringsadress som ska användas för respektive faktura från en leverantör fyller du inte i fältet **Nr.** fältet i snabbfliken **Allmänt**. Välj i stället betalningsleverantörens nummer när du har skapat en inköpsoffert, order eller ett inköpshuvud.

Leverantören är nu registrerad, och leverantörskortet är klart att användas i inköpsdokument.

Om du vill använda detta leverantörskort som en mall när du skapar nya leverantörskort, så fortsätt med att spara den som en leverantörsmall. Mer information finns i [För att spara sidan leverantörskort som en mall](#to-save-the-vendor-card-as-a-template)

### <a name="deleting-and-editing-vendor-information"></a>Ta bort och redigera leverantörsinformation

Du kan när som helst redigera informationen på leverantörskort. Om du har bokfört en transaktion för en leverantör kan du inte ta bort kortet eftersom transaktionerna kan behövas för revision. Om du vill ta bort leverantörskort med transaktioner, kontaktar du Microsoft partner för att göra det via kod.

> [!TIP]
> Du kan ändra IBAN på ett leverantörsbankkonto utan den ändring som påverkar de historiska kreditöverföring journalposterna. Kreditöverföringsjournaler lagrar *mottagarens IBAN*, *Mottagarens bankkontonummer* som har angetts i fälten **leverantörsbankkonto** och **mottagarnamn** på sidan **leverantörskort** när transaktionerna skapades.

> [!TIP]
> Du kan lägga till alternativa adresser på leverantörs kort genom att välja åtgärden **orderadresser**.

## <a name="to-save-the-vendor-card-as-a-template"></a>Om du vill spara leverantörskortet som en mall

1. På sidan **Leverantörskort** väljer du åtgärden **Spara som mall**. Sidan **leverantörsmall** öppnas uppvisar leverantörskortet som mall.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Om du vill återanvända dimensioner i mallar väljer du fönstret **Dimensioner**. Sidan **Dimensionsmallar** öppnas och visar de dimensionskoder som ställts in för leverantören.
4. Ändra eller ange dimensionskoder som ska kopplas till nya leverantörskort som skapas med hjälp av mallen.
5. Välj **OK** när du har slutfört den nya leverantörsmallen.  
   Leverantörsmallen läggs till listan över leverantörsmallar, så att du kan använda det för att skapa nya leverantörskort.

## <a name="see-also"></a>Se även

[Slå samman dubblettposter](sales-how-merge-duplicate-records.md)  
[Skapa nummerserier](ui-create-number-series.md)  
[Skapa bankkonton för leverantörer](purchasing-how-set-up-vendors-bank-accounts.md)  
[Konfigurera inköpare](purchasing-how-setup-purchasers.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Registrera inköp](purchasing-how-record-purchases.md)  
[Använd Online Map för att hitta platser och vägbeskrivningar](across-online-maps.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
