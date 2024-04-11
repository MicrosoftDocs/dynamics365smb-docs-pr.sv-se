---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

> [!IMPORTANT]
> När du ändrar när-händelsen för ett arbetsflödessteg ändras även då-svaren. Ibland kan då-svar från andra när-händelser hänvisa till dessa då-svar som nästa steg i arbetsflödet. När du har ändrat en när-händelse kontrollerar du att nästa steg för då-händelserna är korrekta.  
>
> Till exempel arbetsflödesmallen **Arbetsflöde för leverantörsgodkännande** har en primär när-händelse **Godkännande av en leverantör krävs**. Denna när-händelse har en funktion för att **Skicka godkännandebegäranden för posten och skapa ett meddelande** som andra då-svar refererar till. Om du ändrar den primära när-händelse till **Godkännande av en leverantör krävs** till exempel **En leverantörspost ändras**, rensas då-svaret tillsammans med referenserna.
>
> Då-svaren för **En begäran om godkännande är delegerad** och **En begäran om godkännande på nästa rad** (med **Vid villkor** för **Väntar på godkännanden >0**) när-händelser är exempel på situationer där att ändra en primär när-händelse kan leda till problem. Deras när-svar har sedan ett nästa steg som refererar till sedan-svaret **Skicka godkännandebegäranden för posten och skapa ett meddelande** för när-händelsen **Godkännande av en leverantör krävs**. Eftersom svaret för när-händelsen **Godkännande av en leverantör krävs** inte längre är tillgänglig, kommer de indragna när-händelserna inte att fungera som förväntat.
>
> Du måste ange nästa steg för svaren för då-händelser som hänvisade till den ändrade när-händelsen.