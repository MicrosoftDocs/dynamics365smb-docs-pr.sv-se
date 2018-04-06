---
title: "Designdetaljer: Avstämning med redovisningen | Microsoft Docs"
description: "Det här avsnittet beskriver avstämning med redovisningen när du bokför lagertransaktioner, till exempel försäljningsutleveranser, produktionsutflöde eller negativa justeringar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, reconciliation, general ledger, inventory
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 813af57a2e1de62ce038990116f9cf92f741a78d
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-reconciliation-with-the-general-ledger"></a>Designdetaljer: Avstämning med redovisningen
När lagertransaktioner bokförs till exempel utleveranser, produktionsutflöde eller negativa justeringar registreras antals- och värdeändringarna i lagret i artikeltransaktionerna respektive värdetransaktionerna. Nästa steg i processen går ut på att bokföra lagervärdena på redovisningens lagerkonton.  

Det finns två sätt att stämma av lagerredovisningen med redovisningen:  

* Manuellt genom att köra batch-jobbet **Bokför lagerkostnad i redov.**.  
* Automatiskt, varje gång som du bokför en lagertransaktion.  

## <a name="post-inventory-cost-to-gl-batch-job"></a>Batchjobbet Bokför lagerkostnad i redovisning.  
När batch-jobbet **Bokför lagerkostnad i redov.** körs skapas redovisningstransaktionerna utifrån värdetransaktioner. Du kan sammanställa redovisningstransaktioner för varje värdetransaktion, eller skapa redovisningstransaktioner för varje kombination av bokföringsdatum, lagerställekod, lagerbokföringsmall, generell rörelsebokföringsmall och generell produktbokföringsmall.  

Bokföringsdatum för redovisningstransaktionerna anges till bokföringsdatumet för motsvarande värdetransaktion, utom när värdetransaktionen infaller i en stängd bokföringsperiod. I det här fallet hoppas värdetransaktionen över och du måste ändra antingen redovisningsinställningar eller användarinställningar för att aktivera bokföring i datumintervallet.  

När du kör batch-jobbet **Bokför lagerkostnad i redov.** kan du få fel på grund av med saknad inställning eller inkompatibel dimensionsinställning. Om fel uppstår i batch-jobbets dimensionsinställning ersätter den dessa fel och använder dimensionerna för värdetransaktionen. För andra fel bokför batch-jobbet inte värdetransaktionerna och anger dem vid slutet av rapporten i avsnittet **Transaktioner som hoppats över**. För att bokföra de här transaktionerna måste du först lösa felen. Om en lista över felen ska visas innan batch-jobbet för bokföring ska köras kan rapporten **Bokför lagerkostnad i redovisning**. Alla fel som inträffar under testbokföringen visas i en lista i testrapporten. Därefter går det att korrigera felen och köra batch-jobbet för bokföringen av lagerkostnaden utan att transaktioner hoppas över.  

## <a name="automatic-cost-posting"></a>Automatisk kostnadsbokföring  
Om du vill göra så att kostnadsbokföringen till redovisningen körs automatiskt när du bokför en lagertransaktion markerar du kryssrutan **Automatisk kostnadsbokföring** i fönstret **Lagerinställning**. Bokföringsdatumet för redovisningstransaktionen är detsamma som bokföringsdatumet för artikeltransaktionen.  

## <a name="account-types"></a>Kontotyper  
Under avstämning bokförs lagervärden i lagerkontot i balansräkningen. Samma belopp, men med omvänt tecken, bokförs på det relevanta motkontot. Vanligtvis är motkontot ett resultaträkningkonto. Men när du bokför direkt kostnad som hör till förbrukning eller utflöde är motkontot ett balansräkningskonto. Typen av artikeltransaktion och värdetransaktionen avgör vilket redovisningskonto att bokföra på.  

Transaktionstypen anger vilket redovisningskonto att bokföra på. Det bestäms antingen av antalets tecken i artikeltransaktionen eller det värderade antalet i värdetransaktionen, eftersom antalen har alltid samma tecken. En försäljningspost med ett positivt antal beskriver till exempel en lagerminskning som orsakas av en försäljning, och en försäljningstransaktion med ett negativt antal beskriver en lagerökning som orsakas av en försäljningsretur.  

### <a name="example"></a>Exempel  
Följande exempel visar en cykelkedja som tillverkas av inköpta länkar. I det här exemplet visas hur de olika redovisningskontotyperna används i ett typiskt scenario.  

Kryssrutan **Förväntad kost.bokf. i redovisningen** i fönstret **Lagerinställningar** är markerad i och följande inställning har definierats.  

Följande tabell visar hur länken ställs in på artikelkortet.  

|Inställningsfält|Värde|  
|-----------------|-----------|  
|**Värderingsprincip**|Standard|  
|**Standardkostnad**|1,00 SEK|  
|**Omkostnad**|0,02 SEK|  

Följande tabell visar hur kedjan ställs in på artikelkortet.  

|Inställningsfält|Värde|  
|-----------------|-----------|  
|**Värderingsprincip**|Standard|  
|**Standardkostnad**|150,00 SEK|  
|**Omkostnad**|25,00 SEK|  

Följande tabell visar hur länken produktionsgruppen ställs in på produktionsgruppskortet.  

|Inställningsfält|Värde|  
|-----------------|-----------|  
|**A-pris senaste inköp**|2,00 SEK|  
|**Omkostnad %**|10|  

##### <a name="scenario"></a>Scenario  
1. Användaren köpen 150 länkar och bokför inköpsordern som inlevererad. (Inköp)  
2. Användaren bokför inköpsordern som fakturerad. Det skapas ett omkostnadsbelopp på BVA 3,00 som ska fördelas och ett avvikelsebelopp på BVA 18,00. (Inköp)  

    1. Interimskontona rensas. (Inköp)  
    2. Direkt kostnad bokförs. (Inköp)  
    3. Indirekt kostnad beräknas och bokförs. (Inköp)  
    4. Inköpsvariansen beräknas och bokförs (endast för standardkostnadobjekt). (Inköp)  
3. Användaren säljer en kedja och bokför försäljningsordern som levererad. (Försäljning)  
4. Användaren bokför försäljningsordern som fakturerad. (Försäljning)  

    1. Interimskontona rensas. (Försäljning)  
    2. Kostnaden för sålda varor (KSV) bokförs. (Försäljning)  

        ![Resultatet av försäljningsbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_sales.png "design_details_inventory_costing_3_GL_posting_sales")  
5. Användaren bokför förbrukning av 150 länkar, som är antalet länkar som används för att producera en kedja. (Förbrukning, material)  

    ![Resultatet av materialbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_material.png "design_details_inventory_costing_3_GL_posting_material")  
6. Produktionsgruppen använde 60 minuter för att producera kedjan. Användaren bokför konverteringskostnaden. (Förbrukning, Kapacitet)  

    1. Direkta kostnader bokförs. (Förbrukning, Kapacitet)  
    2. Indirekta kostnader beräknas och bokförs. (Förbrukning, Kapacitet)  

        ![Resultatet av kapacitetsbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_capacity.png "design_details_inventory_costing_3_GL_posting_capacity")  
7. Användaren bokför förväntade kostnaden för en kedja. (Utflöde)  
8. Användaren avslutar produktionsordern och kör batch-jobbet **Justera kost. - artikel trans**. (Utflöde)  

    1. Interimskontona rensas. (Utflöde)  
    2. Den direkta kostnaden överförs från PIA-kontot till lagerkontot. (Utflöde)  
    3. Den indirekta kostnaden (omkostnader) överförs från kontot för indirekt kostnad till lagerkontot. (Utflöde)  
    4. Det resulterar i ett avvikelsebelopp på BVA 157,00. Varianser beräknas endast för standardkostnadobjekt. (Utflöde)  

        ![Resultatet av utflödesbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_output.png "design_details_inventory_costing_3_GL_posting_output")  

        > [!NOTE]  
        >  För enkelhets skull visas bara ett varianskonto. I verkligheten finns fem olika konton:  
        >   
        >  * Materialvarians  
        >  * Kapacitetsvarians  
        >  * Kapacitetsomkostnadsvarians  
        >  * Legotillverkning varians  
        >  * Produktionsomkostnadsvarians  

9. Användaren omvärderar kedjan från BVA 150,00 till BVA 140,00. (Justering/Omvärdering/Avrundning/Överföring)  

    ![Resultatet av justeringsbokföring till G&#47;L-konton](media/design_details_inventory_costing_3_gl_posting_adjustment.png "design_details_inventory_costing_3_GL_posting_adjustment")  

För mer information om sambandet mellan kontotyperna och de olika typerna av värden, se [Designdetaljer: Konton i redovisningen](design-details-accounts-in-the-general-ledger.md).  

## <a name="see-also"></a>Se även  
[Designdetaljer: Lagerkalkylering](design-details-inventory-costing.md)   
[Designdetaljer: Bokföring av förväntad kostnad](design-details-expected-cost-posting.md)   
[Designdetaljer: kostnadsjustering](design-details-cost-adjustment.md)
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

