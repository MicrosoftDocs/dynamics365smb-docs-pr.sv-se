---
title: Skapa kontaktpersoner | Microsoft Docs
description: "Beskriver uppgiften om du vill skapa ett kontaktkort för en person, t.ex. en potentiell kund eller leverantör som bidrar till att definiera relationen och skräddarsy kommunikationen."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 80ab4bd8fe9a5c74f52a334cf8c4a0a297c01bd9
ms.contentlocale: sv-se
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-persons"></a>Skapa kontaktpersoner
Du skapar en kontakt genom att skapa ett kontaktkort för personen. Du kan skapa kontaktpersoner utifrån befintliga kontaktföretag eller skapa oberoende kontaktpersoner.

När du till exempel har träffat ett prospektföretag, träffar du deras inköpare. Du skapar då ett kontaktkort för den här personen så att kommunikationen kan skräddarsys.

Du kanske också behöver få några publikationer om produkterna översatta och efter en del efterforskningar bestämmer dig för att anlita en frilansöversättare. Du registrerar då den här kontakten som en oberoende kontaktperson.

Om du registrerar så många uppgifter som möjligt om en kontaktperson kan alla grupper i företaget hitta relevant information.

Du kan skapa kontaktkort för varje kontakt som arbetar i de företag du har förbindelse med. För varje kontaktföretag kan du ange valfritt antal kontaktpersoner. Du kan också skapa kontaktkort för de personer du vill registrera som oberoende.

> [!TIP]  
>   Innan du skapar en kontakt kan du kontrollera inställningarna av **Arv** på sidan **Affärsstödsinställning**. Inställning av arv tillåter information om kontaktföretag som är vanliga för kontaktpersoner, som till exempel adressinformation, som automatiskt ska kopieras från kontaktföretaget till kontaktpersonen varje gång du skapar en kontaktperson för ett registrerat kontaktföretag.

## <a name="to-create-a-contact-card-for-a-person"></a>Så här skapar du ett kontaktkort för en person
1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra") och ange **Kontakter** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. I fältet **Nr.** anger du ett nummer för kontakten.

    Om du har definierat en nummerserie för kontakter på sidan **Affärsstödsinställning** kan du i stället trycka på Retur så anges nästa tillgängliga kontaktnummer automatiskt. Mer information finns i [Skapa nummerserier](ui-create-number-series.md).
4. I fältet för **Typ**, välj **Person**.
5. Fyll i övriga fält på kontaktkortet.

> [!NOTE]  
>   Innehållet i de fält du markerat i avsnittet **Arv** på sidan **Marknadsföringsinställningar** kopieras från företaget till personerna i företaget.

## <a name="see-also"></a>Se även
[Skapa kontaktföretag](marketing-create-contact-companies.md)  
[Skapa kontaktpersoner](marketing-create-contact-persons.md)  
[Använda profilfrågeformulär för att klassificera affärskontakter](marketing-create-contact-profile-questionnaire.md)  
[Arbeta med Business Central](ui-work-product.md)

