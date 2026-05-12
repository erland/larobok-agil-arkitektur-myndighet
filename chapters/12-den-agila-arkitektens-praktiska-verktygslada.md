# Kapitel 12: Den agila arkitektens praktiska verktygslåda

## Varför detta kapitel finns

De tidigare kapitlen har rört sig genom situationer som många lösnings- och IT-arkitekter känner igen: osäkra behov, löpande kravarbete, team som vill börja bygga, design som sker under arbetets gång, beroenden som bromsar, dokumentation som både behövs och skaver, säkerhet som måste byggas in och forum som behöver stödja snarare än stoppa.

Det här avslutande kapitlet samlar bokens viktigaste arbetssätt i en praktisk verktygslåda. Syftet är inte att introducera ännu en modell som ska ersätta allt annat. Syftet är att ge arkitekten ett antal frågor, perspektiv och enkla arbetssätt som går att bära med sig in i vardagen.

För Sara på Myndigheten för samhällstjänster har resan inte handlat om att sluta vara arkitekt. Den har handlat om att använda sin erfarenhet på ett annat sätt. Hon har fortfarande ansvar för helhet, kvalitet, beroenden och långsiktighet. Men hon har behövt släppa föreställningen att trygghet alltid skapas genom mer förhandsanalys, mer detaljerade dokument och fler formella beslut innan utvecklingen startar.

Kapitlets centrala skifte är:

> Från att arkitekten främst skapar arkitekturprodukter till att arkitekten utvecklar organisationens förmåga att fatta bra arkitektur- och designbeslut över tid.

Det betyder inte att arkitekturdokument, principer, beslutsunderlag eller forum blir oviktiga. Det betyder att de behöver förstås som delar av en levande praktik.

## Situationen: när allt är samtidigt

Mot slutet av moderniseringsarbetet på Myndigheten för samhällstjänster sitter Sara i ett möte med Erik, Lina och Amir. Teamen har levererat flera inkrement av den nya medborgartjänsten. Det äldre handläggningssystemet är fortfarande kvar, men vissa delar har frikopplats. Dokumentationen är inte lika omfattande som i tidigare projekt, men den används oftare. Arkitekturforumet har börjat lägga mer tid på riktning och hinder än på sena godkännanden.

Samtidigt är arbetet långt ifrån friktionsfritt.

Ett team vill göra en teknisk förenkling som kan påverka framtida integrationer. Verksamheten vill prioritera en ny funktion som inte fanns med i den ursprungliga målbilden. Säkerhetsfunktionen vill se tydligare riskbeslut kring loggning och behörighet. Förvaltningen undrar hur lösningen ska kunna tas om hand långsiktigt. En extern part har ändrat sina tidsplaner, vilket påverkar ett beroende.

Det är en typisk agil arkitektursituation: flera perspektiv är sanna samtidigt.

Sara märker att hennes viktigaste bidrag inte är att ensam formulera den perfekta lösningen. Hennes viktigaste bidrag är att hjälpa gruppen att förstå vilken typ av fråga de står inför, vilket beslut som behövs nu, vilka risker som är verkliga, vilka antaganden som behöver testas och vilka ramar som behöver vara tydliga för att teamen ska kunna fortsätta.

Det är här den agila arkitektens verktygslåda behövs.

## Det invanda sättet att agera

I ett mer fasorienterat arbetssätt har arkitekten ofta lärt sig att skapa trygghet genom att:

- analysera helheten tidigt,
- identifiera beroenden i förväg,
- dokumentera målbild och lösningsdesign,
- ta fram beslutsunderlag,
- förankra lösningen i forum,
- säkerställa att krav och lösning hänger ihop,
- minska risken för överraskningar senare.

Det är värdefulla förmågor. Boken har inte argumenterat för att de ska överges.

Men när utvecklingen blir mer iterativ kan samma förmågor skapa friktion om de används på ett sätt som förutsätter att lösningen först ska förstås fullt ut och därefter realiseras. Arkitekten kan då hamna i ett mönster där varje osäkerhet leder till mer utredning, varje risk leder till mer kontroll och varje otydlighet leder till att teamen behöver vänta.

Det invanda sättet kan sammanfattas så här:

> “Jag skapar trygghet genom att göra lösningen tydligare innan andra går vidare.”

I en mer agil miljö behöver arkitekten ofta komplettera detta med ett annat förhållningssätt:

> “Jag skapar trygghet genom att hjälpa organisationen lära, besluta och justera utan att tappa riktning.”

Skillnaden är liten i ord, men stor i vardagligt beteende.

## Varför det kan skapa friktion i agil utveckling

Friktionen uppstår inte för att arkitekten bryr sig för mycket om kvalitet. Den uppstår när kvalitet bara kan hanteras genom tidig kontroll.

I agil utveckling kommer vissa behov, risker och lösningsdetaljer att bli tydliga först när arbetet pågår. Det gäller särskilt när organisationen arbetar med äldre system, många intressenter, externa beroenden, starka regelkrav och oklara verksamhetseffekter. En myndighet kan inte lösa all sådan osäkerhet genom att planera mer i början.

Det betyder inte att “allt får växa fram”. Det betyder att arkitekten behöver skilja mellan olika typer av osäkerhet.

Vissa frågor behöver tydliga svar tidigt:

- Vilken information får hanteras i tjänsten?
- Vilka säkerhets- och behörighetsprinciper gäller?
- Vilka beroenden kan stoppa första leveransen?
- Vilka beslut är svåra att ändra senare?
- Vilka delar av det äldre systemet får inte påverkas utan särskild kontroll?

Andra frågor kan med fördel undersökas stegvis:

- Vilken användarresa ger störst nytta först?
- Hur detaljerad behöver integrationen vara i första inkrementet?
- Vilken teknisk lösning ger bäst balans mellan snabb leverans och långsiktig hållbarhet?
- Vilken dokumentationsnivå räcker för att nästa team ska förstå beslutet?
- Vilket forum behöver informeras, och vilket behöver faktiskt fatta beslut?

När allt behandlas som om det måste lösas före byggstart blir arkitekten lätt en broms. När allt behandlas som om det kan lösas senare skapas risk, omarbete och bristande ansvar. Den agila arkitektens praktik ligger i att skilja dessa frågor åt.

## Ett mer agilt förhållningssätt

Ett mer agilt arkitektförhållningssätt kan sammanfattas i tre huvudbegrepp: arkitektonisk närvaro, reflekterande arkitektpraktik och situationsbaserat arkitektledarskap.

### Arkitektonisk närvaro

Arkitektonisk närvaro betyder att arkitekten finns nära de sammanhang där viktiga beslut växer fram. Det handlar inte om att delta i alla möten eller svara på alla frågor. Det handlar om att vara tillräckligt nära för att upptäcka när ett lokalt beslut håller på att få större konsekvenser.

Arkitektonisk närvaro kan innebära att Sara:

- deltar i utvalda refinement-samtal där krav påverkar arkitektur,
- har korta återkommande avstämningar med teamet,
- följer beslutsloggen och reagerar på mönster,
- hjälper produktägaren att förstå arkitektoniska konsekvenser av prioriteringar,
- bjuder in säkerhet och förvaltning tidigt när risker börjar synas,
- formulerar principer som teamen kan använda utan att fråga varje gång.

Närvaro är inte samma sak som kontroll. En närvarande arkitekt behöver inte äga varje beslut. Men hon behöver förstå vilka beslut som är på väg att fattas, vilka antaganden som styr dem och när ett samtal behöver breddas.

### Reflekterande arkitektpraktik

Reflekterande arkitektpraktik betyder att arkitekten regelbundet undersöker sitt eget sätt att skapa värde.

För Sara innebär det att hon inte bara frågar “är lösningen bra?” utan också:

- Vilket beteende hos mig själv förstärker den här situationen?
- Skapar jag tydlighet eller väntan?
- Hjälper jag teamet att fatta bättre beslut, eller gör jag dem beroende av mig?
- Dokumenterar vi för faktisk användning eller för att känna oss trygga?
- Har jag gjort skillnad mellan risk, osäkerhet och obehag?
- Försöker jag lösa en fråga som egentligen behöver utforskas?

Det här är inte självkritik för sakens skull. Det är professionell kalibrering. En erfaren arkitekt har starka mönster och vältränade reflexer. I många situationer är de en tillgång. I andra situationer behöver de justeras.

### Situationsbaserat arkitektledarskap

Situationsbaserat arkitektledarskap betyder att arkitekten anpassar sitt agerande efter situationens karaktär.

Ibland behöver arkitekten vara tydlig och avgränsande:

> “Det här beslutet påverkar informationssäkerhet och förvaltning. Det behöver inte bli en lång process, men vi behöver fatta det med rätt personer i rummet.”

Ibland behöver arkitekten vara utforskande:

> “Vi vet inte ännu vilken integrationslösning som är bäst. Låt oss avgränsa ett inkrement som hjälper oss lära utan att låsa målbilden.”

Ibland behöver arkitekten vara möjliggörande:

> “Teamet kan fatta de här designbesluten själva om vi är överens om principerna och dokumenterar avvikelser.”

Ibland behöver arkitekten vara bromsande:

> “Här riskerar vi att skapa ett beroende som blir dyrt att ändra. Innan vi går vidare behöver vi förstå konsekvensen.”

Poängen är inte att alltid vara snabbare, lättare eller mer tillåtande. Poängen är att agera medvetet utifrån vilken sorts fråga organisationen faktiskt står inför.

## Exempel: Myndigheten för samhällstjänster

Sara börjar använda en enkel reflektionsmodell i sitt arbete. Hon kallar den för “frågekortet”, men det är egentligen bara fem återkommande frågor som hon använder i möten, forum och samtal med team.

### Fråga 1: Vilken typ av fråga är detta?

När en fråga dyker upp försöker Sara först förstå om den främst handlar om:

- verksamhetsnytta,
- användarbeteende,
- juridik eller regelefterlevnad,
- informationssäkerhet,
- integration,
- data och informationsmodell,
- teknisk design,
- förvaltning,
- beroenden,
- mandat och beslut.

Det gör att gruppen snabbare ser vilka perspektiv som behöver vara med.

När Lina säger att teamet vill förenkla integrationen mot handläggningssystemet frågar Sara inte först efter en detaljerad lösningsskiss. Hon frågar:

> “Är det här främst en teknisk förenkling, eller påverkar det vilken information handläggarna kommer kunna lita på?”

Den frågan förändrar samtalet. Det visar sig att förenklingen både påverkar teknisk komplexitet och informationskvalitet. Då behöver Erik och Amir också vara med i diskussionen.

### Fråga 2: Vad behöver beslutas nu?

I stället för att försöka lösa hela frågan hjälper Sara gruppen att skilja mellan beslut som behövs nu och beslut som kan vänta.

För integrationen behöver teamet besluta hur första inkrementet ska läsa data. Men det behöver ännu inte besluta hela den framtida integrationsstrategin. Däremot behöver de undvika ett vägval som gör framtida frikoppling orimligt dyr.

Sara formulerar det så här:

> “Vi behöver inte välja slutlig målbild i dag, men vi behöver välja ett första steg som inte gör målbilden omöjlig.”

Det är ett typiskt uttryck för tillräcklig arkitektur.

### Fråga 3: Vad är svårt att ändra senare?

Gruppen går igenom vad som är reversibelt och svårreversibelt.

Det visar sig att vissa delar av teamets förslag är enkla att ändra senare, medan valet av datamodell och behörighetsprinciper kan bli svårare. Sara föreslår därför att teamet får stor frihet i implementationen, men att datamodell, behörighetsprincip och spårbarhet dokumenteras som arkitekturbeslut.

Det gör att teamet kan fortsätta utan att allt behöver lyftas till arkitekturforumet.

### Fråga 4: Vilket lärande behöver vi skapa?

Sara frågar vad första inkrementet faktiskt ska lära organisationen.

Är syftet att testa användarvärde? Att minska teknisk risk? Att pröva ett nytt arbetssätt mellan team och säkerhet? Att se om äldre system klarar belastningen? Att förstå handläggarnas informationsbehov?

När gruppen svarar blir det tydligare vad som ska följas upp. Det första inkrementet behöver inte bara leverera funktion. Det behöver också skapa kunskap inför nästa beslut.

### Fråga 5: Hur gör vi beslutet synligt?

Till sist hjälper Sara gruppen att dokumentera beslutet kort:

- Vad har vi beslutat?
- Varför?
- Vilka antaganden bygger beslutet på?
- Vilka risker accepterar vi?
- När behöver vi ompröva beslutet?
- Vem behöver känna till det?

Beslutet blir inte ett stort dokument. Det blir en användbar beslutslogg som både teamet, förvaltningen, säkerhetsfunktionen och arkitekturforumet kan förstå.

## Verktygslåda: fem praktiska arbetssätt

### 1. Beslutsradarn

Beslutsradarn är ett enkelt sätt att upptäcka när en vardagsfråga egentligen är ett arkitekturbeslut.

Fråga:

- Påverkar detta fler än ett team?
- Påverkar detta data, säkerhet, integration eller förvaltning?
- Blir detta svårt att ändra senare?
- Skapar detta ett beroende?
- Behöver andra kunna förstå beslutet om sex månader?

Om svaret är ja på någon av frågorna är det troligen inte bara en lokal detalj. Då behöver beslutet synliggöras, även om det fortfarande kan fattas nära teamet.

### 2. Startvillkor utan fasgrind

När ett team vill börja bygga kan arkitekten använda startvillkor som stöd i stället för som godkännandegrind.

Exempel på startvillkor:

- Vi vet vilken användar- eller verksamhetsnytta första inkrementet ska pröva.
- Vi vet vilka säkerhets- och informationsfrågor som inte får lämnas öppna.
- Vi vet vilka beroenden som kan stoppa arbetet.
- Vi vet vilka arkitekturbeslut som behöver dokumenteras.
- Vi vet vad första inkrementet ska hjälpa oss att lära.

Startvillkor ska vara lätta nog att använda, men tydliga nog att skydda arbetet från onödig risk.

### 3. Principer före detaljstyrning

När flera team behöver fatta många designbeslut fungerar detaljgodkännande dåligt. Då behöver arkitekten formulera principer.

En bra princip är:

- begriplig,
- användbar i vardagen,
- möjlig att följa upp,
- tydlig med varför den finns,
- inte mer detaljerad än nödvändigt.

Exempel:

> “Personuppgifter ska inte kopieras mellan system utan tydligt syfte, ansvar och rensningsregel.”

En sådan princip hjälper teamen att fatta beslut utan att Sara behöver godkänna varje lösningsdetalj.

### 4. Dokumentation med mottagare

Innan dokumentation tas fram bör arkitekten fråga:

- Vem ska använda detta?
- Vilket beslut, vilken samordning eller vilket ansvar ska dokumentationen stödja?
- Hur ofta behöver den uppdateras?
- Vad händer om den inte finns?
- Vad händer om den finns men inte används?

Det flyttar dokumentation från leveransprodukt till arbetsredskap.

### 5. Forumfrågan

Innan något lyfts till arkitekturforum kan arkitekten fråga:

- Behöver forumet fatta beslut?
- Behöver forumet ge riktning?
- Behöver forumet undanröja hinder?
- Behöver forumet bara informeras?
- Kan frågan avgöras närmare teamet inom befintliga principer?

Det hjälper forumet att bli en stödstruktur snarare än en kö.

## Vanliga fallgropar

- Fallgrop: Att göra verktygslådan till en ny process.
  - Varför den uppstår: Organisationer som vill skapa ordning kan snabbt omvandla frågor och arbetssätt till obligatoriska steg.
  - Vad arkitekten kan göra i stället: Behandla verktygen som stöd för professionellt omdöme, inte som en ny fasmodell.

- Fallgrop: Att tolka agil arkitektur som mindre arkitektur.
  - Varför den uppstår: När fokus ligger på snabbare leveranser kan arkitektur misstas för något tungt eller försenande.
  - Vad arkitekten kan göra i stället: Visa hur arkitektur kan minska väntan, beroenden och omarbete genom tydliga principer och beslut i rätt tid.

- Fallgrop: Att tro att allt ska beslutas nära teamet.
  - Varför den uppstår: Teamautonomi kan ibland tolkas som att varje team ska kunna fatta alla beslut själv.
  - Vad arkitekten kan göra i stället: Skilj mellan lokala beslut, delade beslut och beslut som påverkar myndighetens helhet.

- Fallgrop: Att fortsätta vara den tysta kvalitetssäkraren.
  - Varför den uppstår: Erfarna arkitekter ser ofta risker tidigt, men väntar med att lyfta dem tills det finns ett tydligt underlag.
  - Vad arkitekten kan göra i stället: Dela observationer tidigt som frågor, inte som färdiga invändningar.

- Fallgrop: Att söka trygghet i dokumentation som ingen använder.
  - Varför den uppstår: Dokumentation kan kännas som kontroll även när den inte påverkar beslut eller beteenden.
  - Vad arkitekten kan göra i stället: Börja med mottagare, användning och livscykel innan dokumentet skapas.

## Frågor att ställa i situationen

När du som arkitekt hamnar i en oklar situation kan följande frågor användas som en praktisk checklista:

1. Vilken typ av fråga står vi inför?
2. Vilka perspektiv saknas i samtalet?
3. Vad behöver beslutas nu?
4. Vad kan vänta?
5. Vad behöver undersökas genom ett inkrement?
6. Vad är svårt att ändra senare?
7. Vilka antaganden styr vårt resonemang?
8. Vilka beroenden skapar eller minskar vi?
9. Vilken dokumentation behövs för att beslutet ska kunna förstås senare?
10. Vem behöver mandat, information eller stöd för att nästa steg ska fungera?

Frågorna behöver inte användas varje gång. Värdet ligger i att de hjälper arkitekten att sakta ner precis tillräckligt för att förstå situationen, utan att göra arbetet tungt.

## Reflektionsfrågor

1. Vilka av bokens situationer känner du starkast igen från din egen vardag?
2. När tenderar du att skapa trygghet genom mer förhandsarbete, och när fungerar det väl?
3. Vilka beslut i din organisation fattas för långt från den kunskap som behövs?
4. Vilka beslut fattas för lokalt och borde synliggöras mer?
5. Vilka arkitekturprinciper skulle hjälpa teamen att fatta bättre beslut utan att fråga dig varje gång?
6. Vilken dokumentation i din miljö används faktiskt, och vilken finns mest för att den förväntas finnas?
7. Hur kan du öka din arkitektoniska närvaro utan att bli en flaskhals?
8. Vilket litet beteende kan du pröva i nästa möte för att bidra mer agilt?

## Snabb sammanfattning

- Den agila arkitekten slutar inte ta ansvar för helhet, kvalitet och långsiktighet.
- Ansvarstagandet sker mer genom närvaro, frågor, principer, beslut i rätt tid och stöd till teamens beslutsförmåga.
- Arkitektonisk närvaro handlar om att vara nära viktiga beslut utan att äga alla beslut.
- Reflekterande arkitektpraktik handlar om att undersöka hur det egna beteendet påverkar flöde, lärande och kvalitet.
- Situationsbaserat arkitektledarskap handlar om att kunna vara tydlig, utforskande, möjliggörande eller bromsande beroende på vad situationen kräver.
- Verktygslådan består av praktiska stöd: beslutsradar, startvillkor utan fasgrind, principer före detaljstyrning, dokumentation med mottagare och forumfrågan.
- Bokens kärna är att arkitekten utvecklar organisationens förmåga att fatta bra arkitektur- och designbeslut över tid.

## Nästa steg

Boken är nu komplett som första kapitelutkast. Nästa steg är inte att lägga till fler kapitel, utan att granska helheten.

En lämplig fortsättning är att göra en första sammanhängande genomläsning med tre frågor:

1. Håller boken en konsekvent ton: kollegial, reflekterande och myndighetsnära?
2. Introduceras begreppen i rätt ordning och används de konsekvent?
3. Bildar Saras resa genom Myndigheten för samhällstjänster en tydlig progression från fasorienterad trygghet till agil arkitektpraktik?

Efter en sådan granskning kan boken bearbetas kapitel för kapitel, kompletteras med checklistor eller förberedas för export till exempelvis DOCX, PDF eller EPUB.
