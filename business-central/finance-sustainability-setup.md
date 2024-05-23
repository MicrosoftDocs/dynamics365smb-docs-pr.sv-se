---
title: Hållbarhetskonfiguration
description: Läs om hur du konfigurerar hållbarhetsfunktioner.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 05/08/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="sustainability-setup"></a>Hållbarhetskonfiguration

Innan hållbarhetsmodulen kan fungera korrekt måste du först ställa in några grundläggande kontroller och instruktioner relaterade till hela funktionen.

Följ följande steg för att konfigurera en hållbarhetsmodul:

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

3. På snabbfliken **Beräkningar** konfigurerar du obligatoriska fält som är relaterade till formlerna som används för att beräkna utsläpp.

    | Fält | Description |
    |-------|-------------|
    | **Decimaltal för bränsle/el** | Ange antalet decimaler som visas för mängder för bränsle/elektricitet. Standardinställningen *2:5* anger att minst två decimaler och högst fem decimaler visas för alla belopp. Du kan även ange ett fast nummer. Om du till exempel anger *2* visas två decimaler för alla belopp. |
    | **Antal decimaler för avstånd** | Ange antalet decimaler som visas för avståndsmått. Standardinställningen *2:5* anger att minst två decimaler och högst fem decimaler visas för alla belopp. Du kan även ange ett fast nummer. Om du till exempel anger *2* visas två decimaler för alla belopp. |
    | **Antal decimaler för anpassad mängd** | Ange antalet decimaler som visas för anpassade mängder. Standardinställningen *2:5* anger att minst två decimaler och högst fem decimaler visas för alla belopp. Du kan även ange ett fast nummer. Om du till exempel anger *2* visas två decimaler för alla belopp. |

4. På snabbfliken **Rapportering** slutför du inställningarna genom att konfigurera fälten som är relaterade till rapportering till myndigheter.

    > [!NOTE]
    > I version 24.0 [!INCLUDE[prod_short](includes/prod_short.md)] stöds inte rapportering till någon myndighet. Därför är de fält som är relaterade till konfigurationen av den här funktionen på snabbfliken **Rapportering** avsedda för framtida rapporteringsfunktioner. Partner kan emellertid också använda dessa fält i lokaliserade versioner.

    | Fält | Description |
    |-------|-------------|
    | **Måttenhetskod för utsläppsrapportering** | Ange den måttenhetskod som används för att rapportera utsläpp, eftersom du kan använda olika måttenheter när du rapporterar till myndigheterna. Det här fältet gäller inte standardrapporterna. |
    | **Måttenhetsfaktor för rapportering** | Ange den måttenhetsfaktor som används för att registrera utsläpp, om du kan använda olika måttenheter när du rapporterar till myndigheterna. |
    | **Avrundningsnoggrannhet för utsläpp** | Ange storleken på det intervall som ska användas när utsläppsmängder avrundas när du rapporterar till myndigheter. |
    | **Avrundningstyp för utsläpp** | Ange hur programmet avrundar utsläppsmängder när du rapporterar till myndigheter. Följande alternativ är tillgängliga: **Närmsta**, **Upp** och **Ned**. |

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)  
[Översikt över hållbarhetsstyrning](finance-manage-sustainability.md)  
[Diagram över hållbarhetskonton och redovisning](finance-sustainability-accounts-ledger.md)  
[Registrera hållbarhetstransaktioner](finance-sustainability-journal.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
