---
title: Hitta relaterade transaktioner för dokument
description: 'Lär dig hitta dokument, affärskontakter och artikeltransaktioner som är relaterade till varandra.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: 344
ms.date: 05/23/2022
ms.author: jswymer
---
# <a name="finding-related-entries-for-documents"></a>Hitta relaterade transaktioner för dokument

Lär dig hitta dokument och transaktioner som är relaterade till varandra baserat på gemensam information, t.ex.:

- Dokumentnummer eller bokföringsdatum.
- Typ av företagskontakt, nummer eller externt dokumentnummer.
- Artikelns serienummer eller partinummer.

Funktionen är användbar för att hitta redovisningstransaktionerna som har skapats som ett resultat av vissa transaktioner. När du söker efter dokumentnummer kan du skriva ut sammanfattningen i rapporten **Dokumenttransaktioner**.

## <a name="get-started"></a>Kom i gång

Funktionen Sök transaktioner kan du komma åt på nästan vilken sida som helst genom att trycka på tangenterna <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd>. Från sidor som specifikt visar bokförda dokument eller bokförda dokumentposter&mdash;för både listor och kort&mdash;kan du också öppna funktionen genom att välja åtgärden **Hitta transaktioner**.

På sidan **Hitta transaktioner** finns alla relaterade dokument och transaktioner baserade på dokumentnr och bokföringsdatum. Sidan är uppdelad i tre delar:

- I det övre avsnittet visas fält och åtgärder som du använder för att filtrera sökningen.
- I mitten-avsnittet visas relaterade dokument baserat på sökningen.
- I den nedre delen visas information om källdokumentet som hittades vid sökning.

## <a name="search-for-entries"></a>Söka efter transaktioner

Du kan söka efter transaktioner som bygger på information om antingen dokument, affärskontakt eller artikel. Välj ett av följande alternativ i det övre avsnittet, beroende på vilken typ av information du har:

|Åtgärd|Description|
|------|-----------|
| **Sök efter dokument** | Visa transaktioner baserat på ett visst verifikationsnummer eller bokföringsdatum. |
| **Sök efter företagskontakter** | Visa transaktioner baserat på en viss kontakttyp, ett visst kontaktnummer och/eller externt dokumentnummer. Det här sista alternativet gör det möjligt att söka efter leverantörs- eller kunddokument med hjälp av numret som tilldelats av kontakten. |
| **Sök efter artikelreferenser** | Visa transaktioner baserat på ett serienummer eller partinummer. Du kan ange partinumret eller serienumret, eller ett filter för det parti- eller serienummer som du vill söka efter. Denna åtgärd är användbar när du vill veta var ett specifikt artikelspårningsnummer har använts, vilken leverantör det kom ifrån eller till vilken kund det såldes. |

När du har gjort ett val anger du relevant sökningsinformation i fälten längst upp på sidan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] När du är klar väljer du **Sök** för att påbörja sökningen. Om du ändrar något av filtren, måste du välja **Sök** igen.

> [!TIP]
> Ett par exempel på hur du använder **Hitta transaktioner** finns i [Spåra artikel-Spårade artiklar](inventory-how-to-trace-item-tracked-items.md) och [Genomgång: Spåra serie-/partinummer](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Se även

[Spåra artiklar med artikelspårning](inventory-how-to-trace-item-tracked-items.md)  
[Söka efter bokförda dokument utan inkommande dokumentposter](across-how-find-posted-documents-without-income-document-records.md)  
[Hjälpmedel och kortkommandon](ui-accessibility.md)  
[Arbeta med Business Central](ui-work-product.md)  
[Lägga till en sidåtgärd i ditt rollcenter](ui-bookmarks.md)  
[Söka efter sidor och information med Berätta](ui-search.md)  
[Söka efter sidor med rollutforskaren](ui-role-explorer.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
