---
title: Importera och exportera data i SIE-format (Standard Import Export)
description: Denna artikel förklarar hur du kan importera och exportera redovisningsdata i SIE-format (Standard Import Export) för Sverige.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5264, 5266, 5267, 5270, 5315'
ms.date: 06/08/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="import-and-export-data-in-the-standard-import-export-sie-format"></a>Importera och exportera data i SIE-format (Standard Import Export)

Du kan importera och exportera redovisningsdata i SIE-format (Standard Import Export). Genom att ange SIE-dimensioner och -filtyper kan du definiera vilken detaljnivå import- eller exporttransaktionerna ska ha. Mer information finns i [SIE-grupp](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d).

> [!NOTE]
> Export av SIE-verifieringsfiler är en del av den svenska lokaliseringen. Under version 22.1 kommer svensk lokalisering emellertid att baseras på W1-basobjektet och SIE-funktionen flyttas till tillägget som installeras som standard. Den här funktionen baseras på appen för granskning av uppdateringsfiler som har det förinstallerade SIE-formatet. Mer information om den här ändringen finns i [Export av verifieringsfiler](../../finance-how-to-export-audit-files.md).

Även om funktionen är förinstallerad aktiveras den inte som standard. Följ dessa steg för att aktivera funktionen.

1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du arbetsyta **Funktionshantering** och väljer sedan relaterad länk.
2. Hitta funktionen **Feature update: Enable using SIE Audit Files Exports**. I kolumnen **Aktiverad för** väljer du **Alla användare**.

## <a name="audit-files-export"></a>Export av verifieringsfiler

När du aktiverar **Export av SIE-verifieringsfiler** till funktionshantering kan du konfigurera funktionen med hjälp av en guide. Du kan emellertid installera funktionen senare genom att köra sidan **Installationsguiden för export av SIE-verifieringsfiler**. Om du vill ställa in systemet manuellt följer du instruktionerna i artikeln [exportera verifieringsfiler](../../finance-how-to-export-audit-files.md).

### <a name="set-up-sie-dimensions"></a>Konfigurera SIE-dimensioner

1. Välj ![glödlampan som öppnar funktionen Berätta.](../../media/ui-search/search_small.png "Berätta vad du vill göra") anger du **dimensions-SIE** och väljer sedan relaterad länk.
2. I fältet **Dimensionskod** väljer du en av de standard dimensioner som du vill mappa.
3. I fältet **SIE-dimension** anger du det nummer som du vill tilldela dimensionen.
4. I fältet **Valda** du om dimensionen ska användas när redovisningsdata (redovisning) importeras eller exporteras.

### <a name="audit-file-export-document-for-sie"></a>Export av verifieringsfil dokument för SIE

Sidan **Exportdokument för verifieringsfil** innehåller några fält som är specifika för SIE. Du måste ange dessa fält innan du börjar.

- På snabbfliken **SIE**, i fältet **filtyp** väljer du ett av följande värden för att ange typen av SIE-fil som ska skapas:

    - År – Slutsaldon
    - Periodiska saldon
    - Objektssaldon
    - Transaktioner

    Alla andra fält anges som standard baserat på den föregående inställningen.

## <a name="see-also"></a>Se även

[SIE-grupp](https://go.microsoft.com/fwlink/?LinkID=164870&clcid=0x41d)  
[Lokal funktionalitet för Sverige](sweden-local-functionality.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
