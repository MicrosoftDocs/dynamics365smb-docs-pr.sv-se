---
title: Skapa digitala verifikationer
description: Den här artikeln förklarar hur du ställer in och använder tvingade digitala verifikationer i Microsoft Dynamics 365 Business Central.
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.search.keywords: 'digital voucher, voucher, attachment, setup'
ms.search.form: '5579, 5582, 5587'
ms.date: 11/17/2023
ms.custom: bap-template
---

# Skapa digitala verifikationer

Administratörer kan använda digitala verifikationsfunktioner för att kräva att dokument bifogas specifika transaktioner när de bokförs. Därför möjliggör denna funktionalitet ett källdrivet tillvägagångssätt och ger ett bättre granskningsspår. Olika typer av verkställighet kan konfigureras för detta ändamål, beroende på dokument eller journaltyper.

Termen *digital verifikation* avser en digital eller elektronisk form av en traditionell verifikation inom bokföring. En verifikation är ett dokument som används för att stödja och auktorisera finansiella transaktioner. I bokföringen fungerar en verifikation vanligtvis som bevis på en utgift eller ett mottagande av medel. Verifikationen kan innehålla detaljer som datum för transaktionen, en beskrivning, belopp och eventuella auktoriseringssignaturer.

> [!IMPORTANT]
> I vissa länder och regioner kan du vara begränsad från att konfigurera vissa alternativ, eftersom specifika inställningar kan krävas av juridiska krav. Om du stöter på dessa begränsningar, leta efter en detaljerad förklaring på dokumentationssidan för ditt land eller din region.

## Aktivera digitala verifikationer

Följ dessa steg för att aktivera funktionen digital verifikation.

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") Välj ikonen ange **Konfiguration av digitala verifikationer** och välj sedan relaterad länk.
2. Markera kryssrutan **Aktiverad**.

## Skapa digitala verifikationer

Du kan använda olika inställningar för följande dokument och journaler.

| Transaktionstyp | Beskrivning |
|------------|-------------|
| Försäljningsdokument | Anger bokföringar som slutförs från försäljningsdokument. |
| Inköpsdokument | Anger bokföringar som slutförs från inköpsdokument. |
| Redovisningsjournal | Anger bokföringar som slutförs från den allmänna journalen för alla kontotyper utom de som är relaterade till kund och leverantör. Om du väljer en av dessa kontotyper ändrar du kontroll över bokföringsprocessen. Om du väljer **Kund** som kontotyp kontrollerar systemet din inställning som är relaterad till försäljningsjournalen. Om du väljer **Leverantör** som kontotyp kontrollerar systemet din inställning som är relaterad till inköpsjournalen. |
| Försäljningsjournal | Anger de bokföringar som genomförs från försäljningsjournalen och den allmänna journalen var **Kund** väljs som kontotyp. |
| Inköpsjournal | Anger de bokföringar som genomförs från inköpsjournal och den allmänna journalen var **Leverantör** väljs som kontotyp. |

Följ dessa steg för att definiera hur din organisation använder påtvingade digitala verifikationer.

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") ikonen ange **Konfiguration av digital verifikationstransaktion** och välj sedan relaterad länk. Alternativt på sida **Konfiguration av digital verifikation**, välj **Ingångsinställningar**.
2. I kolumnen **Transaktionstyp** väljer du ett alternativ.
3. I kolumnen **Checktyp** väljer du ett alternativ för tillämpning. Om du väljer **Ingen**, kan du lägga upp den valda typen av inlägg utan en digital verifikation. Om du väljer **Bilaga**, måste transaktionen innehålla en bilaga. Om du väljer **Bilaga eller anmärkning**, kan du inkludera en bilaga eller en anteckning för posten. 
4. Markera kryssrutan **Generera automatiskt** för att generera den digital verifikationen automatiskt. Om du till exempel inte vill lägga till en försäljningsfaktura manuellt i din transaktion markerar du den här kryssrutan. Sedan är det bara att bokföra dokumentet. Systemet skapar automatiskt dokumentet, baserat på din rapportlayout och bifogar det till transaktionen.
5. Välj kryssrutan **Hoppa över om manuellt lagts till** om du inte vill lägga till en automatiskt genererad digital verifikation om användaren redan har lagt till en manuell bilaga.

### Använd källkoder för installationen

Om du vill använda verkställighet för journaler, men inte för alla transaktionstyper, ansluter du den specifika källkoden för att identifiera postningstypen allmän journal, försäljningsjournal eller inköpsjournal.

Följ dessa steg för att ställa in specifika källkoder för digitala verifikationer.

1. På sidan **Konfiguration av digital verifikationstransaktion**, välj **Ursprungskoder**.
2. På sida **Källkoder för verifikationstransaktion**, välj källkoderna som du vill konfigurera.
3. Stäng sidan.

## Använd funktionen

Öppna ett inköps- eller försäljningsdokument och ange information i de obligatoriska fälten. Innan du bokför dokumentet måste du följa dessa steg för att bifoga en digital verifikation.

1. I faktabox **Inkommande dokumentfiler**, välj **Bifoga fil**.
2. Dra en fil direkt till sidan **Infoga fil** eller bläddra till filen från den här sidan.

Dokumentet har bifogats till faktabox **Inkommande dokumentfiler**. För varje rad kan du hitta dokumentets namn och typ.

Om du av misstag bifogar fel verifikation, följ dessa steg för att radera den innan du bokför dokumentet.

1. I faktabox **Inkommande dokumentfiler** från dokumentraden, välj **Inkommande dokument**.
2. På sidan **Inkommande dokument**, välj **Radera**.

> [!NOTE]
> Om bifogning av en digital verifikation är konfigurerad som obligatorisk och du försöker bokföra dokument eller journaler utan att bifoga en verifikation, hindrar systemet dig från att bokföra. Du får följande felmeddelande: "Det går inte att bokföra utan att bifoga den digitala verifikationen."

### Hitta bifogade verifikationer i transaktioner

Du hittar den bifogade verifikationen från det upplagda dokumentet eller från sidan **Redovisningstransaktioner** genom att titta i faktabox **Inkommande dokumentfiler**.

Du kan inte ta bort ett bifogat dokument efter att bokföringen är klar. Du kan dock lägga till fler bilagor efter att bokföringen är klar.

## Se även

[Ekonomihantering](finance.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
