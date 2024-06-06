---
title: Skaffa Business Central på din stationära dator
description: I den här artikeln beskrivs hur du skaffar Business Central-appen på stationär Windows eller Mac iOS.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: get-started
ms.search.keywords: 'phone, tablet'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="get-the-business-central-desktop-app"></a>Hämta skrivbordsappen för Business Central

Om du har en Windows- eller macOS-dator kan du installera en [!INCLUDE [prod_short](includes/prod_short.md)]-app på datorn. Appen fungerar med [!INCLUDE [prod_short](includes/prod_short.md)] Online och lokalt.

## <a name="why-use-the-app"></a>Varför ska du använda appen?

[!INCLUDE [prod_short](includes/prod_short.md)] app liknar webbklienten, men har följande fördelar:

- Appen är lätt tillgänglig på **Start**-menyn, du kan enkelt fästa den i uppgiftsfältet eller låta den startas som standard när du startar datorn.
- I allmänhet är appen också en snabbare och smidigare att rendera på skärmen, utan prestanda skillnader, jämfört med att köras [!INCLUDE[prod_short](includes/prod_short.md)] i webbläsaren.
- Appen öppnas i ett eget fönster oberoende av alla webbläsarfönster. Den här funktionen gör det enklare att hitta när du kör ett stort antal appar eller webbläsare.
- Om det finns mer än en [!INCLUDE [prod_short](includes/prod_short.md)]-miljö (endast online), kan du installera appen separat för varje miljö.

     När du öppnar appen för en specifik miljö ingår miljönamnet i fönster rubriken. När du arbetar i flera [!INCLUDE[prod_short](includes/prod_short.md)] miljöer visas varje appfönster separat. Namnet gör det enklare att se vilket fönster som är kopplat till varje miljö.

## <a name="install-the-app-for--online"></a>Installera appen för [!INCLUDE [prod_short](includes/prod_short.md)] online

Det finns två sätt att installera appen för [!INCLUDE [prod_short](includes/prod_short.md)] online. Du kan installera den direkt från webbläsaren eller från Microsoft Store. Oavsett vilken metod du använder är det samma app. Skillnaden är att när du installerar från webbläsaren kan du installera appen för varje miljö när det finns fler än en.

### <a name="from-microsoft-store"></a>Från Microsoft Store

1. Gå till [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=2182870).
2. Välj **Hämta** > **Installera**. 
3. När appen har installerats väljer du **Öppna** och loggar sedan in på [!INCLUDE [prod_short](includes/prod_short.md)].

Nästa gång du vill öppna appen söker du efter den i **Start**-menyn.

### <a name="from-the-browser"></a>Från webbläsaren

1. Öppna [!INCLUDE[prod_short](includes/prod_short.md)] webbklienten i antingen Microsoft Edge eller Google Chrome.

2. Om sidan där du väljer miljön visas kan du göra något av följande:

   - Välj miljön och gå till nästa steg för att installera appen. I så fall öppnar den installerade appen den miljö som du väljer.
   - Välj inte miljön och gå till nästa steg för att installera appen. I så fall öppnar den installerade appen sidan miljö val, i stället för en specifik miljö.

3. Om du vill installera appen, beroende på webbläsare, väljer du ![ ikon för att installera en app i Edge.](media/ui-edge-install-app-icon.png) **App tillgänglig. Installera Business Central** eller ![ ikon för att installera en app i Chrome.](media/ui-chrome-install-app-icon.png) **Installera appen Business Central**, sedan **Installera**.

   | Microsoft Edge | Google Chrome |
   |--|--|
   | :::image type="content" source="media/ui-edge-install-app-v2.png" alt-text="illustration av en knapp för att installera en app i Edge."::: | :::image type="content" source="media/ui-chrome-install-app-v2.png" alt-text="illustration av en knapp för att installera en app i Chrome."::: |

  > [!TIP]
  > Med Edge kan du också installera appen genom att gå till **inställningar och mer** i webbläsaren i och sedan välja **Appar** > **Installera den här webbplatsen som en app** > **Installera**.

När programmet installerats visas det på **Start**-menyn. Om du har valt en specifik miljö för appen läggs miljönamnet till i programnamnet på **Start**-menyn.

## <a name="install-the-app-for--on-premises"></a>Installera appen för [!INCLUDE [prod_short](includes/prod_short.md)] lokalt

Installationen av skrivbordsappen när du använder [!INCLUDE [prod_short](includes/prod_short.md)] lokalt görs direkt från webbläsaren enligt [anvisningarna ovan](#from-the-browser). Om du bara har en innehavare öppnar du först [!INCLUDE [prod_short](includes/prod_short.md)] i webbläsaren och väljer sedan någon av ![ikonerna för att installera en app i Edge.](media/ui-edge-install-app-icon.png) **App tillgänglig. Installera Business Central** eller ![ ikon för att installera en app i Chrome.](media/ui-chrome-install-app-icon.png) **Installera Business Central** enligt anvisningarna ovan.

Skillnaden är när du har flera innehavare. Till skillnad från [!INCLUDE[prod_short](includes/prod_short.md)] online, där du kan installera appen för olika miljöer, kan du bara installera appen för en klientorganisation. Innan du installerar appen när du har flera klientorganisationer måste du därför växla till rätt klientorganisation. När du öppnar appen när du har installerat den öppnas innehavaren direkt.

## <a name="see-also"></a>Se även

[Vanliga frågor och svar om mobilappar](ui-mobile-faq.yml)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
