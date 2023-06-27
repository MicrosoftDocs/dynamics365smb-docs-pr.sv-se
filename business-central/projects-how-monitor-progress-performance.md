---
title: Övervaka projektframsteg och -resultat
description: Beskriver hur du skapar en PIA-metod och beräknar PIA för att uppskatta det ekonomiska värdet i lika jobb medan de pågår.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.search.keywords: 'project management, KPI, work in process, work in progress'
ms.search.form: '89, 92, 1010'
---
# <a name="monitor-job-progress-and-performance" />Övervaka projektframsteg och -resultat

Med funktionen Produkter i arbete (PIA) kan du uppskatta det ekonomiska värdet av pågående jobb i huvudboken.

Allt eftersom ett jobb fortskrider förbrukas material och resurser och utgifter uppstår som måste bokföras till jobbet. I många fall kan du bokföra kostnader för ett projekt innan du fakturerar. Om endast kostnader bokförts blir er finansiella rapport oriktig. Om du vill följa upp det verkliga värdet för projektet beräknar du PIA och bokför det i redovisningen. Läs mer [om hur du förstår PIA-metoder](projects-understanding-wip.md).

Du kan beräkna PIA baserat på:

* Kostnadsvärde
* Försäljningsvärde
* Identifierbar kostnad
* Procent färdigställt
* Slutfört kontrakt

<!--If you want to view the result using a different method, change the method and calculate WIP again. There's no limit to the number of times you calculate WIP; it doesn't get automatically posted to the general ledger. After you've calculated WIP using the method you prefer, you can post to the general ledger.-->
<!--Unhide the above paragraph?-->

## <a name="create-a-job-wip-method" />Skapa en PIA-metod

Skapa en PIA-metoden för projektet som visar behoven i organisationen och ange som standard.  

> [!NOTE]
> När du har använt den nya metoden för att skapa PIA-transaktioner kan du ändra eller ta bort den metoden  

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **PIA-metoder för projekt** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Stäng sidan.   
4. För att göra denna nya metod till standard, välj ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projektinställningar** och väljer sedan relaterad länk.  
5. I fältet **Standard-PIA-metod** väljer du metoden i listan.

## <a name="define-a-wip-method-for-a-job" />Definiera en PIA-metod för ett projekt

När du skapar ett nytt projekt måste du ange vilken PIA-metod för projektet som gäller. I vissa fall är den PIA-metod för projekt som du använder redan angiven som standard.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.
2. Välj åtgärden **Ny**. Läs mer i [skapa jobb](projects-how-create-jobs.md).  
3. PÅ sidan **Projektkort**, i fältet **PIA-metod**, väljer du en PIA-metod i listan. Om en standardmetod har definierats, kan du välja ett annat alternativ vid behov.  

### <a name="define-a-wip-method-for-a-job-task" />Definiera du en PIA-metod för ett projekt

Du kan definiera en PIA-metod för en projektaktivitet, utelämna vissa projekt aktiviteter från PIA-beräkning eller gruppera aktiviteter så att de beräknas tillsammans. 

Om du vill beräkna PIA för varje projekt aktivitet för sig, skapar du PIA-bokföring med definierade dimensioner för de specifika aktiviteterna.

**PIA-Total** anger jobbuppgifter som du vill gruppera vid beräkning av PIA och igenkänning. I en grupp med aktiviteter måste det finnas en aktivitet som uppfyller två villkor:
<!--But doesn't the parenthetical below contradict this -* if there is no total, the application sets the total for you, meaning the condition does not HAVE to be satisfied, right? Or am I missing something?-->

* Har en **PIA-total** mängd till *total*. (Om det inte finns några projektaktiviteter med **PIA-totalen** angiven på *Totalt* ska *Totalt* anges automatiskt på den sista projektaktivitetsraden när PIA beräknas för första gången.)

* Har ett **Projektaktivitetsnr.** som är det slutgiltiga antalet i gruppen eller intervallet av projektaktiviteter.

De tre alternativen beskrivs i tabellen nedan:

| Fält | Description |
|--|--|
| **\<blank\>** | Ska lämnas tom om projektaktiviteten utgör en del av en projektaktivitetsgrupp. |
| **Summa** | Definierar intervallet eller gruppen av aktiviteter som ingår i PIA- och resultatbeloppsberäkningen. Inom gruppen ska **Typ av projektaktivitet** som angetts som **Bokföring** ingå i PIA-totalen om inte fältet **PIA-total** angetts som **Exklusive**. |
| **Exklusive** | Gäller endast en uppgift med **Typ av projektaktivitet** av **Bokföring**, i vilket fall uppgiften inte inkluderas när PIA och igenkänning beräknas. |

I följande exempel är projekt aktiviteter uppdelade i två PIA totalt antal grupperingar som visar hur fältet **PIA-totalen** arbetar:

|Projektaktivitetsnr.|Description|Typ av projektaktivitet|Fältet **PIA-Total**|  
|------------------|----------------------|----------------------|----------------------|  
|1 000|Förberedelse|Från-summa|\<blank\>|
|1010|.    Städning och renhållning|Bokföra|**Exklusive**|
|1099|Fullständig förberedelse|Till-summa|\<blank\>|
|1100|Mattläggning|Från-summa|\<blank\>|
|1110|.    Limma golv|Bokföra|**Exklusive**|
|1120|.    Lägga ut matta|Bokföra|\<blank\>|
|1199|Summa mattläggning|Till-summa|\<blank\>|
|1200|Slutför|Från-summa|\<blank\>|
|1210|.    Dammsugning av matta|Bokföra|\<blank\>|
|1299|Summa ytbehandling|Till-summa|**Summa**|
|1300|Felkorrigering|Från-summa|\<blank\>|
|1310|.    Felkorrigering|Bokföra|\<blank\>|
|1399|Summa felkorrigering|Till-summa|**Summa**|

Du kommer att märka:

* *1000* till *1299*: PIA kommer att beräknas separat för den här gruppen av projektaktiviteter. Observera dock att två av uppgifterna, 1010 och 1110, inte ingår i PIA-beräkningen eftersom deras projekt aktivitetstyp **bokföra**.

* *1300* till *1399*: PIA kommer att beräknas separat för den här gruppen av projektaktiviteter.

## <a name="calculate-wip" />Beräkna PIA

Du kan fastställa PIA-beloppet som ska bokföras på balansräkningskonton för periodslutsrapporteringen. Använd batch-jobbet **Projekt – Beräkna PIA** om du vill göra detta.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt – Beräkna PIA** och väljer sedan relaterad länk.  
2. Välj åtgärden **Beräkna PIA**.
3. På sidan **Projekt – Beräkna PIA** fyller du i fälten efter behov.
4. Välj **OK**.  

> [!NOTE]  
>   Batchjobbet beräknar endast PIA, det bokförs inte till huvudboken. Om du vill bokföra måste du köra batch-jobbet **Bokför PIA i redovisning** när du har beräknat PIA. Läs mer i följande procedur.

## <a name="post-wip" />Bokföra PIA

När du har beräknat PIA kan du bokföra det på balansräkningskonton för rapportering vid periodens slut. Använd batch-jobbet **Projekt – Bokför PIA i redovisning** om du vill göra detta.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt – Bokför PIA i redovisning** och väljer sedan relaterad länk.  
2. På sidan **Projekt – Bokför PIA i redovisning** fyller du i fälten efter behov.  
3. Välj **OK**.

## <a name="calculate-and-post-job-completion-entries" />Beräkna och bokföra slutförda projekt

När du har slutfört alla aktiviteter i ett projekt, bland annat bokföringen och faktureringen av förbrukning, måste du uppdatera projektet så att projektet får **Statusen** **Slutförd**. Sedan måste du återföra alla PIA som har bokförs i redovisningen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj ett öppet projekt och välj sedan åtgärden **Redigera**.
3. Markera **Slutförd** i fältet **Status** .
4. Följ hjälpstegen steg för att beräkna och bokföra PIA. Följ steg 5 och 6 för att göra det manuellt.  
5. Välj åtgärden **Beräkna PIA**.
6. På sidan **Projekt – Beräkna PIA** fyller du i fälten efter behov.  

     De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.  
7. Välj åtgärden **Projekt – Bokför PIA i redovisning**.
8. På sidan **Projekt – Bokför PIA i redovisning** fyller du i fälten efter behov.  

     De PIA-transaktioner för jobbet som skapas när du kör batch-jobbet kommer nu att ha fältet **Slutfört projekt** markerat för att visa att de är slutförda.

## <a name="view-job-ledger-entries" />Visa projekttransaktioner

Alla projektrelaterade transaktioner registreras i bokförda projektjournaler och numreras i ordningsföljd med start från nummer ett. I den bokförda projektjournalen kan du få en överblick över alla projekttransaktioner.    

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **projektjournaler** och väljer sedan relaterad länk.
2. Välj en relevant journal och välj sedan åtgärden **Projekttransaktioner**.

På sidan **Projekttransaktioner** kan du granska de transaktioner som är kopplade till alla projekt.  

## <a name="find-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/paths/calculate-post-job-wip/)

## <a name="see-also" />Se även

[Genomgång: Beräkna produkter i arbete för ett projekt](walkthrough-calculating-work-in-process-for-a-job.md)
[Hantera projekt](projects-manage-projects.md)  
[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
