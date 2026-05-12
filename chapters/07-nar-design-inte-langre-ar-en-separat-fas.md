# Kapitel 7: När design inte längre är en separat fas

## Varför detta kapitel finns

I många fasorienterade arbetssätt har design en tydlig plats. Först analyseras behov och krav, därefter tas en lösning eller design fram, och sedan bygger teamet utifrån den. Det kan ge ordning, spårbarhet och en känsla av kontroll. För en arkitekt är det också ett välbekant sätt att bidra: samla in information, väga alternativ, formulera designprinciper, beskriva lösningen och lämna över ett genomtänkt underlag till dem som ska realisera den.

När utvecklingen blir mer agil förändras designens rytm. Design sker inte längre bara före utveckling. Den sker också under utveckling, i små beslut, i tekniska avvägningar, i samtal mellan teammedlemmar, i refinement, i kodgranskning, i testning, i incidenter och i återkoppling från användare. Design blir mindre av en separat fas och mer av en kontinuerlig praktik.

Det betyder inte att design blir mindre viktigt. Tvärtom kan design bli viktigare, eftersom många beslut fattas närmare implementationen och därför behöver stöd av tydliga principer, gemensam förståelse och arkitektonisk närvaro. Om designarbetet blir helt lokalt och osynligt kan lösningen gradvis glida isär. Om arkitekten å andra sidan försöker hålla kvar all design som en separat kontrollpunkt kan flödet stanna och teamets lärande försvagas.

Det här kapitlet handlar om hur arkitekten kan bidra till **kontinuerlig design**: designarbete som sker löpande, men inte slumpmässigt. Målet är att skapa en balans där teamet kan fatta många lokala beslut, samtidigt som lösningen hålls ihop över tid.

Kapitlets kärnfråga är:

> Hur kan arkitekten bidra till sammanhållen design när designbesluten uppstår löpande i utvecklingsarbetet?

## Situationen: “Det där löser vi när vi bygger”

På Myndigheten för samhällstjänster arbetar teamet vidare med den nya medborgartjänsten. Efter kapitel 6 har Sara och teamet kommit överens om några arkitektoniska startvillkor. Teamet får börja med en smal läsvy för ärendestatus, men med tydliga ramar för identitet, loggning, informationskällor och vad som får visas externt.

Efter några veckor märker Sara något nytt. Teamet rör sig snabbt framåt, men många designbeslut fattas i vardagen utan att de syns särskilt tydligt.

Lina säger på ett möte:

> “Vi löste statusöversättningen i tjänstelagret tills vidare. Det var enklast.”

En utvecklare fyller i:

> “Och vi lade till en liten lokal tabell för visningsnamn, annars blev det för mycket beroende till gamla systemet.”

Erik, produktägaren, är nöjd:

> “Bra. Då kan vi visa något för verksamheten nästa vecka.”

Sara är också nöjd med framdriften. Men hon får en gnagande känsla. Varje beslut verkar rimligt i stunden. Samtidigt påverkar besluten helheten:

- Var ska verksamhetsregler egentligen ligga?
- Hur många lokala översättningar och specialfall är acceptabla?
- När blir en tillfällig tabell en del av den långsiktiga lösningen?
- Vem ser att flera små beslut tillsammans skapar en ny arkitektur?
- Hur dokumenteras varför teamet valde just denna väg?
- Hur vet nästa team vilka principer som gäller?

Det är inte så att teamet gör fel. De försöker leverera värde och lösa konkreta problem. Men design håller på att ske i många små steg. Om Sara inte är närvarande riskerar hon att upptäcka helhetsmönstret först när det redan är svårt att ändra.

Samtidigt vill hon inte säga:

> “Stopp, vi behöver en designfas.”

Det skulle skicka arbetet tillbaka till ett mönster som organisationen försöker lämna. Sara behöver i stället hitta ett sätt att göra designen synlig, gemensam och styrbar utan att dra ut den ur flödet.

## Det invanda sättet att agera

Det invanda sättet att skapa god design är ofta att samla designarbetet i en avgränsad aktivitet. Arkitekten tar fram en lösningsdesign, beskriver komponenter, gränssnitt, informationsflöden, säkerhetslösning, integrationer och centrala regler. Därefter granskas designen och används som underlag för implementation.

Detta arbetssätt har flera styrkor:

- Det tvingar fram helhetstänkande.
- Det gör viktiga avvägningar synliga innan de omsätts i kod eller konfiguration.
- Det skapar dokumentation som kan granskas och förankras.
- Det minskar risken för att olika delar av lösningen utvecklas åt olika håll.
- Det ger arkitekten möjlighet att se beroenden och konsekvenser.

I en myndighetsmiljö är dessa styrkor viktiga. Det finns ofta krav på spårbarhet, förvaltningsbarhet, säkerhet, informationshantering och ansvar. Design kan inte bara vara något som “råkar bli” medan teamet bygger.

Problemet uppstår när designfasen blir den enda plats där design anses få ske. Då kan arkitekten hamna i ett mönster där design behöver vara färdig innan utveckling får börja, och där förändringar under utvecklingen uppfattas som avvikelser från den tänkta lösningen.

Det invanda agerandet kan då bli att:

- efterfråga mer komplett design innan teamet går vidare,
- vilja granska varje större designbeslut innan implementation,
- dokumentera lösningen i detalj för att undvika missförstånd,
- hålla designansvaret nära arkitektrollen,
- se teamets löpande designbeslut som risker snarare än som nödvändiga delar av lärandet.

Detta kan vara förståeligt. Arkitekten försöker skydda helheten. Men i ett agilt utvecklingsflöde kan det också skapa distans mellan arkitektur och faktisk lösning. Designen på papper blir då något som finns bredvid arbetet, medan den verkliga designen växer fram i teamets dagliga beslut.

## Varför det kan skapa friktion i agil utveckling

Friktionen uppstår när design behandlas som en leverans i stället för som en förmåga.

I en fasorienterad logik är det ofta naturligt att fråga:

> “Är designen klar?”

I en mer agil logik behöver frågan ofta vara:

> “Har vi tillräcklig designriktning för nästa steg, och har vi ett arbetssätt som fångar upp nya designbeslut?”

Skillnaden är stor. Om design ska vara klar tidigt behöver arkitekten försöka förutse många detaljer innan teamet har lärt sig vad som faktiskt är svårt. Det kan leda till omfattande antaganden. Några av dem kommer att visa sig riktiga. Andra kommer att ändras när teamet möter verkliga data, äldre system, användarbeteenden, prestandakrav eller säkerhetsbegränsningar.

Om design däremot lämnas helt till teamets löpande arbete finns en annan risk: många små lokala beslut kan tillsammans skapa en lösning som ingen egentligen valt medvetet. Det kan handla om duplicerade regler, olika mönster för felhantering, varierande integrationssätt, olika tolkningar av säkerhetskrav eller otydliga ansvar mellan komponenter.

Friktionen visar sig ofta i vardagliga kommentarer:

- “Det där löser vi i teamet.”
- “Vi hinner inte ta upp varje detalj med arkitektur.”
- “Arkitekten är inte tillräckligt nära för att förstå varför vi valde så här.”
- “Teamet har byggt något som inte följer målbilden.”
- “Målbilden var för generell för att hjälpa i beslutet.”
- “Vi dokumenterar senare när lösningen stabiliserat sig.”

Alla dessa kommentarer kan vara rimliga ur sitt perspektiv. De visar bara att organisationen saknar ett fungerande sätt att göra löpande designbeslut synliga och gemensamma.

För arkitekten blir utmaningen att inte svara med mer kontroll än situationen behöver. I stället behöver arkitekten skapa strukturer som hjälper teamet att designa bra i vardagen.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt till design börjar med en viktig insikt:

> Designansvar kan delas utan att helhetsansvar försvinner.

Det betyder att arkitekten inte behöver fatta alla designbeslut själv. Däremot behöver arkitekten bidra till att rätt beslut fattas på rätt nivå, att besluten hänger ihop och att viktiga konsekvenser blir synliga.

Kontinuerlig design bygger på tre delar:

1. **Tydliga designprinciper**
2. **Återkommande designsamtal**
3. **Synliga designbeslut**

### Tydliga designprinciper

Designprinciper är inte detaljerade lösningar. De är vägledande regler som hjälper teamet att fatta många mindre beslut utan att behöva fråga om allt.

För Myndigheten för samhällstjänster kan sådana principer till exempel vara:

- Medborgartjänsten ska inte innehålla egna kopior av information som är juridiskt styrande.
- Verksamhetsregler som påverkar ärendehantering ska vara spårbara till ansvarig verksamhetsprocess.
- Integrationer mot äldre system ska kapslas in så att framtida modernisering underlättas.
- Säkerhets- och behörighetsbeslut ska vara explicita, inte inbyggda som antaganden i gränssnitt.
- Tillfälliga lösningar ska ha en dokumenterad ägare och ett tydligt omprövningstillfälle.

Sådana principer hjälper teamet att agera självständigt. De säger inte exakt hur varje komponent ska byggas, men de gör det tydligare vilka avvägningar som är viktiga.

### Återkommande designsamtal

Kontinuerlig design kräver forum, men inte nödvändigtvis tunga forum. Det kan räcka med korta, regelbundna samtal där arkitekt, team och ibland produktägare eller säkerhetsroller tittar på aktuella designfrågor.

Syftet är inte att arkitekten ska godkänna allt. Syftet är att upptäcka mönster, avvikelser och nya beslut i tid.

Frågor i ett sådant samtal kan vara:

- Vilka designbeslut har teamet fattat sedan sist?
- Vilka beslut närmar sig som kan påverka andra team eller system?
- Finns det något tillfälligt som riskerar att bli permanent?
- Har vi brutit mot någon princip, och var det i så fall medvetet?
- Behöver något beslut dokumenteras som ett arkitekturbeslut?
- Behöver någon annan roll kopplas in tidigare?

Det viktiga är rytmen. Om designsamtalet sker ofta och nära arbetet behöver det inte bli stort. Om det sker sällan tenderar det att bli en granskning av mycket som redan är byggt.

### Synliga designbeslut

I agil utveckling fattas många designbeslut löpande. Det är inte ett problem i sig. Problemet är när besluten försvinner.

Alla beslut behöver inte dokumenteras på samma sätt. Ett lokalt val av intern kodstruktur kanske inte behöver lyftas. Men beslut som påverkar beroenden, informationsansvar, säkerhet, integration, förvaltning eller framtida handlingsutrymme behöver fångas.

En enkel beslutslogg kan räcka:

- Vad beslutades?
- Varför beslutades det?
- Vilka alternativ övervägdes?
- Vilka konsekvenser accepterar vi?
- När behöver beslutet omprövas?
- Vem behöver känna till det?

Detta gör designen lärbar. Nästa team kan förstå varför lösningen ser ut som den gör. Förvaltningen kan förstå vilka avvägningar som gjorts. Arkitekturforum kan se mönster utan att behöva godkänna varje detalj.

## Exempel: Myndigheten för samhällstjänster

Sara bestämmer sig för att inte försöka återinföra en designfas. I stället bokar hon ett kort veckovis designsamtal med Lina och två utvecklare från teamet. Erik deltar när frågorna påverkar prioritering eller verksamhetsregler. Amir från informationssäkerhet bjuds in vid behov, särskilt när behörighet, loggning eller personuppgifter påverkas.

Första samtalet börjar konkret.

Sara säger:

> “Jag vill inte att vi stoppar flödet. Men jag vill att vi ser vilka designbeslut vi faktiskt håller på att fatta.”

Teamet går igenom tre beslut från veckan:

1. Statusvärden översätts i tjänstelagret.
2. En lokal tabell används för visningsnamn.
3. Fel från handläggningssystemet visas som generella meddelanden för medborgaren.

Varje beslut hade ett gott skäl. Men i samtalet ser gruppen att de tillsammans rör vid en större fråga: var ska översättning mellan interna ärendebegrepp och medborgarnära begrepp äga rum?

Det är inte bara en teknisk fråga. Det påverkar verksamhetsansvar, spårbarhet, kommunikation med medborgare och framtida möjlighet att återanvända begrepp i andra digitala tjänster.

Sara föreslår inte en lång utredning. Hon formulerar i stället ett designbeslut:

> “För första inkrementet får teamet hantera visningsnamn i tjänstelagret, men begreppsöversättning som påverkar juridisk eller verksamhetsmässig innebörd ska ägas av verksamhetsprocessen och dokumenteras som en separat regel. Beslutet omprövas innan fler ärendetyper läggs till.”

Detta blir varken en fullständig målarkitektur eller ett fritt lokalt val. Det är ett medvetet, begränsat och omprövningsbart designbeslut.

Efter några veckor har teamet en liten lista med designprinciper:

- Skilj medborgarnära begrepp från interna handläggningsbegrepp.
- Undvik direkta beroenden från medborgartjänsten till handläggningssystemets interna datamodell.
- Dokumentera tillfälliga lösningar med omprövningsdatum.
- Lyft beslut som påverkar andra tjänster, inte varje lokal koddetalj.
- Bjud in säkerhet och juridik när designen påverkar informationens exponering eller spårbarhet.

Sara märker att hennes roll förändras. Hon designar fortfarande, men inte genom att äga varje lösningsdetalj. Hon hjälper teamet att se mönster, formulera principer och göra viktiga beslut synliga.

## Vanliga fallgropar

- **Fallgrop: Att kalla allt teamet gör för “bara implementation”.**
  - Varför den uppstår: I en fasorienterad logik skiljs design och implementation ofta tydligt åt.
  - Vad arkitekten kan göra i stället: Se att implementation ofta innehåller designbeslut och hjälp teamet att identifiera vilka beslut som har arkitektonisk betydelse.

- **Fallgrop: Att försöka granska varje designbeslut.**
  - Varför den uppstår: Arkitekten vill skydda helheten och undvika framtida problem.
  - Vad arkitekten kan göra i stället: Skilj mellan lokala beslut, beslut som påverkar teamets lösning och beslut som påverkar flera system eller framtida handlingsutrymme.

- **Fallgrop: Att designprinciper blir för abstrakta.**
  - Varför den uppstår: Principer formuleras ibland som allmänna ideal, till exempel “lösningen ska vara flexibel”.
  - Vad arkitekten kan göra i stället: Formulera principer så att de hjälper teamet att välja mellan konkreta alternativ.

- **Fallgrop: Att tillfälliga designval blir permanenta av misstag.**
  - Varför den uppstår: Teamet behöver lösa ett problem snabbt och saknar en tydlig rytm för omprövning.
  - Vad arkitekten kan göra i stället: Dokumentera tillfälliga beslut med ägare, konsekvens och tidpunkt för omprövning.

- **Fallgrop: Att gemensamt designansvar blir otydligt ansvar.**
  - Varför den uppstår: När fler deltar i designen kan det bli oklart vem som ser helheten.
  - Vad arkitekten kan göra i stället: Tydliggör vilka beslut teamet äger, vilka arkitekten stödjer och vilka som behöver lyftas till bredare forum.

## Frågor att ställa i situationen

När design inte längre är en separat fas kan arkitekten använda frågor som gör designarbetet synligt utan att bromsa det:

- Vilka designbeslut har vi faktiskt fattat den senaste veckan?
- Vilka av dessa beslut påverkar bara teamet, och vilka påverkar andra?
- Vilka principer använder teamet när det väljer mellan olika lösningar?
- Finns det tillfälliga lösningar som behöver ett omprövningsdatum?
- Har vi skapat nya beroenden som inte var synliga tidigare?
- Har vi flyttat verksamhetsregler, säkerhetslogik eller informationsansvar utan att märka det?
- Behöver något beslut dokumenteras för förvaltning, spårbarhet eller framtida team?
- Vilka personer behöver vara med i nästa designsamtal för att beslutet ska bli tillräckligt belyst?

## Reflektionsfrågor

1. I vilka delar av ditt arbete behandlas design fortfarande som en separat fas?
2. Var sker de verkliga designbesluten i din organisation i dag?
3. Vilka designbeslut fattar teamen utan att de blir synliga för arkitektur eller förvaltning?
4. Vilka designprinciper skulle hjälpa teamen att fatta bättre beslut utan att fråga om allt?
5. När brukar du själv känna behov av att granska, och vad är det egentligen du försöker skydda?
6. Hur kan du skapa en rytm för designsamtal som stödjer flödet i stället för att bli en ny kontrollpunkt?
7. Vilka tillfälliga lösningar i din miljö borde få ett tydligt omprövningsdatum?
8. Hur kan du se skillnad på design som behöver styras centralt och design som bör växa fram nära teamet?

## Snabb sammanfattning

- I agil utveckling sker design inte bara före implementation, utan löpande under arbetets gång.
- Det betyder inte att design blir mindre viktig; det betyder att design behöver göras synlig i flödet.
- Arkitekten behöver gå från att äga alla designprodukter till att skapa förutsättningar för bra designbeslut över tid.
- Kontinuerlig design kräver tydliga designprinciper, återkommande designsamtal och synliga designbeslut.
- Team kan fatta många lokala beslut självständigt, men beslut som påverkar beroenden, säkerhet, information, förvaltning eller framtida handlingsutrymme behöver uppmärksammas.
- Tillfälliga lösningar behöver ägare, konsekvensbeskrivning och tidpunkt för omprövning.
- Gemensamt designansvar fungerar bara om ansvarsnivåer och eskaleringsvägar är tydliga.

## Nästa steg

När designbeslut sker löpande blir beroenden ofta synligare. Vissa beroenden är tekniska, till exempel integrationer mellan system. Andra är organisatoriska, till exempel väntan på beslut, leverantörer, forum eller andra team. I nästa kapitel går vi vidare till situationen där beroenden börjar bromsa flödet, och hur arkitekten kan bidra genom att inte bara kartlägga beroenden utan också minska, frikoppla och göra dem mer hanterbara.
