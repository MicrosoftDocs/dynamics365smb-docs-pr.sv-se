---
title: Diagram över hållbarhetskonton och redovisning
description: 'Lär dig hur du hanterar Schema över hållbarhetskonton, kategorier och underkategorier och detaljer om hållbarhetstransaktioner.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="chart-of-sustainability-accounts-and-ledger"></a>Diagram över hållbarhetskonton och redovisning

## <a name="chart-of-sustainability-accounts"></a>Kontoplan för hållbarhetskonton

**Diagram över hållbarhetskonton** (CoSA) utgör den grundläggande strukturerade listan som används för registrering av alla utsläppsdata. Det fungerar som ett ramverk som kategoriserar och organiserar hållbarhetskonton baserat på deras attribut, till exempel scope eller andra grupperingar. Varje konto tilldelas vanligtvis en unik kod eller ett unikt nummer för enkel referens och spårning, enligt samma struktur som en traditionell **kontoplan** men anpassad specifikt för övervakning av hållbarhetsrelaterade data och mätvärden inom en organisation. 
 
Användare kan lägga till **kontokategorier** och **underkategorier** för att definiera hur systemet beter sig, välja dedikerade utsläpp för spårning, emissionsfaktorer, formler och liknande konfigurationer.  

>[!NOTE]
>För att bli bekant med scopes, baserade på GHG (växthusgaser)-standarderna, finns det tre utsläpps-scopes:  
>- **Scope 1 utsläpp**: inkluderar utsläpp som släpps ut från pappersvaror och mobil förbränning och från oavsiktliga flyktiga utsläpp. 
>- **Scope 2 utsläpp**: inkluderar indirekta utsläpp från den energigenerering som köps från elleverantörer. 
>- **Scope 3 utsläpp**: inkluderar ett brett spektrum av utsläpp, från köpta varor och tjänster och kapitalvaror, bränsle- och energirelaterade aktiviteter, uppströms och nedströms transporter, genererat avfall, affärsresor och personalpendling, etc. 

Från **Diagram över hållbarhetskonton** (CoSA), kan du göra sådant som:  

-   Visa rapporter som visar hållbarhetstransaktioner och saldon. 
-   Öppna **Kort för hållbarhetskonto** om du vill lägga till eller ändra inställningar.  
-   Se kategorin och underkategorin för kontot.   
-   Visa separata saldon för var och en av utsläppen för ett enskilt konto. 
-   Lägg till en eller flera **dimensioner** i vart och ett av kontona och ange dimensionsfilter. 
    
Du kan lägga till, ändra eller ta bort **hållbarhetskonton**. För att förhindra avvikelser kan du dock inte ta bort ett **hållbarhetskonto** om det finns en eller flera transaktioner kopplade till kontot.  

### <a name="add-or-change-accounts"></a>Lägga till eller ändra konton

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Diagram över hållbarhetskonton** och väljer sedan relaterad länk. 
2. På sidan **Diagram över hållbarhetskonton** (CoSA) kan du öppna varje **Hållbarhetskonto** och lägga till eller ändra inställningar. Placera markören över ett fält om du vill läsa en kort beskrivning. 

För konton av typen **Summa** måste fältet **Summeringsintervall** fyllas i. För konton av typen **Till-summa** fylls det här fältet i automatiskt med hjälp av funktionen Indrag. När du har skapat alla konton väljer du åtgärden **Indrag av kontoplan för hållbarhetskonton** för att göra det.  

>[!IMPORTANT]
>Om du har angett definitioner i fälten **Summeringsintervall** för konton av typen **Till-summa** innan indragsfunktionen används, måste du ange dessa igen eftersom värdena i alla **Till-summa**-fält skrivs över med funktionen.  

### <a name="delete-accounts"></a>Ta bort konton

Du kan ta bort ett **Hållbarhetskonto**. Innan du tar bort det måste du emellertid vara säker på att det finns en eller flera transaktioner kopplade till det här kontot, eftersom Business Central hindrar dig från att ta bort ett **hållbarhetskonto** i den här situationen.  

## <a name="account-categories"></a>Kontokategorier

Användare måste lägga till **Kategori för hållbarhetskonto** till vart och ett av **hållbarhetskontona** för att definiera hur systemet beter sig, välja utsläpps-scopes, dedikerade utsläpp för spårning, formler och liknande konfigurationer.  

Följ stegen för att granska **Kategorier för hållbarhetskonto**: 

1.  Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kategorier för hållbarhetskonto** och väljer sedan relaterad länk. 
2.  På sidan **Kategorier för hållbarhetskonton** kan du redigera den befintliga listan eller skapa en ny kategori. Om du vill skapa en ny kategori väljer du åtgärden **Ny**.  
3.  Fyll i fälten **Kod** och **Beskrivning**.   
4.  Ställ in fältet **Utsläpps-scope** och välj ett av omfattningsalternativen.  
5.  Välj de gasutsläpp som du vill spåra. För närvarande kan du använda ett av alternativen: **CO2**, **CH4** eller **N2O**. Du kan välja vilken kombination du vill spåra, men du måste ha minst ett utsläpp för spårning.  
6.  I fältet **Beräkningsgrund** kan du välja vilken formel som helst som du vill använda, om du inte vet den exakta utsläppsmängden. Här kan du ange den beräknade grunden (formeln) för utsläppsberäkningen. Du kan välja något av följande alternativ: **Bränsle/el**, **Avstånd**, **Installation** eller **Anpassad**. 
7.  Om du väljer formeln **Anpassad** kan du konfigurera en anpassad beskrivning i fältet **Anpassat värde**.  

>[!NOTE]
>Om den här uppsättningen erbjudna formler i fältet **Beräkningsgrund** inte räcker kan du utöka det här fältet och lägga till fler beräkningar i systemet som ska användas i **hållbarhetsjournalerna**.  

Om du använder **beräkningsgrund** (formler) finns det en förklaring, hur systemet kommer att beräkna baserat på det alternativ du har valt (**EF** är den **emissionsfaktor** som du kan konfigurera på sidan **Underkategori för hållbarhetskonto**): 

|  Utsläppstyp  |  Beräkningsgrund  |  Formel         | Kommentar      |
|------------|--------------|------------------------------|---------------------------------|
| **SCOPE 1**  |
| Stationär förbränning | Bränsle/elektricitet | Utsläpp = bränsle * EF | _dvs Bränsle = Mängden bränsle som används för pannor, värmare, termiska oxidanter..._ |
| Mobil förbränning | Bränsle/elektricitet | Utsläpp = bränsle * EF | _dvs. Bränsle = Mängden bränsle som används för vägfordon eller andra fordon, järnväg..._ |
|  |  |  Utsläpp = Avstånd * EF | _dvs. Avstånd = Körsträcka för fordon på väg eller icke-vägfordon, järnväg..._ |
| Flyktiga utsläpp | Installation | Utsläpp = Multiplikator för installation * Anpassat belopp/100 * Tidsfaktor | _dvs. Anpassad mängd = monteringsförluster, årlig läckagefrekvens..._ |
| **SCOPE 2**  |
| Leverantörer av allmännyttiga tjänster | Bränsle/elektricitet | Utsläpp = Elektricitet * EF | _dvs bränsle/el = elmängd, ångmängd, värmeenhet..._ |
|  | Anpassat | Utsläpp = Anpassad mängd * EF | _dvs anpassad mängd = termisk enhet, tontimme..._ |
| **SCOPE 3**  |
| Inköpta varor och tjänster samt kapitalvaror | Anpassat | Utsläpp = Anpassad mängd * EF | _dvs Anpassad mängd = Kostnad (GL)..._ |
| Uppströms transport och distribution | Avstånd | Utsläpp = Avstånd * EF |  |
|  | Avstånd | Utsläpp = Avstånd * Multiplikator * EF | _Multiplikator = Ton last_ |
| Nedströms transport och distribution | Avstånd | Utsläpp = Avstånd * EF |  |
|  | Avstånd | Utsläpp = Avstånd * Multiplikator * EF | _Multiplikator = Ton last_ |
| Avfall som genereras vid verksamhet och slutbehandling av sålda produkter | Anpassat | Utsläpp = Anpassad mängd * EF | _dvs Anpassad mängd = Avfall_ |
| Affärsresor och personalpendling | Avstånd | Utsläpp = Avstånd * EF | _dvs Avstånd = Körsträcka för tjänstebil, hyrbil, tåg, flyg..._ |
|  | Anpassat | Utsläpp = Anpassad mängd * EF | _dvs Anpassat belopp = Hotellvistelser..._ |
|  | Bränsle/elektricitet | Utsläpp = bränsle * EF | _dvs Bränsle = Mängden bränsle som förbrukas i tjänstebilen, hyrbilen..._ |

## <a name="account-subcategories"></a>Underkategorier för konto

Användare måste lägga till **Underkategori för hållbarhetskonto** till varje **Hållbarhetskonto** för att definiera emissionsfaktorer som ska användas i formlerna, men den baseras på valet för utsläppsspårning i **Kategori för hållbarhetskonto**.  

Följ stegen för att granska **Underkategorier för hållbarhetskonto**:  

1.  Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Underkategorier för hållbarhetskonto** och väljer sedan relaterad länk. 
2.  På sidan **Underkategorier för hållbarhetskonton** kan du redigera den befintliga listan eller skapa en ny kategori. Om du vill skapa en ny kategori väljer du åtgärden **Ny**.  
3.  Fyll i fälten **Kod** och **Beskrivning**.   
4.  Baserat på de gasutsläpp som du vill spåra i **kategorin hållbarhetskonto** och koppla den här underkategorin till kan du också fylla i en eller flera emissionsfaktorer: 

   - **Emissionfaktor CO2** – Anger emissionsfaktorn för CO2-utsläpp.  
   - **Emissionfaktor CH4** – Anger emissionsfaktorn för CH4-utsläpp. 
   - **Emissionfaktor N2O** – Anger emissionsfaktorn för N2O-utsläpp.  

5.  Om underkategorin är relaterad till förnybar energi markerar du fältet **Förnybar energi**.   

>[!NOTE]
>Fälten **Importera data** och **Importera från** är avsedda för potentiell integrering med externa system som används för insamling av emissionsfaktorer, men i **2024 utgivningscykel** kan de inte användas som en funktion som standard.  

## <a name="sustainability-ledger-entries"></a>Hållbarhetstransaktioner

**Hållbarhetsredovisningen** lagrar historiken för alla bokförda hållbarhetstransaktioner och organiserar all utsläppsdata enligt **Diagram över hållbarhetskonton**. När en användare bokför **hållbarhetsjournalen** registreras alla viktiga data där. Alla aktiva rapporter genereras baserat på **hållbarhetstransaktionerna**.   

Användaren kan öppna den här redovisningen för ett visst konto med hjälp av åtgärden **Redovisningstransaktioner** från sidan **Kontoplan för hållbarhetskonton** eller för att öppna alla transaktioner, välj ![glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Hållbarhetstransaktioner** och välj sedan relaterad länk. Placera markören över ett fält om du vill läsa en kort beskrivning.  

>[!IMPORTANT]
>När du har bokfört dina data i hållbarhetsredovisning kan du inte ta bort dem. Om du har gjort ett misstag kan du bokföra den omvända åtgärden med samma uppgifter, men med hjälp av det negativa tecknet för belopp.  

## <a name="see-also"></a>Se även
[Ekonomi](finance.md)    
[Översikt över hållbarhetshantering](finance-manage-sustainability.md)
[Hållbarhetskonfiguration](finance-sustainability-setup.md)
[Så här registrerar du utsläpp](finance-sustainability-journal.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
