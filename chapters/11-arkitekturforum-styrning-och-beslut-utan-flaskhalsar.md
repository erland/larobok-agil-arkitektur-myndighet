# Kapitel 11: Arkitekturforum, styrning och beslut utan flaskhalsar

## Varför detta kapitel finns

I många myndigheter finns etablerade forum för arkitektur, säkerhet, portföljstyrning, prioritering och förändringsbeslut. De finns ofta av goda skäl. Myndigheten behöver kunna ta ansvar för helheten, följa regler, använda resurser klokt och undvika att enskilda initiativ skapar problem för andra delar av verksamheten.

När utvecklingen blir mer agil uppstår ändå en återkommande spänning. Teamen behöver kunna fatta beslut nära arbetet och röra sig framåt utan lång väntan. Samtidigt behöver organisationen säkerställa att viktiga arkitekturfrågor inte löses lokalt på ett sätt som skapar risker, dubbelarbete eller långsiktiga låsningar.

Arkitekten hamnar ofta mellan dessa behov. Å ena sidan vill Sara inte att teamen ska behöva vänta på forum för frågor de själva kan hantera. Å andra sidan vet hon att vissa beslut påverkar fler än ett team, flera system, säkerhet, förvaltning och framtida handlingsutrymme. Då räcker det inte att säga att teamet “äger lösningen”.

Det här kapitlet handlar om hur arkitekturforum och styrning kan stödja agil utveckling utan att bli en flaskhals. Fokus ligger inte på att avskaffa forum, utan på att tydliggöra vad de ska vara bra på.

Kapitlets centrala skifte är:

> Från arkitekturforum som granskande godkännandepunkt till arkitekturforum som stödstruktur för riktning, mandat, lärande och beslut i rätt tid.

## Situationen: forumet både behövs och bromsar

På Myndigheten för samhällstjänster finns ett arkitekturforum som träffas varannan torsdag. Forumet består av flera arkitekter, representanter från IT-styrning, säkerhet, förvaltning och ibland verksamhet. I forumets uppdrag står att det ska “säkerställa arkitekturell kvalitet och följsamhet mot myndighetens principer”.

I praktiken har forumet blivit en plats där många typer av frågor hamnar:

- team som vill få en lösningsskiss godkänd,
- projekt som behöver ett arkitekturutlåtande inför styrgrupp,
- integrationsfrågor som påverkar flera system,
- undantag från tekniska riktlinjer,
- säkerhetsfrågor som inte hittat någon annan beslutsväg,
- förvaltningsfrågor som kräver samordning,
- frågor där ingen riktigt vet vem som har mandat.

Sara ser att forumet gör nytta. Det fångar upp beroenden, skapar gemensam riktning och gör att viktiga frågor inte försvinner i lokala teamdiskussioner.

Samtidigt börjar teamen uppleva forumet som en kö.

Lina, teamets utvecklingsledare, säger:

> “Vi vill gärna göra rätt, men om varje större fråga måste vänta på nästa forum tappar vi tempo. Ibland behöver vi bara veta om vi är på rätt väg.”

Erik, produktägaren, uttrycker en annan frustration:

> “Vi får ofta nya frågor från forumet, men inte alltid ett tydligt beslut. Då blir det svårt att planera nästa steg.”

Amir, som representerar säkerhet och dataskydd, tycker samtidigt att teamen ibland kommer för sent:

> “När frågan väl kommer hit har lösningen redan börjat byggas. Då blir det svårt att påverka utan att det upplevs som stopp.”

Sara känner igen mönstret. Forumet är inte problemet i sig. Problemet är att det används för många olika syften samtidigt: rådgivning, granskning, beslut, förankring, eskalering, informationsdelning och ibland risköverföring.

När ett forum blir allt detta på en gång blir det lätt en flaskhals.

## Det invanda sättet att agera

I en mer fasorienterad utvecklingslogik är det vanligt att forum används som tydliga kontroll- och beslutspunkter. Ett projekt tar fram underlag, presenterar en lösning, får synpunkter och går sedan vidare till nästa fas eller beslut.

Det kan fungera väl när arbetet rör sig i större steg och när underlagen är relativt stabila. Forumet får då en tydlig roll: att granska, kvalitetssäkra, förankra och fatta beslut innan nästa större åtagande görs.

Det invanda sättet att agera kan se ut så här:

1. Teamet eller projektet tar fram en lösningsbeskrivning.
2. Arkitekten sammanställer risker, beroenden och vägval.
3. Ärendet bokas in till arkitekturforum.
4. Forumet ställer frågor och begär kompletteringar.
5. Teamet återkommer vid nästa tillfälle.
6. Beslut eller rekommendation dokumenteras.
7. Arbetet går vidare.

I en fasorienterad logik kan detta skapa trygghet. Det finns en tydlig punkt där organisationen samlar sig, granskar och bekräftar att lösningen är tillräckligt genomtänkt.

Men när utvecklingen sker i kortare cykler förändras förutsättningarna. Frågorna kommer oftare, underlagen är mer rörliga och många beslut är mindre än de beslut forumet tidigare var byggt för. Då riskerar det invanda arbetssättet att ge samma processvikt till små, medelstora och stora beslut.

Det leder till tre vanliga problem.

För det första blir forumet överbelastat. Om alla frågor ska dit får de frågor som verkligen behöver gemensam hantering konkurrera med frågor som kunde ha lösts närmare teamet.

För det andra blir beslut för sena. När forumet väl behandlar frågan kan teamet redan ha gjort antaganden, byggt delar av lösningen eller planerat kommande arbete utifrån en riktning som ännu inte är förankrad.

För det tredje blir ansvar otydligt. Om forumet förväntas godkänna mycket kan team och arkitekter börja vänta på forumet även i frågor där de egentligen har tillräcklig kunskap och mandat.

## Varför det kan skapa friktion i agil utveckling

Agil utveckling bygger inte på att alla får bestämma allt lokalt. Den bygger heller inte på att styrning försvinner. Men den förutsätter att beslut kan fattas med rimlig hastighet, nära den kunskap som behövs och med lagom mycket koordinering.

När arkitekturforum blir en generell godkännandepunkt uppstår flera former av friktion.

### Väntan ersätter ansvar

Om teamet vet att forumet ändå ska godkänna en lösning kan det bli rationellt att vänta. Frågan flyttas från dem som har mest aktuell kunskap till dem som har formellt mandat. Då tappar organisationen både tempo och lärande.

Det kan också påverka arkitektens roll. Sara riskerar att bli den som “tar frågan till forumet” i stället för den som hjälper teamet att förstå vilket beslut de själva kan fatta, vilket beslut som behöver förankras och vilket beslut som bör eskaleras.

### Forumet får frågor i fel mognadsgrad

Ett forum kan få frågor för tidigt eller för sent.

För tidigt betyder att frågan ännu är så osäker att forumet inte kan fatta ett meningsfullt beslut. Då blir mötet mest en diskussion som avslutas med att teamet behöver återkomma.

För sent betyder att lösningen redan har fått form. Då blir forumets synpunkter svåra att ta om hand utan omarbete, irritation eller förhandling.

I båda fallen uppstår friktion eftersom forumet inte är kopplat till rätt beslutstidpunkt.

### Granskning blandas ihop med stöd

Ett forum som både ska stötta, granska och besluta behöver vara tydligt med vilket läge det befinner sig i. Annars kan teamet komma för rådgivning men uppleva sig granskat. Eller så kommer teamet för beslut men får i stället allmänna råd.

Det skapar osäkerhet:

- Är detta ett beslut eller en rekommendation?
- Behöver teamet ändra lösningen eller bara överväga synpunkterna?
- Vem äger risken om teamet går vidare?
- Vad betyder det att forumet “inte har några invändningar”?

Agilt arbete kräver inte mindre tydlighet än fasorienterat arbete. Ofta kräver det mer tydlighet, eftersom besluten är fler, mindre och mer utspridda.

### Lokala beslut får oavsiktliga helhetseffekter

Om forumet å andra sidan kopplas bort helt kan team fatta beslut som var för sig verkar rimliga, men som tillsammans skapar problem:

- flera team bygger egna integrationsmönster,
- samma information modelleras på olika sätt,
- säkerhetslösningar blir inkonsekventa,
- förvaltningen får fler tekniska varianter att hantera,
- myndigheten tappar överblick över kritiska beroenden.

Det här är skälet till att kapitlets budskap inte är “mindre styrning”. Budskapet är bättre placerad styrning.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt till arkitekturforum börjar med att skilja på fyra olika behov:

1. behov av riktning,
2. behov av stöd,
3. behov av beslut,
4. behov av lärande.

Ett forum som blandar ihop dessa behov blir lätt otydligt. Ett forum som skiljer dem åt kan bli ett viktigt stöd för agil utveckling.

### Forumet som riktning

Vissa frågor bör inte behöva lösas om och om igen av varje team. Myndigheten behöver gemensamma principer, målarkitekturer, tekniska riktlinjer och överenskomna mönster.

Här kan arkitekturforumet skapa riktning genom att svara på frågor som:

- Vilka integrationsprinciper ska vi normalt följa?
- Vilka tekniska plattformar är strategiska?
- Vilka avvikelser är acceptabla och hur dokumenteras de?
- Vilka kvalitetsattribut är särskilt viktiga i våra digitala tjänster?
- Vilka arkitekturella risker ser vi över flera initiativ?

När forumet är bra på riktning behöver färre frågor gå dit för godkännande.

### Forumet som stöd

Många frågor behöver inte beslut direkt. De behöver klargörande, gemensam förståelse eller tidig dialog.

Ett stödjande forum kan hjälpa team att tänka tidigare:

- “Vilka beroenden har ni identifierat?”
- “Vilka beslut är svårreversibla?”
- “Vilka risker behöver säkerhet eller förvaltning titta på?”
- “Vilken dokumentation behöver finnas för att andra ska kunna förstå beslutet?”
- “Vilka alternativ har ni valt bort, och varför?”

När forumet används tidigt som stöd kan senare godkännande ofta bli mindre dramatiskt, eller helt onödigt.

### Forumet som beslutspunkt

Vissa frågor behöver ändå formellt beslut eller tydlig förankring. Det gäller särskilt beslut som påverkar flera team, myndighetens gemensamma plattformar, informationshantering, säkerhet, långsiktiga kostnader eller avsteg från beslutade principer.

Men då behöver forumet vara tydligt:

- Vilket beslut ska fattas?
- Vilka alternativ finns?
- Vad rekommenderas?
- Vilka konsekvenser får beslutet?
- Vem har mandat att fatta beslutet?
- Hur dokumenteras beslutet?
- Hur kommuniceras det till berörda?

Ett agilt arkitekturforum bör inte fatta fler beslut än nödvändigt. Men de beslut det faktiskt fattar behöver vara tydliga nog att hjälpa arbetet framåt.

### Forumet som lärande

När utvecklingen sker iterativt behöver även arkitekturforum lära sig. Forumet bör inte bara fråga om teamen följer riktlinjer. Det bör också fånga upp när riktlinjerna inte längre hjälper.

Exempel på lärandefrågor:

- Vilka frågor kommer ofta tillbaka?
- Var skapar våra principer otydlighet?
- Vilka beslut hamnar för ofta för sent?
- Vilka typer av ärenden fastnar i forumet?
- Vilka beroenden borde lösas strukturellt i stället för att hanteras ärende för ärende?

På så sätt blir forumet inte bara en plats där team granskas. Det blir en plats där organisationens arkitekturförmåga utvecklas.

## Beslutsflöde

Ett centralt begrepp i kapitlet är beslutsflöde.

Med beslutsflöde menar vi hur en fråga rör sig från att den upptäcks till att den blir ett fattat, kommunicerat och omsatt beslut.

I ett svagt beslutsflöde händer ofta något av följande:

- ingen vet om frågan är ett beslut, en risk eller bara en diskussion,
- frågan studsar mellan team, arkitekt, forum och styrgrupp,
- beslut fattas men kommuniceras inte tydligt,
- beslut dokumenteras men påverkar inte arbetet,
- forumet ger synpunkter men ingen vet om de är bindande,
- samma fråga återkommer i flera forum.

Ett starkare beslutsflöde gör det tydligt:

1. Vad är frågan?
2. Varför behöver den hanteras?
3. Vilken typ av beslut handlar det om?
4. Vem har kunskap?
5. Vem har mandat?
6. När behöver beslutet fattas?
7. Hur ska beslutet dokumenteras?
8. Hur ska beslutet följas upp?

För Sara innebär detta att hennes uppgift inte bara är att förbereda underlag till forumet. Hon behöver hjälpa organisationen att forma själva vägen från fråga till beslut.

Det kan vara en enkel förbättring att varje arkitekturärende till forumet tydligt märks med ärendetyp:

| Ärendetyp | Syfte | Exempel |
|---|---|---|
| Tidig dialog | Få perspektiv innan vägval låses | “Vi ser tre möjliga integrationsmönster och vill pröva resonemanget.” |
| Rekommendation | Få stöd för en föreslagen riktning | “Teamet rekommenderar alternativ B, men vill förankra konsekvenserna.” |
| Beslut | Få ett tydligt ja, nej eller villkorat beslut | “Vi behöver besluta om undantag från standardmönstret.” |
| Eskalering | Lyfta en fråga som inte kan lösas lokalt | “Två initiativ prioriterar samma plattformsresurs.” |
| Lärande | Återföra erfarenheter till gemensamma principer | “Det beslutade mönstret fungerar inte bra i den här typen av ärenden.” |

En sådan enkel klassning minskar risken att forumet behandlar alla frågor på samma sätt.

## Mandat nära kunskap

Ett annat centralt begrepp är mandat nära kunskap.

Principen betyder att beslut bör fattas så nära relevant kunskap som möjligt, men inom tydliga ramar. Det betyder inte att alla beslut ska fattas av teamet. Det betyder att varje beslut bör placeras där kombinationen av kunskap, konsekvensförståelse och mandat är bäst.

Vissa beslut hör hemma nära teamet:

- val av intern kodstruktur,
- detaljer i implementationen,
- mindre designbeslut som följer etablerade principer,
- tekniska förbättringar inom teamets komponenter,
- justeringar som är lätta att ändra senare.

Andra beslut behöver arkitektens aktiva stöd:

- mönster för integration,
- informationsmodellering som påverkar flera system,
- avvägningar mellan kortsiktig leverans och teknikskuld,
- designbeslut med påverkan på säkerhet, spårbarhet eller förvaltning,
- frågor där flera team behöver samordnas.

Ytterligare andra beslut behöver forum eller styrning:

- avsteg från gemensamma arkitekturprinciper,
- val av ny strategisk plattform,
- beslut som påverkar flera förvaltningsområden,
- riskacceptans på nivåer teamet inte äger,
- större beroenden mellan initiativ,
- beslut som påverkar myndighetens långsiktiga kostnader eller ansvar.

Sara kan hjälpa genom att inte fråga “ska detta till forumet?” för tidigt. En bättre första fråga är:

> “Var finns den kunskap och det mandat som behövs för att fatta ett bra beslut?”

Ibland är svaret teamet. Ibland är svaret arkitekten tillsammans med teamet. Ibland är svaret ett forum. Ibland är svaret att forumet inte ska fatta beslutet, men behöver skapa riktning så att andra kan fatta beslut snabbare.

## Arkitekturforum som stödstruktur

Ett arkitekturforum blir en stödstruktur när det hjälper arbetet framåt även när det inte fattar beslut.

Det kan göra det genom att:

- tydliggöra principer,
- förenkla beslutsvägar,
- synliggöra beroenden,
- hjälpa team att hitta rätt personer tidigt,
- upptäcka återkommande hinder,
- minska behovet av sena granskningar,
- skapa gemensamt språk för arkitekturbeslut,
- följa upp om beslut faktiskt fungerar.

Ett stödjande forum är inte passivt. Det är inte bara ett rådgivande samtal utan konsekvens. Men dess primära värde är inte att säga ja eller nej. Värdet är att öka organisationens förmåga att fatta bra beslut där besluten hör hemma.

Det kan låta mindre kraftfullt än ett godkännandeorgan, men i agil utveckling kan det vara mer effektivt.

Om forumet lyckas skapa tydliga principer, snabba återkopplingsvägar och rätt mandat nära kunskap behöver färre frågor vänta. Samtidigt får myndigheten bättre helhet än om varje team löser allt själv.

## Exempel: Myndigheten för samhällstjänster

Efter flera möten där ärenden fastnat bestämmer sig Sara för att föreslå en förändring i hur arkitekturforumet arbetar.

Hon börjar inte med att föreslå en ny organisationsmodell. I stället tar hon med tre observationer till forumet:

1. Många ärenden kommer in som “beslutsärenden”, men visar sig egentligen vara behov av tidig dialog.
2. Teamen upplever att forumet ger många synpunkter men ibland otydliga beslut.
3. Forumet lägger mycket tid på frågor som kunde ha hanterats med tydligare principer eller mandat.

Sara föreslår tre små förändringar.

För det första ska varje ärende märkas med ärendetyp: tidig dialog, rekommendation, beslut, eskalering eller lärande.

För det andra ska varje beslutsärende innehålla en kort beslutsruta:

```markdown
Beslut som behövs:
Rekommenderat alternativ:
Alternativ som valts bort:
Konsekvenser:
Berörda team/system:
Föreslaget beslutsmandat:
Hur beslutet dokumenteras:
```

För det tredje ska forumet avsluta varje ärende med en tydlig formulering:

- “Beslut fattat: …”
- “Rekommendation: …”
- “Ingen invändning, teamet har mandat att gå vidare.”
- “Komplettering behövs före beslut: …”
- “Frågan hör hemma i annat forum eller hos annan beslutsägare: …”

Vid nästa möte tar Lina upp en fråga om hur den nya medborgartjänsten ska hämta ärendestatus från det äldre handläggningssystemet. Tidigare hade teamet kanske försökt få hela lösningen godkänd. Nu märks ärendet som tidig dialog.

Teamet presenterar tre alternativ:

1. direkt anrop mot det äldre systemet,
2. ett nytt API-lager,
3. en händelsebaserad lösning där statusändringar publiceras till en gemensam komponent.

Forumet fattar inget slutligt beslut. Däremot hjälper det teamet att se att alternativ 1 kan vara snabbt men riskerar stark koppling, att alternativ 2 kan vara rimligt som första steg och att alternativ 3 kan vara en långsiktig riktning men kräver mer samordning.

Sara sammanfattar:

> “Teamet har mandat att gå vidare och testa alternativ 2 som begränsad lösning, men beslutet ska dokumenteras som ett arkitekturbeslut. Forumet vill se en återkoppling om vilka beroenden som kvarstår och om lösningen bör utvecklas mot den händelsebaserade riktningen senare.”

Det viktiga är inte att forumet löser allt. Det viktiga är att teamet kan gå vidare med tydligare ramar, och att organisationen lär sig något som kan påverka framtida principer.

## Vanliga fallgropar

- Fallgrop: Alla större frågor ska till forumet.
  - Varför den uppstår: Organisationen vill undvika lokala beslut som skapar långsiktiga problem.
  - Vad arkitekten kan göra i stället: Hjälp till att skilja mellan beslut som kräver forum, frågor som bara behöver tidig dialog och beslut som teamet kan fatta inom givna principer.

- Fallgrop: Forumet ger synpunkter men inga beslut.
  - Varför den uppstår: Det är oklart om forumet är rådgivande, beslutande eller granskande i det aktuella ärendet.
  - Vad arkitekten kan göra i stället: Kräv att ärendetyp och önskat utfall är tydligt innan frågan tas upp.

- Fallgrop: Teamen kommer för sent.
  - Varför den uppstår: Forumet upplevs som en sen kontrollpunkt snarare än ett stöd i tidiga vägval.
  - Vad arkitekten kan göra i stället: Skapa lättare former för tidig dialog, till exempel korta arkitektursamtal innan formella ärenden.

- Fallgrop: Forumet blir en ersättning för mandat.
  - Varför den uppstår: Ingen vill äga svåra beslut, och forumet blir en plats där ansvar sprids ut.
  - Vad arkitekten kan göra i stället: Synliggör vem som har kunskap, vem som har mandat och vem som behöver acceptera risk.

- Fallgrop: Styrning tolkas som godkännande.
  - Varför den uppstår: Organisationen har lärt sig att kvalitetssäkring sker genom att någon högre upp säger ja.
  - Vad arkitekten kan göra i stället: Visa att styrning också kan ske genom principer, ramar, beslutsloggar, återkoppling och uppföljning.

- Fallgrop: Forumet optimerar för enskilda ärenden.
  - Varför den uppstår: Varje ärende behandlas för sig, utan att återkommande mönster fångas.
  - Vad arkitekten kan göra i stället: Avsätt tid för lärande: vilka ärenden återkommer, vilka principer saknas och vilka hinder behöver lösas strukturellt?

## Frågor att ställa i situationen

När du som arkitekt står inför frågan om ett ärende ska till forum, kan följande frågor hjälpa:

1. Vad är det egentliga beslutet?
2. Är frågan mogen för beslut, eller behöver den tidig dialog?
3. Vilka alternativ finns?
4. Vilka konsekvenser får beslutet för andra team, system eller förvaltningsområden?
5. Är beslutet reversibelt eller svårreversibelt?
6. Vem har bäst kunskap om frågan?
7. Vem har mandat att acceptera konsekvenserna?
8. Vilka principer eller tidigare beslut påverkar frågan?
9. Behöver forumet fatta beslut, ge rekommendation, undanröja hinder eller bara bli informerat?
10. Hur ska beslutet dokumenteras så att andra kan förstå det senare?

En särskilt användbar fråga är:

> “Vad behöver hända efter forumet för att arbetet faktiskt ska kunna gå vidare?”

Om svaret är oklart är ärendet troligen inte tillräckligt tydligt formulerat.

## Reflektionsfrågor

1. Vilka typer av frågor hamnar oftast i arkitekturforum eller motsvarande styrningsforum i din organisation?
2. Vilka av dessa frågor behöver verkligen forumets beslut?
3. Vilka frågor skulle kunna hanteras snabbare med tydligare principer eller mandat nära teamen?
4. När upplever teamen att forumet hjälper dem framåt?
5. När upplever teamen att forumet främst skapar väntan?
6. Hur tydligt skiljer ni mellan rådgivning, rekommendation och beslut?
7. Vilka beslut fattas i dag för långt från den kunskap som behövs?
8. Vilka återkommande ärenden visar att organisationen saknar en gemensam princip eller riktning?
9. Hur kan du som arkitekt bidra till bättre beslutsflöde utan att själv bli den nya flaskhalsen?

## Snabb sammanfattning

- Arkitekturforum och styrning behövs även i agil utveckling, särskilt i myndighetsmiljö där ansvar, säkerhet, spårbarhet och helhet är viktiga.
- Friktion uppstår när forumet används som generell godkännandepunkt för frågor som egentligen behöver olika typer av hantering.
- Ett mer agilt forum skiljer mellan riktning, stöd, beslut och lärande.
- Beslutsflöde handlar om hur en fråga rör sig från upptäckt till tydligt beslut, kommunikation och uppföljning.
- Mandat nära kunskap innebär att beslut placeras där relevant kunskap och rätt mandat möts.
- Arkitekturforum bör fungera som stödstruktur: skapa riktning, undanröja hinder, synliggöra beroenden och hjälpa organisationen att fatta bättre beslut över tid.
- Arkitektens uppgift är inte bara att ta ärenden till forum, utan att hjälpa organisationen förstå vilka beslut som behövs, var de hör hemma och hur de ska följas upp.

## Nästa steg

I det här kapitlet har vi sett hur arkitekturforum och styrning kan gå från flaskhals till stödstruktur. Det avslutar bokens tredje del om hållbart agilt arkitekturarbete i myndighetsmiljö.

Nästa kapitel samlar bokens viktigaste arbetssätt i en praktisk verktygslåda. Där återvänder vi till Sara och de återkommande situationerna för att formulera frågor, principer och förhållningssätt som arkitekten kan bära med sig i vardagen.
