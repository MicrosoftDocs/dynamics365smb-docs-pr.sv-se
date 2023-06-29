---
title: Arbeta med återkommande intäkter
description: Lär dig mer om tillgängliga alternativ för att automatiskt skicka prenumerationsfakturor till dina kunder och registrera återkommande intäkter.
author: AndreiPanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'recurring, invoicing, subscription, billing'
ms.search.form: 283
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: andreipa
---
# <a name="work-with-recurring-revenue-in-"></a><a name="work-with-recurring-revenue-in-"></a>Arbeta med återkommande intäkter i [!INCLUDE[prod_short](includes/prod_short.md)]

Många företag flyttar från en affärsintäktsmodell där intäkter görs från en kunds engångsinköp till en abonnemangsmodell, där intäkter görs på återkommande basis i utbyte mot löpande tillgång till leverans av en vara eller tjänst.
[!INCLUDE[prod_short](includes/prod_short.md)] erbjuder följande alternativ för att automatisera det sätt på vilket du skickar prenumerationsfakturor till dina kunder och registrerar återkommande intäkter. 

## <a name="register-revenue-with-a-recurring-general-journal"></a><a name="register-revenue-with-a-recurring-general-journal"></a>Registrera intäkter med en återkommande redovisningsjournal

En återkommande journal är en redovisningsjournal med specifika fält för hantering av transaktioner som du ofta bokför med få eller inga ändringar, till exempel hyra, prenumerationer, el och värme. Med fälten för återkommande transaktioner kan du bokföra både fasta och rörliga belopp. Med en återkommande journal kommer transaktioner som ska bokföras regelbundet inte att behöva skrivas in mer än en gång. Det innebär att de konton, dimensioner och dimensionsvärden som du anger kommer att finnas kvar i journalen efter bokföring. Du kan göra eventuella justeringar i samband med varje bokföring.

### <a name="why-use-this-option"></a><a name="why-use-this-option"></a>Varför använda detta alternativ?

Med detta alternativ definierar du flexibla faktureringsperioder med [datumformler](ui-enter-date-ranges.md#use-date-formulas).

Med det här alternativet kan du emellertid inte skriva ut och skicka fakturor i standardversionen av [!INCLUDE[prod_short](includes/prod_short.md)].  

Mer information finns i [Arbeta med återkommande journaler](ui-work-general-journals.md#work-with-recurring-journals).  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a><a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a>Skapa flera fakturor baserat på en återkommande projektjournal

Den återkommande projektjournalen är ett mer avancerat alternativ till redovisningsjournalen. Du kan definiera artiklar, resurser och redovisningskonton som måste upprepas för respektive projekt, samt dessutom återkommandefrekvensen.  

När du har bokfört en återkommande projektjournal kan du skapa flera fakturor med uppgiften **Skapa försäljningsfaktura för projekt**. Du kan granska och bokföra skapade fakturor på sidan **Försäljningsfakturor**.

### <a name="why-use-this-option-1"></a><a name="why-use-this-option-1"></a>Varför använda detta alternativ?

Med det här alternativet följer du standardproceduren för fakturering med alla fördelar denna medför, inklusive standard- och kundlayouter för kommunikationsinställningar. Du kan också definiera priser individuellt för respektive projekt.

För varje ny kund måste du emellertid skapa ett nytt projekt och lägga till rader i den återkommande journalen. 

Mer information finns i [Skapa projektjournalrader](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) och [skapa flera försäljningsfakturor för projekt](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-invoices-based-on-recurring-sales-lines"></a>Skapa flera försäljningsfakturor utifrån återkommande försäljningsrader

Om du ofta behöver skapa försäljnings- och inköpsrader med liknande information, kan du skapa återkommande försäljningsrader som du sedan kan infoga i återkommande försäljnings- och inköpsdokument, till exempel för återkommande påfyllningsorder. Använd batch-jobbet **Skapa återkommande försäljningsfakturor** för att skapa försäljningsfakturor enligt återkommande försäljningsrader som tilldelats till kunderna samt med bokföringsdatum som infaller inom de giltighetsdatum som du anger på de åtekrommande försäljningsraderna.  

### <a name="why-use-this-option-2"></a><a name="why-use-this-option-2"></a>Varför använda detta alternativ?

Med det här alternativet kan du tilldela samma återkommande rader till flera kunder. Du kan ange giltighetsperioden för de återkommandeförsäljningsraderna för en specifik kund. Du kan tilldela flera återkommande rader till samma kund, och alla tas med i fakturan.

Det finns emellertid inget sätt att ställa in fasta priser för artiklar, detta eftersom [!INCLUDE[prod_short](includes/prod_short.md)] använder de faktiska priser och den rabatt som gäller på utfärdat dokumentdatum i syfte att hitta den bästa kombinationen som ger det lägsta priset.  

Mer information finns i [Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md).

## <a name="recurring-invoices-with-service-contract"></a><a name="recurring-invoices-with-service-contract"></a>Återkommande fakturor med servicekontrakt

Ett servicekontrakt innehåller serviceavtalen mellan kunderna och företaget. Ett servicekontrakt innehåller avtal om servicenivå och de serviceartiklar som du utför service på enligt kontraktet.  

Du kan ange kontraktets startdatum, fakturaperiod, huruvida kontraktet är förbetalt eller inte samt prisuppdateringsinformationom du tänker ändra priserna medan kontrakt är aktivt. Du kan använda både serviceartiklar eller artiklar på servicekontraktsraderna.
Du kan skapa kontraktsmallar för att definiera hur vissa typer av kontrakt ska skapas.  

### <a name="why-use-this-option-3"></a><a name="why-use-this-option-3"></a>Varför använda detta alternativ?

Med det här alternativet använder du en del av den avancerade servicehanteringsfunktionen som inte är begränsad till att utfärda återkommande fakturor, men som även stöder verkstads- och fältserviceåtgärder.

Detta alternativ kräver dock en Premium-licens. Att ställa in servicehantering och underhålla denna kanske inte ger enorma fördelar i enklare prenumerationsscenarier.  

Mer information finns i [Arbeta med servicekontrakt och servicekontraktsofferter](service-how-to-create-service-contracts-and-service-contract-quotes.md) och [Fakturera flera servicekontrakt](service-how-create-invoices.md#to-invoice-several-service-contracts).

## <a name="related-features"></a><a name="related-features"></a>Relaterade funktioner
Det finns flera relaterade funktioner i [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="blanket-sales-orders"></a><a name="blanket-sales-orders"></a>Avropsorder, försäljning

En avropsorder utgör ramen för en långsiktig överenskommelse mellan företaget och en kund.
En avropsorder skapas vanligtvis om en kund har lovat att köpa stora antal som ska levereras i flera mindre leveranser under en bestämd tidsperiod. Avropsorder gäller vanligtvis bara en artikel med förbestämda leveransdatum. Huvudanledningen till att en avropsorder används i stället för en försäljningsorder är att det antal som anges på en avropsorder inte påverkar artikeldispositionen – det kan emellertid användas i planeringssyfte.

#### <a name="why-use-this-option-4"></a><a name="why-use-this-option-4"></a>Varför använda detta alternativ?

Med det här alternativet använder du den förutsedda efterfrågan, varför informationen beaktas under de normala planeringsrutinerna. Mer information finns i [Begär prognoser och avropsorder](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Standardversionen erbjuder emellertid ingen färdig möjlighet att hantera flera avropsorder i bulk.

Mer information finns i [Arbeta med försäljningsavropsorder](sales-how-to-create-blanket-sales-orders.md).

### <a name="recurring-orders-norway"></a><a name="recurring-orders-norway"></a>Återkommande order (Norge)

Du kan använda återkommande order för att skapa mallar för avropsorder så att försäljningsorder kan skapas baserat på datumintervall som du definierar. Om du till exempel levererar samma försäljningsorder varannan vecka kan du använda en försäljningsavropsorder och skapa återkommande order.
Du kan använda återkommande grupper om du vill definiera ett intervall med parametrar som visar hur du skapar orderna. Dessa grupper tilldelas till avropsorder som måste skapas regelbundet. Om du vill skapa de återkommande orderna måste du regelbundet köra åtgärden Skapa återkommande order. 

#### <a name="why-use-this-option-5"></a><a name="why-use-this-option-5"></a>Varför använda detta alternativ?

Med det här alternativet kan du välja mellan fasta och bästa priser.

Detta är emellertid bara tillgängligt i Norge. Du kan definiera en giltighets period på den återkommande gruppnivån.

Mer information finns i [Återkommande order](LocalFunctionality/Norway/recurring-orders.md).

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a><a name="recurring-revenue-and-subscription-billing-by-other-providers"></a>Återkommande intäkter och abonnemangsfakturering från andra leverantörer

På [AppSource.microsoft.com](https://appsource.microsoft.com/) kan du hämta tillägg för Business Central. Några tillägg ges ut av Microsoft, och andra tillägg ges ut av andra företag. Listan över tillägg från andra företag växer varje månad. Se därför till att hålla utkik efter [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646) och skaffa appar som hjälper dig med ditt arbete i Business Central.  

## <a name="see-also"></a><a name="see-also"></a>Se även

[Datumformler](ui-enter-date-ranges.md#use-date-formulas)  
[Arbeta med återkommande journaler](ui-work-general-journals.md#work-with-recurring-journals)  
[Skapa projektjournalrader](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Skapa flera projektförsäljningsfakturor](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Skapa återkommande försäljnings- och inköpsrader](sales-how-work-standard-lines.md)  
[Så här arbetar du med servicekontrakt och servicekontraktsofferter](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Fakturera flera servicekontrakt](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Efterfrågeprognoser och avropsorder](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Arbeta med försäljningsavropsorder](sales-how-to-create-blanket-sales-orders.md)  
[Återkommande order (Norge)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
