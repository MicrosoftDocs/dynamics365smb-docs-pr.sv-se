---
title: Skapa lagerställesinnehåll
description: När du har skapat lagerställena kan du ange de artiklar som du vill lagra i dem och skapa regler som styr hur ofta lagerställen fylls i automatiskt.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 7374
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Skapa lagerställesinnehåll

När du har skapat lagerställena kan du skapa deras innehåll. Du kan ange de artiklar som du vill lagra på en viss lagerplats och ange regler som styr hur lagerstället ska fyllas med en viss artikel. Du kan göra detta manuellt på sidan **lagerställesinnehåll** eller automatiskt med sidan **skapa lagerställesinnehåll i kalkylarket**.

## Så här skapar du lagerställesinnehåll manuellt

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Platser** och väljer sedan relaterad länk.  
2. Markera platsen där du vill skapa lagerställesinnehållet och väljer åtgärden **Lagerställen**.  
3. Markera lagerstället där du vill skapa lagerställesinnehållet och väljer åtgärden **Innehåll**.  
4. För varje artikel som du vill lagra på lagerstället fyller du i en rad på sidan **Lagerställesinnehåll** med tillämplig information. Vissa av fälten har redan fyllts i med information om lagerstället.  
5. Fyll först i fältet **Artikelnr** och sedan, om du använder dirigerad artikelinförsel och plockning, fyller du i andra fält som **Enhetskod**, **Max. ant.** och **Min. ant.**.  

Välj **Fast** fältet, om det behövs. Om lagerstället ska användas som standardlagerplats för artikeln markerar du fältet **Standardlagerplats**.  

Om du använder dirigerad artikelinförsel och plockning, och har angett rätt dimensionsinformation på artikelkortet om varje artikels måttenheter, kontrolleras det högsta antalet som du har angett på sidan **Lagerställesinnehåll** mot lagerställets fysiska lagringskapacitet. Sedan används lägsta och högsta antal när lagerplatspåfyllning beräknas och artikelinförsel föreslås.  

Om du markerar fältet **Fast** kopplar du artikeln till lagerstället. Det betyder att [!INCLUDE[prod_short](includes/prod_short.md)] försöker placera den här artikeln på lagerstället om det finns utrymme för den, och den post som kopplar artikeln till lagerstället sparas även om antalet på lagerstället är noll. Andra artiklar kan placeras på lagerstället, även om en viss artikel har kopplats till lagerstället. Andra objekt kan placeras på lagerstället, även om en viss artikel har kopplats till lagerstället.  

> [!NOTE]  
> Du kan skapa flera lagerställesinnehåll samtidigt på sidan **Lagerställesinnehålluppl förslag**.  

## Så här skapar du lagerställesinnehåll i kalkylarket:

När du har skapat lagerställena kan du skapa det lagerställesinnehåll som du vill ha på varje lagerplats i lagerplatsuppläggningskalkylarket.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Lagerställesinnehålluppl kalkylark** och väljer sedan relaterad länk.  
2. I fältet **Namn** i kalkylarkshuvudet väljer du kalkylarket för det lagerställe där du vill skapa lagerställesinnehåll.  
3. I fältet **Lagerplatskod** väljer du den lagerplatskod som du vill definiera lagerplatsinnehåll för.  

    Om lagerstället är inställt på dirigerad artikelinförsel och plockning fylls fälten som rör just den lagerstället i automatiskt, exempelvis **Lagerplatstyp**, **Dist.lager klasskod** och **Lagerplatsordning**. Detta är information som du måste ta hänsyn till när du definierar lagerställesinnehållet.  
4. Välj den artikel som du vill tilldela lagerstället och fyll i de fält som avser lagerställesinnehållet. Om du använder dirigerad artikelinförsel och plockning, och vill använda funktionen **Beräkna lagerplatsåteranskaffning**, fyller du i **Max. ant.** och **Min. ant.**.  

    Om du vill att den här lagerstället ska väljas automatiskt för artikeln, även om lagerplatskvantiteten är **0** och alla övriga artikelinförselvillkor är lika, markerar du fältet **Fast**.  
5. Upprepa steg tre till fyra för varje artikel som du vill tilldela till en lagerplats.  
6. Välj åtgärden **Skriv ut** för att förhandsgranska och skriva ut det lagerställesinnehåll som du har angett i kalkylarket. Fortsätt att revidera lagerställesinnehållet tills du är nöjd.  
7. När du är klar kan du välja åtgärden **skapa lagerställesinnehåll**.  

I det här kalkylarket kan du arbeta med flera lagerställesinnehållsrader för flera lagerställen och på så sätt få en bra översikt över vad du placerar på olika lagerställen i en viss zon, gång eller ställning.  

## Se även

[Warehouse Management – Översikt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Ställa in Warehouse Management](warehouse-setup-warehouse.md)  
[Monteringshantering](assembly-assemble-items.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
