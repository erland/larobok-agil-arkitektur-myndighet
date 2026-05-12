# Kapitel 1: När kartan inte längre ritas färdigt i förväg

## Varför detta kapitel finns

Du som har arbetat länge som lösningsarkitekt eller IT-arkitekt känner sannolikt igen värdet av en tydlig karta. Innan utveckling startar vill man förstå behov, beroenden, målbild, risker, informationsflöden, systemlandskap och möjliga lösningsvägar. Det är inte konstigt. I en myndighetskontext kan otydlighet snabbt få konsekvenser: felaktiga beslut, bristande spårbarhet, svag förankring, säkerhetsrisker eller lösningar som blir svåra att förvalta.

Samtidigt förändras förutsättningarna när organisationen vill arbeta mer agilt. Då räcker det inte alltid att först beskriva hela lösningen och därefter lämna över till utveckling. Behov kan visa sig vara annorlunda än man trodde. Användare kan reagera oväntat. Tekniska beroenden kan visa sig enklare eller svårare än analysen antydde. Nya regler, prioriteringar eller verksamhetsinsikter kan förändra vad som är klokast att göra.

Det här kapitlet handlar om det första skiftet i boken: från att se arkitektur som en karta som behöver ritas färdigt i förväg, till att se arkitektur som ett sätt att skapa tillräcklig riktning för att kunna lära sig säkert och ansvarsfullt under arbetets gång.

Målet är inte att ställa XLPM eller fasorienterade arbetssätt mot agila arbetssätt som om det ena vore rätt och det andra fel. Poängen är snarare att de bygger på olika logik. När logiken förändras behöver även arkitektens sätt att skapa trygghet, riktning och kvalitet förändras.

## Situationen: uppstarten som känns både bekant och ny

Myndigheten för samhällstjänster ska modernisera ett äldre handläggningssystem. Systemet används av handläggare varje dag och har under många år byggts ut steg för steg. Det finns integrationer till andra interna system, beroenden till externa myndigheter, historiska datamodeller, gamla behörighetslösningar och flera manuella rutiner runt systemet.

Sara, erfaren lösningsarkitekt, blir inbjuden till ett tidigt uppstartsmöte.

På mötet finns Erik, produktägare för den nya digitala tjänsten, Lina som representerar utvecklingsteamet och Amir från informationssäkerhet. Verksamheten vill snabbt komma igång med en första digital tjänst för medborgare. Tanken är att en begränsad version ska testas med en mindre användargrupp för att ge återkoppling på flöde, språk, handläggarstöd och tekniska antaganden.

Sara hör flera saker samtidigt.

Erik säger:

> “Vi behöver få ut något litet tidigt, annars kommer vi fortsätta diskutera lösningen i flera månader utan att veta vad som faktiskt fungerar.”

Lina säger:

> “Teamet kan börja med ett smalt flöde, men vi behöver veta vilka arkitekturramar som gäller. Annars riskerar vi att bygga något som vi får göra om.”

Amir säger:

> “Vi kan inte testa med riktiga personuppgifter utan att ha kontroll på informationsklassning, åtkomst, loggning och rättsliga förutsättningar.”

Sara känner igen situationen. Hennes invanda reaktion är att skapa struktur. Hon vill kartlägga nuläget, identifiera beroenden, beskriva målbild, analysera risker och ta fram ett lösningsförslag som kan förankras. Det är ett ansvarsfullt sätt att agera.

Men den här gången förväntar sig organisationen också något annat: att arbetet börjar innan allt är färdiganalyserat.

Frågan blir då inte om Sara ska rita en karta eller inte. Frågan är vilken typ av karta som behövs när terrängen delvis ska upptäckas genom vandringen.

## Det invanda sättet att agera

I en fasorienterad utvecklingslogik är det naturligt att arkitekten kommer in tidigt och bidrar till att skapa en stabil grund för kommande beslut. Ofta finns en tydlig rörelse från behov till krav, från krav till arkitektur, från arkitektur till design och därefter till utveckling, test och införande.

I ett sådant sammanhang blir arkitektens arbete ofta kopplat till att:

- förstå och beskriva nuläge,
- analysera behov och begränsningar,
- identifiera beroenden,
- ta fram målarkitektur eller lösningsarkitektur,
- dokumentera viktiga vägval,
- skapa underlag för beslut,
- minska osäkerhet innan större investeringar görs,
- möjliggöra överlämning till genomförande.

Det finns goda skäl till detta. Stora IT-satsningar i myndigheter behöver ansvar, spårbarhet, budgetlogik, förankring, riskhantering och samordning. En arkitekt som skapar tydlighet tidigt kan förhindra dyra misstag senare.

Det invanda arbetssättet kan därför sammanfattas så här:

> Ju mer vi förstår och beskriver i förväg, desto tryggare kan genomförandet bli.

Detta är inte en orimlig tanke. Den har ofta varit både praktisk och nödvändig. Problemet uppstår när samma tanke används i situationer där en stor del av förståelsen bara kan uppstå genom återkoppling, test, teknisk utforskning och stegvis utveckling.

Då kan det som var tänkt att skapa trygghet i stället skapa väntan.

## Varför det kan skapa friktion i agil utveckling

Agil utveckling bygger på en annan grundlogik. I stället för att utgå från att rätt lösning kan beskrivas tillräckligt komplett i början, utgår man från att förståelsen växer fram. Det betyder inte att man ska börja utan riktning. Det betyder att riktningen behöver kombineras med möjlighet att justera.

Här introducerar vi tre begrepp som följer med genom boken.

**Fasorienterad utvecklingslogik** betyder i den här boken ett arbetssätt där behov, krav, design, utveckling och införande ofta hanteras som tydligt avgränsade faser. Det kan ge struktur, ansvar och tydliga beslutspunkter.

**Agil utvecklingslogik** betyder ett arbetssätt där utveckling sker stegvis, med återkoppling, prioritering och lärande under arbetets gång. Det kan ge snabbare insikt, bättre anpassning och möjlighet att minska risk genom mindre steg.

**Lärandebaserad styrning** betyder att styrningen inte bara utgår från planer och tidiga antaganden, utan också från vad organisationen lär sig genom faktisk utveckling, användning, test och återkoppling.

Friktion uppstår när dessa logiker blandas utan att man pratar om det.

Organisationen kan säga att den vill arbeta agilt, men ändå förvänta sig samma typ av tidigt beslutsunderlag som i en fasorienterad modell. Teamet kan vilja börja bygga iterativt, men sakna tydliga ramar för vilka beslut de får fatta. Arkitekturforum kan vilja kvalitetssäkra, men göra det på ett sätt som skapar väntetider. Verksamheten kan vilja ha snabb nytta, men ändå förvänta sig hög förutsägbarhet kring kostnad, tid och omfattning.

För arkitekten kan detta bli särskilt svårt. Sara förväntas både möjliggöra fart och säkra helhet. Hon ska både släppa fram lärande och skydda organisationen från ogenomtänkta vägval. Hon ska både vara närvarande i teamets vardag och bidra till långsiktiga beslut.

Det är här den gamla kartmetaforen börjar skava. Om kartan måste vara färdig innan resan börjar kommer arbetet att gå långsamt. Om ingen karta finns alls riskerar teamet att gå vilse. Det agila arkitekturarbetet behöver därför en annan sorts karta: en som visar riktning, risker och kända begränsningar, men som också markerar vilka delar av terrängen som ännu behöver utforskas.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt innebär inte att Sara ska avstå från arkitektur. Det innebär att hon behöver ställa andra frågor tidigare.

I stället för att börja med frågan:

> “Hur ska hela lösningen se ut?”

kan hon börja med frågor som:

- Vad behöver vi veta för att kunna ta nästa ansvarsfulla steg?
- Vilka beslut är svåra att ändra senare?
- Vilka antaganden behöver testas innan vi låser lösningen?
- Vilka risker måste vara hanterade innan teamet börjar bygga?
- Vilka ramar behöver teamet för att kunna fatta bra lokala beslut?
- Vilken dokumentation behövs nu för att stödja beslut, samarbete och ansvar?
- Vad är tillräckligt tydligt för att börja lära?

Skillnaden är subtil men viktig.

I en fasorienterad logik blir arkitektens uppgift ofta att reducera osäkerhet innan utveckling startar. I en mer agil logik blir arkitektens uppgift att hjälpa organisationen att hantera osäkerhet medan utvecklingen pågår.

Det kräver fortfarande analys, struktur och omdöme. Men analysen behöver ofta ske i mindre steg. Strukturen behöver kunna utvecklas. Omdömet handlar inte bara om att välja rätt lösning, utan om att avgöra vad som behöver väljas nu och vad som bör hållas öppet.

För Sara kan det innebära att hon inte tar fram en fullständig målarkitektur som första leverans. Hon kan i stället ta fram en första arkitektonisk orientering:

- vilka delar av nuläget som är mest relevanta,
- vilka system och informationsflöden som påverkas,
- vilka kvalitetskrav som inte får tappas bort,
- vilka vägval som verkar svårreversibla,
- vilka antaganden som behöver prövas,
- vilka risker som behöver följas upp,
- vilka ramar teamet behöver för första inkrementet.

Ett *inkrement* betyder här ett avgränsat steg i utvecklingen som ger ny funktion, ny kunskap eller båda. Det behöver inte vara en komplett lösning. Det viktiga är att det för arbetet framåt på ett kontrollerat sätt.

## Exempel: Myndigheten för samhällstjänster

Efter uppstartsmötet väljer Sara att inte börja med att skriva en omfattande lösningsarkitektur. Hon bokar i stället ett kort arbetsmöte med Erik, Lina och Amir. Syftet är att skilja mellan tre typer av frågor:

1. Det vi måste veta innan teamet börjar.
2. Det vi kan undersöka genom ett begränsat första steg.
3. Det vi ännu inte behöver besluta.

De börjar med den första kategorin.

Amir lyfter att informationsklassning och hantering av personuppgifter måste vara tillräckligt tydligt innan någon verklig användardata används. Lina säger att teamet kan bygga en första teknisk prototyp med testdata. Erik vill att prototypen ska spegla ett verkligt användarflöde, men accepterar att den första versionen inte behöver användas skarpt.

Sara sammanfattar:

> “Då verkar det som att vi inte behöver besluta hela framtida lösningen nu. Men vi behöver vara överens om vilka data vi inte får använda, vilka integrationer vi inte ska koppla på än och vilka arkitekturfrågor prototypen ska hjälpa oss att besvara.”

De identifierar tre frågor som första inkrementet ska ge svar på:

- Går det att skapa ett medborgarflöde som handläggare faktiskt kan följa upp i sitt befintliga system?
- Vilka uppgifter behöver tjänsten läsa från det äldre handläggningssystemet?
- Vilka säkerhets- och loggningskrav påverkar lösningens grundstruktur?

Sara dokumenterar inte detta som en fullständig målarkitektur. Hon dokumenterar det som en första arkitektonisk orientering och en lista över öppna antaganden.

Hon ritar en enkel bild över berörda system, markerar vilka kopplingar som är verkliga och vilka som bara är tänkta, och skriver en kort beslutsnotering:

> Första inkrementet ska använda testdata och inte kopplas till produktionsmiljö. Syftet är att undersöka användarflöde, informationsbehov och tekniska beroenden. Beslut om slutligt integrationsmönster skjuts upp tills dessa frågor har prövats.

Det är inte frånvaro av arkitektur. Det är arkitektur i en annan rytm.

## Vanliga fallgropar

- Fallgrop: Att tolka agil utveckling som att arkitektur ska vänta.
  - Varför den uppstår: Organisationen reagerar mot långa förberedelsefaser och vill snabbt börja leverera.
  - Vad arkitekten kan göra i stället: Visa vilken minimal arkitektonisk orientering som behövs för att arbetet ska kunna börja säkert.

- Fallgrop: Att försöka skapa samma arkitekturdokument som tidigare, men snabbare.
  - Varför den uppstår: Arkitekten vill behålla kvalitet och ansvar, men får mindre tid.
  - Vad arkitekten kan göra i stället: Skilj mellan dokumentation som behövs nu, dokumentation som kan växa fram och dokumentation som inte längre fyller ett tydligt syfte.

- Fallgrop: Att låsa lösningen för att skapa trygghet.
  - Varför den uppstår: Osäkerhet upplevs som risk, särskilt i myndighetsmiljö.
  - Vad arkitekten kan göra i stället: Synliggör vilka beslut som verkligen är svåra att ändra och vilka som kan hållas öppna.

- Fallgrop: Att låta teamet börja utan ramar.
  - Varför den uppstår: Organisationen vill undvika tunga processer och överlämningar.
  - Vad arkitekten kan göra i stället: Formulera tydliga startvillkor, risker och principer utan att detaljstyra lösningen.

- Fallgrop: Att prata om “agilt” utan att prata om vilken styrlogik som faktiskt gäller.
  - Varför den uppstår: Begreppet agilt används ofta positivt, men otydligt.
  - Vad arkitekten kan göra i stället: Ställ frågor om beslut, mandat, återkoppling och vad som får ändras när ny kunskap uppstår.

## Frågor att ställa i situationen

När du som arkitekt hamnar i en uppstart där organisationen vill börja agilt men samtidigt efterfrågar tydlig arkitektur, kan följande frågor hjälpa:

- Vad behöver vara sant för att vi ska kunna ta ett första ansvarsfullt steg?
- Vilka risker är oacceptabla att skjuta framför oss?
- Vilka antaganden är så osäkra att de bör testas tidigt?
- Vilka delar av lösningen är dyra eller svåra att ändra senare?
- Vilka beslut kan teamet fatta själv, och vilka behöver bredare förankring?
- Vilken dokumentation behövs för att skapa gemensam förståelse just nu?
- Vilken återkoppling behöver vi efter första steget?
- Vad skulle få oss att ändra riktning?

Dessa frågor hjälper dig att flytta samtalet från “är arkitekturen klar?” till “är vi tillräckligt orienterade för att kunna lära oss på ett kontrollerat sätt?”.

## Reflektionsfrågor

1. När har du själv upplevt att organisationen velat arbeta agilt men samtidigt förväntat sig ett traditionellt beslutsunderlag?
2. I vilka situationer brukar du vilja rita en mer komplett karta innan andra börjar agera?
3. Vilka delar av din arkitekturpraktik skapar trygghet på ett sätt som fortfarande behövs?
4. Vilka delar riskerar att skapa väntan eller låsa lösningen för tidigt?
5. Vad skulle en “första arkitektonisk orientering” kunna innehålla i ditt sammanhang?
6. Vilka beslut behöver du oftare markera som öppna, snarare än försöka lösa direkt?
7. Hur kan du prata med produktägare, team och säkerhetsroller om osäkerhet utan att den uppfattas som brist på kontroll?
8. Vad skulle vara ett litet men ansvarsfullt första steg i ett aktuellt initiativ du känner till?

## Snabb sammanfattning

- Fasorienterad utvecklingslogik och agil utvecklingslogik bygger på olika antaganden om när förståelse uppstår.
- XLPM och liknande arbetssätt behöver inte beskrivas negativt; de kan ge struktur, ansvar och kontroll.
- Friktion uppstår när organisationen vill ha agil utveckling men behåller förväntningar på helt färdiga tidiga underlag.
- Arkitektens uppgift i agil utveckling är inte att släppa riktning, utan att skapa tillräcklig riktning för att möjliggöra lärande.
- En användbar första arkitektonisk orientering kan vara mer värdefull än en omfattande målarkitektur som försöker lösa för mycket för tidigt.
- Den centrala frågan blir: Vad behöver vi veta och besluta nu för att kunna ta nästa ansvarsfulla steg?

## Nästa steg

I nästa kapitel går vi vidare till arkitektens ansvar. Om kartan inte längre ritas färdigt i förväg kan det kännas som att arkitektrollen försvagas. Men det är inte bokens utgångspunkt.

Tvärtom: när utvecklingen blir mer iterativ behöver arkitektens ansvar ofta bli mer aktivt och närvarande. Frågan är inte om arkitekten fortfarande behövs, utan hur arkitekten kan bidra utan att bli en flaskhals.
