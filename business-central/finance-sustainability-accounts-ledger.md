---
title: Kontoplan för hållbarhetskonton och huvudbok
description: 'Lär dig hur du hanterar Schema över hållbarhetskonton (CoSA), kategorier och underkategorier och detaljer om hållbarhetstransaktioner.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Diagram över hållbarhetskonton och redovisning

## Kontoplan för hållbarhetskonton

Diagram över hållbarhetskonton (CoSA) utgör den grundläggande strukturerade listan som används för att registrera alla utsläppsdata. Det fungerar som ett ramverk som kategoriserar och organiserar hållbarhetskonton baserat på deras attribut, till exempel scope eller andra grupperingar. Varje konto tilldelas vanligtvis en unik kod eller ett unikt nummer för enkel referens och spårning. Den har samma struktur som en traditionell kontoplan men är anpassad specifikt för att övervaka hållbarhetsrelaterade data och mätvärden i en organisation.

Användare kan lägga till hållbarhetskontokategorier och underkategorier för hållbarhetskonton för att definiera hur systemet beter sig. På detta sätt kan de välja dedikerade utsläpp att spåra, emissionsfaktorer, formler och liknande konfigurationer.

> [!NOTE]
> Baserat på GHG-standarderna (växthusgaser), finns det tre utsläpps-scopes:
>
> - **Scope 1 utsläpp** inkluderar utsläpp från stationär och mobil förbränning och från oavsiktliga flyktiga utsläpp.
> - **Scope 2 utsläpp** inkluderar indirekta utsläpp från den energigenerering som köps från elleverantörer.
> - **Scope 3 utsläpp** inkluderar ett brett spektrum av utsläpp, från köpta varor och tjänster och kapitalvaror, bränsle- och energirelaterade aktiviteter, uppströms och nedströms transporter, genererat avfall, affärsresor och personalpendling, etc.

Från CoSA kan du göra saker som:

- Visa rapporter som visar hållbarhetstransaktioner och saldon.
- Öppna kort för hållbarhetskonto om du vill lägga till eller ändra inställningar.
- Visa kategorin och underkategorin för kontot. 
- Visa separata saldon för var och en av utsläppen för ett enskilt konto.
- Lägg till en eller flera dimensioner i vart och ett av kontona och ange dimensionsfilter.

Du kan lägga till, ändra eller ta bort hållbarhetskonton. För att förhindra avvikelser kan du dock inte ta bort ett hållbarhetskonto om det finns en eller flera transaktioner kopplade till den.

### Lägga till eller ändra konton

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Diagram över hållbarhetskonton** och väljer sedan relaterad länk.
2. På sidan **Diagram över hållbarhetskonton** kan du öppna varje hållbarhetskonto och lägga till eller ändra inställningar. Placera markören över ett fält om du vill läsa en kort beskrivning.

För konton av typen **Summa** måste fältet **Summeringsintervall** anges.

För konton av typen **Till-summa** fyller funktionen Indrag i fältet **Summering** automatiskt. När du har skapat alla konton väljer du åtgärden **Indrag av kontoplan för hållbarhetskonton** för att köra funktionen Indrag och ange fältet **Summering** .

> [!IMPORTANT]
> Med funktionen Indrag skrivs värdet i alla fält för konton av typen **Till-summa** över. Om du har angett definitioner i fältet  **Summering** för **Till-summa**-konton innan du körde funktionen Indrag måste du därför ange dessa igen efter att du har kört den.

### Ta bort konton

Du kan ta bort ett hållbarhetskonto. Du måste emellertid först se till att inga transaktioner är kopplade till den. Business Central förhindrar att du tar bort ett hållbarhetskonto om det finns en eller flera transaktioner kopplade till den.

## Kontokategorier

Användare måste lägga till en hållbarhetskontokategori till varje hållbarhetskonto för att definiera hur systemet beter sig. De kan välja utsläpps-scopes, dedikerade utsläpp att spåra, formler och liknande konfigurationer.

Följ stegen för att granska kategorier för hållbarhetskonto:

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Kategorier för hållbarhetskonto** och väljer sedan relaterad länk.
2. På sidan **Kategorier för hållbarhetskonton** kan du redigera den befintliga listan eller skapa en ny kategori. Om du vill skapa en ny kategori väljer du åtgärden **Ny**.
3. Ange fälten **Kod** och **Beskrivning**.
4. I fältet **Utsläpps-scope**, välj ett av omfattningsalternativen.
5. Välj de gasutsläpp som du vill spåra. För närvarande är följande alternativ tillgängliga: **CO2**, **CH4** och **N2O**. Du kan välja vilken kombination du vill spåra, men du måste ha minst ett utsläpp.
6. I fältet **Beräkningsgrund** kan du välja den beräkningsgrund (formel) som ska användas för utsläppsberäkningar om du inte vet den exakta utsläppsmängden. Du kan välja något av följande alternativ: **Bränsle/el**, **Avstånd**, **Installation** eller **Anpassad**.

    > [!NOTE]
    > Om uppsättningen tillgängliga formler i fältet **Beräkningsgrund** inte räcker kan du utöka det här fältet och lägga till fler beräkningar i systemet som ska användas i hållbarhetsjournalerna.

7. Om du valde **Anpassad** i fältet **Beräkningsgrund** kan du konfigurera en anpassad beskrivning i fältet **Anpassat värde**.

Om du anger fältet **Beräkningsgrund** förklarar följande tabell hur utsläppen beräknas baserat på det alternativ som du har valt. (I denna tabell representerar *EF* det värde för **Emissionsafktor** som du kan konfigurera på sidan **Underkategori för hållbarhetskonto**.)

| Utsläppstyp | Beräkningsgrund | Formel | Kommentar |
|---------------|------------------------|---------|---------|
| **Scope 1** | | | |
| Stationär förbränning | Bränsle/elektricitet | *Utsläpp* = *bränsle* &times; *EF* | *Bränsle* = Mängden bränsle som används för pannor, värmare, termiska oxidanter, och så vidare |
| Mobil förbränning | Bränsle/elektricitet | *Utsläpp* = *bränsle* &times; *EF* | *Bränsle* = Mängden bränsle som används för vägfordon eller andra fordon, järnväg, och så vidare |
| | | *Utsläpp* = *Avstånd* &times; *EF* | *Avstånd* = Körsträcka för fordon på väg eller icke-vägfordon, järnväg och så vidare |
| Flyktiga utsläpp | Installation | *Utsläpp* = *Multiplikator för installation* &times; *Anpassat belopp* &divide; 100 &times; *Tidsfaktor* | *Anpassad mängd* = monteringsförluster, årlig läckagefrekvens, och så vidare |
| **Scope 2** | | | |
| Leverantörer av allmännyttiga tjänster | Bränsle/elektricitet | *Utsläpp* = *Elektricitet* &times; *EF* | *Bränsle/el* = elmängd, ångmängd, värmeenhet, och så vidare |
| | Anpassat | *Utsläpp* = *Anpassad mängd* &times; *EF* | *Anpassad mängd* = termisk enhet, tontimme, och så vidare |
| **Scope 3** | | | |
| Inköpta varor och tjänster samt kapitalvaror | Anpassat | *Utsläpp* = *Anpassad mängd* &times; *EF* | *Anpassad mängd* = Kostnad (GL), och så vidare |
| Uppströms transport och distribution | Avstånd | *Utsläpp* = *Avstånd* &times; *EF* | |
| | Avstånd | *Utsläpp* = *Avstånd* &times; *Multiplikator* &times; *EF* | *Multiplikator* = Ton last |
| Nedströms transport och distribution | Avstånd | *Utsläpp* = *Avstånd* &times; *EF* | |
| | Avstånd | *Utsläpp* = *Avstånd* &times; *Multiplikator* &times; *EF* | *Multiplikator* = Ton last |
| Avfall som genereras vid verksamhet och slutbehandling av sålda produkter | Anpassat | *Utsläpp* = *Anpassad mängd* &times; *EF* | *Anpassad mängd* = Avfall |
| Affärsresor och personalpendling | Avstånd | *Utsläpp* = *Avstånd* &times; *EF* | *Avstånd* = Körsträcka för tjänstebil, hyrbil, tåg, flyg, och så vidare |
| | Anpassat | *Utsläpp* = *Anpassad mängd* &times; *EF* | *Anpassat belopp* = Hotellvistelser |
| | Bränsle/elektricitet | *Utsläpp* = *bränsle* &times; *EF* | *Bränsle* = Mängden bränsle som förbrukas i tjänstebilen, hyrbilen, och så vidare |

## Underkategorier för konto

Användare måste lägga till en hållbarhetskontokategori till varje hållbarhetskonto. Denna underkategori definierar de emissionsfaktorer som används i formlerna, baserat på valet av utsläppsspårning i hållbarhetskontokategorin.

Följ stegen för att granska underkategorier för hållbarhetskonto:

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Underkategorier för hållbarhetskonto** och väljer sedan relaterad länk. 
2. På sidan **Underkategorier för hållbarhetskonton** kan du redigera den befintliga listan eller skapa en ny kategori. Om du vill skapa en ny kategori väljer du åtgärden **Ny**.
3. Ange fälten **Kod** och **Beskrivning**.
4. Baserat på de gasutsläpp som du vill spåra i kategorin hållbarhetskonto och koppla den här underkategorin till kan du också ange en eller flera emissionsfaktorer: 

    - **Emissionsfaktor CO2** – Emissionsfaktorn för koldioxidutsläpp (CO<sub>2</sub>).
    - **Emissionfaktor CH4** – Emissionsfaktorn för metanutsläpp (CH<sub>4</sub>).
    - **Emissionsfaktor N2O** – Emissionsfaktorn för lustgasutsläpp (N<sub>2</sub>O).

5. Om underkategorin är relaterad till förnybar energi markerar du fältet **Förnybar energi**.

> [!NOTE]
> Fälten **Importera data** och **Importera från** är avsedda att integreras med externa system som används för att samla in emissionsfaktorer. I **2024 utgivningscykel 1** kan dessa fält emellertid inte användas som en funktion som standard.

## Hållbarhetstransaktioner

Hållbarhetsredovisningen lagrar historiken för alla bokförda hållbarhetstransaktioner och organiserar all utsläppsdata enligt CoSA. När en användare bokför hållbarhetsjournalen registreras alla viktiga data där. Alla aktiva rapporter genereras baserat på hållbarhetstransaktionerna.

Om du vill öppna redovisningen för ett visst konto använder du åtgärden **Transaktioner** på sidan **Hållbarhetsplan**. För att öppna transaktioner, välj ![Glödlampa som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Hållbarhetstransaktioner** och välj sedan relaterad länk. Placera markören över ett fält om du vill läsa en kort beskrivning.

> [!IMPORTANT]
> När du har bokfört dina data i hållbarhetsredovisning kan du inte ta bort dem. Om du har gjort ett misstag kan du bokföra en återföringstransaktion med samma uppgifter, men med hjälp av det negativa tecknet för belopp.

## Se även

[Ekonomi](finance.md)  
[Översikt över hållbarhetsstyrning](finance-manage-sustainability.md)  
[Hållbarhetskonfiguration](finance-sustainability-setup.md)  
[Så här registrerar du utsläpp](finance-sustainability-journal.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
