---
author: brentholtorf
ms.topic: include
ms.date: 05/27/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

I försäljningsdokument och journaler kan du ange ett dokumentnummer som refererar till kundens nummersystem. <!--You can enter a maximum of ten characters, both numbers and letters.--> Använd det här fältet för att registrera numret som kunden har tilldelat ordern, fakturan eller kreditnotan. Sedan kan du använda numret om du av någon anledning behöver söka efter den bokförda posten med hjälp av detta nummer.  

Fältet **Ext. Dok.nr obligatoriskt** på sidan **Konfiguration av försäljning och kundreskontra** anger om det är obligatoriskt att ange ett externt dokumentnummer i fältet **Externt dokumentnr** i ett försäljningshuvud och fältet **Externt dokumentnr** på en redovisningsjournalrad.

Om du markerar det här fältet kommer det inte att vara möjligt att bokföra en faktura eller en redovisningsjournalrad utan ett externt verifikationsnummer.

Det externa dokumentnumret inkluderas i de bokförda dokumenten där du kan söka på det aktuella numret. Du kan även söka med hjälp av det externa dokumentnumret när du navigerar i kundreskontratransaktioner.

Olika sätt att hantera externa dokumentnummer är att använda fältet **Din referens**. Om du använder fältet **Din referens** inkluderas numret i bokförda dokument, och du kan söka efter det på samma sätt som för värden från fälten **Externt dokumentnr**. Fältet är dock inte tillgängligt på journalrader.
