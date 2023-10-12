---
author: brentholtorf
ms.topic: include
ms.date: 01/01/2023
ms.author: bholtorf
---

Fälten **Dokumentdatum** och **Bokföringsdatum** i försäljnings- och inköpsdokument kan hjälpa dig uppfylla redovisningsstandarder och säkerställa korrekta ekonomiska beräkningar. Fälten har olika syften:

- För att [!INCLUDE [prod_short](prod_short.md)] ska kunna beräkna dröjsmålsränta och belopp på fakturor korrekt måste **Dokumentdatum** överensstämma med något av följande datum:

   - Datumet på den försäljningsfaktura som du skickar till kunden. 
   - Datumet på den inköpsfaktura som du fick från leverantören.
- **Bokföringsdatumet** anger när ett dokument registrerades i [!INCLUDE [prod_short](prod_short.md)]. Många redovisningsstandarder och föreskrifter kräver att företag registrerar och rapporterar finansiella transaktioner baserat på det datum då de inträffade.

Beroende på dina affärsprocesser kan dessa datum vara identiska eller inte. Om de är identiska kan du konfigurera [!INCLUDE [prod_short](prod_short.md)] i syfte att uppdatera dokumentdatumet på försäljnings- och inköpsdokument med det datum då du bokförde dem.  
  
Om du automatiskt vill ange dokumentdatum till bokföringsdatum aktiverar du växlingsknappen **Länka dokumentdatum till bokföringsdatum** på sidorna **Försäljningsinställningar** och **Inställningar för inköp & leverantör**.

> [!NOTE]
> Inställningen påverkar inte försäljnings- eller inköpsjournaler.