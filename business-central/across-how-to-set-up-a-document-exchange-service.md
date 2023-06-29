---
title: Så här konfigurerar du en dokumentväxlingstjänst | Microsoft Docs
description: Du kan använda en tjänstleverantör för att utbyta elektroniska dokument med dina handelspartner.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="set-up-a-document-exchange-service"></a><a name="set-up-a-document-exchange-service"></a>Konfigurera en tjänst för dokumentutbyte

Som en del av Ramverk för dataintegration kan du utbyta försäljnings- och inköpsdokument med dina handelspartner utan extra instruktioner, till exempel bifoga dokumenten till e-postmeddelanden som PDF-filer. När du är klar att fakturera en kund kan du t.ex. bokföra fakturan och skicka den som en fil som kan tas emot av en kund i ett företagshanteringsprogram. Mer information finns i [Utbyta data elektroniskt](across-data-exchange.md).

> [!NOTE]
> Om du ställer in en dokumentväxlingstjänst för Business Central lokal krävs ytterligare steg för auktoriseringen. Mer information finns i [Konfigurera Business Central lokalt](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a><a name="connecting-with-trading-partners"></a>Ansluta till handelspartner

Utbyte av elektroniska dokument kräver en anslutning till dina handelspartner. För att det ska bli enklare att skapa en säker anslutning [!INCLUDE[prod_short](includes/prod_short.md)] online har konfigurerats för att använda appen Business Central-integrering. Appen finns tillgänglig i Tradeshift App Store och allt du och dina affärspartner måste göra är att skapa ett Tradeshift-konto och sedan aktivera programmet. Appen Business Central-integrering levereras i produktions- och miljö för begränsat läge-versioner. Du kan till exempel använda miljö för begränsat läge-versionen för att testa dokumentutbytet. Du kan växla mellan produktions- och begränsat läge-versioner genom att aktivera eller inaktivera växlingen i **begränsat läge** på sidan **Inställningar för dokumentöverföring**. När du gör det uppdateras informationen på snabbfliken **service** för dig.

Om du vill använda en annan tjänst måste du också ange information för att kunna upprätta anslutningen. Mer information finns i [Så här ansluter du till en dokumentväxlingstjänst](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a><a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Så här ansluter du till programmet Business Central-integration på Tradeshift

Du kan snabbt skapa ett Tradeshift-konto och komma igång med appen Business Central-integration från sidan **Inställningar för dokumentöverföring**. Välj antingen länken **Aktivera app** i meddelandet eller i fältet **App-URL** för att gå till appen i Tradeshift App Store. På inloggningssidan för Tradeshift kan du antingen logga in eller registrera dig.

> [!NOTE]
> När du har loggat in på ditt Tradeshift-konto kanske webbplatsen inte leder till sidan där du aktiverar appen. Det gör du genom att klicka på länken på sidan **Inställningar för dokumentöverföring** i Business Central igen och gå direkt till appen.

Om du väljer att sluta använda appen Business Central-integration bör du inaktivera den i Tradeshift App Store. 

## <a name="to-connect-to-a-document-exchange-service"></a><a name="to-connect-to-a-document-exchange-service"></a>Så här ansluter du till en dokumentväxlingstjänst

Om du hellre vill använda en annan dokumentväxlingstjänst måste du ange en del information för att kunna ansluta till tjänsten.

1. Välj ikonen ![Glödlampa som öppnar funktionen Berätta](media/ui-search/search_small.png "Berätta vad du vill göra"), ange **Inställningar för dokumentväxlingstjänst** och välj sedan tillhörande länk.  
2. Fyll i fälten enligt beskrivningen i följande tabell.  

    |Fält|Beskrivning|  
    |---------------------------------|---------------------------------------|  
    |**Användare**|Ange text som kan användas för att identifiera ditt företag i dokumentväxlingsprocesser.|  
    |**Aktiv**|Ange om anslutningen till tjänsten är aktiverad.<br><br> **Obs!** När du aktiverar tjänsten skapas minst två jobbköposter för att skicka och ta emot elektroniska dokument. När du inaktiverar servicen tas jobbköposterna bort.|  
    |**Sandbox-miljö**|Ange om du vill ansluta till en sandbox-version av dokumentväxlingstjänst.|
    |**URL för registrering**|Ange webbsidan där du registrerade dig för dokumentväxlingstjänsten.|  
    |**App-URL**|Välj länken för att öppna App Store och aktivera eller inaktivera appen Business Central-integrering.|
    |**Servicesida**|Ange adressen till dokumentväxlingstjänsten som ska anropas när du skickar och tar emot elektroniska dokument.|  
    |**Inloggnings-URL**|Ange webbadressen för sidan du använder för att logga in på dokumentväxlingstjänsten. Det här är sidan där du anger ditt företags användarnamn och lösenord.|  
    
    > [!NOTE]  
    > Din inloggningsinformation krypteras automatiskt. Du kan stänga av kryptering.

    > [!NOTE]
    > Om du inte kan ansluta till dokumentväxlingstjänst på grund av ett auktoriseringsfel kan det bero på att [!INCLUDE[prod_short](includes/prod_short.md)] inte kan förnya åtkomsttoken automatiskt. Detta kan till exempel inträffa om du inte har använt servicen under en viss tid. Du kan förnya token manuellt med hjälp av åtgärden **förnya token**.

## <a name="settings-for-business-central-on-premises"></a><a name="settings-for-business-central-on-premises"></a>Inställningar för Business Central lokalt

Om du vill ansluta Business Central lokalt måste du skapa en app i Tradeshift App Store. När du gör det använder du omdirigerings-URL från fältet **omdirigerings-URL** på sidan **Inställningar för dokumentväxlingstjänst**. När du har registrerat din app kommer Tradeshift att tillhandahålla ett klient-ID och en klienthemlighet. I [!INCLUDE[prod_short](includes/prod_short.md)] anger du dessa värden på snabbfliken **auktorisering** på sidan **Inställningar för dokumentväxlingstjänst**.

Om du hellre vill lagra program-ID och hemlighet på en annan plats kan du lämna fälten klient-ID och klienthemlighet tomma och skriva ett tillägg för att hämta ID och hemlighet från platsen. Du kan tillhandahålla hemligheten vid körning genom att prenumerera på händelserna OnGetClientId och OnGetClientSecret i codeunit 1410 "Inställningar för dokumentöverföring."

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relaterad [Microsoft utbildning](/training/modules/electronic-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se även

[Konfigurera dataintegration](across-set-up-data-exchange.md)  
[Utbyta data elektroniskt](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
