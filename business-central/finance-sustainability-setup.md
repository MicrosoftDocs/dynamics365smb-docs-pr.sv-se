---
title: Hållbarhetskonfiguration
description: Läs om hur du konfigurerar hållbarhetsfunktioner.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD'
ms.search.form: null
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Hållbarhetskonfiguration  

För att hållbarhetsmodulen ska fungera korrekt måste du först ställa in några grundläggande kontroller och instruktioner relaterade till hela funktionen.  

Följ följande steg för att konfigurera en hållbarhetsmodul:  

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Hållbarhetskonfiguration** och väljer sedan relaterad länk.  
2. På snabbfliken **Allmänt** konfigurerar du de obligatoriska fälten som är relaterade till den här modulen:   

|  Fält  |  Description  |  
|--------|--------------| 
| **Måttenhet för utsläpp** | Anger den måttenhetskod som används för att registrera utsläpp. |
| **Antal decimaler för utsläpp** | Anger antalet decimaler som visas för utsläppsmängder. Standardinställningen, 2:5, anger att alla mängder visas med minst 2 och högst 5 decimaler. Du kan också ange ett fast tal, till exempel 2, vilket också innebär att mängden visas med två decimaler. |
| **Land/region måste anges** | Anger om land/region måste anges. Du kan använda det här fältet i journaler utan att konfigurera det, men du kan markera det om du vill tvinga användarna att fylla i fältet innan de bokför. |
| **Ansvarsenhet måste anges** | Anger om ansvarsenhet är obligatoriskt, eftersom ansvarsenheten kan användas som en funktion för att mäta anläggningsbaserade utsläpp. Du kan använda det här fältet i journaler utan att konfigurera det, men du kan markera det om du vill tvinga användarna att fylla i fältet innan de bokför. |
| **Blockera ändring av beräkningsgrund om det finns transaktioner** | Anger om ändringen av beräkningsgrunden i kontokategorin är spärrad vid tidpunkten för hållbarhetstransaktionen, vilket innebär att denna formel redan har tillämpats. |
| **Aktivera felkontroll i bakgrunden** | Anger om felkontrollen i bakgrunden av hållbarhetsjournalraderna har aktiverats. |

3.  På snabbfliken **Beräkningar** konfigurerar du obligatoriska fält som är relaterade till formlerna som används för att beräkna utsläpp:  

|  Fält  |  Description  |  
|--------|--------------| 
| **Decimaltal för bränsle/el** | Anger antalet decimaler som visas för mängder för bränsle/elektricitet. Standardinställningen, 2:5, anger att alla mängder visas med minst 2 och högst 5 decimaler. Du kan också ange ett fast tal, till exempel 2, vilket också innebär att mängden visas med två decimaler. |
| **Antal decimaler för avstånd** | Anger antalet decimaler som visas för avståndsmått. Standardinställningen, 2:5, anger att alla mängder visas med minst 2 och högst 5 decimaler. Du kan också ange ett fast tal, till exempel 2, vilket också innebär att mängden visas med två decimaler. |
| **Antal decimaler för anpassad mängd** | Anger antalet decimaler som visas för anpassade mängder. Standardinställningen, 2:5, anger att alla mängder visas med minst 2 och högst 5 decimaler. Du kan också ange ett fast tal, till exempel 2, vilket också innebär att mängden visas med två decimaler. |

4.  Slutför konfigurationen på snabbfliken **Rapportering** avseende rapportering till myndigheter:   

|  Fält  |  Description  |  
|--------|--------------| 
| **Måttenhetskod för utsläppsrapportering** | Anger den måttenhetskod som används för att rapportera utsläpp, eftersom du kan använda olika måttenheter när du rapporterar till myndigheterna. Det här fältet gäller inte standardrapporterna. |
| **Måttenhetsfaktor för rapportering** | Anger den måttenhetsfaktor som används för att registrera utsläpp, om du kan använda olika måttenheter när du rapporterar till myndigheterna. |
| **Avrundningsnoggrannhet för utsläpp** | Anger storleken på det intervall som ska användas när utsläppsmängder avrundas när du rapporterar till myndigheter. |
| **Avrundningstyp för utsläpp** | Anger hur programmet avrundar en utsläppsmängd vid rapportering till myndigheter med hjälp av alternativen: Närmast, Upp eller Ner. |

>[!NOTE]
> I version 24.0 [!INCLUDE[prod_short](includes/prod_short.md)] stöds inte rapportering till någon myndighet. Fält relaterade till konfiguration på snabbfliken **Rapportering** kommer därför att användas för framtida rapporteringsfunktioner, men det kan också användas av partner i lokaliserade versioner.

## Se även  
[Ekonomi](finance.md)    
[Översikt över hållbarhetshantering](finance-manage-sustainability.md)
[Diagram över hållbarhetskonton och redovisning](finance-sustainability-accounts-ledger.md)
[Så här registrerar du utsläpp](finance-sustainability-journal.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
