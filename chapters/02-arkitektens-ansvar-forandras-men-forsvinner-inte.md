# Kapitel 2: Arkitektens ansvar förändras — men försvinner inte

## Varför detta kapitel finns

När en organisation börjar arbeta mer agilt uppstår ofta en osäkerhet kring arkitektrollen. Om teamen ska bli mer självständiga, om krav förfinas löpande och om lösningen får växa fram stegvis — vad ska arkitekten då göra?

En vanlig feltolkning är att agil utveckling gör arkitektur mindre viktig. I praktiken är det ofta tvärtom. När beslut fattas oftare, när fler personer deltar i designarbetet och när lösningen utvecklas i kortare steg blir behovet av arkitektoniskt omdöme större, inte mindre. Skillnaden är att omdömet behöver användas på ett annat sätt.

I en mer fasorienterad logik har arkitekten ofta skapat värde genom att analysera, strukturera, beskriva och förankra en lösning innan utvecklingen tar fart. Det arbetet kan fortfarande behövas. Men i en agil logik räcker det inte att arkitekturen finns som ett underlag vid sidan av teamets vardag. Arkitekturen behöver leva i samtalen, besluten, prioriteringarna och designvalen under hela utvecklingen.

Det här kapitlet handlar därför om ett viktigt skifte: från arkitekten som huvudsaklig producent av färdiga lösningsbeskrivningar till arkitekten som möjliggörare av bra arkitektur- och designbeslut över tid.

## Situationen: teamet vill fatta fler beslut själv

Myndigheten för samhällstjänster har startat arbetet med den första avgränsade medborgartjänsten. Teamet har fått i uppdrag att ta fram ett smalt flöde där en medborgare kan lämna in kompletterande uppgifter digitalt i stället för via blankett.

Sara deltar i ett planeringsmöte tillsammans med Erik, Lina och några utvecklare. Teamet vill komma vidare med tekniska vägval för formulärhantering, åtkomstkontroll, integration mot handläggningssystemet och hur informationen ska visas för handläggaren.

Lina säger:

> “Vi behöver kunna fatta fler beslut i teamet. Annars kommer varje fråga att behöva gå via arkitekturspåret, och då tappar vi tempo.”

Sara förstår poängen. Samtidigt ser hon riskerna. Formulärlösningen kan påverka informationsmodell, loggning, arkivering, integrationer och framtida återanvändning. Behörighetsfrågorna kan påverka både säkerhet och användarupplevelse. Integrationerna kan skapa beroenden till det äldre handläggningssystemet som blir svåra att ändra senare.

Hon märker att hon dras mot två ytterligheter.

Den ena är att säga:

> “Teamet får inte gå vidare förrän vi har rett ut helheten.”

Den andra är att säga:

> “Teamet får bestämma själva, så tar vi eventuella arkitekturfrågor senare.”

Ingen av ytterligheterna känns bra. Den första riskerar att göra arkitekturen till en broms. Den andra riskerar att viktiga vägval sker utan helhetsperspektiv.

Det Sara behöver är inte mer kontroll eller mindre ansvar. Hon behöver ett annat sätt att utöva sitt ansvar.

## Det invanda sättet att agera

För en erfaren lösningsarkitekt är det naturligt att vilja skapa sammanhang innan beslut fattas. När teamet vill gå vidare med lösningsdetaljer kan det invanda agerandet vara att samla in mer information, analysera fler beroenden, beskriva målbilden tydligare och säkerställa att beslut är förankrade.

Det är ett rimligt beteende. Det kommer ofta ur ansvarstagande, inte ur ovilja att förändras. Arkitekten vet att till synes små beslut kan få stora följder. En integrationslösning kan påverka förvaltning i många år. En datamodell kan begränsa framtida tjänster. En behörighetsmodell kan bli dyr att ändra. En genväg i ett första inkrement kan bli normalfallet.

I fasorienterade sammanhang har arkitektens ansvar ofta uttryckts genom tydliga leveranser:

- lösningsbeskrivningar,
- arkitekturbilder,
- designprinciper,
- vägvalsunderlag,
- granskningskommentarer,
- beslutsrekommendationer,
- överlämningar till utveckling eller förvaltning.

När organisationen börjar arbeta mer agilt kan samma ansvar behöva uttryckas mer som närvaro och förmåga:

- att hjälpa teamet förstå konsekvenser,
- att skilja mellan beslut som kan tas lokalt och beslut som behöver lyftas,
- att formulera ramar som ger handlingsutrymme,
- att skapa dialog mellan team, verksamhet, säkerhet och förvaltning,
- att synliggöra risker utan att stoppa allt arbete,
- att dokumentera beslut i den form som faktiskt behövs.

Det invanda sättet är alltså inte fel. Men det kan bli otillräckligt om det bara bygger på att arkitekten först tänker färdigt och sedan förmedlar svaret.

## Varför det kan skapa friktion i agil utveckling

Friktionen uppstår ofta när arkitektens ansvar är organiserat som en separat beslutspunkt medan teamets arbete är organiserat som ett löpande flöde.

Teamet behöver fatta många små och medelstora beslut för att komma framåt. Arkitekten behöver säkerställa att besluten hänger ihop med helheten. Om alla beslut måste vänta på arkitekten uppstår köer. Om inga beslut involverar arkitekten uppstår risk för fragmentering. Utmaningen är att skapa ett arbetssätt där arkitekturen finns med utan att varje fråga blir ett godkännandeärende.

I praktiken syns friktionen ofta på några sätt.

Teamet väntar på arkitekturen, men vet inte exakt vad de väntar på. Arkitekten väntar på tydligare krav, men kraven blir tydligare först när teamet börjar bygga och testa. Produktägaren vill prioritera nytta, men arkitekten ser beroenden som inte syns i backloggen. Säkerhet och förvaltning behöver involveras, men bjuds in först när lösningen redan tagit form.

Det här betyder inte att någon roll gör fel. Det betyder att arbetet behöver kopplas ihop tätare.

Ett särskilt vanligt problem är att arkitektur reduceras till granskning. Arkitekten kommer in när teamet redan har format ett förslag och förväntas säga ja eller nej. Det gör arkitekten sen, reaktiv och ibland bromsande. Det gör också teamet beroende av att gissa vad arkitekten kommer att godkänna.

Ett annat vanligt problem är att teamnära arbete misstolkas som att arkitekten ska släppa helheten. Då fattas beslut nära koden, men utan tillräcklig koppling till långsiktiga egenskaper som förvaltningsbarhet, informationssäkerhet, återanvändbarhet, integration och spårbarhet.

Ett mer agilt arkitekturarbete behöver undvika båda problemen.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt börjar med att skilja mellan ansvar och kontroll.

Arkitekten har fortfarande ansvar för helhet, struktur, viktiga vägval och lösningens långsiktiga egenskaper. Men ansvar behöver inte alltid betyda att arkitekten själv fattar varje beslut eller godkänner varje detalj. Ansvar kan också betyda att skapa ramar, principer, dialoger och beslutsvägar som gör det möjligt för andra att fatta bra beslut.

Det är här tre begrepp blir viktiga: kontinuerligt arkitekturarbete, teamnära arkitektur och arkitekt som möjliggörare.

**Kontinuerligt arkitekturarbete** innebär att arkitekturen utvecklas och förvaltas löpande under arbetets gång. Den finns inte bara i ett dokument före utveckling eller i en granskning efteråt. Den finns i återkommande samtal, i principer, i beslut som dokumenteras när de fattas och i justeringar när ny kunskap uppstår.

**Teamnära arkitektur** innebär att arkitekturen kopplas till teamets vardag. Arkitekten behöver förstå vad teamet försöker åstadkomma nu, vilka beslut som står framför dem och vilka risker som faktiskt är aktuella. Det betyder inte att arkitekten blir teamets chef eller detaljstyr designen. Det betyder att arkitekturen blir tillgänglig när beslut behöver fattas.

**Arkitekt som möjliggörare** innebär att arkitekten hjälper organisationen att fatta bättre beslut, inte bara fler beslut genom arkitekten. Ibland innebär det att själv ta fram ett vägval. Ibland innebär det att formulera en princip. Ibland innebär det att ställa rätt frågor. Ibland innebär det att föra samman personer som annars inte möts förrän för sent.

Ett praktiskt sätt att tänka är att arkitekten bidrar på tre nivåer:

1. **Riktning:** Vilka principer, begränsningar och mål behöver vara tydliga?
2. **Beslutsstöd:** Vilka beslut står vi inför, och vem har bäst kunskap för att fatta dem?
3. **Lärande:** Vad behöver vi pröva, följa upp eller ändra när vi vet mer?

Det här gör arkitektrollen mer aktiv, inte mindre. Men aktiviteten flyttar närmare flödet.

## Exempel: Myndigheten för samhällstjänster

Sara och Lina bestämmer sig för att pröva ett annat upplägg. I stället för att Sara ska ta fram en fullständig lösningsbeskrivning innan teamet går vidare, bokar de ett kort arkitektursamtal två gånger i veckan under de första veckorna.

Syftet är inte att Sara ska godkänna varje detalj. Syftet är att fånga upp beslut som kan påverka helheten.

Inför första samtalet ber Sara teamet att ta med tre typer av frågor:

- beslut de tror att de kan fatta själva,
- beslut där de är osäkra på konsekvenserna,
- beslut som kan påverka andra team, system eller förvaltning.

Teamet kommer med frågor om formulärkomponenter, datalagring, integration och behörighet.

Sara föreslår att formulärkomponenterna kan hanteras lokalt av teamet så länge de följer myndighetens riktlinjer för tillgänglighet och återanvändning. Hon vill däremot att datalagring och integration hanteras mer medvetet, eftersom de kan påverka handläggningssystemet och framtida tjänster.

Tillsammans formulerar de tre enkla arkitekturramar för den första leveransen:

1. Den första versionen får bara omfatta ett smalt ärendeflöde.
2. Personuppgifter får inte lagras i den nya tjänsten utan tydligt beslut om ansvar, gallring och åtkomst.
3. Integration mot handläggningssystemet ska först göras genom ett avgränsat gränssnitt så att teamet inte bygger fast sig i interna detaljer.

Sara dokumenterar inte detta som en omfattande lösningsarkitektur. Hon skriver en kort beslutsanteckning och lägger till vilka frågor som fortfarande är öppna. Hon markerar också vilka frågor som behöver tas med Amir och vilka som kan hanteras av teamet.

På så sätt får teamet mer handlingsutrymme, samtidigt som arkitekturen blir mer närvarande. Sara har inte släppt sitt ansvar. Hon har gjort ansvaret användbart i teamets takt.

## Vad arkitekten fortfarande behöver äga

Agil utveckling förändrar inte behovet av helhet. Vissa frågor behöver fortfarande någon som ser över teamgränser, systemgränser och tidshorisonter.

Arkitekten behöver ofta fortsatt ta ett tydligt ansvar för:

- att synliggöra strukturella konsekvenser av beslut,
- att identifiera beroenden mellan system, team och externa parter,
- att formulera principer som hjälper flera team att fatta samordnade beslut,
- att säkra att viktiga kvalitetsaspekter inte tappas bort,
- att bidra till långsiktig förvaltningsbarhet,
- att dokumentera viktiga vägval på ett sätt som går att förstå senare,
- att hjälpa beslutsforum att fokusera på rätt frågor.

Det här ansvaret ska inte blandas ihop med att arkitekten måste ha sista ordet i alla frågor. I en mer agil miljö är en viktig del av arkitektens professionalitet att veta när ett beslut bör fattas av arkitekten, när det bör fattas av teamet och när det bör fattas tillsammans med verksamhet, säkerhet, juridik, förvaltning eller styrning.

Ett enkelt test är att fråga:

- Påverkar beslutet bara teamets interna implementation?
- Påverkar det andra team, system eller framtida förändringsförmåga?
- Påverkar det myndighetens ansvar för säkerhet, spårbarhet, rättssäkerhet eller förvaltning?
- Är beslutet lätt att ändra senare, eller blir det dyrt att backa?
- Behöver beslutet förstås av andra än teamet om sex månader?

Ju mer beslutet påverkar helhet, långsiktighet eller ansvar, desto mer behöver arkitekten vara involverad. Men involverad behöver inte alltid betyda beslutande. Det kan betyda rådgivande, samordnande, principformulerande eller risktydliggörande.

## Vanliga fallgropar

- Fallgrop: Arkitekten blir en sen granskare.
  - Varför den uppstår: Teamet vill arbeta självständigt och involverar arkitekten först när ett förslag redan finns.
  - Vad arkitekten kan göra i stället: Skapa tidiga och korta arkitektursamtal där beslut och risker fångas innan lösningen låses.

- Fallgrop: Teamnära arkitektur tolkas som detaljstyrning.
  - Varför den uppstår: Arkitekten kommer nära teamets vardag men saknar tydlig roll i samtalen.
  - Vad arkitekten kan göra i stället: Fokusera på principer, konsekvenser och beslut som påverkar helheten, inte på varje teknisk detalj.

- Fallgrop: Självständiga team lämnas utan arkitekturramar.
  - Varför den uppstår: Organisationen vill undvika gamla godkännandeprocesser och går för långt åt andra hållet.
  - Vad arkitekten kan göra i stället: Formulera enkla ramar för beslut, beroenden, dokumentation och eskalering.

- Fallgrop: Arkitekturen blir ett parallellt spår.
  - Varför den uppstår: Arkitekten arbetar vidare med målbild och dokumentation utan tät koppling till teamets aktuella beslut.
  - Vad arkitekten kan göra i stället: Knyt arkitekturarbetet till teamets kommande vägval, risker och lärbehov.

- Fallgrop: Arkitekten släpper för mycket för att inte bromsa.
  - Varför den uppstår: Arkitekten vill stödja agil utveckling och undviker därför att lyfta svåra frågor.
  - Vad arkitekten kan göra i stället: Skilj mellan att bromsa och att tydliggöra konsekvenser. Viktiga risker ska synliggöras tidigt, men inte nödvändigtvis stoppa arbetet.

## Frågor att ställa i situationen

När teamet vill fatta fler beslut själv kan arkitekten ställa frågor som hjälper utan att ta över:

- Vilka beslut står teamet inför de närmaste veckorna?
- Vilka av dessa beslut påverkar andra team, system eller framtida förändringsförmåga?
- Vilka beslut kan teamet fatta inom givna principer?
- Vilka beslut behöver dokumenteras så att andra kan förstå dem senare?
- Vilka kvalitetsaspekter riskerar att tappas bort om vi bara fokuserar på nästa leverans?
- Vilka frågor behöver säkerhet, juridik, förvaltning eller verksamhet vara med i tidigt?
- Vad behöver vara en gemensam arkitekturram, och vad kan vara lokalt teamansvar?
- Hur snabbt kan vi få återkoppling om beslutet visar sig vara fel?

## Reflektionsfrågor

1. I vilka situationer blir du som arkitekt oftast en granskare snarare än en deltagare i beslutet?
2. Vilka typer av beslut brukar du vilja behålla själv, och varför?
3. Vilka beslut skulle ett team kunna fatta bättre om de fick tydligare principer i stället för fler godkännanden?
4. När har du sett självständiga team fatta beslut som senare skapade helhetsproblem?
5. Vad skulle krävas för att du skulle känna dig trygg med att flytta fler beslut närmare teamet?
6. Hur kan du vara mer närvarande i teamets beslut utan att bli en flaskhals?
7. Vilka samtal behöver du initiera tidigare med säkerhet, förvaltning eller verksamhet?
8. Vad är ett konkret steg du kan ta för att gå från kontrollpunkt till möjliggörare?

## Snabb sammanfattning

Arkitektens ansvar försvinner inte i agil utveckling. Det förändras från att i första hand producera färdiga lösningsunderlag till att skapa förutsättningar för bra beslut över tid.

I en mer agil utvecklingslogik behöver arkitekturen vara närvarande i teamens vardag, inte bara i dokument och granskningar. Teamnära arkitektur innebär inte att arkitekten detaljstyr teamet. Det innebär att arkitektens helhetsperspektiv finns tillgängligt när beslut fattas.

En arkitekt som möjliggörare hjälper organisationen att skilja mellan beslut som teamet kan fatta själv, beslut som behöver gemensam dialog och beslut som behöver formell förankring. På så sätt kan teamet få mer handlingsutrymme utan att helhet, säkerhet, förvaltning och långsiktighet tappas bort.

## Nästa steg

I nästa kapitel går vi vidare till frågan om beslut i sig. När arkitektens roll blir mer kontinuerlig och teamnära räcker det inte att fråga vem som fattar beslut. Vi behöver också förstå vilka beslut som behöver fattas tidigt, vilka som kan vänta och vilka som bör hållas öppna tills organisationen har lärt sig mer.

Nästa kapitel handlar därför om skiftet från tidig säkerhet till löpande beslutsförmåga.
