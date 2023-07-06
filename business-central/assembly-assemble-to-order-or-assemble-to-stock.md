---
title: Förstå montering mot kundorder och montering mot lager
description: Lära dig att montera artiklar för försäljningsorder eller för att hålla i lager för framtida försäljning.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a><a name="understanding-assemble-to-order-and-assemble-to-stock"></a><a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Förstå montering mot kundorder och montering mot lager

[!INCLUDE [prod_short](includes/prod_short.md)] låter dig lägga till monteringsartiklar på följande sätt:

* Montering mot kundorder  
* Montering mot lager  

## <a name="assemble-to-order"></a><a name="assemble-to-order"></a><a name="assemble-to-order"></a>Montering mot kundorder

Använd processen montering mot kundorder för artiklar som du inte vill lagerföra. Du kan till exempel ha följande orsaker:

* Du kan anpassa artiklarna efter kundkrav.
* Du vill minimera kostnaden för lagerbehållningen.

I följande lista beskrivs några av fördelarna med processen montering mot kundorder:  

* Anpassa monteringsartiklar, när ta en försäljningsorder.  
* Översikt över tillgänglighet för monteringsartikeln och dess komponenter.  
* Reservera monteringskomponenter direkt för att garantera uppfyllning av order.  
* Bestämma vinst av anpassad order efter att summera priser och kostnad.  
* Integrering med distributionslagret som gör det enklare att montering och leverans.  
* Montering mot order när du skapar en försäljningsorder eller avropsorder.  
* Kombinera lagerkvantiteten med antalet för montering mot kundorder.  

I processen montering mot kundorder monterar du artiklar för en försäljningsorder. Det finns ett-till-ett-länk mellan monteringsordern och försäljningsordern.  

När du anger en artikel för montering mot kundorder på en försäljningsorderrad skapas en monteringsorder automatiskt. Monteringsordern baseras på försäljningsraden och dess rader baseras på artikelns monteringsstruktur. Antalet komponenter i monteringsstrukturen multipliceras med partistorleken. På sidan **montering mot kundorderrad** visar detaljer om de länkade monteringsorderraderna. Informationen kan hjälpa dig att anpassa monteringsartikeln. Leveransdatum är baserat på tillgängligheten av komponenter. Om du vill veta mer om att montera artiklar för försäljningsorder går du till [Sälja artiklar monterade på order](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Även om detta inte är en del av standard processen, kan du sälja lagerkvantiteten och antalet för montering mot kundorder på samma försäljningsorder. För att lära dig mer om att kombinera lager och artiklar för montering mot kundorder, gå till [Sälja lagerartiklar i flöden för montering mot kundorder](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

För att ange att en artikel är monterad på beställning, i fältet **Monteringsmetod** på sidan **Artikelkort** för artikeln, välj **Montering mot kundorder**.  

## <a name="assemble-to-stock"></a><a name="assemble-to-stock"></a><a name="assemble-to-stock"></a>Montering mot lager

Använd processen montering mot lager för artiklar som du monterar och lagrar för framtida försäljning. Artiklar med montering mot lager är standardartiklar, till exempel emballerade satser, som du inte anpassar. Du kan även förbruka dessa artiklar som monteringskomponenter. Artiklarna plockas och bearbetas som enstaka artiklar och hanteras som avslutade produktionsartiklar. För att lära dig mer om monteringsartiklar, gå till [Montera artiklar](assembly-how-to-assemble-items.md).  

När du anger ett montering mot lager artikel på en försäljningsrad behandlas artikeln som alla andra sålda artiklar från lagret. Du kan till exempel [!INCLUDE [prod_short](includes/prod_short.md)] endast kontrollera tillgängligheten för monterad artikel och inte dess komponenter.  

> [!NOTE]  
> Även om detta inte är en del av processen standard, kan du sammanställa en artikel för order, även om artikeln har konfigurerats till att monteras mot lager. Läs mer på [Artiklar för montering mot kundorder och lagerartiklar ihop](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

För att ange att en artikel är monterad på beställning, i fältet **Monteringsmetod** på sidan **Artikelkort** för artikeln, välj **Montering mot kundorder**.  

## <a name="combination-scenarios"></a><a name="combination-scenarios"></a><a name="combination-scenarios"></a>Kombinationsscenarion

När montering mot kundorder och lagerkvantiteter kombineras på försäljningsorder måste antalet för montering mot kundorder levereras först.  

Om en monteringsorder är kopplad till en försäljningsorderrad, kopieras värdet i fältet i **Antal att montera mot kundorder** på försäljningsorderraden till fältet **Antal att montera** via **Antal** på monteringsordern. Läs mer på [Sälja artiklar som monterats mot kundorder](assembly-how-to-sell-items-assembled-to-order.md).  

Värdet i fältet **Antal att montera** är relaterat till fältet **Ant. att utleverera** på försäljningsorderraden. Den här relationen styr hur du levererar delvisa och kompletta montering mot kundorder-antal:

* När hela kvantiteten på försäljningsorderraden är monterad mot kundorder
* I kombinationsscenarion där en del av antalet monteras mot kundorder och en del skickas från lagret.

Kombinations scenariot medger flexibilitet för delvisa leveranser. Du kan använda fältet **Antal att montera** för att ange hur stort antal som ska levereras delvis från lagret och genom att montera ordern.  

Om hela antalet på försäljningsraden måste monteras till order och levereras kopieras värdet i fältet **Ant. att utleverera** till fältet **Antal att montera** i den kopplade monteringsordern när du ändrar antal som ska levereras. Denna uppdatering försäkrar att det antalet som ska levereras uppfyller antalet i montering mot kundorder.  

Dock i kombinationsscenarion, kopieras inte hela värdet i **Ant. att utleverera** till fältet **Antal att montera** på monteringsordern. I stället infogas ett standardvärde i fältet **Antal att montera**. Värdet beräknas från fältet **Ant. att utleverera** för att säkerställa att antalet artiklar för montering mot kund order levereras först.

Om du vill att avvika från standardvärdet, om du till exempel bara vill montera mer eller mindre av antalet i fältet **Ant. att utleverera** kan du ändra **Antal att montera** men endast enligt fördefinierade regler, som illustreras under.  

Ett exempel på varför du vill ändra kvantiteten så att montera, är att du ska delvis bokföra utleveransen av lagersaldot, innan monteringsutflöde kan levereras.  

Följande tabeller förklarar regler som definierar den minimala och maximala värde som du kan ange manuellt i **Antal att montera** för att avvika från standardvärdet i ett kombinationsscenario. Tabellen visar en kombinationsscenario där **Ant. att utleverera** på den kopplade försäljningsordern ändras från 7 till 4, och standard för **Antal att montera** är därför 4.  

**Försäljningsorderrad**

|                | **Antal** | **Ant. att utleverera** | **Antal att montera mot kundorder** | **Utlevererat antal** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Initialt värde**| 10          | 7                | 7                             | 0                    |
|**Förändring**      |              | 4                |                               |                      |

**Monteringsorderhuvud**

|                | **Antal** | **Ant. att utleverera** | **Antal att montera mot kundorder** | **Utlevererat antal** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Initialt värde**| 7           | 7                | 0                             | 7                    |
|**Förändring**      |              | 4 (infoga som standard)|                         |                      |

Utifrån detta exempel kan du endast ändra fältet **Antal att montera** enligt nedan:  

* Den lägsta kvantitet som du kan ange är 1. Du måste åtminstone sammanställa en enhet för att kunna sälja de fyra enheter, antaget att de återstående tre finns i lager.  
* Den höga kvantitet som du kan ange är 4. Den här gränsen garanterar att du inte sätter samman mer av artikeln än vad du behöver för försäljningen.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft-utbildning](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se även

[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med monteringsstrukturer](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Warehouse Management – översikt](design-details-warehouse-management.md)
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
