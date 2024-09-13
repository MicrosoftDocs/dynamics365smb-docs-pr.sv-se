---
title: Hållbarhetskonfiguration
description: Läs om hur du konfigurerar hållbarhetsfunktioner.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, equivalent, CO2e, CO2, carbon, role center, fees'
ms.search.form: '6221, 6235, 6245'
ms.date: 08/22/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="sustainability-module-setup"></a>Inställning av hållbarhetsmodul

Innan hållbarhetsmodulen kan fungera korrekt måste du först ställa in några grundläggande kontroller och instruktioner relaterade till hela funktionen.

Följ följande steg för att konfigurera en hållbarhetsmodul:

## <a name="role-center"></a>Rollcenter

För personer vars primära ansvarsområden omfattar hållbarhetsprocesser rekommenderar vi att du använder *rollcentret Hållbarhetschef* . Så här konfigurerar du det här rollcentret:  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") , ange **Mina inställningar** och Välj sedan relaterad länk.
2. I fältet **Roll** Välj sidan **Tillgängliga roller** .
3.  **Välj raden Hållbarhetschef** .
4. Välj **OK**.

Rollcentret *Hållbarhetschef* underlättar effektiv hantering av alla viktiga områden relaterade till hållbarhet. Det omfattar centrala hållbarhetsfunktioner samt finans- och upphandlingsprocesser. Dessutom ger det insyn i de mest kritiska hållbarhetsrelaterade KPI: erna.

## <a name="sustainability-setup"></a>Hållbarhetskonfiguration

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Hållbarhetskonfiguration** och väljer sedan relaterad länk.
2. På snabbfliken **Allmänt** konfigurerar du de obligatoriska fälten som är relaterade till hållbarhetsmodulen.

    | Fält | Description |
    |-------|-------------|
    | **Måttenhet för utsläpp** | Anger den måttenhetskod som används för att registrera utsläpp. |
    | **Antal decimaler för utsläpp** | Ange antalet decimaler som visas för utsläppsmängder. Standardinställningen *2:5* anger att minst två decimaler och högst fem decimaler visas för alla belopp. Du kan även ange ett fast nummer. Om du till exempel anger *2* visas två decimaler för alla belopp. |
    | **Land/region måste anges** | Anger om land/region måste anges. Användare kan ange fältet land/region i journaler även om du inte markerar det här fältet. Om du väljer det måste du emellertid ange fältet land/region innan de bokför. |
    | **Ansvarsenhet måste anges** | Ange om ansvarsenhet måste anges. Ansvarsenheten kan användas som en anläggning så att du kan mäta anläggningsbaserade utsläpp. Användare kan ange fältet ansvarsenhet i journaler även om du inte markerar det här fältet. Om du väljer det måste du emellertid ange fältet ansvarsenhet innan de bokför. |
    | **Blockera ändring av beräkningsgrund om det finns transaktioner** | Ange om ändringar av beräkningsgrunden (formeln) på kontokategorinivå är blockerade vid tidpunkten för hållbarhetsinförandet, när formeln redan har tillämpats. |
    | **Aktivera felkontroll i bakgrunden** | Ange om felkontrollen i bakgrunden av hållbarhetsjournalraderna har aktiverats. |

    > [!NOTE]
    > När du har aktiverat eller inaktiverat felkontroll i bakgrunden i journaler måste du logga in igen innan du startar den nya installationen.

3.  **På snabbfliken Anskaffning** konfigurerar du de obligatoriska fält som är relaterade till användningen av hållbarhetsfunktioner i inköpsprocessen.  

    | Fält | Description |
    |-------|-------------|
    | **Använda utsläpp i inköpsdokument** | Om du aktiverar det här fältet kommer hållbarhetsrelaterade fält och funktioner att visas i inköpsdokumenten, till exempel **hållbarhetskonto** eller olika utsläpp. |

4. På snabbfliken **Beräkningar** konfigurerar du obligatoriska fält som är relaterade till formlerna som används för att beräkna utsläpp.

    | Fält | Description |
    |-------|-------------|
    | **Decimaltal för bränsle/el** | Ange antalet decimaler som visas för mängder för bränsle/elektricitet. Standardinställningen *2:5* anger att minst två decimaler och högst fem decimaler visas för alla belopp. Du kan även ange ett fast nummer. Om du till exempel anger *2* visas två decimaler för alla belopp. |
    | **Antal decimaler för avstånd** | Ange antalet decimaler som visas för avståndsmått. Standardinställningen *2:5* anger att minst två decimaler och högst fem decimaler visas för alla belopp. Du kan även ange ett fast nummer. Om du till exempel anger *2* visas två decimaler för alla belopp. |
    | **Antal decimaler för anpassad mängd** | Ange antalet decimaler som visas för anpassade mängder. Standardinställningen *2:5* anger att minst två decimaler och högst fem decimaler visas för alla belopp. Du kan även ange ett fast nummer. Om du till exempel anger *2* visas två decimaler för alla belopp. |

5. På snabbfliken **Rapportering** slutför du inställningarna genom att konfigurera fälten som är relaterade till rapportering till myndigheter.

    > [!NOTE]
    > I version 24.0 [!INCLUDE[prod_short](includes/prod_short.md)] stöds inte rapportering till någon myndighet. Därför är de fält som är relaterade till konfigurationen av den här funktionen på snabbfliken **Rapportering** avsedda för framtida rapporteringsfunktioner. Partner kan emellertid också använda dessa fält i lokaliserade versioner.

    | Fält | Description |
    |-------|-------------|
    | **Måttenhetskod för utsläppsrapportering** | Ange den måttenhetskod som används för att rapportera utsläpp, eftersom du kan använda olika måttenheter när du rapporterar till myndigheterna. Det här fältet gäller inte standardrapporterna. |
    | **Måttenhetsfaktor för rapportering** | Ange den måttenhetsfaktor som används för att registrera utsläpp, om du kan använda olika måttenheter när du rapporterar till myndigheterna. |
    | **Avrundningsnoggrannhet för utsläpp** | Ange storleken på det intervall som ska användas när utsläppsmängder avrundas när du rapporterar till myndigheter. |
    | **Avrundningstyp för utsläpp** | Ange hur programmet avrundar utsläppsmängder när du rapporterar till myndigheter. Följande alternativ är tillgängliga: **Närmsta**, **Upp** och **Ned**. |

## <a name="emission-fees"></a>Utsläppsavgifter

Om du vill spåra interna koldioxidavgifter eller beräkna dina utsläpp med koldioxidekvivalenter (CO2) måste du konfigurera **sidan Utsläppsavgifter** . Så här ställer du in den här informationen:  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") , ange **Utsläppsavgifter** och Välj sedan relaterad länk. 
2. I fältet **Utsläppstyp** väljer du det växthusgasutsläpp som du vill konfigurera: **CO2**, **CH4** eller **N2O**. Detta alternativ är obligatoriskt.   
3. Du kan ange omfångstypen **ytterligare**. Om du lämnar det här fältet tomt gäller det för alla omfång, men du kan konfigurera för varje omfång.  
4. Du kan konfigurera **Startdatum** och **Slutdatum**. Det particullary innebär att du kan använda olika konfigurationer för olika perioder. 
5.  **Lands-/regionkod** och **Ansvarskod** är valfria fält som du kan välja om du vill använda dem. Dessa fält kan vara användbara eftersom det är möjligt att ha olika koldioxidavgifter per land eller att använda olika omvandlingar till CO2e per land eller per anläggning (ansvarsenhet).  
6. Fältet **koldioxidavgift** representerar den interna koldioxidavgift som ett företag debiterar sig själv för varje enhet CO2-ekvivalenter som det släpper ut. Den kan användas baserat på vissa lokala eller regionala föreskrifter, men också för interna beräkningar. **koldioxidavgift** kommer att beräknas varje gång du bokför utsläpp och denna information kommer att synas på **hållbarhetstransaktionerna**, utan ytterligare bokföring i **redovisningen**. Du kan ställa in **koldioxidavgift** per enhet som du har i **hållbarhetsinställningen** och den kan bara fyllas i för raden där **utsläppstypen** är **CO2**. 
7.  **Kolekvivalentfaktorn** anger koefficienten som omvandlar effekterna av olika växthusgaser till motsvarande mängd koldioxid baserat på deras globala uppvärmningspotential. Om utsläppstypen **är CO2 kommer kolekvivalentfaktorn**  **alltid att vara** 1 *och du kan inte ändra detta värde, eftersom CO2 är referensgasen som används för att* beräkna den globala uppvärmningspotentialen (GWP) för andra växthusgaser; eftersom CO2 är baslinjen är dess GWP inställd på 1 *.* För andra växthusgasgaser måste användarna konfigurera värdena manuellt. För att göra korrekt beräkning kan du använda följande exempel: Om vi antar att 1 kilo N2O motsvarar 298 kg CO2, måste du beräkna 1/298 och resultatet du behöver fylla blir 0.00336.  

> [!NOTE]
> **Fältet koldioxidavgift** i hållbarhetstransaktionerna **beräknas** inte baserat på CO2-utsläppsvärdena **·** . Istället, som en grund för denna formel, [!INCLUDE[prod_short](includes/prod_short.md)]  kommer att använda **fältet CO2e-utsläpp** . **Fältet CO2e-utsläpp** beräknas baserat på alla utsläpp som bokförts i transaktionen och den **koldioxidekvivalentfaktor** som konfigurerats för var och en **av gaserna på sidan Utsläppsavgifter** .  

Om du inte konfigurerade utsläppsavgifterna innan du bokförde dina hållbarhetsposter, och du vill beräkna dina koldioxidavgifter och CO2e retroaktivt, måste du köra **åtgärden Beräkna utsläppsavgifter** för att uppdatera värdena i **hållbarhetstransaktionerna** . **·**  

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)    
[Översikt över hållbarhetshantering](finance-manage-sustainability.md)    
[Kontoplan för hållbarhetskonton och huvudbok](finance-sustainability-accounts-ledger.md)    
[Registrera hållbarhetstransaktioner](finance-sustainability-journal.md)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
