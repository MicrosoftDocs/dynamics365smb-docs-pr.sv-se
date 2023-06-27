---
title: Skaffa Business Central på din stationära dator
description: I den här artikeln beskrivs hur du skaffar Business Central-appen på stationär Windows eller Mac iOS.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'phone, tablet'
ms.date: 01/11/2022
ms.author: jswymer
---
# <a name="get-business-central-desktop-app" />Hämta appen för Business Central Desktop

Om du har en Windows- eller macOS-dator kan du installera en Business Central-app på stationära datorn. Appen fungerar med Business Central Online och lokalt.

## <a name="why-use-the-app" />Varför ska du använda appen?

Business Central-appen liknar webbklienten, men har följande fördelar:

- Appen är lätt tillgänglig på **Start**-menyn, du kan enkelt fästa den i uppgiftsfältet eller låta den startas som standard när du startar datorn.
- I allmänhet är appen också en snabbare och smidigare att rendera på skärmen, utan prestanda skillnader, jämfört med att köras [!INCLUDE[prod_short](includes/prod_short.md)] i webbläsaren.
- Appen öppnas i ett eget fönster oberoende av alla webbläsarfönster. Den här funktionen gör det enklare att hitta när du kör ett stort antal appar eller webbläsare.
- Om det finns mer än en Business Central-miljö (endast online), kan du installera appen separat för varje miljö.

     När du öppnar appen för en specifik miljö ingår miljönamnet i fönster rubriken. När du arbetar i flera [!INCLUDE[prod_short](includes/prod_short.md)] miljöer visas varje appfönster separat. Namnet gör det enklare att se vilket fönster som är kopplat till varje miljö.

## <a name="install-the-app-for-business-central-online" />Installera appen Business Central Online

Det finns två sätt att installera appen för Business Central Online. Du kan installera den direkt från webbläsaren eller från Microsoft Store. Oavsett vilken metod du använder är det samma app. Skillnaden är att när du installerar från webbläsaren kan du installera appen för varje miljö när det finns fler än en.

### <a name="from-microsoft-store" />Från Microsoft Store

1. Gå till [Microsoft Store](https://go.microsoft.com/fwlink/?linkid=2182870).
2. Välj **Hämta** > **Installera**. 
3. När appen har installerats väljer du **Öppna** och loggar sedan in på Business Central.

Nästa gång du vill öppna appen söker du efter den i **Start**-menyn.

### <a name="from-the-browser" />Från webbläsaren

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

## <a name="install-the-app-for-business-central-on-premises" />Installera appen för Business Central lokalt

Installationen av skrivbordsappen när du använder Business Central lokalt görs direkt från webbläsaren enligt [anvisningarna ovan](#from-the-browser). Om du bara har en innehavare öppnar du först Business Central i webbläsaren och väljer sedan någon av ![ ikonerna för att installera en app i Edge.](media/ui-edge-install-app-icon.png) **App tillgänglig. Installera Business Central** eller ![ ikon för att installera en app i Chrome.](media/ui-chrome-install-app-icon.png) **Installera Business Central** enligt anvisningarna ovan.

Skillnaden är när du har flera innehavare. Till skillnad från [!INCLUDE[prod_short](includes/prod_short.md)] online, där du kan installera appen för olika miljöer, kan du bara installera appen för en klientorganisation. Innan du installerar appen när du har flera klientorganisationer måste du därför växla till rätt klientorganisation. När du öppnar appen när du har installerat den öppnas innehavaren direkt.

> [!IMPORTANT]
> Om du använder Business Central 2021 utgivningscykel 1 (version 18) eller tidigare kan du inte installera appen på det sätt som beskrivs i den här artikeln. Installera i stället appen från [Microsoft Store](https://go.microsoft.com/fwlink/?LinkId=734848). Mer information och hjälp om hur du installerar den här äldre appen finns i [Förbereda och installera Business Central-appen](/dynamics365/business-central/dev-itpro/deployment/install-business-central-app).

## <a name="see-related-microsoft-training" />Se relaterad [Microsoft utbildning](/training/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also" />Se även

[Vanliga frågor och svar om mobilappar](ui-mobile-faq.yml)  
[Gör dig redo att göra affärer](ui-get-ready-business.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
