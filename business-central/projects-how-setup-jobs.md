---
title: 'Ställ in projekt, priser och projektbokföringsmallar'
description: Beskriver hur du ställer in allmän information om projekt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
ms.service: dynamics-365-business-central
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Ställ in projekt, priser och projektbokföringsmallar

Som projektledare kan du skapa jobb som definierar alla projekt som du hanterar i [!INCLUDE[prod_short](includes/prod_short.md)].  Använd sidan **Projektinställning** för att definiera hur du ska använda projektfunktioner.

Ange olika uppgifter för varje projekt:

* Priser för projektartiklar
* Projektresurser
* Redovisningskonton för projekt
* Projektbokföringsmallar (krävs)

## <a name="to-set-general-information-for-jobs"></a>Så här anger du allmän information för projekt

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projektinställningar** och väljer sedan relaterad länk.
2. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Växlingsknappen **Tillämpa användningslänk som standard** på sidan **Projektinställningar** indikerar om projekttransaktioner är länkade till projektplaneringsrader som standard. Aktivera växlingknappen så att den här inställningen tillämpas på alla nya projekt. Du kan aktivera eller inaktivera spårning av projektförbrukning för ett visst projekt genom att aktivera eller inaktivera växlingsknappen **Använd förbrukningslänk** på sidan **Projektkort**.

### <a name="to-set-up-job-usage-tracking"></a>Så här anger du projektförbrukningsspårning

När du arbetar på ett projekt kan det hända att du vill veta hur förbrukningen spåras mot din plan. För att utforska användning kan du skapa en koppling mellan dina projektplaneringsrader och den faktiska förbrukningen. Med länken kan du hålla reda på kostnaderna och förstå hur mycket arbete som återstår. Som standard är projektplaneringsradtypen **Budget**, men radtypen **Både Budget och Fakturerbart** har liknande effekter.

När du har ställt in användningsspårning genom att aktivera växlingsknappen **Använd förbrukningslänk som standard** kan du granska informationen på projektplaneringsraden. Du kan till exempel ange antalet för resursen, artikeln eller redovisningskontot. Du kan också ange antalet att överföra till projektjournalen. Fältet **Återstående antal** på projektplaneringsraden visar vad som återstår att överföra och bokföra till projektjournalen.

>[!NOTE]
> Om **Använd förbrukningslänk** har valts för projektet och fältet **Radtyp** på projektjournalraden eller inköpsraden är **Fakturerbar**, skapas nya projektplaneringsrader av radtypen **Både Budget och Fakturerbart** när du bokför projektjournal eller inköpsdokument.  
>
> Mer information finns i [Registrera förbrukning för projekt](projects-how-record-job-usage.md) och [Hantera projektleveranser](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Om du inte anger ett värde i fältet **Radtyp** på projektjournalraden eller inköpsraden skapas inga projektplaneringsrader när du bokför projekt journalen eller inköpsdokumentet.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>För att skapa priser för resurser, artiklar och redovisningskonton för jobb

> [!NOTE]
> I 2020 års utgivningscykel 2 släppte vi nya processer för att ställa in och hantera priser och rabatter. Om du är en ny kund använder du den nya upplevelsen. Om du är en befintlig kund vilar din användning av den nya versionen på om administratören har aktiverat funktionsuppdateringen **Ny försäljningsprisupplevelse** i **Funktionshantering**. Mer information finns i [Aktivera kommande funktioner i förväg](/dynamics365/business-central/dev-itpro/administration/feature-management).

Du kan skap priser för resurser, artiklar och redovisningskonton relaterade till ett jobb. 

#### [Aktuell upplevelse](#tab/current-experience)

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj jobbet och sedan åtgärden **Resurs**, **Artikel** eller **Redovisningskonto**.
3. På sidorna fyller du i **Priser för jobbresurser**, **Priser för jobbartiklar** eller **Priser för jobbredovisningskonto** efter behov.

När du väljer en resurs, en artikel eller ett redovisningskonto för ett projekt använder [!INCLUDE [prod_short](includes/prod_short.md)] informationen i de valfria fälten på projektplaneringsrader och projektjournaler. I tabellen nedan beskrivs hur du gör.

|Kolumn1  |Kolumn2  |
|---------|---------|
|**Projektresurser**|Fälten **Projektuppgiftsnr.**, **Arbetstyp**, **Valutakod**, **Radrabatt %** och **Styckkostnadsfaktor**. Värdet i fältet **Enhetspris** för resursen kommer att användas i projektjournalerna och projektets planeringsrader när du anger en resurs eller om en resurs tilldelas till resursgruppen. Det här priset åsidosätter de priser som anges på sidan **Resurspris/Resursgruppriser**.|
|**Projektartiklar**|Fälten **Projektaktivitetsnr**, **Valutakod** och **Radrabatt %**. Värdet i fältet **Enhetspris** för artikeln kommer att användas i projektplaneringsraderna och projektjournalerna när den här artikeln anges. Det här priset åsidosätter det vanliga kundpriset (bästa pris-mekanismen) för artiklar. Om du vill använda det vanliga kundpriset anger du inte artikelpriser för projektet.|
|**Redovisningskonton**|Den valfria informationen i fälten **Projektaktivitetsnr.**, **Valutakod**, **Radrabatt %**, **Styckkostnadsfaktor** och **Styckkostnad** kommer att användas i projektplaneringsrader och projektjournaler när detta redovisningskonto anges och läggs till i ett projekt. När du väljer ett huvudbokskonto använder projektplaneringsrader och projektjournaler värdet i fältet **Enhetspris** för projektkostnaden för redovisningskontot.|

#### [Ny upplevelse](#tab/new-experience)

1. Välj ![glödlampan som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Projekt** och väljer sedan relaterad länk.  
2. Välj relevant projekt och sedan åtgärden **Försäljningsprislistor**.

---

## <a name="to-set-up-job-posting-groups"></a>Så här lägger du upp projektbokföringsmallar

En aspekt av att planera projektet är att bestämma vilka bokföringskonton som ska användas för projektvärdering. Om du vill kunna bokföra projekt måste du lägga upp bokföringskonton för varje projektbokföringsmall. En bokföringsmall representerar en länk mellan projektet och hur det ska hanteras i redovisningen. När du skapar ett projekt anger du en bokföringsmall och, som standard, kopplar du varje aktivitet som du skapar för projektet till den här bokföringsmallen. Men medan du skapar aktiviteter kan du välja att åsidosätta standarden och välja en annan, mer lämplig, bokföringsmall.  

> [!NOTE]  
> Du måste ställa in konton måste registreras innan du registrerar bokföringsmallar. Mer information finns i [Ställa in eller ändra kontoplanen](finance-setup-chart-accounts.md).  

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **projektbokföringsmallar** och väljer sedan relaterad länk.  
2. Välj åtgärden **Ny** och fyll sedan i fälten enligt instruktionerna i följande tabell.  

| Kontofält | Description | Används i PIA-typ |
| --- | --- |  --- |
| **Kod** |En identifierare för bokföringsmallen. Du kan ange upp till 10 tecken inklusive blanksteg. | |
| **Konto för PIA-kostnader** |PIA-kontot för den beräknade kostnaden för projektets PIA, vilket är ett konto för anläggningstillgångar i balansräkningen. | Tillämpad kostnad, bokförda kostnader|
| **Konto för upplupna PIA-kostnader** |Ett konto för kostnadsvärdet eller kostnad för försäljningsmetod för PIA-beräkning. Detta konto är för upplupna kostnader i din balansräkning. När en PIA-justering kräver att du ökar de användningskostnader som du bokför till din resultaträkning bokför du på detta konto. | Upplupna kostnader|
| **Konto för kopplade projektkostnader** |Ett balanskonto för PIA-kostnadskontot, som är ett motkonto för ett negativt kostnadskonto. Används när **PIA-bokföringsmetod som används** är *Projekt*. | Tillämpade kostnader, bokförda kostnader|
| **Konto för kopplade artikelkostnader** |Samma som  **Konto för kopplade projektkostnader**, men används när **Använd bokföringsmetod för PIA** anges till *Projekttransaktion*.| |
| **Konto för kopplade resurskostnader** |Samma som  **Konto för kopplade projektkostnader**, men används när **Använd bokföringsmetod för PIA** anges till *Projekttransaktion*.| |
| **Konto för kopplade redovisningskostnader** |Samma som  **Konto för kopplade projektkostnader**, men används när **Använd bokföringsmetod för PIA** anges till *Projekttransaktion*.| |
| **Konto för projektkostnadsjustering** |Balanskontot för kontot för upplupna PIA-kostnader, som är ett kostnadskonto. | Upplupna kostnader|
| **Konto för redovisningskostnader (budget)** |Försäljningskontot som ska användas för redovisningskostnader i projektaktiviteter med den här bokföringsmallen. Om fältet lämnas tomt kommer det redovisningskonto som har angetts på projektplaneringsraden att användas. | |
| **Konto för upplupen PIA-försäljning** |PIA-kontot för det beräknade försäljningsvärdet för PIA, vilket är ett konto för upplupen intäkt i balansräkningen. När en PIA-justering kräver att du ökar den redovisade intäkten bokför du på detta konto. | Upplupen försäljning, Bokförd försäljning|
| **Konto för fakturerad PIA-försäljning** |Kontot för värdet för fakturerad PIA-försäljning som inte kan bokföras. Det är ett konto för förutbetald intäkt i balansräkningen. | Bokförd försäljning, upplupen försäljning|
| **Konto för kopplad projektförsäljning** |Balanskontot för kontot för fakturerad PIA-försäljning, vilket är ett motkonto för inkomst. | Bokförd försäljning, upplupen försäljning|
| **Konto för projektförsäljningsjustering** |Balanskontot för PIA-projektförsäljningskontot, som är ett inkomstkonto. | Upplupen försäljning|
| **Konto för bokförda kostnader** |Det kostnadskonto som innehåller bokförda kostnader för projektet. Kontot är vanligtvis ett debetkonto för kostnader. | Bokförda kostnader|
| **Konto för bokförd försäljning** |Inkomstkontot som innehåller den bokförda inkomsten för projektet. Kontot är vanligtvis ett kreditkonto för inkomst. | Bokförd försäljning|

## <a name="see-also"></a>Se även

[Konfigurera projekthantering](projects-setup-projects.md)  
[Video: Hur du skapar du ett projekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Hantera projekt](projects-manage-projects.md)  
[Ekonomi](finance.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
