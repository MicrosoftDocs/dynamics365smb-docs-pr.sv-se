---
title: Ångra en bokföring genom att bokföra en mottransaktion
description: Om du hittar ett misstag i en bokförd allmän journal kan du använda åtgärden Återför transaktion för att ångra bokföringen med en korrekt redovisningsspårning.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---
# Återföra journalbokningar och ångra inleveranser/utleveranser

Återföring av journalbokningar används till exempel för att korrigera fel och rensa en gammal periodisering innan du registrerar en ny. En omvänd post är densamma som den ursprungliga posten, men har ett motsatt tecken i fältet **belopp**. Den omvända posten måste ha samma dokumentnummer och bokföringsdatum som den ursprungliga posten. När du har återfört en post måste du skapa en korrekt post.

Du kan endast återföra poster som har bokförts från en redovisningsjournalrad. En transaktion kan endast återföras en gång.

Om du vill ångra en bokföring av inleverans eller utleverans innan de bokförs som fakturerade kan du använda funktionen **ångra** i det bokförda dokumentet. Du kan ångra kvantiteter av typen **Artikel** och **Resurs**.

Om du har bokfört fel negativt antal, till exempel om en inköpsorder med fel antal artiklar och bokfört den som inlevererad men inte fakturerad, kan du ångra bokföringen.

Om du har bokfört fel positivt antal, till exempel en utleverans eller en inköpsreturorder med fel antal artiklar och bokfört den som levererad men inte fakturerad, kan du ångra bokföringen.

## Att återföra bokföringen av en redovisningstransaktion journal

Du kan återföra poster från alla sidor **Transaktioner**. Följande procedur baseras sidan **redovisningstransaktioner**.

> [!NOTE]
> Observera att det måste komma från en journalbokföring.
>
> Du kan inte ångra transaktioner som har bokförts med information från ett projekt eller som har realiserade vinster och förluster inom samma transaktion.

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ange **Redovisningstransaktioner** och välj sedan relaterad länk.
2. Markera den transaktion som du vill återföra och välj sedan åtgärden **återföringstransaktion**.
3. Välj åtgärden **Återför** på sidan **Återför transaktionsposter**.
4. Klicka på knappen **Ja** för att återföra.

## Bokföra en negativ transaktion  

Använd fältet **Korrigering** för att bokföra en negativ debet istället för en kredit, eller för att bokföra en negativ kredit istället för en debet för ett konto. Som standard är fältet tillgängligt i alla journaler. Fälten **Debetbelopp** och **Kreditbelopp** innehåller både ursprungstransaktionen och den korrigerade transaktionen. Dessa fält påverkar inte kontosaldot.  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **redovisningsjournaler** och väljer sedan relaterad länk  
2. Välj önskat batch-namn i fältet **Batch-namn**.  
3. Ange information i relevanta fält.  
4. På journalraden som du vill aktivera för negativa poster väljer du kryssrutan **Korrigering**.  
5. Välj åtgärden **Bokför** och välj sedan knappen **Ja** för att bokföra journalen.

## Så här ångrar du ett antal i en bokförd inköspleverans  

Nedan beskrivs hur du återställer en bokförd inleverans eller bokförda resurser. Momenten är liknande för bokförda utleveranser.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Bokförda inköpsleveranser** och väljer sedan relaterad länk.  
2. Öppna den bokförda inleveransen som du vill ångra.  
3. Markera de rader som du vill ångra.  
4. Välj åtgärden **Ångra inleverans**.

En rättningsrad lagts till under den valda inleveransraden. Om antalet har inlevererats i en lagerinleverans infogas en rättningsrad i den bokförda lagerinleveransen.  

Fälten **Inlevererat antal** och **Inlevrd. antal ej faktrd.** på den relaterade inköpsordern är nollställda.

## Så här ångrar du ett bokfört antal i bokförda returleveranser

I följande steg finns beskrivningar om att:

* Ångra en bokförd returutleverans av artiklar eller resurser.
* Bokför inköps returen igen med en ny kvantitet.

Momenten är liknande för bokförda returinleveranser.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Bokförda returutleveranser** och väljer sedan relaterad länk.  
2. Öppna den bokförda returutleveransen.
3. Markera de rader som du vill ångra.  

4. Välj åtgärden **Ångra returutleverans**.  

    En rättningsrad införs nu i det bokförda dokumentet och fälten **Returant. levererat** och **Retur levererat ej faktrd** på returordern ändras till noll.  

    Gå nu tillbaka till inköpsreturordern som är klar att bokföras.  

5. Observera antalet i fältet **Returordernr** på sidan **Returordernr**. .  
6. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **inköpsreturorder** och väljer sedan relaterad länk.  
7. Öppna returordern i fråga och välj åtgärden **öppna igen**.  
8. Korrigera värdet i fältet **Antal** och bokför inköpsreturordern igen.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## Se även

[Ångra monteringsboking](assembly-how-to-undo-assembly-posting.md)  
[Bokföra transaktioner direkt i redovisningen](finance-how-post-transactions-directly.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Ekonomi](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]