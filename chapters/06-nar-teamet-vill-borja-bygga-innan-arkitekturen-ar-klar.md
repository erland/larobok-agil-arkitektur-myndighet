# Kapitel 6: När teamet vill börja bygga innan arkitekturen är klar

## Varför detta kapitel finns

En av de vanligaste friktionerna i övergången från ett mer fasorienterat arbetssätt till agil IT-utveckling uppstår när teamet vill börja bygga innan arkitekten upplever att arkitekturen är klar. Situationen är lätt att känna igen: produktägaren vill få fram något konkret, teamet vill minska osäkerhet genom att börja implementera och arkitekten ser fortfarande öppna frågor kring integrationer, informationsmodell, säkerhet, behörighet, drift, förvaltning och beroenden.

I ett fasorienterat arbetssätt är det ofta rimligt att utveckling startar först när centrala lösningsfrågor är utredda och dokumenterade. Det ger en tydlig övergång från analys och design till byggande. I ett mer agilt arbetssätt kan samma logik däremot skapa väntan. Om allt måste vara färdigtänkt innan något får byggas riskerar organisationen att skjuta upp lärande, upptäcka fel antaganden sent och skapa stora beslutsunderlag för frågor som egentligen kunde ha prövats i mindre skala.

Men motsatsen är inte heller hållbar. Att “bara börja bygga” utan arkitektonisk riktning kan skapa teknikskuld, svåra beroenden och lösningar som fungerar lokalt men blir problematiska i helheten. För en myndighet kan det dessutom leda till brister i spårbarhet, informationssäkerhet, rättssäkerhet och förvaltningsbarhet.

Det här kapitlet handlar därför om ett praktiskt mellanläge: **tillräcklig arkitektur**. Det betyder inte minimal arkitektur eller frånvaro av styrning. Det betyder att arkitekten hjälper teamet att förstå vilka beslut och förutsättningar som behöver vara tydliga för att utveckling ska kunna börja på ett kontrollerat sätt, och vilka frågor som kan undersökas genom stegvis implementation.

Kapitlets kärnfråga är:

> Vad behöver vara arkitektoniskt klart för att teamet ska kunna börja lära sig utan att skapa oacceptabel risk?

## Situationen: “Vi behöver börja bygga nu”

På Myndigheten för samhällstjänster har arbetet med den nya medborgartjänsten kommit till en punkt där teamet vill skapa en första fungerande version. Målet är begränsat: en medborgare ska kunna logga in och se grundläggande status för ett ärende.

Erik, produktägaren, vill komma vidare:

> “Vi har pratat länge nog. Vi behöver få upp något som verksamheten och några användare kan reagera på.”

Lina, teamets utvecklingsledare, håller med:

> “Vi kan börja med en smal version. En ärendetyp, ett fåtal statusvärden, bara läsning. Då lär vi oss hur integrationen fungerar och vad som är svårt.”

Sara ser nyttan med detta. Samtidigt ser hon flera öppna arkitekturfrågor:

- Vilket system ska vara källa för ärendestatus?
- Ska tjänsten läsa direkt från handläggningssystemet eller via ett integrationslager?
- Vilka statusvärden får visas externt?
- Hur ska behörighet och identitet hanteras?
- Vilken information får cachas?
- Vilka händelser behöver loggas?
- Hur påverkas förvaltning och support?
- Hur ska lösningen fungera om handläggningssystemet är otillgängligt?
- Vilka designval riskerar att bli svåra att ändra senare?

I en tidigare projektlogik hade Sara sannolikt velat ta fram en mer komplett lösningsbeskrivning innan teamet började implementera. Hon hade velat analysera integrationsmönster, informationsflöden, säkerhetskrav och målarkitektur. Det är inte orimligt. Frågorna är viktiga.

Men nu finns också en annan risk: om allt ska utredas först kan teamet tappa tempo, verksamheten tappa engagemang och flera antaganden förbli oprövade. Det är inte säkert att en mer omfattande förstudie skulle ge bättre svar. Vissa svar kanske bara går att få genom att bygga något begränsat och se vad som händer.

Sara behöver därför inte välja mellan fullständig arkitektur och att släppa taget. Hon behöver formulera vad som är **tillräckligt för att börja**.

## Det invanda sättet att agera

När arkitekten möter ett team som vill börja bygga innan arkitekturen är klar är det invanda agerandet ofta att bromsa. Inte av ovilja, utan av ansvarskänsla.

Arkitekten kan tänka:

- “Vi vet inte tillräckligt om helheten.”
- “Om teamet bygger fel nu blir det dyrt att rätta senare.”
- “Vi behöver säkerställa målarkitekturen först.”
- “Vi måste förstå alla beroenden innan implementationen startar.”
- “Det här kommer att bli en punktlösning om vi inte håller ihop designen.”

Det ligger mycket klokskap i dessa reaktioner. Arkitekten har ofta sett vad som händer när team bygger lokalt fungerande lösningar som senare visar sig skapa problem i integration, drift, säkerhet eller förvaltning. I en myndighetsmiljö kan konsekvenserna bli större än enbart tekniskt omarbete. Felaktiga vägval kan påverka informationshantering, medborgarnas förtroende, rättssäkerhet eller möjligheten att följa upp beslut.

Det invanda sättet att skapa trygghet blir därför att kräva mer utredning innan byggstart. Arkitekten försöker reducera osäkerhet genom analys, dokumentation, granskning och förankring.

Det är ofta rätt när besluten är svårreversibla och riskerna stora. Men det kan bli problematiskt när samma arbetssätt används för alla frågor, även sådana som är mindre riskfyllda, reversibla eller möjliga att undersöka i liten skala.

## Varför det kan skapa friktion i agil utveckling

I agil utveckling är byggande inte bara produktion. Det är också ett sätt att lära. En begränsad implementation kan visa om en integration fungerar, om informationen är begriplig, om ett API är tillräckligt, om användarna förstår begreppen eller om en teknisk lösning håller.

När arkitekten kräver att arkitekturen ska vara “klar” innan något byggs kan flera typer av friktion uppstå.

För det första kan arkitekturbegreppet bli för stort. Allt som är oklart hamnar under rubriken “arkitektur”, och därmed blir nästan ingenting möjligt att börja med. Frågor som faktiskt måste avgöras tidigt blandas med frågor som kan utforskas senare.

För det andra kan teamets lärande försenas. Vissa problem upptäcks först när någon försöker implementera, integrera eller testa. Om teamet väntar på fullständig klarhet kan organisationen lägga mycket tid på antaganden som ändå behöver ändras.

För det tredje kan arkitekten bli en fasgrind, även om organisationen säger sig arbeta agilt. Teamet lär sig då att utveckling startar när arkitekten har godkänt lösningen, snarare än när riskerna är tillräckligt förstådda och arbetet är upplagt för kontrollerat lärande.

För det fjärde kan dialogen mellan arkitekt och team försämras. Om arkitekten uppfattas som den som säger nej kan teamet börja undvika arkitekturdialogen eller komma med färdiga lösningar för sent. Det minskar arkitektens möjlighet att påverka när det verkligen behövs.

Det agila alternativet är inte att börja utan riktning. Det är att skilja mellan tre frågor:

1. Vad måste vi veta innan vi börjar?
2. Vad kan vi lära oss genom att börja begränsat?
3. Vad får vi absolut inte råka låsa utan medvetet beslut?

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt innebär att arkitekten hjälper teamet att skapa en trygg startpunkt, inte en färdig slutbild. Det kan göras genom tre begrepp: **tillräcklig arkitektur**, **arkitektoniska startvillkor** och **utforskande implementation**.

### Tillräcklig arkitektur

Tillräcklig arkitektur är den nivå av arkitektonisk riktning som behövs för att utveckling ska kunna starta utan oacceptabel risk.

Det innebär att arkitekten inte frågar:

> Är arkitekturen klar?

Utan snarare:

> Är arkitekturen tillräckligt tydlig för nästa steg?

Det är en viktig skillnad. “Klar” antyder ett slutläge. “Tillräcklig för nästa steg” kopplar arkitekturarbetet till det som faktiskt ska göras nu.

För Saras team innebär det att första versionen inte behöver ha hela framtida medborgartjänstens arkitektur färdig. Men teamet behöver förstå vissa gränser:

- vilken information de får visa,
- vilken systemkälla de får använda,
- hur identitet och behörighet ska hanteras i första steget,
- vilka antaganden som inte får byggas in permanent,
- vilka beslut som måste dokumenteras,
- vilka risker som behöver följas upp innan nästa steg.

Tillräcklig arkitektur är alltså inte en ursäkt för otydlighet. Det är ett sätt att vara tydlig på rätt nivå.

### Arkitektoniska startvillkor

Arkitektoniska startvillkor är de minsta förutsättningar som behöver vara på plats för att teamet ska kunna börja arbeta ansvarsfullt.

De kan exempelvis handla om:

- vilka system eller datakällor som får användas,
- vilka säkerhetsprinciper som gäller,
- vilka integrationer som får vara tillfälliga,
- vilka delar som måste vara spårbara från början,
- vilka beslut som kräver särskild förankring,
- vilka begränsningar teamet inte får överskrida,
- vilka frågor som ska undersökas i första inkrementet.

Bra startvillkor är konkreta, begränsade och möjliga att använda. De ska inte vara en förtäckt kravspecifikation eller en ny fasgrind. De ska hjälpa teamet att komma i gång på ett sätt som bevarar handlingsutrymme.

Ett exempel på startvillkor för Saras team kan vara:

- Första versionen får endast läsa information, inte ändra ärendedata.
- Endast en ärendetyp ingår.
- Informationen hämtas via en avgränsad integrationslösning, inte genom direkt åtkomst till handläggningssystemets databas.
- Endast statusvärden som verksamhet och juridik har bedömt som lämpliga får visas externt.
- Alla arkitekturbeslut och öppna antaganden dokumenteras i en enkel beslutslogg.
- Teamet ska efter första inkrementet återkomma med lärdomar om integration, datakvalitet och användarförståelse.

Detta är inte hela arkitekturen. Men det kan vara tillräckligt för att börja.

### Utforskande implementation

En utforskande implementation är en begränsad implementation som görs för att lära, inte för att låtsas att hela lösningen redan är färdig.

Det kan vara en prototyp, en teknisk spike, en smal första version eller ett kontrollerat inkrement. Det viktiga är att syftet är tydligt:

- Vilket antagande vill vi testa?
- Vilken risk vill vi minska?
- Vilket beslut vill vi kunna fatta bättre efteråt?
- Vad får implementationen inte bli utan nytt beslut?

I Saras fall kan teamet använda en utforskande implementation för att pröva hur ärendestatus kan hämtas och visas. Men då behöver alla vara överens om vad som är utforskande och vad som är långsiktigt vägval.

Det är här arkitektens roll är central. Sara kan hjälpa teamet att undvika att en tillfällig lösning smyger sig in som permanent arkitektur. Hon kan också hjälpa produktägaren att se att ett första inkrement inte bara levererar funktion, utan även kunskap.

## Exempel: Myndigheten för samhällstjänster

Sara bokar ett kort arbetsmöte med Erik, Lina och Amir från informationssäkerhet. Syftet är inte att granska en färdig lösning, utan att formulera startvillkor för första inkrementet.

Hon inleder:

> “Jag tror att teamet kan börja bygga en smal version. Men vi behöver vara tydliga med vad vi vet, vad vi antar och vad vi absolut inte ska låsa i första steget.”

De delar upp tavlan i fyra rubriker:

1. Beslut som måste tas före byggstart.
2. Antaganden som får testas.
3. Begränsningar som inte får överskridas.
4. Frågor som ska följas upp efter första inkrementet.

Under första rubriken skriver de:

- Tjänsten ska endast visa information, inte ändra ärenden.
- Endast medborgare med säker inloggning får se ärendestatus.
- Första inkrementet gäller en avgränsad ärendetyp.
- Direkt databasåtkomst till handläggningssystemet är inte tillåten.
- Loggning av åtkomst ska finnas från början.

Under antaganden skriver de:

- De befintliga statusvärdena går att översätta till begripligt medborgarspråk.
- Handläggningssystemet kan leverera statusinformation med tillräcklig aktualitet.
- En enkel integrationslösning räcker för första inkrementet.

Under begränsningar skriver de:

- Ingen generell integrationsplattform väljs i detta steg.
- Ingen permanent informationsmodell fastställs för alla ärendetyper.
- Ingen lösning för aviseringar byggs innan rättsliga och informationsmässiga frågor är tydligare.
- Ingen statusinformation visas externt utan verksamhetsmässig och juridisk bedömning.

Under uppföljning skriver de:

- Vad lärde vi oss om datakvalitet?
- Vilka statusvärden var svåra att förstå?
- Vilka integrationsproblem uppstod?
- Vilka beslut behöver fattas inför nästa inkrement?
- Vilka delar av lösningen kan behållas, och vilka var endast utforskande?

Efter mötet säger Lina:

> “Det här hjälper. Nu vet teamet vad vi får göra, vad vi inte ska röra och vad vi ska lära oss.”

Erik säger:

> “Och jag kan förklara för styrgruppen varför vi börjar smalt utan att låtsas att hela lösningen är beslutad.”

Sara har inte skapat en fullständig arkitekturbeskrivning. Men hon har skapat riktning, gränser och ett sätt att lära utan att tappa kontrollen. Det är tillräcklig arkitektur i praktiken.

## Att skilja mellan startbeslut och framtidsbeslut

En viktig färdighet i den här situationen är att skilja mellan beslut som behövs för att starta och beslut som hör hemma senare.

Startbeslut handlar om att göra nästa steg möjligt och säkert nog. Framtidsbeslut handlar om hur hela lösningen ska utvecklas över tid. Problemet uppstår när framtidsbeslut krävs innan teamet ens har börjat lära sig.

För arkitekten kan det vara hjälpsamt att dela in öppna frågor i fyra kategorier.

### 1. Måste beslutas före start

Detta är frågor där felaktigt eller uteblivet beslut kan skapa oacceptabel risk direkt. Det kan handla om säkerhet, åtkomst, dataskydd, systemgränser, rättsliga begränsningar eller svårreversibla tekniska vägval.

Exempel:

- Får den här informationen visas för medborgaren?
- Vilken identitets- och behörighetsprincip gäller?
- Vilka systemgränser får teamet inte bryta?
- Finns det ett vägval som blir mycket dyrt att ändra senare?

### 2. Kan beslutas efter utforskning

Detta är frågor där organisationen behöver mer kunskap innan ett bra beslut kan fattas. Här kan en begränsad implementation ge bättre underlag än ytterligare analys.

Exempel:

- Vilket integrationsmönster fungerar bäst i praktiken?
- Hur behöver statusvärden översättas för att vara begripliga?
- Vilken svarstid upplever användare som acceptabel?
- Hur ofta behöver informationen uppdateras?

### 3. Kan vara tillfälligt med tydlig märkning

Vissa lösningar kan accepteras tillfälligt om de dokumenteras och avgränsas. Det farliga är inte alltid att göra något tillfälligt. Det farliga är att det tillfälliga blir permanent utan beslut.

Exempel:

- En enkel integrationslösning för första inkrementet.
- Manuell hantering av en viss kontroll under kort tid.
- Begränsat stöd för endast en ärendetyp.
- En förenklad informationsmodell för att testa begrepp.

### 4. Ska inte beslutas ännu

Vissa beslut bör uttryckligen skjutas upp. Det kan kännas ovant för arkitekten, men är ibland det mest ansvarsfulla. Ett beslut som fattas för tidigt kan minska handlingsutrymmet utan att minska risken.

Exempel:

- Slutlig målarkitektur för alla medborgartjänster.
- Val av generell integrationsstrategi för hela myndigheten.
- Permanent modell för alla ärendetyper.
- Fullständig framtida förvaltningsorganisation för en lösning som ännu inte är validerad.

Den här indelningen gör arkitektens resonemang mer konkret. I stället för att säga “arkitekturen är inte klar” kan Sara säga:

> “De här tre besluten behöver vi fatta före start. De här fyra frågorna kan teamet undersöka. Den här tillfälliga lösningen är acceptabel i ett inkrement om vi märker den tydligt. Och de här två besluten bör vi inte låsa ännu.”

Det är ett mer användbart bidrag än ett generellt ja eller nej.

## Tillräcklig arkitektur är inte samma sak som svag arkitektur

En vanlig missuppfattning är att tillräcklig arkitektur betyder mindre arkitektur. Det stämmer inte. I många fall kräver tillräcklig arkitektur mer professionellt omdöme än en omfattande förhandsdesign.

En omfattande förhandsdesign kan ibland dölja osäkerhet bakom detaljerade beskrivningar. Tillräcklig arkitektur behöver i stället göra osäkerheten synlig:

- Vad vet vi?
- Vad antar vi?
- Vad behöver vi lära?
- Vilka risker accepterar vi?
- Vilka risker accepterar vi inte?
- Vilket handlingsutrymme vill vi bevara?

Det kräver att arkitekten är tydlig, inte vag. Det kräver också att arkitekten vågar säga både ja och nej.

Ett agilt arkitekturbidrag kan därför låta så här:

> “Ja, teamet kan börja bygga en första läsande vy. Nej, vi ska inte välja permanent integrationsmönster för alla framtida tjänster i det här steget. Ja, vi ska dokumentera vilka antaganden vi testar. Nej, vi får inte visa statusvärden externt innan verksamhet och juridik har bedömt dem.”

Det är varken full kontroll i förväg eller fri byggstart utan gränser. Det är kontrollerat lärande.

## När arkitekten bör bromsa

Det finns situationer där arkitekten faktiskt bör bromsa byggstart. Att arbeta agilt betyder inte att alla risker ska tas genom implementation.

Arkitekten bör vara tydlig när:

- teamet riskerar att hantera skyddsvärd information utan tillräcklig kontroll,
- ett tekniskt vägval är svårreversibelt och underlaget är för svagt,
- en tillfällig lösning sannolikt kommer att bli permanent utan styrning,
- teamet saknar förståelse för viktiga beroenden,
- lösningen kan påverka rättssäkerhet, integritet eller myndighetens ansvar,
- det saknas mandat för ett beslut som teamet är på väg att fatta,
- ingen har formulerat vad implementationen ska lära organisationen.

Skillnaden ligger i hur arkitekten bromsar. Ett fasorienterat bromsande kan bli:

> “Ni kan inte börja förrän arkitekturen är klar.”

Ett mer agilt bromsande kan bli:

> “Ni kan börja med vissa delar, men inte med den här delen innan vi har hanterat de här riskerna.”

Eller:

> “Jag föreslår att vi gör första inkrementet smalare så att teamet kan börja utan att vi låser ett svårreversibelt vägval.”

Det andra sättet skyddar fortfarande helheten, men försöker samtidigt bevara flöde och lärande.

## Frågor att ställa i situationen

När ett team vill börja bygga innan arkitekturen är klar kan arkitekten använda följande frågor.

### Om nästa steg

- Vad är det minsta meningsfulla nästa steget?
- Är syftet att leverera funktion, minska risk, testa ett antagande eller skapa beslutsunderlag?
- Vilka delar behöver fungera på riktigt redan nu?
- Vilka delar kan vara avgränsade, tillfälliga eller manuella?

### Om risk

- Vilka beslut i detta steg är svårreversibla?
- Vilka risker är acceptabla för ett begränsat inkrement?
- Vilka risker är inte acceptabla ens i liten skala?
- Vad kan gå fel om teamet börjar utan ytterligare arkitekturarbete?

### Om gränser

- Vilka systemgränser får teamet inte bryta?
- Vilka data får användas?
- Vilka integrationer får teamet skapa eller anropa?
- Vilka säkerhets- eller regelefterlevnadskrav gäller från första dagen?

### Om lärande

- Vad ska vi veta efter första inkrementet som vi inte vet i dag?
- Hur ska vi dokumentera lärdomarna?
- När ska vi ompröva de tillfälliga vägvalen?
- Vilka beslut ska första inkrementet hjälpa oss att fatta bättre?

### Om ansvar

- Vem har mandat att acceptera riskerna?
- Vem behöver vara med i dialogen innan teamet startar?
- Hur kommuniceras startvillkoren till team, produktägare och styrning?
- Hur säkerställer vi att tillfälliga lösningar inte blir permanenta av misstag?

## Vanliga fallgropar

- Fallgrop: Att kräva fullständig arkitektur före varje byggstart.
  - Varför den uppstår: Arkitekten vill minska risk och skapa trygghet genom tydliga underlag.
  - Vad arkitekten kan göra i stället: Skilj mellan beslut som måste tas före start och frågor som kan undersökas genom ett begränsat inkrement.

- Fallgrop: Att låta teamet börja utan tydliga gränser.
  - Varför den uppstår: Organisationen vill undvika att arkitektur uppfattas som bromsande.
  - Vad arkitekten kan göra i stället: Formulera arkitektoniska startvillkor som ger teamet frihet inom tydliga ramar.

- Fallgrop: Att kalla allt för “tillfälligt” utan uppföljning.
  - Varför den uppstår: Tillfälliga lösningar gör det lättare att komma i gång.
  - Vad arkitekten kan göra i stället: Märk tillfälliga vägval, dokumentera varför de görs och bestäm när de ska omprövas.

- Fallgrop: Att blanda ihop prototyp, spike och produktionslösning.
  - Varför den uppstår: Teamet bygger något som fungerar, och organisationen börjar använda det.
  - Vad arkitekten kan göra i stället: Var tydlig med vad som är utforskande implementation och vad som är avsett att leva vidare.

- Fallgrop: Att arkitekten säger nej för sent.
  - Varför den uppstår: Arkitekten involveras först när teamet redan har börjat implementera.
  - Vad arkitekten kan göra i stället: Var närvarande tidigt i planering och refinement så att risker och startvillkor formuleras innan teamet investerar för mycket.

## Reflektionsfrågor

1. När har du själv upplevt att ett team ville börja bygga innan du tyckte att arkitekturen var tillräckligt klar?
2. Vad var det egentligen du saknade: beslut, analys, dokumentation, förankring, riskhantering eller egen trygghet?
3. Vilka arkitekturfrågor i din miljö måste vara besvarade före byggstart?
4. Vilka frågor skulle ni kunna lära er mer om genom en begränsad implementation?
5. Hur tydligt brukar ni skilja mellan tillfälliga vägval och långsiktiga arkitekturbeslut?
6. Vilka startvillkor skulle hjälpa team i din organisation att komma i gång utan att skapa oacceptabel risk?
7. När behöver du som arkitekt bli bättre på att säga “ja, men inom de här ramarna” i stället för bara ja eller nej?
8. Vilka signaler visar att en tillfällig lösning håller på att bli permanent utan medvetet beslut?

## Snabb sammanfattning

När teamet vill börja bygga innan arkitekturen är klar behöver arkitekten inte välja mellan att bromsa allt eller släppa kontrollen. Det mer användbara bidraget är att skapa **tillräcklig arkitektur** för nästa steg.

Det innebär att arkitekten hjälper team och produktägare att förstå:

- vilka beslut som måste fattas före start,
- vilka frågor som kan undersökas genom byggande,
- vilka risker som är acceptabla i liten skala,
- vilka gränser teamet inte får överskrida,
- vilka tillfälliga vägval som behöver märkas och följas upp.

Arkitektoniska startvillkor gör det möjligt att börja utan att låtsas att allt är klart. Utforskande implementation gör det möjligt att använda byggande som lärande, inte bara som produktion.

För arkitekten handlar skiftet om att gå från frågan:

> “Är arkitekturen klar?”

Till frågan:

> “Är arkitekturen tillräcklig för att vi ska kunna ta nästa steg på ett ansvarsfullt sätt?”

## Nästa steg

I nästa kapitel fördjupas frågan om design. När teamen börjar arbeta mer iterativt blir design inte längre en separat fas som avslutas före implementation. I stället behöver design ske kontinuerligt, nära teamens vardag, men fortfarande med riktning, principer och helhetssyn.

Nästa kapitel handlar därför om situationen: **när design inte längre är en separat fas**.
