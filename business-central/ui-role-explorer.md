---
title: Utforska och bläddra i sidor per roll
description: Du kan få en översikt över alla affärsfunktioner som är tillgängliga för din roll och för andra roller med Rollutforskare.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
---

# Söka efter sidor med rollutforskaren

Du kan få en översikt över alla affärsfunktioner som är tillgängliga för din roll och för andra roller om du går ett steg längre. I följande dokumentation kallas denna funktionsöversikt *rollutforskaren.*

Varje element i rullutforskaren är en åtgärd som öppnar en sida. Därför kan du också använda rollutforskaren som ett sätt att navigera i [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## Öppna rollutforskaren

Du kan öppna rullutforskaren från rollcentret och alla listsidor och från fönstret **Berätta**.

- I Rollcenter eller någon listsida, välj ![menyknappen.](media/ui_menu_button.png "Menyknapp") Knappen till höger om navigeringsfältet eller väljer <kbd>Shift</kbd>+<kbd>F12</kbd>.
- I fönstret **Berätta**, välj åtgärden **utforska** längst ned.

När du först öppnar rollcentret visas länkar till de flesta funktioner som är tillgängliga för din roll.

## Navigera i funktioner

De åtgärder som öppnar sidor ordnas under noder som namnges efter funktionerna eller modulerna. Varje nod kan komprimeras eller expanderas individuellt och du kan komprimera/expandera alla noder tillsammans.

- Om du vill expandera eller komprimera en enskild nod väljer du noden. Detta gäller noder på den översta nivån och undernoder.
- Om du vill visa/dölja alla noder på översta nivån på sidan, men låt undernoderna vara de du vill ha, väljer du **...** längst upp och välj sedan **Visa** eller **Dölj**.
- Om du vill expandera/komprimera alla toppnivåer och alla undernoder under den väljer du **...** längst upp, välj sedan **Expandera alla** eller **Visa alla**.

## Söka efter funktioner

Du kan snabbt hitta funktioner genom att välja **Sök** och sedan ange ett ord eller en fras för funktionen som du söker efter. I rollcentret markeras all matchande text. Om en funktion är dold från att visas i en komprimerad nod, markeras den komprimerade noden med en punkt. 

## Utforska andra roller

Om du vill utforska andra roller än dina egna markerar du **utforska fler roller**. Rollcentret visar varje roll under sin egen rubrik, med länkar till dess funktioner. Du kan sedan navigera och söka efter funktioner på samma sätt som när du utforskar din roll.

> [!NOTE]
> Du kan bara se roller som är inställda för att visas i roll Utforskaren. Om det inte finns någon roll som du förväntar dig, är den antagligen inte konfigurerad för den. Mer information finns i [Hantera profiler](admin-users-profiles-roles.md). 

När du utforskar andra roller kan du också begränsa prospekteringen genom att använda **rapporten och analys** och **administration** åtgärder överst i rollcentret.

- **Rapport och analys** visar endast funktioner som är kategoriserade som rapporter och analysfunktioner.
- **Administration** visar bara de funktioner som kategoriseras som administrationsfunktioner.

> [!TIP]
> För utvecklare klassificerar du sidor och rapporter genom att ange [egenskapen UsageCategory](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) i objektets Al-kod.
<!--
 
## Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You will only see roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## Expandera och komprimera noder i rollutforskaren

De åtgärder som öppnar sidor ordnas under noder som namnges efter funktionerna eller modulerna. Varje nod kan komprimeras eller expanderas individuellt och du kan komprimera/expandera alla noder tillsammans.

- Om du vill expandera eller komprimera en nod väljer du noden. Detta gäller noder på den översta nivån och undernoder.
- Om du vill expandera/komprimera alla noder på översta nivån på sidan väljer du åtgärden **Expandera** eller **Komprimera** i det övre högra hörnet.
- Så här expanderar/komprimerar du alla noder på översta nivån och alla undernoder under denna:
  - Välj <kbd>Ctrl</kbd>+<kbd>Shift</kbd> medan du väljer åtgärden **Expandera** eller **Dölj** i det övre högra hörnet.
  - Välj **...** i det övre högra hörnet och sedan åtgärden **Expandera alla** eller **Dölj alla**.

## Se även
[Söka efter sidor och information med berätta](ui-search.md)  
[Hantera profiler](admin-users-profiles-roles.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]