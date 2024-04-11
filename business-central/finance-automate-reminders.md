---
title: Automatisera betalningspåminnelser i samlingar
description: 'I den här artikeln beskrivs hur du sparar tid i samlingar genom att automatisera processerna för att skapa, utfärda och skicka påminnelser till kunder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Automatisera betalningspåminnelser i samlingar

Gör dina insamlingar mer effektiva genom att automatisera processen för att skapa, utfärda och skicka påminnelser till dina kunder. Automatisering kan avsevärt minska den tid du spenderar på insamlingar, ge en bättre översikt över processen och ge dig full kontroll över varje steg.

På sidan **Automatisering av påminnelser** definierar du de enskilda åtgärderna (stegen). Du kan kombinera stegen för att skapa, utfärda och skicka påminnelser, eller så kan du skapa en separat automatisering för varje steg om det är bättre för dina insamlingsprocesser. Automatiseringar baseras på betalningspåminnelsevillkor och betalningspåminnelsenivåer. Om du vill veta mer, gå till [Konfigurera villkor och nivåer för betalningspåminnelser](finance-setup-reminders.md). Du kan ange filter för betalningspåminnelsevillkor för en automatisering som helhet och ange filter för varje åtgärd i automatiseringen. Du kan också bifoga utestående fakturor till e-postmeddelanden som PDF-filer.

Automatisering sker via en projektkötransaktioner. När du ställer in en automatisering använder du fältet **Kadens** för att ange hur och när den ska köras. Om du väljer **Manuell** körs automatiseringen en gång när du använder åtgärden **Starta**. Du kan också välja **Varje vecka**, **Varje månad** eller välja **Anpassad** för att ställa in en mer detaljerad kadens. Om du väljer **Anpassad** måste du ange en dataformel. Mer information om hur du anger en datumformel finns i [Använda datumformler](ui-enter-date-ranges.md#use-date-formulas). När du väljer ett annat alternativ än **Manuell** körs automatiseringen tills du pausar den för att pausa den. Om du vill vara ännu mer specifik om när den körs kan du använda åtgärden **Jobbkötransaktioner** för att öppna sidan **Jobbkötransaktioner** och justera upprepningen, till exempel till en daglig eller en viss veckodag.

## Automatisera påminnelseflödet

I följande avsnitt beskrivs hur du ställer in betalningspåminnelser så att de skapas, skickas ut och skickas automatiskt.

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Automatisering av betalningspåminnelser** och väljer sedan relaterad länk.
1. Välj **Ny** och fyll sedan i fälten på snabbfliken **Allmän**.
1. I fältet **Filter för betalningspåminnelsevillkor** väljer du det eller de betalningspåminnelsevillkor som automatiseringen ska användas för.
1. I fältet **Kadens** väljer du hur ofta automatiseringen ska köras.
1. På snabbfliken **Åtgärder** väljer du **Ny** och väljer sedan om automatiseringen ska skapa, utfärda eller skicka påminnelser. Klicka på **OK**.
1. Beroende på vilken typ av åtgärd som automatiseringen utför fyller du i fälten efter behov på inställningssidan. Om du vill veta mer om inställningarna går du till [Inställningar för påminnelseåtgärder](#settings-for-reminder-actions).
1. När du har ställt in åtgärderna för automatiseringen kan du använda åtgärderna **Flytta upp** och **Flytta ned** för att justera i vilken ordning de körs.

## Inställningar för påminnelseåtgärder

Inställningsinställningarna skiljer sig för åtgärderna Skapa, Utfärda och Skicka påminnelse. I följande avsnitt finns beskrivningar om att använda dem.

### Skapa

* Ange högsta nivå på alla påminnelserader.  
* Skapa betalningspåminnelser för transaktioner som har spärrats. Den här inställningen är till exempel användbar om du befinner dig i en pågående tvist med en kund och vill att de ska se helheten.
* Skapa påminnelser för alla obetalda fakturor och inte bara för förfallna. I rapporten visas förfallna fakturor och fakturor som bara är obetalda men inte förfallna i separata avsnitt.
* Ställ in filter för att göra påminnelsen mer specifik.

### Utskick

När du skickar ut en betalningspåminnelse skapar du transaktioner i kundreskontran som innehåller bokföringsdatum och skattedatum. Använd inställningarna på sidan **Inställningar för betalningspåminnelser** för att ange om informationen på den utskickade påminnelsen ska ersättas med informationen från den skapade påminnelsen. Om du till exempel skapade påminnelsen igår och skickar ut den i dag flyttas förfallodatumet en dag.

### Skicka

> [!NOTE]
> Skicka automatiseringen kräver att du har konfigurerat e-post i [!INCLUDE [prod_short](includes/prod_short.md)]. Om du vill ha mer information om hur du ställer in e-post går du till [Ställ in e-post](admin-how-setup-email.md).

Innehållet i e-postmeddelandena, till exempel bifogade texter, e-postbrödtexter och språk kommer från inställningen för påminnelseperioden. Om du vill veta mer om inställning av e-post, gå till [Konfigurera villkor och nivåer för betalningspåminnelser](finance-setup-reminders.md).

Använd inställningarna på sidan **Skicka påminnelseinställningar** för att kontrollera följande:

* Allmänna inställningar, till exempel beskrivning, och hur många gånger du skickar samma påminnelse.
* Inställningar för vad som ska tas med i betalningspåminnelsen.
* Inställningar för att spåra påminnelser som du skickar genom att skapa interaktioner, oavsett om du skriver ut eller skickar påminnelsen via e-post och om du endast vill bifoga förfallna fakturor, alla fakturor eller inga fakturor. 

## Öppna historiken för en påminnelse

[!INCLUDE [prod_short](includes/prod_short.md)] håller reda på varje gång en automatisering körs. Du kan komma åt historiken genom att välja åtgärden **Loggtransaktioner**. Du kan också använda åtgärden **Utskickade påminnelser** för att komma åt en lista över de påminnelser som du har skickat.

## Hantera fel

På snabbfliken **Åtgärder** kan du för varje åtgärd ange om du vill att automatiseringen ska stoppas om åtgärden innehåller ett fel. Om du gör det kommer automatiseringen inte att bearbeta de åtgärder som kommer efteråt. Om du vill aktivera eller inaktivera den här funktionen använder du åtgärderna **Ange stopp vid fel** eller **Rensa stopp vid fel**.

## Ändra åtgärdsinställningar för en automatisering

Du kan när som helst ändra inställningarna för en automatisering. På snabbfliken **Åtgärder** väljer du **Inställningar** och gör sedan ändringarna.

## Se även

[Konfigurera villkor och nivåer för betalningspåminnelser](finance-setup-reminders.md)  
[Skicka påminnelser om utestående saldon](receivables-send-reminders.md)  
