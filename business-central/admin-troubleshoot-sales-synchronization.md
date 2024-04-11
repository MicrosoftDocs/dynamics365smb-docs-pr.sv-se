---
title: Felsöka synkroniseringsfel
description: 'Det här avsnittet ger lite vägledning för att identifiera, felsöka och lösa synkroniseringsfel.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="troubleshoot-synchronization-errors"></a>Felsöka synkroniseringsfel


Det finns många rörliga delar som används för att integrera [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[prod_short](includes/cds_long_md.md)] och ibland kan det bli fel. I det här avsnittet beskrivs några vanliga fel som uppstår och du får tips om hur du åtgärdar dem.

Fel inträffar ofta antingen på grund av något som en användare har gjort i fråga om kopplade poster, eller också är något fel med hur integreringen har upprättats. För fel som rör kopplade poster kan användare matcha dem själva. Dessa fel orsakas av åtgärder som att ta bort data i en – men inte båda – affärsappar och sedan synkronisera. För mer information, se [Visa status för en synkronisering](admin-how-to-view-synchronization-status.md).

Fel som rör hur integreringen ställs in kräver vanligt vis en administratörs uppmärksamhet. Du kan visa dessa fel på sidan **Integreringssynkroniseringsfel**. 

Följande tabell innehåller exempel på vanliga problem:  

|Problem  |Upplösning  |
|---------|---------|
|Behörigheterna och rollerna som tilldelats integrationsanvändaren är inte korrekta. | Felet kommer från [!INCLUDE[prod_short](includes/cds_long_md.md)] och innehåller ofta följande text: huvudanvändare (Id=\<user id>, typ=8) saknar \<privilegeName> privilegium. Det här felet inträffar på grund av att integrationsanvändaren saknar ett privilegium som tillåter åtkomst till en entitet. Vanligtvis inträffar det här felet om du synkroniserar anpassade entiteter, eller om du har installerat en app [!INCLUDE[prod_short](includes/cds_long_md.md)] som kräver åtkomst till andra [!INCLUDE[prod_short](includes/cds_long_md.md)] entiteter. Lös problemet genom att tilldela behörigheten till integrationsanvändaren i [!INCLUDE[prod_short](includes/cds_long_md.md)].<br><br> Integrationsanvändarens namn finns på sidan **Dataverse anslutningsinställningar**. I felmeddelandet finns namnet på behörigheten, som kan hjälpa dig identifiera den entitet som du behöver behörighet till. Om du vill lägga till saknad behörighet loggar du in på [!INCLUDE[prod_short](includes/cds_long_md.md)] med ett administratörskonto och redigerar den säkerhetsroll som har tilldelats integrationsanvändaren. Mer information finns i avsnittet [Skapa eller redigera en säkerhetsroll för att hantera åtkomst](/power-platform/admin/create-edit-security-role). |
|Du kopplar en post som använder en annan post som inte är kopplad. Det kan till exempel vara en kund vars valuta inte är kopplad eller en artikel för vilken måttenheten inte är kopplad. | Du måste först koppla den beroende posten, t.ex. en valuta eller en måttenhet och sedan försöka göra om kopplingen. |

Nedan finns några verktyg på sidan för att integrera synkroniseringsfel som kan hjälpa dig att lösa problemen manuellt.  

* Fälten **Källa** och **Mål** kan innehålla länkar till den rad där felet hittades. Klicka på länken för att undersöka felet.  
* Åtgärderna **Ta bort transaktioner som är äldre än 7 dagar** och **Ta alla transaktioner** rensar listan. Vanligtvis använder du dessa åtgärder när du har löst orsaken till ett fel som påverkar många poster. Var försiktig. De här åtgärderna kan ta bort fel som fortfarande är relevanta.
* Åtgärden **Visa anropsstack för fel** visar information som kan hjälpa till att identifiera orsaken till felet. Om du inte själv kan lösa problemet själv och du bestämmer dig för att skicka in ett supportärende, ska du ta med informationen i supportärendet.

## <a name="see-also"></a>Se även
[Integrera med Microsoft Dataverse](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Ställa in konton för integrering med Microsoft Dataverse](admin-setting-up-integration-with-dynamics-sales.md)  
[Ställ in en anslutning till Microsoft Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Koppla och synkronisera poster manuellt](admin-how-to-couple-and-synchronize-records-manually.md)  
[Visa status för en synkronisering](admin-how-to-view-synchronization-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
