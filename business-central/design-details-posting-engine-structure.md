---
title: Designdetaljer – Bokföringsmotorstruktur
description: Bokföringsgränssnittet använder funktioner för bokföringsmotorn i kodmodul 12 använder funktioner i bokföringsmotorn för att förbereda och infoga redovisningstransaktioner och momstransaktionsposter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designdetaljer: Bokföringsmotorstruktur
Bokföringsgränssnittet och vissa andra funktioner i kodmodul 12 använder funktioner i bokföringsmotorn för att förbereda och infoga redovisningstransaktioner och momstransaktionsposter. Bokföringsmotorn är också ansvarig för att skapa en registrering av redovisningen.  
  
 Funktionerna i följande tabell tillhandahåller ett standardramverk för att utforma bokföringsprocedurer (t. ex. Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry och Reverse) samt exklusiv åtkomst till tabell 17, redovisningstransaktion.  
  
|Routine|Description|  
|-------------|---------------------------------------|  
|StartPosting|initialiserar bokföringsbufferten TempGLEntryBuf, låser redovisningstransaktions- och momstransaktionstabellerna och initialiserar bokföringsperiod, bokförd redovisningsjournal och valutakurser. Bör bara anropas en gång, sedan är NextEntryNo 0.|  
|ContinuePosting|Kontrollerar och bokför orealiserad moms för föregående transaktion, ökar NextTransactionNo och förbereder bokföringen av nästa rad.|  
|FinishPosting|Slutför bokföringen genom att infoga redovisningstransaktioner från den tillfälliga bufferten i databastabellen. Används alltid tillsammans med StartPosting. Söker efter inkonsekvenser.|  
|InitGLEntry|Används för att initialisera en ny redovisningstransaktion för standardredovisningsjournalrad. Returnerar GLEntry som parameter.|  
|InitGLEntryVAT|Samma som InitGLEntry men tilldelar också Motkonto och SummarizeVAT.|  
|InitGLEntryVATCopy|Samma som InitGLEntryVAT men kopierar också bokföringsmalldata från momstransaktionen innan SummarizeVAT.|  
|InsertGLEntry|Den enda funktion som infogar redovisningstransaktionen i den globala TempGLEntryBuf-tabellen. Använd alltid den här funktionen för att infoga.|  
|CreateGLEntry|Utför InitGLEntry, tilldelar alt. valutabelopp och utför sedan InsertGLEntry. Ersätter flera rader av kod med ett enda funktionsanrop.|  
|CreateGLEntryBalAcc|Samma som CreateGLEntry men tilldelar också Motkontotyp och Motkonto.|  
|CreateGLEntryVAT|Samma som CreateGLEntry men med ytterligare bearbetning för bokföringsmallar och lagring i en tillfällig momsbuffert:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Samma som CreateGLEntry men med ytterligare insamling av justeringar och lagring i en tillfällig momsbuffert:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Samma som CreateGLEntry men kopierar även bokföringsmallar från momstransaktion.|  
  
## Se även  
 [Designdetaljer: Bokföringsgränssnittsstruktur](design-details-posting-interface-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]