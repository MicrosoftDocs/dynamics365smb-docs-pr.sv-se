---
author: brentholtorf
ms.topic: include
ms.date: 09/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Öka effektiviteten på ditt distributionslager genom korrekt realtidsinformation om faktorer som kan påverka tillgängliga kvantiteter. Till exempel: 

* Lagernivåer
* Platser
* Bearbetningsstadier
* Objekt i karantän
* Reservationer

Du kan komma åt information om artikeltillgänglighet från följande källdokument:

* Försäljningsorder
* Produktionsorder
* Monteringsorder
* Projekt

Informationen tar även hänsyn till andra faktorer som påverkar tillgängligheten. Till exempel dedikerade lagerplatser, låsta lagerplatser och artiklar som inte är tillgängliga för plockning. Artiklar kan till exempel vara reserverade eller pågående artikelinförsel- eller utleveransåtgärder. På sidan **Plocksammanfattning** kan du granska artiklar som [!INCLUDE [prod_short](prod_short.md)] inte inkluderade i plockningsdokument och vidta nödvändiga åtgärder.

> [!NOTE]
> Denna funktion kräver att du aktiverar växlingsknappen **Dirigerad artikelinförsel och plockning** för de platser som du använder i plockningsprocessen.

### <a name="set-up-previews"></a>Konfigurera förhandsversioner

Om du vill ha information om vad som plockas och vad som inte plockas aktiverar du växlingsknappen **Visa sammanfattning (dirigerad artikelinförsel och plockning)** på sida **Dist.lagerkälla – Skapa dokument** eller **Dist.-leverans – Skapa plockning**.

### <a name="determine-the-quantity-you-can-pick"></a>Bestäm hur mycket du kan plocka

På raderna på sidan **Skapa plockningssammanfattning** visar fältet **Ant. att hantera (bas)** vilka och hur många artiklar som [!INCLUDE [prod_short](prod_short.md)] försökte plocka. I faktaboxen **Sammanfattning** finns mer information.

För enkla undersökningar kanske **Plockbart ant.** kan ge dig tillräckligt med information. Fältet visar hur många artiklar som finns tillgängliga. Om det plockbara antalet är mindre än förväntat undersöker du lagerplatsinnehållet.

**Plockbart ant.** är den högsta kvantitet som [!INCLUDE [prod_short](prod_short.md)] kan implementera vid plockning. Denna kvantitet består av artiklar på plockbara lagerplatser. Kvantiteten exkluderar kvantiteter som finns på spärrade eller dedikerade lagerplatser, eller artiklar som plockas i plockningsdokument för distributionslager. Om artikeln som du vill plocka kräver artikelspårning inkluderas inte spärrade parti- eller serienummer som lagras på plockbara lagerplatser i det plockbara antalet.

Om det plockbara antalet skiljer sig från antalet på plockbara lagerplatser kan ett problem ha uppstått. Utforska lagerplatsinnehållet för att hitta blockerade lagerplatser eller kvantiteter i aktiva dokument.

I fältet **Antal i distributionslager** visas den totala kvantitet som finns i distributionslagret om du utför en inventering. Du kan öka detaljnivån till lagertransaktionerna från det här fältet. Om fältet visar en kvantitet som är mindre än kvantiteten i **Antal på plockbara lagerplatser** uppstår en avvikelse mellan lagerställe- och lagerkvantiteter. I så fall använder du åtgärden **Beräkna lagerjustering** på sidan **Artikeljournal** och skapar sedan distributionslagerplockningen igen.

Följande bild illustrerar den maximala kvantitet som beaktas för plockning.

:::image type="content" source="../media/pickable-qty.png" alt-text="Maximal kvantitet som beaktas för plockning.":::

**Förklaring**

|Bokstav  |Beskrivning  |
|---------|---------|
|P     |Lagerplatser med innehåll av typen Plocka         |
|D     |Lagerplatser med innehåll av typen Plocka markerade som dedikerade lagerplatser        |
|A     |Lagerplatser med innehåll av typen Plocka i de aktiva dokumenten (som en annan plockning)       |
|D     |Lagerplatser med innehåll av typen Plocka med objekt med spärrad spårning         |
|B     |Lagerplatser med innehåll av typen Plocka med spärrad avgående transport         |
|O     |Andra lagerplatser         |

### <a name="reservations"></a>Reservationer

Om det finns reservationer för den artikel som plockas fortsätter beräkningen. Tanken är att reserverad efterfrågan har högre prioritet än icke-reserverad, vilket innebär att plockning för icke-reserverad efterfrågan inte bör förhindra plockning för reserverad efterfrågan senare.

Kontrollera att kvantiteten kan täcka en efterfrågan genom att jämföra värdet **Plockbart ant.** i faktaboxen **Sammanfattning** med värdet i fältet **Ant. att hantera (bas)** på raderna.

Du hittar reservationer i fältet **Totalt reserverat antal i distributionslager**. Reserverade kvantiteter som redan har plockats och är klara för leverans, användning eller förbrukning påverkar inte tillgängligheten. I fältet **Reserverat antal på plock-/utleveranslagerplatser** visas denna kvantitet.

Fältet **Disponibel kvantitet exklusive utleveranslagerplats** visar det antal som är tillgängligt, exklusive kvantiteter för vilka följande gäller:

* De har redan plockats för leverans.
* De finns i spärrade artikelpartier eller serienummer.
* De finns i blockerade lagerplatser.

Dessa kvantiteter kanske är tillgängliga, men du kanske inte kan plocka dem ännu. De kan fortfarande finnas i mottagnings-, lagrings- eller kvalitetssäkringsområdena. Du kan flytta dem till plockningsområdet genom att bearbeta ett förslag för artikelinförsel eller transport.

Skillnaden mellan **Disponibel kvantitet exklusive utleveranslagerplats** och reserverat antal i distributionslagret är den kvantitet som är tillgänglig för plockning utan att påverka reserverat lager.

### <a name="other-details"></a>Annan information

Om artiklar kräver artikelspårning kan du även hitta antalet i spärrade partier eller serienummer, vilket medför följande minskningar:

* Plockbar kvantitet
* Disponibelt antal exklusive lagerplats för utleverans
* Reserverat antal i distributionslager 

Om du plockar samma artikel för flera källdokument eller rader, vilket också är fallet när du plockar serienummer, visas även information om plockning för andra rader eftersom detta minskar det plockbara antalet.
