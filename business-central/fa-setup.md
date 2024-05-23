---
title: Ställa in anläggningstillgångar
description: 'Få information om de åtgärder som du måste göra om du vill ställa in anläggningstillgångar, till exempel maskiner eller byggnader.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5607,'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="setting-up-fixed-assets"></a>Ställa in anläggningstillgångar

Innan du kan arbeta med anläggningstillgångar, måste du definiera ett par saker:  

* Så här skriver du av anläggningstillgångar.  
* Hur du registrerar anskaffningskostnader, avskrivningar och andra värden i redovisningen.  
* Valfritt, hur du registrerar försäkring och underhåll för anläggningstillgångar.

I avsnitten i den här artikeln finns mer information om hur du ställer in anläggningstillgångar. När du är klar med inställningarna kan du börja arbeta med anläggningstillgångar. Mer information finns i [Använda anläggningstillgångar](fa-manage.md).  

> [!NOTE]  
> Du kan bokföra anläggningstillgångstransaktioner på sidan **Anl.tillg. redovisningsjournal** eller **Anlägg.tillg.journal** beroende på om transaktionerna är för finansiell rapportering eller för intern hantering. Hjälpartiklarna för anläggningstillgångar beskriver endast hur du använder sidan **Anl.tillg. redovisningsjournal**.  

När du aktiverar en anläggningstillgångsaktivitet i avsnittet **Redov.integrering** på sidan **Avskrivningsregelkort**, sedan kommer sidan **Anl.tillg. redovisningsjournal** att användas till att bokföra transaktionerna för aktiviteten i fråga.

## <a name="required-setup-tasks"></a>Nödvändiga inställningsuppgifter

Följande tabell innehåller en serie uppgifter för att skapa anläggningstillgångar samt länkar till relaterade artiklar.

| Till | Gå till |
|---|---|
| Skapa standardredovisningskonton, fördelningsnycklar, journalmallar och batcher för fasta anläggningstillgångar och ställ in indelningar och underklasser för fasta anläggningstillgångar som till exempel Materiella och Immateriella. |[Skapa allmän information om anläggningstillgångar](fa-how-setup-general.md) |
| Skapa avskrivningsregler, definiera avskrivningsmetoder, integrera med redovisningen och tillåta att transaktioner kan kopieras till flera avskrivningsregler. |[Konfigurera avskrivning av anläggningstillgångar](fa-how-setup-depreciation.md) |

## <a name="optional-setup-tasks-insurance-maintenance-and-user-defined-depreciation-methods"></a>Valfria inställningsuppgifter (försäkring, underhåll och användardefinierade avskrivningsmetoder)

Följande tabell innehåller en serie valfria uppgifter för att ställa in anläggningstillgångar, t.ex. försäkring, underhåll och avskrivningsmetoder och länkar till relaterade artiklar. 

| Till | Gå till |
|---|---|
| Aktivera försäkringsskydd för anläggningstillgångar, ange allmän försäkringsinformation, ett försäkringskort per brev och förbered journaler för att bokföra försäkringkostnader. |[Skapa försäkring för anläggningstillgångar](fa-how-setup-insurance.md) |
| Aktivera underhåll av anläggningstillgångar, ange allmän underhållsinformation, skapa konton för bokföring av underhåll och definiera typer av underhållsarbete. |[Konfigurera underhåll av anläggningstillgång](fa-how-setup-maintenance.md) |
| Så här använder du avskrivningsmetoder. |[Konfigurera användardefinierade avskrivningsmetoder](fa-how-setup-user-defined-depreciation-method.md) |

## <a name="see-also"></a>Se även

[Översikt över anläggningstillgångar](fa-manage.md)  
[Översikt över analys av anläggningstillgångar](fa-analytics-overview.md)   
[Ekonomi](finance.md)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
