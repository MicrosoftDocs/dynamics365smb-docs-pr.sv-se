---
title: Ställ in ej avdragsgill moms
description: I den här artikeln beskrivs hur du konfigurerar ej avdragsgill moms i Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="set-up-non-deductible-vat" />Ställ in ej avdragsgill moms

Ej avdragsgill moms (VAT) är den moms som betalas av en inköpare, men det är inte avdragsgill från köparens egen momsskuld. Företag kan vanligtvis återställa moms på inköp av varor och tjänster som hör till deras affärsaktiviteter. I vissa fall ådrar sig dock en verksamhet moms som inte är avdragsgill. Dessa situationer är vanligen relaterade till lokala bestämmelser och kan skilja sig från land till land. Modellen för användning av ej avdragsgill eller delvis avdragsgill moms är emellertid densamma. Du kan använda proportionell moms för att beräkna moms när det finns avdragsgill och ej avdragsgill moms.

I allmänhet kan moms inte dras av för vissa inköp på grund av följande faktorer:

- **Vilken typ av varor eller tjänster som köps** – Moms är helt eller delvis ej avdragsgill genom en bestämmelser om varor som t.ex. bilar, mobiltelefoner och livsmedel som köps på restauranger.
- **Delvis avdragsgill moms** – Moms är proportionell enligt förhållandet mellan de försäljningsåtgärder som momsen gäller för och alla åtgärder som har utförts. Moms som överstiger detta förhållande kan inte dras av.

Eftersom det kan vara svårt att veta var och hur en artikel används, måste du kontakta lokala skattemyndigheter i ditt land för att avgöra om en viss procent andel av momsen är avdragsgill baserat på historiska data. 

> [!IMPORTANT]
> Denna globala funktion är tillgänglig i alla länder med aktiverad moms **förutom Belgien, Italien, Norge och Spanien**. De här lokaliseringarna har redan befintlig lokal funktion och kommer att uppgraderas i framtiden. Kör inte den här funktionen i dessa länder eftersom uppgraderingsproceduren inte finns.

## <a name="use-non-deductible-vat" />Använd ej avdragsgill moms

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Momsinställningar** och väljer sedan relaterad länk.
2. Markera kryssrutan **Aktivera ej avdragsgill moms**.

    > [!IMPORTANT]
    > När du har aktiverat ej avdragsgill moms kan du inte inaktivera den, eftersom funktionen kan innehålla ändringar av data och eventuellt initiera en uppgradering av vissa databastabeller. Microsoft rekommenderar att du först aktiverar och testar den här funktionen i miljön för begränsat läge innan du aktiverar den i produktionsmiljön.

3. Konfigurera hur systemet ska behandla ej avdragsgilla momsvärden.

    1. I fältet **Använd för artikelkostnad** anger du om den ej avdragsgilla momsen ska läggas till på varukostnaden när du köper varor. Annars kommer inte den ej avdragsgilla momsen att påverka artikelkostnaden och hela beloppet registreras endast på redovisningsnivå.
    2. Markera kryssrutan **Använd för kostnad för anläggningstillgång** för att lägga till den ej avdragsgilla momsen på kostnaden för anläggningstillgång när du köper nya anläggningstillgångar. Annars kommer inte den ej avdragsgilla momsen att påverka kostnaden för anläggningstillgångar och hela beloppet registreras endast på redovisningsnivå.
    3. Markera kryssrutan **Använd för projektkostnad** om du vill ange att den ej avdragsgilla momsen måste läggas till projektkostnaderna när du köper in artiklar för projektet. Annars kommer inte den ej avdragsgilla momsen att påverka projektkostnaden och hela beloppet registreras endast på redovisningsnivå.
    4. Markera kryssrutan **Visa ej avdragsgill moms på rader** för att ange att den ej avdragsgilla momsen måste visas på dokumentradsidor för enklare manipulering av momsbelopp.

## <a name="use-the-non-deductible-vat-percentage" />Använd den ej avdragsgilla momsprocenten

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokföringsinställningar för moms** och väljer sedan relaterad länk.
2. På sidan **Bokföringsinställningar för moms** anger du fälten enligt beskrivningen i följande tabell.

    | Fält | Description |
    |-------|-------------|
    | Tillåt icke-avdragsgill moms | Anger om ej avdragsgill moms beaktas för denna aktuella kombination av rörelsebokföringsmall med moms och produktbokföringsmall med moms. |
    | Icke-avdragsgill moms % | Ange den procentandel av transaktionsbeloppet som moms inte tillämpas på. |
    | Konto för icke-avdragsgill ingående moms | Ange kontot som är kopplat till momsbeloppet som inte dras av på grund av den typ av varor eller tjänster som köpts. |

    > [!NOTE]
    > För att ha redovisningstransaktioner som använder det dedikerade kontot istället för försäljnings-/köpkontot, kan du antingen lämna fältet**Konto för ej avdragsgill ingående moms** tomt eller ange fältet **Redovisningskonto**.

3. Välj **OK**.

> [!NOTE]
> Du kan inte använda orealiserad moms tillsammans med ej avdragsgill moms.
>
> Använd inte samma värde för **Momsidentifierare** för både vanlig moms där fältet **Ej avdragsgill moms %** anges till **0** (noll) och vanlig moms där fältet **Ej avdragsgill moms %** anges till ett värde som inte är noll. Annars kommer det totala ej avdragsgilla momsbeloppet att beräknas felaktigt.

## <a name="see-also" />Se även

[Ekonomihantering](finance.md)  
[Konfigurera beräknings- och bokföringsmetoder för moms](finance-setup-vat.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
