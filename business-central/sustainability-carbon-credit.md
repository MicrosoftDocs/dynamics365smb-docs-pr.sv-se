---
title: Arbeta med koldioxidkrediter
description: Läs om hur du ställer in och köper koldioxidkrediter.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, carbon, credit, CO2'
ms.search.form: null
ms.date: 08/20/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: solsen
---

# <a name="work-with-carbon-credit"></a>Arbeta med koldioxidkrediter

När företag inte kan minska sina utsläpp av olika skäl kan de köpa koldioxidkrediter för att kompensera sina utsläpp. Genom att köpa koldioxidkrediter kan ett företag fortfarande släppa ut motsvarande mängd gaser samtidigt som det förblir koldioxidneutralt. Dessa krediter köps från specialiserade leverantörer, vilket stimulerar utsläppsminskningar.  

I allmänhet är kolkrediter tillstånd som gör det möjligt för ägaren att släppa ut en viss mängd koldioxid (CO₂) eller andra växthusgaser (GHG). En kolkredit representerar vanligtvis rätten att släppa ut ett ton CO₂ eller motsvarande mängd av en annan växthusgas, så det är viktigt att aktivera detta alternativ för vissa organisationer.  

## <a name="set-up-the-carbon-credit"></a>Ställ in koldioxidkrediten

Carbon Credit in [!INCLUDE[prod_short](includes/prod_short.md)] kan ställas in som **Artikel**. Så här ställer **du in artikeln** som en koldioxidkredit:
  
1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Artiklar** och välj sedan relaterad länk. 
2. [Skapa nytt objekt enligt förklaringen](inventory-how-register-new-items.md).   
3. När artikeln har skapats Välj fältet Växthusgaskredit på snabbfliken Hållbarhet **och lägger till** värdet på koldioxidkrediten med hjälp **av fältet Koldioxidkredit per UOM** . **·** 

> [!NOTE]
> **Carbon Credit Per UOM** representerar mängden CO₂ i den måttenhet som konfigurerats i **Emission Unit of Measure Code** i **Sustainability Setup**. Så detta betyder det totala värdet av kolkredit som mängden krediterad CO₂ per en **basenhet för** använd artikel.  

> [!NOTE]
> Du kan ställa in alla typer av artiklar, oavsett om det är lager, service eller icke-lager, som en kolkredit.  

## <a name="to-purchase-carbon-credit"></a>Så här köper du koldioxidkrediter

### <a name="purchase-documents"></a>Inköpsdokument

Om du vill arbeta med inköpsrelaterade dokument följer du stegen:

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta vad du vill göra") och:  
   1. Ange **Inköpsfakturor** om du vill att faktura ska vara en **dokumenttyp** och Välj sedan relaterad länk.  
   2. Ange **Inköpsorder** om du vill att order ska vara en **Dokumenttyp** och Välj sedan relaterad länk.   
2. Fyll i dokumenthuvudet baserat på följande instruktion [hur du arbetar med inköpsfakturor och order](purchasing-how-record-purchases.md). 
3. Välj den artikel som konfigurerats som en kolkredit i Nr **.** På inköpsdokumentraderna och lägg till lämplig **kvantitet** och **direkt styckkostnad**. 
4.  **Lägg till hållbarhetskontonr.** du skulle använda för att minska ditt koldioxidvärde (CO₂). Värdet i **fältet Utsläpp CO2** fylls i automatiskt baserat på det värde du har konfigurerat i **fältet Koldioxidkredit per UOM** på **artikeln**  kort.
5. Bokför dokumentet.

> [!NOTE]
> Även om kolkrediter kommer att minska värdet på poster, ser du en positiv mängd värde i utsläpp **CO2**. Men när du har bokfört dokumentet ser du ett värde med en negativ logg i hållbarhetstransaktionen med växthusgaskrediten **som** dokumenttyp **.**  **·**  

### <a name="sustainability-journals"></a>Hållbarhetsjournaler

För att arbeta med **Sustainability Journal** följ stegen:  

1. Välj ![glödlampan som öppnar funktionen Berätta 3.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Hållbarhetsjournal** och väljer sedan relaterad länk. 
2.  **På sidan Hållbarhetsjournal** anger du så många rader som du tänker bokföra i samma batch.  
3. Välj GHG-kredit **i** fältet **Dokumenttyp** .    
4. I fältet **Kontonr.** kan du bara välja icke-spärrade hållbarhetskonton där fältet **Direktbokföring** är markerat och fältet **Bokföringstyp** anges till **Bokföring**. Kontona måste också ha konfigurerats med kategori och underkategori. Välj lämpligt konto för att bokföra koldioxidkrediter.
5. Välj **Manuell inmatning** och ange det värde du vill bokföra som en koldioxidkredit i **fältet Utsläpp CO2** .  
6. Bokför journalen.   

## <a name="see-also"></a>Se även

[Ekonomi](finance.md)    
[Registrera hållbarhetstransaktioner](finance-sustainability-journal.md)    
[Översikt över hållbarhetshantering](finance-manage-sustainability.md)    
[Hållbarhetskonfiguration](finance-sustainability-setup.md)   
[Diagram över hållbarhetskonton och redovisning](finance-sustainability-accounts-ledger.md)  
[Ad hoc-analys av data för hållbarhet](ad-hoc-analysis-sustainability.md)    
[Hållbarhetsrapporter och analyser inom [!INCLUDE[prod_short](includes/prod_short.md)]](sustainability-reports.md)   
[Hållbarhets-API](/dynamics365/business-central/dev-itpro/api-sustainability/sustainability-api?toc=/dynamics365/business-central/toc.json)    
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
