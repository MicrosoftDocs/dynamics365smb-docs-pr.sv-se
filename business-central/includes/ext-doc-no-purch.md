---
author: brentholtorf
ms.topic: include
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

I inköpsdokument och journaler kan du ange ett dokumentnummer som refererar till leverantörens nummersystem. Använd det här fältet för att registrera numret som leverantören har tilldelat ordern, fakturan eller kreditnotan. Sedan kan du använda numret om du av någon anledning behöver söka efter den bokförda posten med hjälp av detta nummer.

Fältet **Ext. Dok.nr obligatoriskt** på sidan **Konfiguration av inköp och leverantörsreskontra** anger om det är obligatoriskt att ange ett externt dokumentnummer i följande situationer:

* I fältet **Leverantörens fakturanr**, fältet **Leverantörens ordernr** eller fältet **Leverantörens kreditnotanr** i ett inköpshuvud

* I fältet **Externt dokumentnr** på en redovisningsjournalrad, där fältet **Dokumenttyp** är inställt på *Faktura*, *Kreditnota* eller *Räntefaktura* och fältet **Kontotyp** är inställt på *Leverantör*.

Om du markerar det här fältet kommer det inte att vara möjligt att bokföra en faktura, en kreditnota eller den typ av journalrad som beskrivits ovan utan ett externt dokumentnummer.

Det externa dokumentnumret inkluderas i de bokförda dokumenten där du kan söka på det aktuella numret. Du kan även söka med hjälp av det externa dokumentnumret när du navigerar i leverantörsreskontratransaktioner.

Olika sätt att hantera externa dokumentnummer är att använda fältet **Din referens**. Om du använder fältet **Din referens** inkluderas numret i bokförda dokument, och du kan söka efter det på samma sätt som för värden från fälten **Externt dokumentnr**. Fältet är dock inte tillgängligt på journalrader.
