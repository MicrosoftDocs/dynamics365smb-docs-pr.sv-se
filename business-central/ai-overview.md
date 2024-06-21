---
title: Översikt över förslag på marknadsföringstext med Copilot
description: Få en översikt över funktionerna för att generera AI-innehåll i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 10/29/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---
# Översikt över förslag på marknadsföringstext med Copilot

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

I den här artikeln får du en översikt över den AI-drivna kapacitet som medföljer Copilot i Business Central.

## Vad är marknadsföringstext för AI-baserad artikel med Copilot

Copilot tillhandahåller AI-baserad skrivhjälp för Business Central-användare som ansvarar för att skapa marknadsföringstext (produktbeskrivningar) på varor som säljs i onlinebutiker, som Shopify. Med ett klick på en knapp genererar Copilot text som är engagerande, kreativ och framhäver nyckelattributen för det specifika föremålet. Efter granskning och redigering är det dags att publicera.

Copilot använder [Microsoft Azure OpenAI Service](/azure/cognitive-services/openai/overview) för att komma åt språkmodeller som känner igen, förutsäger och genererar text som är baserad på utbildade datauppsättningar.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Videon visar inte exakt hur funktionen fungerar eller hur produkten ser ut. Funktionen har ändrats sedan videon tillverkades. Men det ger en allmän uppfattning om funktionen och vad du kan använda den till.*
  
## Där den används

Copilot är tillgänglig på artikelkort i Business Central. I Business Central är artiklar som produkter i andra program och butiker. Varje artikel kan hanteras från ett kort där du anger information om artikeln, t.ex. dess dimensioner, kostnad eller bild. Det här kortet innehåller också en ruta där du kan lägga till marknadsföringstext. Den här marknadsföringstexten kan publiceras på din onlinebutik för att flytta upp objektet. Här kommer Copilot in. Genom att välja åtgärden **Utkast med Copilot** på artikelkortet kommer Copilot generera en intelligent utkasttext åt dig. När du får det första utkastet kan du köra Copilot igen tills du får ett utkast som du gillar. När du har ett förslag som du gillar granskar och redigerar du det för noggrannhet och sparar det sedan.

Om Business Central är konfigurerad för att ansluta till Shopify, kan du ta denna text ännu längre genom att publicera den med artikeln direkt till din butik genom att välja **Lägg till Shopify**.

## Varför och hur du använder den

Med AI-genererad text kan du snabbare förbättra produkternas tid-till-marknad i onlinebutiker genom att begränsa den tid som används vid copywriting. Några viktiga fördelar:

- Hjälper användare att lösa skrivarens blockering genom att komma igång med ett intelligent utkast.
- Låser upp kreativitet för att ge mer engagerande produktbeskrivningar.
- Förbättrar konsistensen av marknadsföringsinnehåll för produktlinjer.

Du bör betrakta den AI-genererade texten som en *endast förslag*. Förslag kan i vissa fall innehålla misstag och till och med olämplig text, så att mänsklig insyn och andra undersökningar krävs. Innan du gör texten tillgänglig för allmänheten måste du kontrollera att den är korrekt och göra lämpliga ändringar.

## Aktuella begränsningar

I det här avsnittet beskrivs de aktuella begränsningarna för AI-genererad text kapacitet från Copilot.

- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]
- Dåliga förslag kan uppstå när obestämd eller generiska produktnamn används och detaljer om en vara saknas, som nyckelattribut eller en kategori.
- Copilot stöds endast i Business Central Online. Inte privata molnmiljöer eller lokala Business Central-miljöer.
- Copilot stöds inte via anslutningar till din egen Azure OpenAI Service-resurs i din Azure-prenumeration.

<!-- Partner extensibility of the AI capability by using AL code isn't supported.-->

## Nästa steg

För att komma igång måste du ha en Business Central-miljö (v23.1 och senare) som aktiveras med Copilot.

- Om du är en befintlig Business Central-kund måste du som är Business Central-administratör konfigurera en miljö som är aktiverad för förslag på marknadsföringstext. Mer information finns i [Konfigurera Copilot- och AI-funktioner](enable-ai.md).

- Om du inte är en Business Central-kund, men vill prova kan du registrera dig för en kostnadsfri utvärderingsversion. Mer information finns i [Registrera dig för en kostnadsfri Dynamics 365 Business Central utvärderingsversion](trial-signup.md).

När du har en miljö eller ett spår som är klart går du till [Lägg till marknadsföringstext till objekt med Copilot](item-marketing-text.md).  

## Se även

[Konfigurera Copilot- och AI-funktioner](enable-ai.md)  
[Lägg till marknadsföringstext för artiklar med Copilot](item-marketing-text.md)  
[Frågor och svar om marknadsföringstext för artikel](faqs-marketing-text.md)  
[Komma i gång med Shopify-anslutningsprogrammet](shopify/get-started.md)  
