---
title: Registrera distributionslagerpersonal
description: Alla användare som utför distributionslageraktiviteter måste registreras som distributionslageranställda som är tilldelade ett standardlagerställe och eventuellt andra lagerställen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/25/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
ms.service: dynamics-365-business-central
---
# <a name="set-up-warehouse-employees"></a>Konfigurera distributionslagerpersonal

Du måste konfigurera varenda användare som utför distributionslageraktiviteter och tilldela dem till ett standardlagerställe. [!INCLUDE [prod_short](includes/prod_short.md)] filtrerar lageraktiviteterna till medarbetarens standardlagerställe. De kan bara utföra lageraktiviteter på lagerstället. Du kan också tilldela en användare till andra lagerställen. De kan komma åt men inte utföra aktiviteter på dessa lagerställen.

## <a name="to-set-up-warehouse-employees"></a>Så här registrerar du distributionslagerpersonal

1. Välj ikonen med ![glödlampan som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **distributionslagerpersonal** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny**.  
3. Välj **Användar-ID** fältet och markera användaren som ska läggas till som distributionslageranvändare. Välj **OK**.  
4. Gå till fältet **Lagerställekod** och ange koden för lagerstället där användaren ska arbeta.  
5. Aktivera växlingen **Standard** för att ange att detta är det enda lagerställe som den anställda kan utföra aktiviteter på.  
6. Upprepa de här stegen om du vill tilldela andra anställda till lagerställen, eller tilldela andra lagerställen till befintliga anställda.  

> [!TIP]
> Du kan också använda åtgärden **Lägg till mig som lageranställd** för att snabbt lägga till dig själv i listan över lageranställda. Detta är till exempel praktiskt när du testar funktionerna.

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in lagerstyrning](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definiera en bokföringspolicy för faktura för användare](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
