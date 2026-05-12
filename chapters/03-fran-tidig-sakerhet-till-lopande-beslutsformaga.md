# Kapitel 3: Från tidig säkerhet till löpande beslutsförmåga

## Varför detta kapitel finns

I en fasorienterad utvecklingslogik skapas ofta trygghet genom att viktiga vägval görs tidigt. Arkitektur tas fram, granskas och förankras innan utvecklingen går vidare. Det kan vara ett rationellt sätt att minska osäkerhet när uppdraget, lösningsrymden och ansvarsfördelningen är relativt stabila.

I agil IT-utveckling är förutsättningarna ofta mer rörliga. Behov, prioriteringar, tekniska möjligheter, regelkrav och användarinsikter kan förändras medan arbetet pågår. Då räcker det inte att försöka fatta alla viktiga beslut tidigt. Arkitekten behöver i stället bidra till en löpande beslutsförmåga: förmågan att fatta rätt beslut i rätt tid, med rätt personer och med lagom mycket information.

Det betyder inte att beslut ska skjutas upp av bekvämlighet. Det betyder att arkitekten behöver skilja mellan beslut som måste fattas tidigt, beslut som kan vänta och beslut som bör utforskas innan de låses.

## Situationen: när alla vill ha trygghet men ingen vet tillräckligt

Sara är med i arbetet med den nya medborgartjänsten på Myndigheten för samhällstjänster. Tjänsten ska låta medborgare följa sitt ärende digitalt och komplettera uppgifter utan att kontakta handläggare manuellt.

Redan i början uppstår flera arkitekturfrågor:

- Ska tjänsten läsa data direkt från det äldre handläggningssystemet eller via ett mellanlager?
- Hur ska behörighet och åtkomstkontroll hanteras?
- Vilka händelser behöver loggas för spårbarhet?
- Ska tjänsten byggas som en fristående komponent eller nära befintlig plattform?
- Hur mycket av informationsmodellen behöver vara stabil innan teamet börjar bygga?

Flera personer vill ha ett tydligt svar. Produktägaren vill veta vad som går att leverera först. Teamet vill veta vad de kan börja bygga. Säkerhetsfunktionen vill förstå riskerna. Förvaltningen vill undvika en lösning som blir svår att ta över. Styrgruppen vill ha trygghet i att vägvalen är genomtänkta.

Sara känner igen mönstret. I tidigare projekt hade hon ofta tagit fram en mer komplett lösningsarkitektur innan utvecklingen startade. Det gav en känsla av kontroll. Men den här gången är flera grundantaganden fortfarande osäkra. Om hon låser för mycket nu riskerar lösningen att bygga på gissningar. Om hon inte låser något alls riskerar teamet att gå åt olika håll.

Frågan blir därför inte: “Vilken arkitektur ska vi bestämma nu?”

Frågan blir snarare: “Vilka beslut behöver vi fatta nu, vilka behöver vi förbereda, och vilka behöver vi lära oss mer om innan vi låser?”

## Det invanda sättet att agera

När osäkerheten är hög är det vanligt att arkitekten försöker skapa trygghet genom att göra mer analys. Det kan innebära att samla in fler krav, beskriva fler lösningsalternativ, rita fler vyer, boka fler avstämningar och försöka få fler principbeslut på plats innan teamet börjar bygga.

Det invanda beteendet är ofta välmenande. Arkitekten vill undvika kostsamma fel, sena omtag och otydliga ansvar. I en myndighetsmiljö är det dessutom rimligt att vara försiktig. Beslut kan påverka rättssäkerhet, informationssäkerhet, spårbarhet, upphandling, förvaltning och samverkan med andra aktörer.

Men i agil utveckling kan det invanda beteendet skapa tre problem.

För det första kan arkitekten råka behandla alla beslut som om de vore lika viktiga. Då läggs mycket tid på att låsa detaljer som senare visar sig vara lätta att ändra, medan verkligt svåra beslut kanske inte blir tillräckligt synliga.

För det andra kan arbetet hamna i vänteläge. Teamet väntar på arkitekturen. Arkitekten väntar på krav. Kravarbetet väntar på verksamhetsbeslut. Verksamheten väntar på att se vad som är möjligt. Alla väntar på någon annans tydlighet.

För det tredje kan tidiga beslut få för hög status. När ett beslut väl är dokumenterat och förankrat kan det bli svårt att ändra, även om ny kunskap visar att beslutet byggde på fel antaganden.

## Varför det kan skapa friktion i agil utveckling

Agil utveckling bygger på att viss kunskap uppstår genom arbetet. Det går ofta inte att tänka sig fram till alla svar. Vissa svar kommer först när teamet bygger något, testar en integration, möter användare, analyserar faktisk data eller upptäcker en begränsning i befintlig miljö.

Om arkitekturarbetet utgår från att osäkerhet alltid ska reduceras genom mer förarbete, kan det bromsa lärandet. Arkitekturen blir då något som ska vara färdigt innan utvecklingen får börja, i stället för något som hjälper utvecklingen att lära sig på ett kontrollerat sätt.

Samtidigt vore det oansvarigt att säga att “allt kan växa fram”. Vissa beslut är dyra att ändra. Vissa säkerhets- och informationsfrågor behöver hanteras tidigt. Vissa integrationer eller datamodeller påverkar många delar av lösningen. Vissa vägval kan skapa beroenden som blir svåra att lösa senare.

Friktionen uppstår alltså inte för att arkitektur behövs eller inte behövs. Den uppstår när organisationen saknar ett gemensamt sätt att avgöra vilka beslut som behöver tas när.

Här blir arkitektens roll central. Arkitekten behöver hjälpa organisationen att sortera beslut, inte bara fatta dem.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt är att arbeta med beslutsförmåga snarare än enbart beslutspunkter.

En beslutspunkt är ett tillfälle där organisationen säger ja, nej eller välj alternativ A. Beslutsförmåga är bredare. Det handlar om att skapa förutsättningar för bra beslut över tid.

Det innebär att arkitekten hjälper organisationen att:

- se vilka beslut som finns framför den,
- förstå vilka beslut som är brådskande och vilka som kan vänta,
- skilja mellan reversibla och svårreversibla beslut,
- dokumentera beslut på ett sätt som gör dem möjliga att följa upp,
- synliggöra antaganden bakom beslut,
- skapa lärande innan svåra beslut låses,
- se när ett tidigare beslut behöver omprövas.

### Reversibla och svårreversibla beslut

Ett reversibelt beslut är ett beslut som går att ändra senare utan orimlig kostnad, risk eller påverkan. Exempel kan vara en lokal komponentstruktur, ett namn på en intern modul eller en mindre implementationsteknik som bara påverkar ett team.

Ett svårreversibelt beslut är ett beslut som blir dyrt eller svårt att ändra. Exempel kan vara ett integrationsmönster mellan flera system, en grundläggande informationsmodell, en säkerhetsmodell, ett plattformsval eller ett beroende till en extern leverantör.

Poängen är inte att alla beslut kan delas perfekt i två kategorier. Poängen är att frågan hjälper arkitekten och teamet att föra ett bättre samtal.

En enkel fråga kan vara:

> Om vi har fel om detta beslut, hur svårt blir det att ändra senare?

Om svaret är “ganska enkelt” kanske beslutet kan ligga närmare teamet och fattas snabbare. Om svaret är “mycket svårt” behöver beslutet troligen mer gemensam analys, tydligare dokumentation och bredare förankring.

### Lagom sena beslut

I traditionellt projektarbete talar man ofta om vikten av tidiga beslut. I agil utveckling är det ofta mer användbart att tala om lagom sena beslut.

Ett lagom sent beslut fattas inte tidigare än nödvändigt, men inte heller så sent att det skapar väntan, risk eller omarbete.

Det kräver omdöme. Om beslutet fattas för tidigt kan det bygga på svaga antaganden. Om det fattas för sent kan teamet sakna riktning eller bygga in fel struktur.

Arkitektens bidrag blir att formulera beslutets “senaste ansvarsfulla tidpunkt”. Det är inte ett exakt datum i alla lägen, utan en praktisk bedömning:

- När behöver teamet veta detta för att kunna fortsätta?
- Vilka andra beslut påverkas?
- Vilken risk ökar om vi väntar?
- Vilken kunskap kan vi få om vi väntar lite?
- Vad kan vi göra nu för att hålla flera alternativ öppna?

### Beslut, antaganden och lärande

I agil utveckling är det viktigt att skilja mellan beslut och antaganden.

Ett beslut är något organisationen väljer att agera utifrån.

Ett antagande är något organisationen tror, men ännu inte vet.

Många arkitekturdiskussioner blir svåra för att antaganden behandlas som beslut. Någon säger till exempel: “Det äldre systemet klarar nog inte realtidsanrop.” Om detta skrivs in som en begränsning utan att testas kan hela lösningen formas runt något som kanske inte stämmer. Om det i stället behandlas som ett antagande kan teamet planera en teknisk undersökning, en dialog med förvaltningen eller en begränsad testimplementation.

Arkitektens fråga blir då:

> Vet vi detta, har vi beslutat detta, eller antar vi detta?

Den frågan kan låta enkel, men den förändrar samtalet. Den hjälper teamet att se vad som är fast, vad som är valt och vad som behöver undersökas.

## Exempel: Myndigheten för samhällstjänster

Sara samlar produktägaren Erik, teamrepresentanten Lina och säkerhetsspecialisten Amir för att prata om medborgartjänstens åtkomst till ärendedata.

Från början låter diskussionen som en vanlig lösningsdiskussion.

Erik vill att medborgarna snabbt ska kunna se status på sina ärenden. Lina vill veta vilket API teamet ska bygga mot. Amir vill säkerställa att åtkomstkontroll, loggning och spårbarhet inte blir efterhandskonstruktioner. Sara ser att valet av integrationsmönster kan påverka både säkerhet, prestanda, förvaltning och framtida tjänster.

I stället för att direkt föreslå en målarkitektur ritar Sara upp tre kolumner på tavlan:

1. Beslut som behöver fattas nu.
2. Beslut som kan vänta.
3. Antaganden som behöver undersökas.

I den första kolumnen hamnar att medborgartjänsten inte får läsa mer information än vad medborgaren har rätt att se, och att alla åtkomster till ärendeinformation behöver vara spårbara. Det är inte detaljerad design, men det är arkitektoniska startvillkor.

I den andra kolumnen hamnar exakt teknik för hur statusinformationen ska presenteras i gränssnittet. Det påverkar inte de svåraste vägvalen ännu.

I den tredje kolumnen hamnar antagandet att det äldre handläggningssystemet inte klarar den typ av anrop som tjänsten skulle behöva. Teamet får i uppgift att undersöka detta genom en begränsad teknisk spike och dialog med förvaltningen.

Sara dokumenterar inte detta som en färdig lösningsarkitektur. Hon dokumenterar det som en beslutsbild:

- vad som är beslutat,
- varför det är beslutat,
- vad som fortfarande är öppet,
- vilka antaganden som behöver testas,
- när frågan behöver tas upp igen.

Efter mötet har teamet tillräcklig riktning för att börja undersöka lösningen. Samtidigt har de viktigaste riskerna inte gömts undan. De har blivit synliga.

## Vanliga fallgropar

- Fallgrop: Alla beslut behandlas som arkitekturbeslut.
  - Varför den uppstår: Arkitekten vill säkra helheten och undvika lokala beslut som får oväntade konsekvenser.
  - Vad arkitekten kan göra i stället: Skilj mellan beslut som påverkar helhet, kvalitet och handlingsutrymme och beslut som teamet kan fatta lokalt.

- Fallgrop: Beslut skjuts upp utan plan.
  - Varför den uppstår: Organisationen vill vara agil och undvika att låsa sig för tidigt.
  - Vad arkitekten kan göra i stället: Formulera vad som behöver läras innan beslutet tas och när beslutet senast behöver fattas.

- Fallgrop: Antaganden dokumenteras som fakta.
  - Varför den uppstår: I tidiga diskussioner blandas erfarenhet, oro och tidigare sanningar ihop med verifierad kunskap.
  - Vad arkitekten kan göra i stället: Märk tydligt vad som är känt, vad som är beslutat och vad som är antaget.

- Fallgrop: Tidiga beslut blir svåra att ompröva.
  - Varför den uppstår: När ett beslut har presenterats i styrning eller dokumentation får det ofta organisatorisk tyngd.
  - Vad arkitekten kan göra i stället: Dokumentera beslutets grund, giltighet och omprövningspunkter.

- Fallgrop: Teamet tolkar öppna beslut som att allt är fritt.
  - Varför den uppstår: Arkitekten vill ge teamet handlingsutrymme men är otydlig med ramarna.
  - Vad arkitekten kan göra i stället: Beskriv tydliga startvillkor, principer och riskområden även när detaljlösningen är öppen.

## Frågor att ställa i situationen

När du som arkitekt hamnar i en osäker beslutssituation kan följande frågor hjälpa:

1. Vilket beslut är det egentligen vi försöker fatta?
2. Vad händer om vi väntar med beslutet?
3. Vad händer om vi fattar beslutet nu och har fel?
4. Är beslutet reversibelt eller svårreversibelt?
5. Vilka antaganden ligger bakom beslutet?
6. Vilken kunskap saknas för att fatta ett bättre beslut?
7. Kan vi lära oss det genom en begränsad undersökning?
8. Vem har bäst kunskap för att vara med i beslutet?
9. Vem påverkas av beslutet senare?
10. Hur behöver beslutet dokumenteras för att vara användbart?

## Reflektionsfrågor

1. Vilka typer av beslut brukar du vilja få på plats tidigt?
2. Vilka av dessa beslut är faktiskt svårreversibla?
3. Vilka beslut i din vardag fattas ofta för tidigt av vana?
4. Vilka beslut skjuts ofta upp för länge?
5. Hur brukar ni dokumentera varför ett arkitekturbeslut fattades?
6. När omprövar ni tidigare arkitekturbeslut?
7. Vilka antaganden behandlas ofta som fakta i din organisation?
8. Vad skulle förändras om ni oftare frågade: “Vad behöver vi lära oss innan vi låser detta?”

## Snabb sammanfattning

- I agil utveckling behöver arkitekten bidra till löpande beslutsförmåga, inte bara till tidiga beslutspunkter.
- Alla beslut är inte lika viktiga. Arkitekten behöver hjälpa organisationen att sortera beslut efter risk, påverkan och reversibilitet.
- Reversibla beslut kan ofta fattas snabbare och närmare teamet.
- Svårreversibla beslut kräver mer omsorg, tydligare förankring och bättre dokumentation.
- Ett lagom sent beslut fattas när tillräcklig kunskap finns, men innan väntan, risk eller omarbete blir för stort.
- Antaganden bör inte smygas in som fakta. De bör synliggöras och undersökas.
- Arkitektens uppgift är inte att eliminera all osäkerhet, utan att göra osäkerheten möjlig att hantera.

## Nästa steg

Nästa kapitel går in i en situation där osäkerheten ofta börjar: när behovsbilden ännu inte är stabil. Där ser vi hur arkitekten kan bidra redan innan verksamheten har formulerat ett tydligt kravpaket, utan att för tidigt låsa lösningen.
