# Kapitel 5: När kravarbete blir löpande snarare än avslutat

## Varför detta kapitel finns

För många arkitekter är kravarbete en central del av vägen mot en fungerande lösning. Krav hjälper till att avgränsa, prioritera, analysera konsekvenser och skapa underlag för design. Särskilt i en myndighetsmiljö kan krav dessutom behöva bära spårbarhet, rättssäkerhet, informationssäkerhet och ansvar. Det är därför naturligt att arkitekten vill att kravbilden ska vara tillräckligt tydlig innan viktiga arkitekturbeslut fattas.

I ett mer fasorienterat arbetssätt är det vanligt att kravarbete får karaktären av en leverans. Behov analyseras, krav dokumenteras, lösningsförslag tas fram och först därefter startar utvecklingen på allvar. Det ger en känsla av ordning: krav först, design sedan, utveckling därefter.

I agil IT-utveckling förändras detta. Kravarbete upphör inte, men det blir mer löpande. Krav preciseras, omprövas och kompletteras när organisationen lär sig mer. En *backlog*, alltså en prioriterad lista över sådant som kan behöva göras, ersätter ofta den färdiga kravspecifikationen som det huvudsakliga arbetsunderlaget för teamet. Det kan vara både kraftfullt och frustrerande.

För arkitekten uppstår en viktig fråga: hur kan arkitektur och design ta höjd för krav som ännu inte är fullständigt formulerade?

Det här kapitlet handlar om just den situationen. Fokus är inte att överge kravarbete, utan att förändra hur arkitekten samverkar med krav, verksamhet och team när detaljer växer fram över tid.

## Situationen: “Det ligger i backloggen, men det är inte färdigkravställt”

På Myndigheten för samhällstjänster fortsätter arbetet med den nya digitala medborgartjänsten. Teamet har börjat bygga en första begränsad vy där medborgaren ska kunna se status för sitt ärende. Erik, produktägaren, har prioriterat ett antal backloggposter som han menar ger snabb nytta:

- Visa aktuell ärendestatus.
- Visa senaste datum för komplettering.
- Ge möjlighet att ladda upp en bilaga.
- Skicka avisering när status ändras.

Sara tittar på backloggen och ser att varje post är kortfattad. Hon saknar flera saker som hon normalt hade förväntat sig i en kravspecifikation:

- Vilka statusvärden får visas för medborgaren?
- Är statusvärdena samma som handläggarna ser internt?
- Ska olika ärendetyper visa olika information?
- Hur ska bilagor viruskontrolleras, klassificeras och kopplas till ärendet?
- Vilka metadata behöver sparas?
- Vilka händelser ska loggas?
- Vilka krav finns på tillgänglighet och svarstider?
- Hur ska aviseringar hanteras om kontaktuppgifter saknas eller är felaktiga?

Lina från teamet säger:

> “Vi vet att allt inte är färdigt. Men vi kan börja med den enklaste ärendetypen och lära oss därifrån.”

Erik fyller i:

> “Vi vill inte skriva en full kravspecifikation innan vi vet om medborgarna ens förstår statusinformationen.”

Sara förstår poängen. Samtidigt ser hon risken. Om teamet börjar bygga utifrån för tunna krav kan viktiga arkitekturfrågor komma för sent. Om bilagehantering byggs enkelt nu men senare visar sig kräva starkare spårbarhet, informationsklassning och arkivering kan det bli dyrt att rätta. Om statusinformationen bygger direkt på interna koder i det gamla systemet kan tjänsten bli svår att förändra.

Det invanda sättet att agera vore att be om mer kravarbete innan teamet fortsätter. Men i den här situationen är frågan inte om kraven ska bli tydligare. Det ska de. Frågan är hur tydliggörandet ska ske utan att arbetet förvandlas till en ny kravfas vid sidan av utvecklingen.

## Det invanda sättet att agera

När kravbilden är ofullständig är det lätt att arkitekten försöker återskapa den trygghet som en komplett kravspecifikation brukar ge. Det kan visa sig på flera sätt.

Arkitekten kan be om att kraven “måste bli klara” innan designen kan fortsätta. Det kan vara rimligt när viktiga rättsliga, säkerhetsmässiga eller tekniska förutsättningar saknas. Men det kan också bli ett sätt att skjuta lärandet framför sig.

Arkitekten kan börja fylla i luckorna själv. Det är vanligt att erfarna arkitekter snabbt ser vad som saknas och därför börjar formulera antaganden om informationsmodell, integrationsmönster, behörighet, loggning och förvaltningsbarhet. Det kan hjälpa arbetet framåt, men det kan också leda till att arkitekten i praktiken tar över kravtolkningen från verksamheten.

Arkitekten kan också försöka skapa en separat lista över arkitekturkrav vid sidan av teamets backlogg. Den listan kan innehålla viktiga saker: prestanda, säkerhet, tillgänglighet, spårbarhet, integrationer och tekniska begränsningar. Problemet uppstår om listan inte kopplas till teamets prioritering och vardagliga arbete. Då riskerar arkitekturkraven att bli något som upptäcks vid granskning, snarare än något som påverkar lösningen under arbetets gång.

Bakom dessa beteenden finns ofta en legitim oro: att viktiga egenskaper ska tappas bort när kraven blir kortare, mer rörliga och mer verksamhetsnära. Den oron ska tas på allvar. Men svaret är inte alltid att återgå till mer omfattande kravdokument. Ofta behöver arkitekten i stället hjälpa organisationen att göra rätt krav tydliga vid rätt tidpunkt.

## Varför det kan skapa friktion i agil utveckling

När arkitekten kräver en mer komplett kravbild innan teamet går vidare kan det skapa friktion på flera nivåer.

För det första kan det bromsa återkoppling. Om organisationen inte vet hur medborgare tolkar statusinformationen kan en lång kravfas ge skenbar säkerhet. Den beskriver vad man tror behövs, men prövar inte om det faktiskt fungerar. I sådana lägen kan en enkel implementation, användartestning eller genomgång med handläggare ge bättre kunskap än ytterligare dokumentation.

För det andra kan det skapa parallella verkligheter. Teamet arbetar i backloggen, produktägaren prioriterar utifrån nytta och arkitekten för en separat diskussion om kravkvalitet. Då uppstår lätt glapp. Det som arkitekten ser som nödvändiga lösningsförutsättningar kan teamet uppfatta som senare granskning eller extraarbete. Det som produktägaren ser som snabb nytta kan arkitekten uppfatta som otillräckligt analyserat.

För det tredje kan kravens form bli viktigare än deras funktion. En välskriven kravspecifikation kan vara värdefull, men bara om den hjälper människor att fatta bättre beslut. Ett kort backloggobjekt kan vara otillräckligt, men det kan också vara fullt tillräckligt om teamet, produktägaren och arkitekten har en gemensam förståelse för vad som ska läras, vilka begränsningar som gäller och vilka beslut som ännu är öppna.

För det fjärde kan arkitekturfrågor komma in för sent om arkitekten väntar på “rätt” kravunderlag. I agil utveckling formas många krav i samtal, refinement, demonstrationer och återkoppling. *Refinement* betyder här att teamet och berörda roller stegvis förtydligar och delar upp arbetet så att det blir begripligt och möjligt att genomföra. Om arkitekten inte deltar i dessa samtal riskerar viktiga arkitekturfrågor att dyka upp först när teamet redan har valt riktning.

Friktionen beror alltså inte på att kravarbete har blivit oviktigt. Den beror på att kravarbete har flyttat närmare utvecklingsflödet, och att arkitekten behöver följa med dit.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt till kravarbete börjar med en enkel insikt: alla krav behöver inte vara lika detaljerade samtidigt.

Vissa krav behöver vara tydliga tidigt, eftersom de påverkar lösningens grundstruktur. Det kan handla om informationssäkerhet, rättsliga begränsningar, centrala informationsobjekt, integrationsriktning, behörighetsmodell, spårbarhet eller krav på arkivering. Om dessa frågor hanteras för sent kan de påverka stora delar av lösningen.

Andra krav kan förfinas stegvis. Det kan handla om exakt formulering av texter, ordning på fält, detaljer i användarflöden eller vilka statusmeddelanden som ger bäst förståelse för medborgaren. Dessa krav kan ofta bli bättre genom prototyper, användaråterkoppling och successiv utveckling.

Arkitektens uppgift blir att hjälpa organisationen att skilja mellan dessa kravtyper.

### Löpande kravförfining

Löpande kravförfining innebär att krav inte ses som färdiga en gång för alla. De förtydligas när ny kunskap uppstår. Det betyder inte att allt är flytande eller informellt. Det betyder att kravens detaljnivå anpassas efter risk, närhet till implementation och beslutens konsekvens.

För Sara innebär det att hon inte behöver kräva en komplett kravspecifikation för hela medborgartjänsten. Däremot behöver hon vara tydlig med vilka frågor som måste upp på bordet innan teamet bygger vissa delar.

Hon kan till exempel säga:

> “För att börja visa ärendestatus för en begränsad ärendetyp behöver vi inte ha hela tjänsten färdigkravställd. Men vi behöver förstå vilka statusvärden som får visas externt, om de behöver översättas från interna begrepp och vilken spårbarhet som krävs när status visas för medborgaren.”

Det är en annan typ av kravdialog. Den frågar inte efter allt. Den frågar efter det som behövs för nästa meningsfulla beslut.

### Icke-funktionella krav som kontinuerlig dialog

Icke-funktionella krav är krav på egenskaper hos lösningen, till exempel säkerhet, prestanda, tillgänglighet, robusthet, användbarhet, spårbarhet och förvaltningsbarhet. I en traditionell kravspecifikation får de ofta ett eget avsnitt. I agil utveckling behöver de också finnas i samtalen där arbetet planeras, delas upp och genomförs.

Det är särskilt viktigt i myndighetsmiljö. Krav på rättssäkerhet, informationssäkerhet, tillgänglighet och spårbarhet är inte detaljer som kan läggas till i slutet. De påverkar designen.

Samtidigt fungerar det sällan bra att formulera alla icke-funktionella krav som generella kravsatser från början. “Systemet ska vara säkert” eller “lösningen ska vara förvaltningsbar” hjälper inte teamet särskilt mycket. Arkitektens bidrag är att göra sådana krav situationsspecifika.

För bilageuppladdning kan Sara till exempel hjälpa teamet att ställa frågor som:

- Vilka filtyper ska tillåtas?
- Hur hanteras skadlig kod?
- Vilken information får bilagan innehålla?
- När blir bilagan en allmän handling?
- Hur kopplas bilagan till rätt ärende och rätt person?
- Vilken loggning behövs för att kunna följa vad som hänt?
- Hur ska fel hanteras om uppladdningen avbryts?

På så sätt blir icke-funktionella krav inte en lista vid sidan av. De blir en del av designen.

### Krav som beslutsunderlag

I ett fasorienterat arbetssätt kan krav ibland uppfattas som beställning: verksamheten beskriver vad som ska byggas, IT tar fram lösningen. I ett mer agilt arbetssätt behöver krav ofta fungera mer som beslutsunderlag.

Det innebär att krav hjälper team, produktägare och arkitekt att förstå vilka avvägningar som behöver göras. Ett krav kan visa att det finns en konflikt mellan snabb leverans och långsiktig förvaltningsbarhet. Ett annat krav kan visa att en till synes enkel funktion egentligen kräver informationsklassning, juridisk tolkning eller förändring i ett äldre system.

När Sara ser backloggposten “Skicka avisering när status ändras” kan hon behandla den som en beställning: bygg avisering. Men hon kan också använda den som beslutsunderlag:

- Vilka statusändringar är viktiga för medborgaren?
- Får alla ärendetyper aviseras på samma sätt?
- Vilka kontaktvägar är tillåtna?
- Vad får stå i aviseringen?
- Behöver medborgaren samtycka till vissa typer av avisering?
- Vad händer om aviseringen misslyckas?
- Är aviseringen en del av myndighetens formella kommunikation eller bara en servicefunktion?

Dessa frågor behöver inte alla besvaras innan något arbete får börja. Men de behöver synliggöras så att teamet inte bygger in antaganden som senare visar sig fel.

## Exempel: Myndigheten för samhällstjänster

Sara föreslår ett arbetssätt för de kommande veckorna. Hon vill inte stoppa teamets första inkrement, men hon vill göra kravförfiningen mer arkitektoniskt medveten.

Hon ber Erik och Lina att tillsammans med henne gå igenom de högst prioriterade backloggposterna. För varje post ställer de tre frågor:

1. Vilken nytta eller vilket lärande ska denna post ge?
2. Vilka arkitektoniska eller myndighetsnära risker kan den beröra?
3. Vilka frågor måste vara besvarade innan teamet bygger just denna del?

När de går igenom “Visa aktuell ärendestatus” kommer de fram till att teamet kan börja med en begränsad ärendetyp. Men innan implementation behöver de veta om interna statuskoder kan visas direkt eller om de måste översättas till medborgarvänliga statusbegrepp. De behöver också veta om vissa statuslägen inte får visas på grund av sekretess, pågående handläggning eller risk för missförstånd.

När de går igenom “Ladda upp bilaga” blir gruppen mer försiktig. Här finns fler frågor om informationssäkerhet, handlingar, lagring, viruskontroll och koppling till ärendet. Sara föreslår därför att teamet inte börjar med full bilageuppladdning direkt. I stället kan de först undersöka flödet, informationsobjekten och säkerhetskraven. Det kan göras genom en begränsad teknisk och verksamhetsmässig genomgång, kanske tillsammans med Amir från informationssäkerhet.

När de går igenom “Skicka avisering” ser de att nyttan är tydlig, men att det finns flera oklara regel- och kommunikationsfrågor. Erik tar med sig att verksamheten behöver avgöra vilka aviseringar som är serviceinformation och vilka som kan påverka formell kommunikation med medborgaren.

Resultatet blir inte en komplett kravspecifikation. Men det blir en tydligare backlogg, där vissa poster kan gå vidare, vissa behöver delas upp och vissa behöver kompletteras med arkitektur- eller riskfrågor.

Sara dokumenterar inte allt som ett stort kravdokument. I stället kompletterar hon varje berörd backloggpost med korta arkitekturkommentarer, öppna frågor och beslut som behöver fattas. Hon skapar också en enkel lista över återkommande icke-funktionella krav som teamet ska använda vid refinement:

- informationsklassning,
- behörighet,
- loggning,
- spårbarhet,
- felhantering,
- tillgänglighet,
- förvaltningsbarhet,
- integrationspåverkan.

Det viktiga är att listan används i samtalen. Den blir inte en bilaga som någon läser senare, utan ett stöd för löpande kravförfining.

## Vanliga fallgropar

- Fallgrop: Att kräva färdiga krav innan arkitekten kan bidra.
  - Varför den uppstår: Arkitekten är van vid att krav är den stabila grund som designen vilar på.
  - Vad arkitekten kan göra i stället: Identifiera vilka krav som behöver vara tydliga nu och vilka som kan förfinas genom lärande.

- Fallgrop: Att acceptera för tunna backloggposter utan arkitekturdialog.
  - Varför den uppstår: Arkitekten vill inte bromsa teamet eller uppfattas som fasorienterad.
  - Vad arkitekten kan göra i stället: Delta i refinement och ställa frågor som synliggör risker, beroenden och kvalitetskrav.

- Fallgrop: Att lägga icke-funktionella krav i en separat lista som inte påverkar arbetet.
  - Varför den uppstår: Det känns ordnat att samla sådana krav på ett ställe.
  - Vad arkitekten kan göra i stället: Koppla kraven till konkreta backloggposter, designbeslut och acceptanskriterier där det är relevant.

- Fallgrop: Att arkitekten själv fyller i verksamhetens kravluckor.
  - Varför den uppstår: Erfarna arkitekter ser snabbt konsekvenser och vill hjälpa arbetet framåt.
  - Vad arkitekten kan göra i stället: Formulera antaganden öppet och be produktägare, verksamhet eller specialister bekräfta, avfärda eller undersöka dem.

- Fallgrop: Att behandla alla krav som lika viktiga att precisera tidigt.
  - Varför den uppstår: Det är svårt att veta vilka krav som påverkar grundstrukturen.
  - Vad arkitekten kan göra i stället: Sortera krav efter risk, reversibilitet, påverkan på arkitektur och närhet till implementation.

## Frågor att ställa i situationen

När kravarbete blir löpande kan arkitekten använda frågor som hjälper gruppen att komma vidare utan att låsa för mycket.

### Frågor om kravets funktion

- Vad behöver vi förstå för att kunna ta nästa steg?
- Ska detta krav ge användarnytta, minska risk, skapa lärande eller möjliggöra senare arbete?
- Vilket beslut ska kravet hjälpa oss att fatta?
- Vad händer om vi missförstår detta krav?

### Frågor om arkitektonisk påverkan

- Påverkar kravet informationsmodell, integrationer, behörighet, loggning eller lagring?
- Påverkar kravet hur lösningen ska förvaltas?
- Skapar kravet beroenden till andra system, team, myndigheter eller leverantörer?
- Är detta ett krav som kan ändras lätt senare, eller påverkar det svårreversibla beslut?

### Frågor om myndighetskontext

- Finns krav på rättssäkerhet, spårbarhet eller likabehandling?
- Berör kravet personuppgifter, sekretess eller informationsklassning?
- Behöver juridik, informationssäkerhet eller arkivfunktion involveras?
- Behöver beslutet dokumenteras för att kunna förstås i efterhand?

### Frågor om arbetsform

- Behöver kravet delas upp?
- Behöver det kompletteras med acceptanskriterier?
- Behöver vi en kort utforskning innan vi bygger?
- Vem behöver delta i nästa refinement för att kravet ska bli tillräckligt tydligt?

## Reflektionsfrågor

1. Vilka typer av krav brukar du själv vilja ha tydliga innan du känner dig trygg med arkitekturen?
2. När har du sett att ett krav blev tydligare först efter att teamet började bygga eller visa något?
3. Vilka icke-funktionella krav riskerar oftast att komma in för sent i din organisation?
4. Hur brukar du som arkitekt delta i refinement eller motsvarande kravdialog i dag?
5. Vilka kravluckor brukar du fylla i själv, snarare än att synliggöra dem som antaganden?
6. Hur kan du hjälpa produktägare och team att se arkitektoniska konsekvenser utan att göra kravdialogen tung?
7. Vilka krav behöver dokumenteras mer formellt i din miljö, och vilka kan hanteras genom levande dialog och tydliga beslut?
8. Vad skulle vara ett litet första steg mot mer löpande kravförfining i ditt nuvarande sammanhang?

## Snabb sammanfattning

När kravarbete blir löpande försvinner inte behovet av tydlighet. Det förändras.

Arkitekten behöver inte kräva att alla krav är färdiga innan utveckling kan börja. Däremot behöver arkitekten hjälpa organisationen att förstå vilka krav som påverkar arkitekturbeslut, vilka som kan förfinas stegvis och vilka som måste kopplas till säkerhet, spårbarhet, förvaltning och myndighetsansvar.

Ett mer agilt förhållningssätt innebär att krav, arkitektur och design utvecklas i samspel. Backloggen blir inte bara en lista över funktioner, utan ett ställe där nytta, risk, lärande och beslut möts. Arkitektens bidrag är att göra de osynliga konsekvenserna synliga i tid.

Det centrala skiftet är:

> Från: “Kraven ska vara tillräckligt kompletta för att arkitekturen ska kunna tas fram.”  
> Till: “Arkitektur- och kravarbete behöver löpande hjälpa varandra att bli tydligare.”

## Nästa steg

I nästa kapitel flyttas fokus från kravens detaljnivå till startpunkten för själva utvecklingen. Vad händer när teamet vill börja bygga innan arkitekturen känns klar? Då behöver arkitekten kunna avgöra vilka arkitektoniska startvillkor som faktiskt krävs, vilka frågor som kan undersökas genom implementation och hur “tillräcklig arkitektur” kan fungera utan att bli en ny fasgrind.
