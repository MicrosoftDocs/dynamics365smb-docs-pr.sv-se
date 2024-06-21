---
title: Ändra det årliga beloppet på servicekontrakt eller kontraktofferter
description: Du kan ändra beloppet som ska faktureras per år för servicekontraktet eller kontraktsofferten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="change-the-annual-amount-on-service-contracts-or-contract-quotes"></a>Ändra det årliga beloppet på servicekontrakt eller kontraktofferter
Du kan ändra det årliga beloppet på ett servicekontrakt eller en kontraktsoffert om du vill korrigera det årliga faktureringsbeloppet.  

## <a name="to-change-the-annual-amount-of-the-service-contract-or-contract-quote"></a>Så här ändrar du det årliga beloppet på ett servicekontrakt eller en kontraktsoffert

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Servicekontrakt** eller **Servicekontraktsofferter** och sedan väljer du relaterad länk.  
2. Välj kontraktet eller kontraktsofferten.  
3. Välj åtgärden **Öppna kontrakt** om du vill öppna och redigera kontraktet eller skontraktsofferten.  
4. Välj **Tillåt ej balanserade belopp** om du vill ändra det årliga beloppet och distribuera differensen för det årliga beloppet manuellt på kontraktsraderna. Annars kommer differensen för det årliga beloppet automatiskt att distribueras på kontraktsraderna när du har ändrat det årliga beloppet.  
5. Ändra innehållet i fältet **Årligt belopp**. Tänk på att du inte kan signera (konvertera till ett servicekontrakt om du arbetar med en kontraktsoffert) eller låsa ett servicekontrakt som har ett negativt årligt belopp. Om det årliga beloppet anges till noll, måste värdet i fältet **Fakturaperiod** vara **Ingen** när du signerar eller låser servicekontraktet.  
6. Beroende på om rutan i fältet **Tillåt ej balanserade belopp** är markerad eller inte, använder du antingen manuell eller automatisk distribution av differensen för det årliga differensbeloppet. Detta medför att kontraktsraderna uppdateras på ett sätt så att fältet **Beräknat årligt belopp** är lika med det nya årliga beloppet.  

## <a name="distributing-differences-between-new-and-calculated-annual-amounts"></a>Fördela skillnaden mellan nya och beräknade årliga belopp
Om du ändrar det årliga beloppet för ett servicekontrakt eller en kontraktsoffert kan du bli tvungen att distribuera differensen mellan de nya och beräknade årliga beloppen på kontraktsraderna. Det finns tre sätt att fördela belopp:

* Jämn fördelning  
* Fördelning baserad på radbelopp  
* Fördelning baserad på vinst

### <a name="even-distribution"></a>Jämn fördelning
Om du ändrar det årliga beloppet för servicekontraktet eller kontraktsofferten kan du bli tvungen att distribuera differensen mellan de nya och beräknade årliga beloppen på kontraktsraderna. Jämn distribution är en av de automatiska distributionsmetoder som du kan använda om du vill ha en jämn fördelning av differensen mellan de nya och beräknade årliga beloppen mellan radbeloppen på kontraktsraderna. Metodens huvuddrag beskrivs i listan över distributionsprocessen nedan:  

1. Differensen mellan de nya värdena i fälten **Årligt belopp** och **Beräknat årligt belopp** divideras med antalet kontraktsrader på servicekontraktet eller på kontraktsofferten.  
2. Värdet i fältet **Radbelopp** uppdateras med värdet från den föregående operationen.  
3. Innehållet i fälten **Radrabattbelopp**, **Radrabatt %** och **Vinst** uppdateras med det nya värdet i fältet **Radrabatt** på följande sätt:   
    * Radrabatt = Radvärde - Radbelopp.  
    * Radrabatt % = Radrabatt / Radvärde × 100.  
    * TB = Radbelopp – Radkostnad  

 Upprepa stegen för varje kontraktsrad.  

#### <a name="example"></a>Exempel
Det finns ingen markering i fältet **Tillåt ej balanserade belopp** i servicekontraktet som innehåller tre kontraktsrader med dylik information.  

|Artikel|Radkostnad|Radvärde|Radrabatt %|Radrabattbelopp|Radbelopp|TB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|30,00|40,00|0,00|0,00|40,00|10,00|  
|Artikel 2|40,00|50,00|10,00|5,00|45,00|5,00|  
|Artikel 3|50,00|70,00|10,00|7,00|63,00|13,00|  

Fältvärdet för **Årligt belopp** är lika med innehållet i fältet **Beräknat årligt belopp** som alltid har angetts till summan av radbeloppen. I det här fallet är det lika med följande: 40 + 45 + 63 = 148.  

Om du ändrar **Årligt belopp** till 139, beräknas det belopp som ska läggas till i varje **Radbelopp**-fält. Detta belopp beräknas genom att subtrahera **Beräknat årligt belopp** från det nya värdet i fältet **Årligt belopp** dividerat med antalet kontraktsrader i servicekontraktet. I det här fallet är det lika med följande: (139 – 148) / 3 = -3. Sedan läggs den senast beräknade siffran till i värdet för varje **Radbelopp**-fält och värdena i fälten **Radrabatt %**, **Radrabatt** och **Vinst** uppdateras med hjälp av formlerna i de steg som beskrivs ovan.  

Slutligen innehåller kontraktsraderna följande information.  

|Artikel|Radkostnad|Radvärde|Radrabatt %|Radrabattbelopp|Radbelopp|TB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|30,00|40,00|7,50|3,00|37,00|7,00|  
|Artikel 2|40,00|50,00|16.00|8.00|42.00|2.00|  
|Artikel 3|50.00|70.00|14.29|10.00|60.00|10.00|  

### <a name="distribution-based-on-line-amount"></a>Fördelning baserad på radbelopp
Om du ändrar det årliga beloppet för servicekontraktet eller kontraktsofferten kan du bli tvungen att distribuera differensen mellan de nya och beräknade årliga beloppen på kontraktsraderna. Distribution beräknad på radbelopp är en automatisk metod som du kan använda om du vill ha en jämn fördelning av differensen mellan de nya och de beräknade årliga beloppen mellan radbeloppen på kontraktsraderna. Distributionen görs i proportion till radbeloppsandelarna av det beräknade årliga beloppet. Följande lista med distributionsprocedursteg för varje kontraktsrad beskriver huvuddragen för den här metoden:  

1. Procentuell radbeloppsandel beräknas på följande sätt: innehållet i fältet **Radbelopp** divideras med värdena i fältet **Beräknat årligt belopp** på alla kontraktsrader.  
2. Värdet i fältet **Radbelopp** uppdateras genom ett tillägg av differensen mellan nytt och beräknat årligt belopp, som multipliceras med den procentuella radbeloppsandelen.  
3. Innehållet i fälten **Radrabattbelopp**, **Radrabatt %** och **Vinst** uppdateras utifrån det nya värdet i fältet **Radrabattbelopp** på följande sätt:  

    * Radrabatt = Radvärde – Radbelopp.  
    * Radrabatt % = Radrabatt / Radvärde × 100  
    * TB = Radbelopp – Radkostnad  

Upprepa stegen för varje kontraktsrad.  

#### <a name="example-1"></a>Exempel
Det finns ingen markering i fältet **Tillåt ej balanserade belopp** i servicekontraktet som innehåller tre kontraktsrader med dylik information.  

|Artikel|Radkostnad|Radvärde|Radrabatt %|Radrabattbelopp|Radbelopp|TB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|15,00|17,00|3,00|0,51|25,00|1,49|  
|Artikel 2|20,00|23,00|Ingen|0,00|55,10|3,00|  
|Artikel 3|24,00|27,00|3,00|0,81|112,70|2,19|  

Fältvärdet för **Årligt belopp** är lika med innehållet i fältet **Beräknat årligt belopp** som alltid har angetts till summan av radbeloppen. I det här fallet är det lika med följande: 16,49 + 23,00 + 26,19 = 65,68.  

Om du ändrar **Årligt belopp** till 60, beräknas procentuella TG för varje kontraktsrad:  

* Artikel 1 – 5 / (5 + 5,1 +12,7) = 0,2193 %  
* Artikel 2 –5.1 / (5 + 5,1 +12,7) = 0,2237  
* Artikel 3 – 12,7 / (5 + 5,1 + 12,7) = 0,557  

Därefter uppdateras värdet i fältet **Radbelopp** på varje kontraktsrad med hjälp av formeln: Radbelopp = Radbelopp + skillnaden mellan nya och beräknade årliga belopp × Procentuellt bidrag. Sedan uppdateras värdena i fälten **Radrabattbelopp**, **Radrabatt %** och **Vinst** med hjälp av formlerna i den process som beskrivs ovan.  

Slutligen innehåller kontraktsraderna följande information.  

|Artikel|Radkostnad|Radvärde|Radrabatt %|Radrabattbelopp|Radbelopp|TB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|15,00|17,00|11,41|1,94|15,06|0,06|  
|Artikel 2|20,00|23,00|8.65|1.99|21.01|1.01|  
|Artikel 3|24.00|27.00|11.37|3.07|23.93|–0,07|  

### <a name="distribution-based-on-profit"></a>Fördelning baserad på vinst
Om du ändrar det årliga beloppet för servicekontraktet eller kontraktsofferten kan du bli tvungen att distribuera differensen mellan de nya och beräknade årliga beloppen på kontraktsraderna. Distribution beräknad på TB är en av de automatiska metoder som du kan använda om du vill ha en jämn fördelning av differensen mellan de nya och beräknade årliga beloppen mellan radbeloppen på kontraktsraderna. Distributionen görs i proportion till andelarna av total kontrakts-TB eller kontraktsoffert-TB. Följande lista med distributionsprocedursteg för varje kontraktsrad beskriver huvuddragen för den här metoden:  

1. Procentuell TB-andel beräknas på följande sätt: innehållet i fältet **TB** divideras med summan av värdena i fältet **TB** för alla kontraktsrader.  
2. Värdet i fältet **Radbelopp** uppdateras genom ett tillägg av differensen mellan nytt och beräknat årligt belopp, som multipliceras med den procentuella TB-andelen.  
3. Innehållet i fälten Radrabattbelopp, Radrabatt % och Vinst uppdateras med det nya värdet i fältet **Radbelopp** på följande sätt:  

    * Radrabatt = Radvärde – Radbelopp.  
    * Radrabatt % = Radrabatt / Radvärde × 100  
    * TB = Radbelopp – Radkostnad  

#### <a name="example-2"></a>Exempel
Det finns ingen markering i fältet **Tillåt ej balanserade belopp** i servicekontraktet som innehåller tre kontraktsrader med dylik information.  

|Artikel|Radkostnad|Radvärde|Radrabatt %|Radrabattbelopp|Radbelopp|TB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|20,00|25,00|0,00|0,00|25,00|5,00|  
|Artikel 2|50,00|58,00|5,00|2,90|55,10|5,10|  
|Artikel 3|100,00|115,00|2,00|2,30|112,70|12,70|  

Fältvärdet för **Årligt belopp** är lika med innehållet i fältet **Beräknat årligt belopp** som alltid har angetts till summan av radbeloppen. I det här fallet är det lika med följande: 25,00 + 55,10 + 112,70 = 192,80.  

 Om du ändrar **Årligt belopp** till 180, beräknas procentuella TG för varje kontraktsrad:  

* Artikel 1 –5 / (5 + 5,1 +12,7) = 0,2193 %  
* Artikel 2 –5.1 / (5 + 5,1 +12,7) = 0,2237  
* Artikel 3 – 12,7 / (5 + 5,1 + 12,7) = 0,557  

Därefter uppdateras värdet i fältet **Radbelopp** på varje kontraktsrad med hjälp av formeln: Radbelopp = Radbelopp + skillnaden mellan nya och beräknade årliga belopp × Procentuellt bidrag. Sedan uppdateras värdena i fälten **Radrabatt**, **Radrabatt %**  och **TB** med hjälp av formlerna i steg 3 i den process som beskrivs ovan.  

Slutligen innehåller kontraktsraderna följande information.  

|Artikel|Radkostnad|Radvärde|Radrabatt %|Radrabattbelopp|Radbelopp|TB|  
|----------|---------------|----------------|---------------------|--------------------------|-----------------|------------|  
|Artikel 1|20,00|25,00|11,24|2,81|22,19|2,19|  
|Artikel 2|50,00|58,00|9.93|5.76|52.24|2.24|  
|Artikel 3|100.00|115.00|8.20|9.43|105.57|5.57|  

## <a name="see-also"></a>Se även
[Så här skapar du servicekontrakt och servicekontraktsofferter](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Ställa in tjänstehantering](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
