---
title: Konfigurera marknadsföringstext för AI-baserad artikel (förhandsversion) med Copilot
description: I den här artikeln beskrivs hur du skaffar en Copilot testversion av Business Central och aktiverar Copilot för en miljö.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Konfigurera marknadsföringstext för AI-baserad artikel (förhandsversion) med Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

I den här artikeln beskrivs hur du kan styra möjligheten att skapa marknadsföringstext för AI-baserad artikel med Copilot för organisationen. Den här uppgiften utförs av en administratör. Det finns två krav som du måste uppfylla för att funktionen ska vara tillgänglig för användare:

- Aktivera funktionen **Skapa AI-baserade produktbeskrivningar med Copilot**.
- Samtycke till villkoren för [förhandsversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) och [Microsoft sekretesspolicy](https://go.microsoft.com/fwlink/?LinkId=521839) för organisationens räkning.

Om något av dessa krav inte uppfylls kan funktionen inte användas.

## Förutsättningar

Du använder en [förhandsversion](ai-preview-getstarted.md) av Business Central som har aktiverats för Copilot. Att aktivera Copilot utförs av en administratör. Om du vill ha mer information går du till [Konfigurera marknadsföringstext för AI-baserad artikel med Copilot](enable-ai.md).

## Aktivera eller inaktivera funktionen Skapa AI-baserade produktbeskrivningar med Copilot

1. I Business Central söker du efter och öppnar sidan **Funktionshantering**.
2. Ange kolumnen **Aktiverad för** för **Funktion i förhandsversion: Skapa AI-baserade produktbeskrivningar med Copilot** till **Alla användare** för att aktivera funktionen eller **ingen** för att inaktivera den.

   Mer information om funktionshantering i allmänhet finns i [Funktionshantering](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Samtycke till eller avvisa förhandsgranskning och sekretessvillkor för alla användare

1. I Business Central, sök efter och öppna sidan **Status för sekretessmeddelanden**.
2. I kolumnen **Integrationsnamn**, välj **Azure OpenAI**, läs sedan villkoren som presenteras för dig.
3. I raden **Azure OpenAI**, markera kryssrutan **Acceptera för alla** för att samtycka till **Acceptera inte för alla** för att avvisa.

## Nästa steg

När du har aktiverat om godkänt funktionen kan du testa Copilot för artiklar i Business Central. Gå till [Lägg till marknadsföringstext för artiklar](item-marketing-text.md).  

## Se även

[Översikt över marknadsföringstext för AI-baserad artikel med Copilot](ai-overview.md)  
[Skapa marknadsföringstext för artiklar som använder Copilot](item-marketing-text.md)  
[Marknadsföringstext för AI-baserad artikel med vanliga frågor om Copilot](ai-faq.md)  
