---
title: Om styckkost. beräkningstyp
description: Läs om hur värderingsprincipen och andra faktorer påverkar fältet Styckkostnad på artikelkortet.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: edupont
---
# Om styckkost. beräkningstyp

Varje artikel har en styckkostnad som beräknas med hjälp av företagets värderingsprincip och andra faktorer. Som regel med *Standard* värderingsprinciperna **Styckkostnad** fältvärdet baseras på standardkostnaden för artikeln. För alla andra kalkylmetoder (*FIFO*, *LIFO*, *Specifik* och *Genomsnitt*), styckkostnaden beräknas utifrån den genomsnittliga styckkostnaden över en tidsperiod.  

Mer information finns i [Administrera lagerkostnader](finance-manage-inventory-costs.md).  

## När uppdateras styckkostnadsfältet

Den valda kalkylmetoden påverkar när **Styckkostnad** uppdateras.

När kalkylmetoden är satt som *Standard*, fältet **Styckkostnad** uppdateras när standardkostnaden ändras och användare inte kan redigera fältet **Styckkostnad**. För mer information, se [Uppdateras standardkostnader](finance-how-to-update-standard-costs.md).

Om värderingsprincipen är *FIFO*, *LIFO*, *Specifik* eller *Genomsnitt*, sedan uppdateras **styckkostnaden** i följande fall:

* När artikeln kostnadsjusteras, automatiskt eller genom en [Justera kostnad](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually) aktivitet.
* När du bokför inköpsfakturor, utflöde, eller positiv justering om något av följande villkor gäller:
  * Det fakturerade antalet för artikeln ändras från negativt eller noll till positivt.
  * Den aktuella styckkostnaden är noll.

Om något av dessa villkor gäller uppdateras fältet **styckkostnaden** med värdet i fältet **Sista direkta kostnad** på artikelkortet.

> [!NOTE]
> Fältet **Styckkostnad** uppdateras inte om den aktuella styckkostnaden är högre än noll och den nya styckkostnaden är noll. En styckkostnad på noll betraktas som ett undantag från den ordinarie verksamheten. Därför bibehålls den aktuella styckkostnaden för att ge det senast kända, relevanta värdet. Detta undantag gäller även om det befintliga lagret har omvärderats till noll.

I fältet **Styckkostnad** på artikelkortet kan du drilla ner för att se historiken för transaktioner som den genomsnittliga kostnaden för tillgängliga enheter beräknas från i fönstret **Översikt: Beräkning av genomsnittskostnad**.

## Beräkna styckkostnad vid inköp

När du köper in artiklar kopieras alltid värdet i fältet **Senaste direkt kostnad** på artikelkortet till fältet **Inköpspris** på en inköpsrad eller till raden **A-pris** på en artikeljournalrad.

Ditt val i fältet **Värderingsprincip** påverkar hur [!INCLUDE[prod_short](includes/prod_short.md)] beräknar innehållet i fältet **Styckkostnad** på raderna.

### Värderingsprincip FIFO, LIFO, Serienr eller Genomsnitt

[!INCLUDE[prod_short](includes/prod_short.md)] beräknar innehållet i fältet **Styckkostnad (BVA)** på inköpsraden eller innehållet i fältet **Styckkostnad** på artikeljournalraden enligt följande formel:

*Styckkostnad (BVA) = (Inköpspris – (Rabattbelopp/Antal)) x (1 + Indirekt kostnad %/100) + Overheadkostnad*

### Värderingsprincip Standard

Fältet **Styckkostnad (BVA)** på inköpsraden, eller fältet **Styckkostnad** på artikeljournalraden, fylls i med värdet i fältet **Styckkostnad** på artikelkortet. Med värderingsprincipen som *Standard* beräknas detta värde alltid enligt standardkostnaden.

När du bokför inköpet använder [!INCLUDE[prod_short](includes/prod_short.md)] styckkostnaden från inköpsraden eller artikeljournalraden till transaktionsrad för den inköpta artikeln. Du kan se den i artikelns transaktionslista.

### Samtliga värderingsprinciper

Innehållet i fältet Kost.belopp aktuellt, eller i vissa fall fältet **Kost.belopp (faktisk)** eller, om tillämpligt, fältet **Kost.belopp (förväntat)** för den här artikeltransaktionen, beräknas alltid enligt styckkostnaden från raden i källdokumentet, oavsett vilken värderingsprincip som används för artikeln.

## Beräkning av styckkostnad vid försäljning

När du säljer artiklar, kopieras styckkostnaden från fältet **Styckkostnad** på artikelkortet till försäljnings- eller artikeljournalraden.

När du bokför, kopieras styckkostnaden till en rad på försäljningsfakturan. Styckkostnaden visas på artikelns transaktionslista. [!INCLUDE[prod_short](includes/prod_short.md)] använder styckkostnaden från källdokumentraden för att beräkna innehållet i **Kost.belopp (aktuellt)** eller, om tillämpligt, fältet **Kost.belopp(förväntat)** oavsett vilken värderingsprincip som används för artikeln.

## Se även

[Hantera lagerkostnader](finance-manage-inventory-costs.md)  
[Registrera nya artiklar](inventory-how-register-new-items.md)  
[Om lagerkalkylering](finance-learn-about-costing.md)  
[Lager](inventory-manage-inventory.md)  
[Försäljning](sales-manage-sales.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Designdetaljer: Icke-avdragsgill moms](design-details-nondeductible-vat.md)
[Ställa in bästa praxis: Värderingsprincip](setup-best-practices-costing-method.md)  
[Designdetaljer: Värderingsprinciper](design-details-costing-methods.md)  
[Designdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
