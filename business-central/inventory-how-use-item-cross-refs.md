---
title: Använd artikelreferenser
description: 'Skapa referenser mellan beskrivningar, måttenheter och varianter som du och leverantören eller kunden använder för en artikel.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/27/2021
ms.author: edupont
---
# <a name="use-item-references" />Använd artikelreferenser

Om du köper eller säljer artiklar som du och leverantören eller kunden använder olika villkor för kan du ställa in en referens mellan villkoren för artiklarna och villkoren som kunden eller leverantören för artikeln använder. På så sätt infogas leverantörens eller kundens artikelbeskrivning, enhet eller variantkod automatiskt på de relevanta dokumenten när du fyller i fältet **Artikelreferensnummer.** .  

> [!NOTE]
> [!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]
>
> Alla företag använder inte artikelreferenser. För att minimera sammanhängande sidor vi har dolt de relaterade fälten och åtgärderna som standard. Om du bestämmer dig för att använda väljer du fältet **Använd artikelreferenser** på sidan **Lagerinställning**. När du har aktiverat artikelreferenser finns fälten och åtgärderna på artikel-, leverantörs- och kundkortsidor och från försäljnings- och inköpsdokument.
>
> I versioner tidigare än utgivningscykel 2, 2021 kan administratören aktivera funktionen *Skriv längre artikelreferenser* på sidan [Funktionshantering](https://businesscentral.dynamics.com/?page=2610) (länken kräver att du har en [!INCLUDE [prod_short](includes/prod_short.md)]-klientorganisation). Hur du använder referenser ändras inte, men namn på sådant som sidor och knappar gör det. Exempelvis kommer sidan **Transaktioner för korsreferens av artikel** att bli sidan **Transaktioner för artikelreferens**.

## <a name="to-start-using-item-references" />Börja använda artikelreferenser

[!INCLUDE [2021_releasewave2](includes/2021_releasewave2.md)]

1. Välj ikonen :::image type="icon" source="media/ui-search/search_small.png" border="false":::, ange **lagerinställning** och välj sedan relaterad länk.
2. Välj fältet **Använd artikelreferenser**.

## <a name="to-set-up-an-item-reference" />Så här ställer du in en artikelreferens

1. Välj ikonen :::image type="icon" source="media/ui-search/search_small.png" border="false":::, ange **Artiklar** och välj sedan relaterad länk.
2. Öppna kortet för en artikel som du vill skapa en referens för.
3. Välj åtgärden **Artikelreferens**.

     Om du inte hittar åtgärden **Artikelreferenser** väljer du om du vill visa fler alternativ och sedan söker du under **Relaterat** > **Artikel**.
  
4. På en ny rad på sidan **Artikel referenstrans.**, fyll i fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Följande procedur beskriver hur du anger artikelreferensen på en inköpsorder. Liknande steg gäller för försäljningsdokument och andra inköpsdokument.  

## <a name="to-enter-a-vendors-item-description-on-a-document" />Ange leverantörens artikelbeskrivning på ett dokument

1. Välj ikonen :::image type="icon" source="media/ui-search/search_small.png" border="false":::, ange **inköpsorder** och välj sedan relaterad länk.
2. Skapa en inköpsorder för leverantören som du ställer in en artikelreferens för ovan.
3. Skapa en inköpsorderrad för artikeln som du ställer in en artikelreferens för ovan.
4. I **Artikelreferensnummer.** välj relevant artikelreferens och välj sedan knappen **OK**.

Fältet **beskrivning** på raden skrivs över med leverantörens artikelbeskrivning som ställs in på referensartikelns transaktion. Om artikelreferensen innehåller en variantkod eller en måttenhet kopieras dessa värden också till dokumentet.  

## <a name="see-also" />Se även

[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
