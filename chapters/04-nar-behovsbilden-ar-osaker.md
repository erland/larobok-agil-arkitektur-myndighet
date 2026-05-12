# Kapitel 4: När behovsbilden är osäker

## Varför detta kapitel finns

Många arkitekter är vana vid att komma in när ett behov har börjat ta form. Det kan finnas en förstudie, ett projektdirektiv, en effektbeskrivning, en kravbild eller åtminstone en relativt tydlig formulering av vad verksamheten vill åstadkomma. Utifrån det kan arkitekten analysera konsekvenser, identifiera beroenden, formulera lösningsalternativ och skapa beslutsunderlag.

I mer agil IT-utveckling är behovsbilden ofta mindre stabil när arbetet börjar. Det är inte alltid ett tecken på bristande styrning. Ibland är det själva poängen: organisationen vill snabbare undersöka vad som faktiskt skapar nytta, vad användare behöver, vilka regelmässiga begränsningar som är avgörande och vilka tekniska vägval som är rimliga.

Det kan kännas obekvämt för en erfaren arkitekt. Om behovet är oklart blir också lösningsrymden otydlig. Om lösningsrymden är otydlig är det svårt att veta vilka arkitekturbeslut som behöver fattas. Och om besluten inte fattas i tid kan teamet bygga något som senare visar sig vara svårt att ändra, förvalta, säkra eller samordna med andra system.

Det här kapitlet handlar om hur arkitekten kan bidra när behovsbilden är osäker. Inte genom att kräva fullständig klarhet innan något får börja, men inte heller genom att acceptera oklarhet som något teamet får lösa längs vägen. Arkitektens bidrag blir i stället att göra osäkerheten begriplig, prövbar och hanterbar.

## Situationen: “Vi behöver bara en enklare digital tjänst”

På Myndigheten för samhällstjänster vill verksamheten skapa en ny digital tjänst där medborgare ska kunna följa sitt ärende och komplettera uppgifter digitalt. I den första beskrivningen låter behovet relativt enkelt:

> “Medborgaren ska kunna logga in, se status i sitt ärende och ladda upp kompletterande underlag.”

Erik, som är verksamhetsnära produktägare, vill gärna komma igång. Han ser att dagens manuella hantering leder till många telefonsamtal, långa väntetider och frustration både hos medborgare och handläggare. Lina och teamet ser också att det borde gå att skapa ett första inkrement ganska snabbt: en inloggad vy, några statusmeddelanden och en möjlighet att skicka in en fil.

Sara lyssnar och ser direkt flera öppna frågor:

- Vilka ärendetyper ska tjänsten stödja först?
- Är statusinformationen begriplig för medborgaren, eller är den skriven för interna handläggare?
- Vilka uppgifter får visas digitalt?
- Vilka kompletteringar får lämnas in utan manuell kontroll?
- Hur ska handlingar kopplas till rätt ärende?
- Vilka data kommer från det äldre handläggningssystemet?
- Behöver tjänsten fungera för ombud eller bara för den person ärendet gäller?
- Vilka krav finns på spårbarhet, arkivering och informationssäkerhet?

I ett fasorienterat arbetssätt hade Saras naturliga reaktion kanske varit att föreslå en fördjupad behovsanalys innan lösningsarbetet går vidare. Det hade inte varit orimligt. Behovet påverkar många delar av lösningen. Men i den här situationen vill organisationen arbeta mer iterativt. Den vill inte vänta flera månader på en komplett behovsbild innan den lär sig något av användare och handläggare.

Frågan blir därför inte om behovsbilden är tillräckligt komplett för att göra hela arkitekturen. Frågan blir: vad behöver vi förstå nu för att kunna ta nästa ansvarsfulla steg?

## Det invanda sättet att agera

När behovsbilden är osäker kan arkitektens invanda arbetssätt ofta se ut så här:

1. Be om tydligare behovsbeskrivning.
2. Efterfråga mer kompletta krav.
3. Identifiera luckor och beroenden.
4. Vänta med lösningsförslag tills verksamheten har preciserat vad den vill ha.
5. Ta fram flera lösningsalternativ när behovet är mer stabilt.
6. Förankra ett alternativ genom beslutsunderlag.

Detta sätt att agera har flera styrkor. Det minskar risken att arkitekten designar mot fel problem. Det hjälper verksamheten att se konsekvenser av otydliga behov. Det kan också skydda organisationen från att starta utveckling på alltför lösa grunder.

Men i en agil kontext kan samma arbetssätt skapa friktion. Om varje oklarhet gör att arkitekturen väntar på mer analys kan teamet tappa fart. Om arkitekten blir den som hela tiden pekar på allt som ännu inte är utrett kan rollen uppfattas som bromsande. Och om behovsanalysen försöker skapa för mycket säkerhet i början kan organisationen ändå upptäcka senare att den analyserade fel saker.

Den viktiga skillnaden är att osäkerhet inte alltid ska elimineras innan utveckling startar. Ofta behöver den struktureras så att den kan undersökas.

## Varför det kan skapa friktion i agil utveckling

Agil utveckling utgår från att viss kunskap uppstår genom arbetet. Det gäller inte bara teknisk kunskap, utan också verksamhetskunskap. Användare kan ha svårt att beskriva vad de behöver innan de ser något konkret. Handläggare kan beskriva ett arbetssätt som det borde fungera, men först i mötet med ett nytt digitalt stöd blir undantag, specialfall och tysta regler synliga. Juridiska eller säkerhetsmässiga frågor kan också bli tydligare när lösningsalternativen konkretiseras.

Det betyder inte att arkitekten ska acceptera vaga behov. Det betyder att arkitekten behöver skilja mellan tre typer av oklarhet:

## 1. Oklarhet som måste reduceras innan start

Vissa frågor kan vara så grundläggande att arbetet inte bör gå vidare innan de är tydligare. Exempel:

- Vilken målgrupp tjänsten gäller.
- Om informationen över huvud taget får visas digitalt.
- Om det finns rättsligt stöd för den tänkta behandlingen av personuppgifter.
- Om ett centralt system kan tillhandahålla nödvändiga data.
- Om lösningen kräver en förändring som ligger utanför teamets mandat.

Här behöver arkitekten hjälpa till att stoppa, pausa eller avgränsa arbetet tills frågan är hanterad. Det är inte att vara bakåtsträvande. Det är att skydda organisationen från att bygga på en grund som kan visa sig felaktig.

## 2. Oklarhet som kan undersökas genom ett begränsat steg

Andra frågor behöver inte lösas helt innan arbetet börjar. De kan undersökas genom ett smalt inkrement, en prototyp, ett tekniskt test, en användardialog eller ett begränsat lösningsspår. Exempel:

- Vilken statusinformation medborgare faktiskt förstår.
- Vilka kompletteringar som är vanligast.
- Hur handläggarna vill bli notifierade.
- Vilken integrationslösning som fungerar bäst i praktiken.
- Hur mycket av det äldre systemets datamodell som behöver exponeras.

Här blir arkitektens uppgift att hjälpa teamet att formulera vad man behöver lära sig, vilka risker som ska hållas begränsade och vilka beslut som inte bör låsas för tidigt.

## 3. Oklarhet som är acceptabel tills vidare

En tredje kategori är frågor som är verkliga men inte avgörande just nu. Exempel:

- Hur tjänsten ska skalas till alla ärendetyper på sikt.
- Exakt hur förvaltningsorganisationen ska se ut efter införandet.
- Hur framtida analysfunktioner kan kopplas på.
- Vilka rapporteringsbehov som kan uppstå om två år.

Dessa frågor ska inte ignoreras, men de behöver kanske inte styra dagens designbeslut. Arkitekten kan dokumentera dem som antaganden, framtida beslut eller bevakningspunkter.

Friktionen uppstår ofta när alla tre typer av oklarhet behandlas på samma sätt. Om allt måste utredas före start blir arbetet tungt och långsamt. Om inget behöver utredas före start blir arbetet riskfyllt. Arkitektens värde ligger i att kunna göra skillnaden synlig.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt till osäkra behov innebär att arkitekten rör sig från att fråga:

> “Är behovet tillräckligt tydligt för att vi ska kunna ta fram lösningen?”

till att fråga:

> “Vilken del av behovet behöver vi förstå bättre för att kunna ta nästa kloka steg?”

Det förändrar arkitektens bidrag på flera sätt.

## Från krav på klarhet till struktur på osäkerhet

Sara behöver inte acceptera att behovet beskrivs som “en enklare digital tjänst”. Men hon behöver inte heller kräva en komplett behovsspecifikation innan något kan hända. Hon kan i stället hjälpa gruppen att dela upp osäkerheten:

- Vad vet vi?
- Vad tror vi?
- Vad antar vi?
- Vad måste vara sant för att lösningen ska fungera?
- Vad behöver vi undersöka först?
- Vilka antaganden kan bli dyra om de är fel?

Den typen av frågor gör behovsbilden mer användbar utan att låtsas att den är färdig.

## Från lösningsförslag till lösningsrymd

Ett centralt begrepp i detta kapitel är **lösningsrymd**. Med lösningsrymd menar vi det möjliga utrymme av lösningar som kan möta ett behov, innan ett visst vägval har låsts.

När behovet är osäkert är det ofta för tidigt att välja en detaljerad lösning. Däremot är det värdefullt att beskriva lösningsrymden:

- Vilka lösningstyper verkar möjliga?
- Vilka vägval skulle begränsa oss snabbt?
- Vilka alternativ håller flera möjligheter öppna?
- Vilka begränsningar är verkliga redan nu?
- Vilka kvalitetskrav påverkar alla rimliga alternativ?

För Sara kan det innebära att hon inte direkt ritar en målarkitektur för hela medborgartjänsten. Hon kan i stället beskriva tre möjliga vägar:

1. En enkel visningstjänst som läser status från handläggningssystemet.
2. En mer självständig tjänst med ett mellanlager som skyddar det äldre systemet.
3. En stegvis väg där första inkrementet bara hanterar en ärendetyp och en begränsad mängd information.

Poängen är inte att välja allt direkt. Poängen är att ge samtalet struktur.

## Från kravinsamling till hypotesdriven behovsanalys

Ett annat begrepp är **hypotesdriven behovsanalys**. Det betyder att behov, antaganden och lösningsidéer behandlas som något som behöver prövas och förfinas, inte bara samlas in och dokumenteras.

I stället för att säga:

> “Medborgare behöver kunna följa sitt ärende digitalt.”

kan teamet formulera en hypotes:

> “Om medborgare kan se tydlig status och vilka kompletteringar som saknas, minskar antalet telefonsamtal till handläggarna och medborgaren upplever större kontroll.”

Den formuleringen gör flera saker tydliga. Den säger vem nyttan gäller. Den antyder vilken funktion som behövs. Den kopplar funktionen till en effekt. Den visar också vad som behöver följas upp.

För arkitekten är detta användbart eftersom arkitekturfrågor kan kopplas till hypotesen:

- Vilken information krävs för att visa status?
- Hur aktuell behöver informationen vara?
- Vilka kompletteringar får visas eller skickas in digitalt?
- Vilka risker uppstår om statusen är otydlig eller fel?
- Vilket integrationsmönster räcker för att pröva hypotesen?

Hypotesdriven behovsanalys gör alltså inte arkitekturen mindre viktig. Den ger arkitekten ett tydligare sätt att koppla arkitekturfrågor till verksamhetslärande.

## Från tekniska konsekvenser till arkitektoniska konsekvenser av behov

Det tredje begreppet är **arkitektoniska konsekvenser av behov**. Ett behov är sällan bara en önskad funktion. Det kan påverka information, integrationer, säkerhet, ansvar, processer, prestanda, datakvalitet, förvaltning och framtida förändringsförmåga.

När verksamheten säger “medborgaren ska kunna komplettera sitt ärende digitalt” hör Sara flera möjliga konsekvenser:

- Kompletteringen behöver kopplas till rätt ärende.
- Filformat och filstorlekar behöver hanteras.
- Det kan krävas viruskontroll eller annan teknisk kontroll.
- Handläggare behöver se vad som har kommit in.
- Händelsen behöver loggas.
- Informationen kan behöva diarieföras eller arkiveras.
- Det behöver vara tydligt vem som får komplettera.
- Det kan finnas krav på tillgänglighet och begriplighet.
- Tjänsten kan skapa nya belastningsmönster på äldre system.

Arkitektens uppgift är inte att göra alla dessa frågor till hinder. Uppgiften är att visa vilka konsekvenser ett till synes enkelt behov kan få, så att gruppen kan välja ett klokt första steg.

## Exempel: Myndigheten för samhällstjänster

Sara föreslår ett kort arbetsmöte med Erik, Lina, Amir från informationssäkerhet och två handläggare från verksamheten. Syftet är inte att skriva en komplett kravspecifikation. Syftet är att förstå vilken del av behovet som är mest värdefull och mest riskfylld att undersöka först.

Hon ritar upp tre kolumner på en digital tavla:

1. Det vi vet.
2. Det vi antar.
3. Det vi behöver undersöka.

Under “det vi vet” skriver gruppen:

- Många medborgare ringer för att fråga om status.
- Handläggare lägger mycket tid på återkommande frågor.
- Det äldre handläggningssystemet har statuskoder, men de är skrivna för intern användning.
- Vissa ärenden innehåller känsliga personuppgifter.
- Myndigheten vill börja med en begränsad ärendetyp.

Under “det vi antar” skriver gruppen:

- Medborgare vill främst veta om något saknas.
- En enkel statusvy kan minska antalet telefonsamtal.
- Handläggningssystemets statuskoder går att översätta till medborgarvänlig text.
- Det går att läsa status utan att påverka det äldre systemets stabilitet.
- De flesta kompletteringar gäller ett fåtal dokumenttyper.

Under “det vi behöver undersöka” skriver gruppen:

- Vilka statuskoder som faktiskt kan visas externt.
- Vilka formuleringar medborgare förstår.
- Hur aktuell statusinformationen behöver vara.
- Om kompletteringar ska ingå i första inkrementet eller vänta.
- Vilka säkerhets- och dataskyddsfrågor som måste vara hanterade innan test med riktiga användare.

Sara märker att samtalet förändras. I stället för att diskutera om behovet är “klart” börjar gruppen diskutera vilket lärande som behövs först.

Lina föreslår att teamet börjar med att visa status för en enda ärendetyp, utan möjlighet till komplettering. Erik är först tveksam eftersom kompletteringarna var en viktig del av nyttan. Men handläggarna säger att många samtal faktiskt handlar om status, inte kompletteringar. Amir påpekar att en ren statusvy kan vara enklare att riskbedöma än filuppladdning.

Sara formulerar ett första arkitektoniskt antagande:

> Första inkrementet ska pröva om en extern statusvy för en avgränsad ärendetyp kan minska osäkerheten kring informationsvisning, begrepp och integration, utan att samtidigt införa de risker som följer av digital komplettering.

Det är inte en färdig arkitektur. Men det är ett tydligt steg. Det säger vad man ska pröva, vad man medvetet avgränsar bort och varför.

## Att ställa bättre frågor tidigare

När behovsbilden är osäker behöver arkitekten ofta bidra med frågor som öppnar samtalet snarare än stänger det. Det är skillnad på frågor som indirekt säger “det här är inte tillräckligt utrett” och frågor som hjälper gruppen att förstå vad som behöver bli tydligare.

Mindre hjälpsamma frågor kan vara:

- “Var finns den fullständiga kravspecifikationen?”
- “Har verksamheten bestämt exakt vad den vill ha?”
- “Vem har godkänt behovsbilden?”
- “Hur ska jag kunna ta fram arkitektur utan tydliga krav?”

De frågorna kan vara begripliga, men de riskerar att leda till väntan eller försvar. Mer hjälpsamma frågor är ofta:

- “Vilken nytta vill vi kunna se först?”
- “Vilket antagande är mest riskabelt om det visar sig vara fel?”
- “Vilka behov påverkar arkitekturen mest?”
- “Vad behöver vi veta innan teamet bygger något som blir svårt att ändra?”
- “Vilken del av lösningen kan hjälpa oss att lära utan att låsa för mycket?”
- “Vilka begränsningar gäller oavsett vilket lösningsalternativ vi väljer?”

Sådana frågor gör att arkitekten fortfarande tar ansvar för kvalitet och helhet, men på ett sätt som hjälper arbetet framåt.

## Att skilja mellan behov, lösning och begränsning

En vanlig källa till otydlighet är att behov, lösningsidéer och begränsningar blandas ihop.

Verksamheten kan säga:

> “Vi behöver en app.”

Det kan låta som ett behov, men är egentligen en lösningsidé. Behovet kanske är att medborgaren ska kunna få snabb återkoppling, lämna kompletteringar eller förstå vad som händer i ärendet. En app kan vara en lösning, men kanske inte den bästa eller första.

Verksamheten kan också säga:

> “All information måste hämtas i realtid.”

Det kan låta som ett krav, men kan vara ett antagande. Kanske behöver vissa uppgifter vara aktuella direkt, medan andra kan uppdateras med viss fördröjning. Skillnaden påverkar arkitekturen kraftigt.

Eller så kan någon säga:

> “Det äldre systemet klarar inte fler integrationer.”

Det kan vara en verklig begränsning, men det kan också vara en historisk erfarenhet som behöver undersökas. Kanske gäller det bara vissa typer av belastning. Kanske går det att skydda systemet med ett mellanlager. Kanske är begränsningen organisatorisk snarare än teknisk.

Arkitektens roll blir att hjälpa gruppen att sortera:

- Behov: Vad ska bli bättre, för vem och varför?
- Lösningsidé: Hur skulle behovet kunna mötas?
- Begränsning: Vad sätter ramar för möjliga lösningar?
- Antagande: Vad tror vi, men behöver pröva?
- Beslut: Vad väljer vi att göra nu?

Den sorteringen kan verka enkel, men den förändrar ofta samtalet. Den gör det möjligt att börja utan att låsa sig.

## Arkitektens balans: tillräckligt kritisk, tillräckligt nyfiken

När behovsbilden är osäker behöver arkitekten hålla två perspektiv samtidigt.

Det första är det kritiska perspektivet. Arkitekten behöver se risker, beroenden, motsägelser och konsekvenser. Det är en viktig del av rollen. Om ingen ställer de svåra frågorna kan teamet bygga snabbt men fel.

Det andra är det nyfikna perspektivet. Arkitekten behöver också hjälpa organisationen att lära. Alla oklarheter är inte fel. Vissa oklarheter är en naturlig del av att arbeta med verkliga behov i komplexa miljöer.

Om arkitekten bara är kritisk uppstår väntan. Om arkitekten bara är nyfiken uppstår risk. Balansen ligger i att vara tydlig med vad som är farligt att lämna oklart och vad som är klokt att undersöka stegvis.

En användbar fråga är:

> “Vad är det minsta vi behöver förstå för att kunna ta nästa steg utan att skapa onödig framtida inlåsning?”

Den frågan håller ihop ansvar och lärande.

## Vanliga fallgropar

- Fallgrop: Att kräva komplett behovsbild innan något får börja.
  - Varför den uppstår: Arkitekten vill undvika felaktiga lösningsbeslut och skydda organisationen från omarbete.
  - Vad arkitekten kan göra i stället: Skilj mellan frågor som måste klargöras före start, frågor som kan undersökas genom ett begränsat inkrement och frågor som kan bevakas senare.

- Fallgrop: Att acceptera vaga behov för att inte uppfattas som bromsande.
  - Varför den uppstår: Arkitekten vill stödja det agila arbetssättet och undvika att bli en kontrollpunkt.
  - Vad arkitekten kan göra i stället: Hjälp gruppen att formulera antaganden, hypoteser och arkitektoniska konsekvenser utan att kräva en fullständig kravspecifikation.

- Fallgrop: Att omvandla behovsosäkerhet till teknisk lösning för snabbt.
  - Varför den uppstår: Tekniska lösningsbilder kan kännas mer konkreta och hanterbara än otydliga verksamhetsbehov.
  - Vad arkitekten kan göra i stället: Beskriv först lösningsrymden och vilka vägval som bör hållas öppna.

- Fallgrop: Att behandla alla osäkerheter som lika viktiga.
  - Varför den uppstår: Erfarna arkitekter ser många konsekvenser samtidigt och vill fånga helheten.
  - Vad arkitekten kan göra i stället: Prioritera osäkerheter utifrån risk, beslutspåverkan och kostnad om antagandet visar sig fel.

- Fallgrop: Att låta “agilt” betyda att behov inte behöver analyseras.
  - Varför den uppstår: Organisationen vill bort från långa förstudier och tunga överlämningar.
  - Vad arkitekten kan göra i stället: Gör behovsanalysen mer löpande, mer hypotesdriven och närmare teamets lärande.

## Frågor att ställa i situationen

När du som arkitekt möter en osäker behovsbild kan följande frågor hjälpa:

### Frågor om nytta

- Vilken förändring vill vi åstadkomma för medborgare, handläggare eller myndigheten?
- Hur skulle vi märka att första steget skapar nytta?
- Vilken del av nyttan är viktigast att pröva först?

### Frågor om antaganden

- Vad bygger vår lösningsidé på för antaganden?
- Vilket antagande är mest riskabelt om det är fel?
- Vilket antagande kan vi testa genom ett begränsat steg?

### Frågor om arkitektoniska konsekvenser

- Vilka behov påverkar information, integrationer, säkerhet eller förvaltning?
- Vilka beslut skulle bli svåra att ändra senare?
- Vilka vägval bör vi undvika att låsa för tidigt?

### Frågor om avgränsning

- Vilken ärendetyp, målgrupp eller process kan vara ett klokt första avgränsat område?
- Vad ska första inkrementet medvetet inte hantera?
- Vilka risker accepterar vi genom avgränsningen, och vilka minskar vi?

### Frågor om ansvar

- Vilka roller behöver vara med i behovsdialogen redan nu?
- Vem kan avgöra om ett antagande är rimligt?
- Vem behöver förstå konsekvenserna av det första steget?

## Reflektionsfrågor

1. När har du själv varit med om att ett till synes enkelt behov visade sig ha stora arkitektoniska konsekvenser?
2. Hur brukar du reagera när verksamheten beskriver behov på en mycket övergripande nivå?
3. Vilka typer av oklarheter brukar du vilja reda ut innan teamet börjar bygga?
4. Vilka oklarheter skulle i stället kunna undersökas genom ett begränsat inkrement?
5. Hur kan du hjälpa en produktägare att se skillnaden mellan behov, lösningsidé och begränsning?
6. Vilka antaganden i din nuvarande miljö behandlas som sanningar utan att någon nyligen har prövat dem?
7. Hur kan du formulera arkitekturfrågor så att de stödjer lärande snarare än stoppar arbetet?
8. Vad skulle det innebära i din vardag att se behovsanalys som något mer hypotesdrivet?

## Snabb sammanfattning

- Osäker behovsbild är inte alltid ett problem som måste lösas före start. I agil utveckling är det ofta en del av arbetet.
- Arkitektens uppgift är att göra osäkerheten begriplig, prövbar och hanterbar.
- All oklarhet är inte likadan. Vissa frågor måste klargöras tidigt, andra kan undersökas genom begränsade steg och vissa kan bevakas tills vidare.
- Lösningsrymd hjälper gruppen att se möjliga vägar utan att låsa en lösning för tidigt.
- Hypotesdriven behovsanalys kopplar behov, antaganden och arkitekturfrågor till lärande.
- Arkitektoniska konsekvenser av behov gör det möjligt att se hur även enkla verksamhetsönskemål kan påverka information, integrationer, säkerhet, ansvar och förvaltning.
- Ett mer agilt arkitektbeteende är inte att släppa behovsanalysen, utan att göra den mer löpande, prövande och kopplad till nästa kloka steg.

## Nästa steg

I nästa kapitel går vi vidare från osäkra behov till löpande kravarbete. När behovsbilden inte är färdig från början blir kraven inte heller något som kan betraktas som avslutat innan design och utveckling startar. Det förändrar hur arkitekten behöver samarbeta med produktägare, kravanalytiker, verksamhet och team.

Nästa kapitel handlar därför om situationen: när kravarbete blir löpande snarare än avslutat.
