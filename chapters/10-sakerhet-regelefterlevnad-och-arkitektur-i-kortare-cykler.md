# Kapitel 10: Säkerhet, regelefterlevnad och arkitektur i kortare cykler

## Varför detta kapitel finns

I statlig myndighet är säkerhet, integritet, rättssäkerhet och regelefterlevnad inte sidofrågor. De är en del av uppdraget. Ett digitalt stöd som hanterar ärenden, personuppgifter, beslut eller samhällsviktig information behöver inte bara fungera tekniskt. Det behöver också kunna förklaras, granskas, skyddas och förvaltas över tid.

När utvecklingen blir mer agil uppstår därför en särskild spänning. Teamen vill leverera stegvis, lära sig av användning och minska ledtider. Säkerhets-, juridik- och dataskyddsfunktioner vill försäkra sig om att lösningen inte skapar oacceptabla risker. Arkitekten hamnar ofta mitt i denna spänning.

Det invanda svaret är ofta att försöka “säkerställa allt” tidigt eller att lägga in tydliga kontrollpunkter sent i flödet. Båda strategierna kan kännas ansvarsfulla. Men i kortare utvecklingscykler räcker de sällan. För mycket tidig kontroll bygger på antaganden som senare förändras. För sen kontroll upptäcker risker när det redan är dyrt att ändra.

Det här kapitlet handlar om hur arkitekten kan bidra till att säkerhet och regelefterlevnad blir en levande del av utvecklingsarbetet.

Kapitlets centrala skifte är:

> Från säkerhet och regelefterlevnad som tidiga krav och sena kontroller till säkerhet och regelefterlevnad som återkommande riskdialog, designbegränsningar och inbyggd kontroll.

## Situationen: alla vill göra rätt, men ingen vill stoppa flödet

Sara är med i ett planeringsmöte för den nya medborgartjänsten på Myndigheten för samhällstjänster. Teamet har byggt en första intern version där en medborgare kan följa status i sitt ärende. Tjänsten hämtar information från det äldre handläggningssystemet och visar en förenklad vy.

Erik, produktägaren, vill gå vidare med en pilot för en begränsad användargrupp.

Lina, teamets utvecklingsledare, säger att den tekniska lösningen är tillräckligt stabil för att testas.

Amir, som arbetar med informationssäkerhet och dataskyddsfrågor, är tveksam. Han frågar:

> “Vilka personuppgifter exponeras? Hur vet vi att rätt person ser rätt ärende? Hur loggar vi åtkomst? Finns det risk att vi visar mer information än nödvändigt?”

Teamet svarar att flera av frågorna finns med i backloggen. Erik säger att piloten är begränsad. Amir vill se tydligare underlag innan tjänsten används utanför teamet.

Sara känner igen situationen. Alla har rimliga perspektiv:

- Erik vill skapa nytta och få återkoppling.
- Lina vill undvika att utvecklingen fastnar i långa utredningar.
- Amir vill undvika att myndigheten tar risker som inte är förstådda.
- Sara vill att arkitekturen ska stödja både säkerhet och stegvis utveckling.

Frågan är inte om säkerhet och regelefterlevnad är viktiga. Frågan är hur de kommer in i arbetet på ett sätt som både skapar trygghet och gör fortsatt lärande möjligt.

## Det invanda sättet att agera

I en mer fasorienterad utvecklingslogik hanteras säkerhet och regelefterlevnad ofta genom särskilda moment:

- krav på säkerhet och regelverk samlas in tidigt,
- lösningen analyseras mot dessa krav,
- risker dokumenteras,
- kontrollfunktioner granskar underlag,
- godkännande sker inför nästa fas, inför test eller inför produktionssättning.

Detta kan ge tydlighet. Det blir klart vem som behöver granska vad. Det finns underlag att hänvisa till. Ansvar kan dokumenteras. För en myndighet är detta ofta nödvändigt i någon form.

Men när utvecklingen sker i kortare cykler blir det problematiskt om säkerhet och regelefterlevnad bara kommer in som separata kontrollpunkter. Då uppstår lätt två oönskade mönster.

Det första mönstret är att allt försöker lösas för tidigt. Arkitekten, säkerhetsfunktionen och juridiken försöker förutse alla tänkbara risker innan teamet börjar bygga. Resultatet blir ofta omfattande analyser av en lösning som ännu inte finns, eller av antaganden som senare ändras.

Det andra mönstret är att kontrollen kommer in för sent. Teamet bygger vidare, och först nära leverans upptäcks att behörighet, loggning, informationsklassning, gallring, spårbarhet eller rättslig grund inte är tillräckligt genomtänkta. Då upplevs säkerhet och regelefterlevnad som bromsar, trots att frågorna egentligen borde ha påverkat designen från början.

Det invanda sättet kan därför skapa en falsk uppdelning:

- teamet “bygger”,
- arkitekten “designar”,
- säkerhet och juridik “granskar”,
- styrningen “godkänner”.

I ett agilt arbetssätt behöver dessa aktiviteter i stället kopplas samman oftare och tidigare, utan att allt måste formaliseras lika tungt varje gång.

## Varför det kan skapa friktion i agil utveckling

Friktionen uppstår ofta för att olika delar av organisationen arbetar med olika rytm.

Teamet arbetar i korta cykler. Det vill kunna dela upp arbetet, testa antaganden och leverera stegvis. Säkerhets- och regelefterlevnadsfrågor arbetar ofta med en annan logik: konsekvenser behöver förstås, ansvar behöver vara tydligt och vissa risker kan inte lämnas öppna.

När dessa rytmer inte möts skapas väntan och frustration. Teamet upplever att kontrollfunktioner ställer frågor som kommer för sent eller är för omfattande för den aktuella förändringen. Kontrollfunktionerna upplever att teamet rör sig för snabbt och att viktiga risker göms bakom ord som “pilot”, “MVP” eller “första inkrement”.

Arkitekten kan då lockas att gå in som översättare och problemlösare på egen hand. Sara kan till exempel börja skriva ett större säkerhets- och arkitekturunderlag för att lugna Amir och samtidigt försöka skydda teamets tempo. Det kan hjälpa kortsiktigt, men riskerar att förstärka bilden av att säkerhet är något arkitekten “tar hand om” vid sidan av teamets arbete.

I stället behöver arkitekten hjälpa organisationen att föra in säkerhet och regelefterlevnad i själva arbetssättet. Det betyder inte att alla i teamet ska bli jurister eller säkerhetsspecialister. Det betyder att riskfrågor, designbegränsningar, kontrollbehov och dokumentationskrav behöver bli synliga i rätt tid och på rätt nivå.

Tre begrepp är särskilt viktiga i det skiftet:

- **Inbyggd kontroll**: kontroller som byggs in i lösning, arbetssätt, automatisering eller återkommande dialog i stället för att bara ske som sena granskningar.
- **Kontinuerlig riskdialog**: återkommande samtal om risker, avvägningar och åtgärder mellan arkitektur, team, säkerhet, juridik, dataskydd och verksamhet.
- **Säkerhet som designbegränsning**: synsättet att säkerhet inte bara är krav att bocka av, utan begränsningar som påverkar hur lösningen bör utformas.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt börjar med att skilja mellan tre typer av frågor:

1. Frågor som måste vara tillräckligt utredda innan utveckling eller pilot får gå vidare.
2. Frågor som kan hanteras stegvis, om riskerna är synliga och avgränsade.
3. Frågor som bör byggas in i teamets löpande arbetssätt.

För Sara innebär det att hon inte bara frågar: “Är lösningen godkänd ur säkerhetssynpunkt?” Hon frågar också:

- Vilka risker påverkar arkitekturen redan nu?
- Vilka beslut är svåra att ändra senare?
- Vilka kontroller kan byggas in i lösningen?
- Vilka kontroller behöver ske genom granskning eller beslut?
- Vilka antaganden behöver testas innan vi skalar upp?
- Vilka roller behöver prata med varandra oftare?

Det handlar om att skapa en rytm där säkerhet och regelefterlevnad inte blir en separat fas, men heller inte reduceras till en punkt på en checklista.

### 1. Gör riskerna synliga tidigt, men på rätt detaljnivå

Tidigt i arbetet behöver Sara inte ha alla svar. Men hon behöver hjälpa teamet att se vilka säkerhets- och regelefterlevnadsfrågor som kan påverka lösningens form.

För medborgartjänsten kan det handla om:

- vilken information som visas för medborgaren,
- hur identitet och behörighet säkerställs,
- vilka händelser som behöver loggas,
- om tjänsten hanterar känsliga personuppgifter,
- hur länge information behöver sparas,
- vilka integrationer som öppnar nya angreppsytor,
- om det finns beslut eller statusuppgifter som kan misstolkas,
- vilka fel som kan få rättsliga eller praktiska konsekvenser för individen.

Detta behöver inte innebära ett stort dokument i första steget. Det kan börja som en enkel riskkarta: vilka frågor är kritiska, vilka är osäkra, vilka kan vänta och vilka behöver en särskild dialog?

Det viktiga är att riskerna blir synliga medan designen fortfarande kan påverkas.

### 2. Behandla säkerhet som en del av lösningens form

Ibland beskrivs säkerhet som något som “läggs till” efteråt. Det leder lätt fel. Behörighet, loggning, informationsflöden, dataminimering, integrationer och spårbarhet påverkar lösningens struktur.

För arkitekten betyder det att säkerhetsfrågor behöver översättas till designfrågor.

Exempel:

- Om endast vissa handläggningsuppgifter får visas för medborgaren behöver lösningen ha en tydlig informationsmodell och filtrering.
- Om åtkomst måste kunna följas upp behöver loggning vara en del av designen, inte något som läggs till inför driftsättning.
- Om olika ärendetyper har olika sekretessnivåer behöver behörighetsmodellen stödja den variationen.
- Om externa integrationer används behöver felhantering och ansvarsfördelning vara tydlig.
- Om information inte ska sparas längre än nödvändigt behöver livscykel och gallring påverka både dataflöde och lagring.

När säkerhet behandlas som designbegränsning blir den inte bara ett kontrollkrav. Den hjälper teamet att forma en lösning som är möjlig att använda ansvarsfullt.

### 3. Skapa kontinuerlig riskdialog

Kontinuerlig riskdialog innebär inte att alla riskfrågor ska diskuteras på varje möte. Det innebär att det finns en återkommande, lättillgänglig form för att lyfta risker när de påverkar arbetet.

Sara kan till exempel hjälpa till att etablera en enkel rutin:

- Vid större förändringar i informationsflöde, behörighet eller integration bokas en kort riskdialog.
- Teamet tar med aktuell skiss, öppna frågor och tänkt nästa steg.
- Amir eller annan specialist hjälper till att sortera risker och avgöra vad som kräver mer underlag.
- Beslut och antaganden dokumenteras kort i beslutsloggen eller arkitekturdokumentationen.
- Frågor som inte behöver lösas direkt läggs som synliga uppföljningspunkter.

Det viktiga är att dialogen sker medan den fortfarande kan påverka design och prioritering. Om säkerhetsfunktionen bara ser lösningen när teamet vill gå i produktion blir dialogen nästan alltid svårare.

### 4. Bygg in kontroll där det går

Inbyggd kontroll kan vara teknisk, organisatorisk eller dokumentationsmässig.

Teknisk inbyggd kontroll kan till exempel vara:

- automatiska kontroller i bygg- och leveransflöden,
- loggning av känsliga händelser,
- behörighetskontroller som återanvänds konsekvent,
- testfall för säkerhetskritiska regler,
- övervakning av avvikelser,
- konfigurationsstyrning.

Organisatorisk inbyggd kontroll kan vara:

- att säkerhet och dataskydd deltar i återkommande riskdialoger,
- att riskfrågor finns med i refinement för relevanta backloggposter,
- att teamet har tydliga kriterier för när specialiststöd ska kopplas in,
- att produktägaren förstår vilka riskbeslut som behöver eskaleras.

Dokumentationsmässig inbyggd kontroll kan vara:

- en beslutslogg för viktiga risk- och arkitekturbeslut,
- en enkel informationsflödesbild som hålls uppdaterad,
- en lista över öppna riskantaganden,
- tydliga länkar mellan krav, designbeslut och riskåtgärder.

Poängen är inte att all kontroll ska automatiseras eller förenklas. Poängen är att kontrollen ska finnas där den gör mest nytta och inte enbart som sen granskning.

### 5. Skilj mellan pilot, experiment och skarp användning

I agila sammanhang används ofta ord som pilot, experiment, MVP och första version. De kan vara värdefulla, men de får inte bli ett sätt att otydliggöra ansvar.

Sara behöver därför hjälpa organisationen att vara tydlig med vad ett steg faktiskt innebär.

En intern teknisk prototyp har en typ av risk. En pilot med verkliga handläggare har en annan. En medborgartjänst som visar verklig ärendestatus för en begränsad grupp har en tredje. En fullskalig produktionssättning har ytterligare en annan riskbild.

Frågan är inte bara hur liten leveransen är. Frågan är vilken information, vilka användare, vilka beslut och vilka konsekvenser som berörs.

Ett begränsat steg kan absolut vara rätt väg. Men begränsningen behöver vara verklig och begriplig:

- Vilka användare omfattas?
- Vilka data används?
- Vilka funktioner är aktiva?
- Vilka beslut kan påverkas?
- Hur upptäcker vi fel?
- Hur avbryter eller rullar vi tillbaka?
- Vem äger riskbeslutet?

När dessa frågor är tydliga blir stegvis leverans inte ett sätt att komma runt ansvar. Det blir ett sätt att ta ansvar med kontrollerat lärande.

## Exempel: Myndigheten för samhällstjänster

Efter mötet samlar Sara, Lina, Erik och Amir en kort arbetsdialog. Sara ritar upp tre enkla vyer på en digital whiteboard:

1. Vilken information medborgaren ska se.
2. Varifrån informationen hämtas.
3. Vilka beslut och kontroller som krävs innan nästa steg.

Det visar sig snabbt att ordet “ärendestatus” betyder olika saker. För Erik betyder det att medborgaren ska kunna se om ärendet är mottaget, under handläggning eller beslutat. För teamet betyder det ett tekniskt statusfält från det äldre systemet. För Amir betyder det en fråga om vilken information som kan avslöja mer än myndigheten avsett.

Sara ställer frågan:

> “Vilken minsta statusinformation ger medborgaren nytta utan att vi exponerar känsliga detaljer?”

Det leder till ett annat designalternativ. I stället för att visa det interna statusfältet direkt skapar teamet en förenklad extern statusmodell. Den visar färre lägen, med språk som är begripligt för medborgaren och som inte avslöjar interna handläggningsdetaljer.

Amir påpekar att åtkomst behöver loggas, särskilt när ärenden innehåller skyddsvärd information. Lina svarar att teamet redan har teknisk loggning, men att den inte är utformad för uppföljning av medborgaråtkomst. Sara fångar det som ett arkitekturbeslut:

> “Medborgaråtkomst till ärendestatus ska loggas som en verksamhetsrelevant händelse, inte enbart som teknisk systemlogg.”

Beslutet läggs i beslutsloggen med tre delar:

- varför beslutet fattades,
- vilken konsekvens det får för designen,
- vilka frågor som fortfarande är öppna.

Erik vill fortfarande göra piloten. Amir säger att det kan vara möjligt om piloten begränsas till ärenden utan särskilda skyddsmarkeringar, om åtkomst sker via befintlig säker inloggning, om loggningen är på plats och om teamet dokumenterar kvarvarande risker.

Sara sammanfattar:

> “Vi stoppar inte piloten, men vi gör den smalare och tydligare. Vi använder den för att lära, inte för att smyga ut en full lösning.”

Det blir ett konkret exempel på inbyggd kontroll och kontinuerlig riskdialog. Säkerhet och regelefterlevnad blir inte en sen spärr. De påverkar själva utformningen av nästa steg.

## Vanliga fallgropar

- Fallgrop: Att använda “agilt” som skäl för att skjuta upp säkerhetsfrågor.
  - Varför den uppstår: Teamet vill undvika tidiga utredningar och tänker att detaljer kan lösas senare.
  - Vad arkitekten kan göra i stället: Skilj mellan frågor som kan vänta och frågor som påverkar lösningens grundläggande form.

- Fallgrop: Att försöka säkerställa allt innan något får byggas.
  - Varför den uppstår: Osäkerhet känns riskabel, särskilt i myndighetsmiljö.
  - Vad arkitekten kan göra i stället: Identifiera vilka risker som måste hanteras före nästa steg och vilka som kan undersökas genom kontrollerad utveckling.

- Fallgrop: Att behandla säkerhet som en checklista vid sidan av designen.
  - Varför den uppstår: Säkerhetskrav dokumenteras ofta separat från arkitektur- och designbeslut.
  - Vad arkitekten kan göra i stället: Översätt säkerhetskrav till designbegränsningar, principer och konkreta beslut.

- Fallgrop: Att kalla något pilot utan att tydliggöra risknivån.
  - Varför den uppstår: Ordet pilot låter begränsat och ofarligt.
  - Vad arkitekten kan göra i stället: Beskriv exakt vilka användare, data, funktioner, miljöer och konsekvenser piloten omfattar.

- Fallgrop: Att göra säkerhetsfunktionen till en sen godkännare.
  - Varför den uppstår: Organisationen har invanda gransknings- och beslutsvägar.
  - Vad arkitekten kan göra i stället: Skapa återkommande riskdialoger där specialister kommer in när designen fortfarande går att påverka.

- Fallgrop: Att arkitekten själv försöker bära hela risköversättningen.
  - Varför den uppstår: Arkitekten vill skydda teamets flöde och samtidigt tillfredsställa kontrollbehoven.
  - Vad arkitekten kan göra i stället: Gör risker, antaganden och beslut synliga så att rätt roller kan ta ansvar tillsammans.

## Frågor att ställa i situationen

När säkerhet, regelefterlevnad och arkitektur behöver hanteras i kortare cykler kan arkitekten använda följande frågor:

1. Vilken information hanteras, visas, lagras eller skickas vidare?
2. Vilka användare, roller eller externa aktörer berörs?
3. Vilka fel kan få störst konsekvens för individ, verksamhet eller myndighet?
4. Vilka säkerhets- och regelkrav påverkar lösningens struktur redan nu?
5. Vilka beslut är svåra att ändra senare?
6. Vilka risker kan vi minska genom att begränsa nästa steg?
7. Vilka kontroller kan byggas in i lösningen eller arbetssättet?
8. Vilka risker behöver dokumenteras som medvetna avvägningar?
9. Vilka specialister behöver delta i dialogen innan vi går vidare?
10. Vad behöver vara sant för att nästa inkrement ska vara ansvarsfullt?

Frågorna är inte tänkta som en komplett granskningsmall. De är ett sätt att hjälpa arkitekten föra rätt samtal i rätt tid.

## Reflektionsfrågor

1. När kommer säkerhet, juridik, dataskydd eller regelefterlevnad typiskt in i dina utvecklingsflöden i dag?
2. Vilka frågor brukar upptäckas för sent?
3. Vilka frågor försöker organisationen ibland lösa för tidigt, innan lösningen är tillräckligt begriplig?
4. Hur kan du som arkitekt göra risker synliga utan att omedelbart skapa en tung utredningsfas?
5. Vilka säkerhets- eller regelefterlevnadskrav påverkar arkitekturen i dina vanligaste lösningar?
6. Vilka kontroller skulle kunna byggas in i teamets arbetssätt i stället för att göras som sena granskningar?
7. Hur tydligt skiljer ni i dag mellan prototyp, pilot, begränsad produktionssättning och fullskalig användning?
8. Vilken återkommande riskdialog skulle skapa mest nytta i din organisation just nu?

## Snabb sammanfattning

- I myndighetsmiljö är säkerhet, integritet, rättssäkerhet och regelefterlevnad en del av lösningens kvalitet, inte externa tillägg.
- Kortare utvecklingscykler kräver att riskfrågor kommer in återkommande, inte bara tidigt eller sent.
- Arkitekten behöver hjälpa team och kontrollfunktioner att mötas medan designen fortfarande kan påverkas.
- Säkerhet bör ofta behandlas som designbegränsning: något som formar lösningens struktur, informationsflöden, behörighet, loggning och spårbarhet.
- Inbyggd kontroll kan finnas i teknik, arbetssätt och dokumentation.
- En pilot eller ett experiment behöver tydliga gränser för användare, data, funktioner, risker och ansvar.
- Målet är inte att minska myndighetens ansvar, utan att ta ansvar på ett sätt som fungerar i iterativ utveckling.

## Nästa steg

När säkerhet och regelefterlevnad blir en del av det löpande arbetet blir nästa fråga hur beslut ska fattas utan att organisationen fastnar i väntan. Arkitekturen behöver forum, mandat och styrning, men dessa behöver stödja flöde snarare än skapa parallella köer.

Nästa kapitel handlar därför om arkitekturforum, styrning och beslut utan flaskhalsar.
