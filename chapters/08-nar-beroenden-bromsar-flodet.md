# Kapitel 8: När beroenden bromsar flödet

## Varför detta kapitel finns

I ett fasorienterat arbetssätt hanteras beroenden ofta genom planering, samordning och beslutspunkter. Man kartlägger vilka system, leverantörer, verksamhetsdelar och beslut som påverkar varandra. Därefter försöker man lägga en plan där beroendena hanteras i rätt ordning. För en arkitekt är detta välbekant arbete: att se kopplingarna, förstå konsekvenserna och hjälpa organisationen att undvika överraskningar.

I agil utveckling försvinner inte beroendena. Ofta blir de tvärtom mer synliga. När team försöker leverera i kortare cykler märks det snabbt om de måste vänta på ett annat system, ett beslut, en miljö, en integration, en säkerhetsbedömning eller en leverantör. Det som i en lång projektplan kunde se hanterbart ut blir i ett iterativt flöde till konkret väntan.

Det här kapitlet handlar om arkitektens roll när beroenden bromsar utvecklingsflödet. Fokus ligger inte bara på att identifiera beroenden, utan på att förstå vilka beroenden som kan minskas, vilka som behöver göras tydligare och vilka som måste hanteras genom bättre samspel.

Kapitlets kärnfråga är:

> Hur kan arkitekten hjälpa organisationen att gå från beroendekartläggning till aktiv beroendehantering?

## Situationen: “Vi är klara, men vi väntar på tre andra”

På Myndigheten för samhällstjänster har teamet kommit vidare med den nya medborgartjänsten. De har byggt en första version av en vy där medborgaren kan se status på sitt ärende. Funktionen är smal, men användbar. Den visar inte allt, men den räcker för att börja testa nytta och förståelse med en begränsad grupp användare.

På ett avstämningsmöte sammanfattar Lina läget:

> “Själva vyn är nästan klar. Men vi kan inte släppa den förrän integrationen mot handläggningssystemet är ändrad, loggningen är godkänd och den externa myndigheten har bekräftat sitt datagränssnitt.”

Erik, produktägaren, ser frustrerad ut:

> “Så vi är klara, men ändå inte klara?”

Sara känner igen situationen. Teamet har arbetat iterativt och fokuserat. Ändå står leveransen still. Det finns beroenden till:

- det äldre handläggningssystemet,
- en integrationsplattform,
- informationssäkerhetsfunktionen,
- en extern myndighet,
- ett separat team som ansvarar för behörighet,
- en förvaltningsgrupp som behöver acceptera nya driftflöden,
- ett arkitekturforum som ska ta ställning till ett undantag.

I en projektplan hade dessa beroenden kanske funnits som aktiviteter, milstolpar och samordningspunkter. I teamets vardag blir de i stället väntan, osäkerhet och omprioriteringar. Teamet kan inte leverera det de har byggt, och produktägaren får svårt att skapa tydliga förväntningar.

Sara märker att hennes första impuls är att göra en mer komplett beroendekarta. Det är inte fel. Men hon inser också att en karta inte räcker. Om beroendena är inbyggda i lösningen, organisationen och beslutsvägarna behöver de hanteras mer aktivt.

Hon börjar därför ställa andra frågor:

- Vilka beroenden är nödvändiga?
- Vilka beroenden har vi själva skapat genom designval?
- Vilka beroenden kan ersättas av tydligare gränssnitt?
- Vilka beroenden kan hanteras genom tillfälliga lösningar medan vi lär oss?
- Vilka beroenden kräver beslut på en annan nivå?
- Vilka beroenden behöver göras synliga för styrning och prioritering?

Det är här arkitektens bidrag blir centralt. Inte genom att ensam lösa alla beroenden, utan genom att hjälpa organisationen att förstå vilka beroenden som går att reducera, vilka som behöver koordineras och vilka som visar på djupare strukturella problem.

## Det invanda sättet att agera

Det invanda sättet att arbeta med beroenden är ofta att kartlägga dem, beskriva dem och planera runt dem. Arkitekten identifierar vilka system som påverkas, vilka gränssnitt som behövs, vilka beslut som måste fattas och vilka parter som behöver involveras. Resultatet kan bli beroendekartor, integrationsöversikter, tidplaner, ansvarsmatriser och risklistor.

Detta kan vara mycket värdefullt. I en myndighetsmiljö finns ofta verkliga beroenden som inte kan ignoreras. Äldre system kan innehålla verksamhetskritisk logik. Andra myndigheter kan äga data eller processer. Säkerhet, juridik och förvaltning behöver ofta involveras. Vissa beroenden är helt enkelt en del av uppdragets natur.

Problemet uppstår när beroendehantering stannar vid kartläggning och koordinering. Då kan arkitekten hjälpa organisationen att förstå varför arbetet är svårt, men inte nödvändigtvis hjälpa den att bli mindre beroende.

I en fasorienterad logik kan det kännas tillräckligt att veta vilka beroenden som finns och när de ska hanteras. I en agil logik behöver man oftare fråga om beroendet kan förändras. Annars riskerar teamet att få ett agilt arbetssätt på ytan, men ett långsamt beroendenät under ytan.

Typiska invanda reaktioner är:

- att skapa en mer detaljerad beroendeplan,
- att kalla till fler samordningsmöten,
- att eskalera beroenden till styrgrupp,
- att vänta in andra parter innan teamet får gå vidare,
- att acceptera beroenden som givna eftersom “så ser landskapet ut”,
- att behandla alla beroenden som planeringsproblem snarare än designproblem.

Alla dessa åtgärder kan behövas ibland. Men de räcker inte alltid. Om beroendena återkommer i leverans efter leverans behöver arkitekten också undersöka om lösningens struktur, ansvarsfördelning eller tekniska gränser behöver förändras.

## Varför det kan skapa friktion i agil utveckling

Agil utveckling bygger på att team kan skapa värde stegvis, få återkoppling och anpassa sig. Många beroenden gör detta svårt. Varje gång ett team behöver vänta på någon annan innan det kan testa, leverera eller ändra något minskar möjligheten till lärande.

Beroenden skapar friktion på flera sätt.

För det första skapar de väntan. Teamet kan ha gjort sitt arbete, men ändå inte kunna leverera eftersom ett annat system, beslut eller godkännande saknas.

För det andra skapar de omarbete. När ett beroende ändras sent kan teamet behöva ändra design, implementation eller prioritering.

För det tredje skapar de otydligt ansvar. Om flera team och funktioner behöver agera samtidigt blir det lätt oklart vem som faktiskt äger framdriften.

För det fjärde skapar de falsk lokal effektivitet. Varje team kan vara upptaget och produktivt, men helheten rör sig långsamt eftersom arbetet fastnar mellan team, system och beslutspunkter.

För det femte kan beroenden dölja arkitektoniska problem. Ett team som alltid väntar på samma system kanske inte bara har ett planeringsproblem. Det kan ha ett kopplingsproblem. Ett team som alltid måste gå via samma forum kanske inte bara har ett styrningsproblem. Det kan ha ett mandatproblem.

För arkitekten innebär detta en viktig förskjutning:

> Beroenden är inte bara något som ska samordnas. De är signaler om hur lösningen och organisationen faktiskt är strukturerade.

När arkitekten ser beroenden på det sättet blir frågan större än “hur planerar vi runt detta?”. Den blir också “vad i vår arkitektur gör att detta beroende fortsätter att bromsa oss?”.

## Ett mer agilt förhållningssätt

Ett mer agilt förhållningssätt börjar med att skilja mellan olika typer av beroenden. Alla beroenden är inte likadana, och de ska inte hanteras på samma sätt.

En enkel indelning är:

1. **Tekniska beroenden**  
   Beroenden till system, plattformar, integrationer, miljöer, datakällor eller tekniska komponenter.

2. **Informationsberoenden**  
   Beroenden till datamodeller, informationsägare, begreppsdefinitioner, informationsklassning eller datakvalitet.

3. **Organisatoriska beroenden**  
   Beroenden till team, enheter, leverantörer, förvaltning, drift eller externa myndigheter.

4. **Beslutsberoenden**  
   Beroenden till forum, styrgrupper, arkitekturgranskningar, säkerhetsbeslut eller formella godkännanden.

5. **Kompetensberoenden**  
   Beroenden till enskilda personer eller specialistfunktioner som behövs för att arbetet ska kunna gå vidare.

När beroendet är synligt kan arkitekten hjälpa till att välja strategi. Det finns åtminstone fem möjliga strategier.

### 1. Acceptera beroendet och gör det synligt

Vissa beroenden är verkliga och rimliga. En myndighet kan inte ensidigt ändra ett gränssnitt hos en annan myndighet. Ett team kan inte bortse från informationssäkerhetskrav. En juridisk bedömning kan vara nödvändig innan viss information exponeras.

Då är målet inte att låtsas att beroendet kan tas bort. Målet är att göra det synligt tidigt, formulera vad som behövs och skapa realistiska förväntningar.

Frågor att ställa:

- Vad väntar vi på?
- Vem äger beroendet?
- När behöver vi besked?
- Vad händer om beskedet dröjer?
- Finns det ett mindre steg vi kan ta under tiden?

### 2. Minska beroendet genom design

Vissa beroenden finns därför att lösningen är starkt kopplad. Om varje liten ändring i medborgartjänsten kräver ändring i handläggningssystemet kommer teamet att bromsas gång på gång.

Här kan arkitekten bidra genom beroendereducerande design. Det kan handla om tydligare gränssnitt, mellanlager, händelsebaserad kommunikation, stabilare kontrakt, bättre informationsmodeller eller att flytta ansvar till rätt del av lösningen.

Poängen är inte att införa en teknisk lösning för sakens skull. Poängen är att minska den praktiska väntan och göra teamens arbete mer självständigt där det är rimligt.

Frågor att ställa:

- Varför behöver detta team vänta på detta system?
- Är beroendet tekniskt nödvändigt eller historiskt uppkommet?
- Kan ett stabilt gränssnitt minska koordineringen?
- Kan vi dela upp ansvaret annorlunda?
- Vilken koppling kostar mest i återkommande väntan?

### 3. Skapa en tillfällig frikoppling för att lära

Ibland behöver teamet komma vidare för att testa ett antagande, även om alla integrationer inte är färdiga. Då kan en tillfällig lösning vara rimlig, till exempel en begränsad testdatakälla, en simulerad tjänst, en manuell kontroll i ett tidigt skede eller en smal implementation som inte kräver full integration.

Detta är inte samma sak som att bygga slarvigt. Skillnaden ligger i tydlighet. En tillfällig frikoppling behöver ha ett syfte, en tidsgräns och ett beslut om hur den ska hanteras senare.

Frågor att ställa:

- Vad behöver vi lära oss innan beroendet är löst?
- Kan vi testa användarvärde utan full integration?
- Vilken tillfällig lösning är acceptabel ur riskperspektiv?
- Hur dokumenterar vi att detta är tillfälligt?
- När behöver den tillfälliga lösningen ersättas?

### 4. Flytta beslut närmare kunskap

Vissa beroenden uppstår för att beslut måste tas långt från dem som har mest aktuell kunskap. Om teamet behöver vänta på ett forum för beslut som egentligen ryms inom etablerade principer kan styrningen skapa onödig väntan.

Arkitekten kan då hjälpa till att tydliggöra vilka beslut teamet får fatta själv, vilka som kräver arkitektdialog och vilka som behöver formellt forum.

Frågor att ställa:

- Behöver detta beslut verkligen fattas i ett forum?
- Finns det principer som gör att teamet kan fatta beslutet själv?
- Vilken risk motiverar en högre beslutsnivå?
- Kan forumet ge ramar i stället för att godkänna varje enskilt vägval?

### 5. Förändra planeringen utifrån beroendets natur

När ett beroende inte kan tas bort kan arbetet behöva planeras annorlunda. Det kan innebära att ta beroendefrågor tidigare, skapa gemensamma planeringspunkter, synkronisera med externa parter eller välja ett annat första inkrement.

Det viktiga är att planeringen inte bara utgår från vad teamet vill bygga, utan också från vad beroendena gör möjligt att lära och leverera.

Frågor att ställa:

- Vilket inkrement ger värde med minst kritiska beroenden?
- Vilket beroende behöver lösas först för att öppna flera senare steg?
- Kan vi välja en annan ordning som minskar väntan?
- Vilka beroenden behöver vara en del av prioriteringen, inte bara genomförandet?

## Exempel: Myndigheten för samhällstjänster

Sara samlar Lina, Erik och Amir för att titta på varför den första versionen av medborgartjänsten har fastnat. Hon ritar inte en fullständig beroendekarta över hela myndigheten. I stället börjar hon med den konkreta leveransen som står still.

De identifierar fyra beroenden.

Det första är integrationen till det äldre handläggningssystemet. Teamet behöver läsa ärendestatus, men handläggningssystemet är inte byggt för tät extern åtkomst. Varje ändring kräver samordning med förvaltningsgruppen.

Det andra är loggning. Amir påpekar att åtkomst till ärendestatus behöver kunna följas upp, särskilt eftersom informationen kan vara känslig.

Det tredje är begreppsdefinitioner. Verksamheten använder flera interna statuskoder som inte är begripliga för medborgare.

Det fjärde är en extern myndighet som äger vissa kompletterande uppgifter. Den integrationen kommer inte att vara klar inom den närmaste tiden.

Tidigare hade Sara kanske främst sammanställt beroendena och lyft dem till styrning. Nu väljer hon att sortera dem.

- Integrationen till handläggningssystemet är både tekniskt och organisatoriskt beroende.
- Loggningen är ett säkerhets- och regelefterlevnadsberoende.
- Statuskoderna är ett informationsberoende.
- Den externa myndigheten är ett externt beroende som teamet inte kan styra över.

När de sorterar beroendena ser de att alla inte behöver lösas på samma sätt.

För den första versionen beslutar de att bara visa status för ett begränsat antal ärendetyper. Det minskar beroendet till handläggningssystemets mest komplexa delar.

För loggningen tar Sara och Amir fram ett arkitektoniskt startvillkor: ingen extern visning utan spårbar åtkomstlogg. Men de gör också klart vilken miniminivå som räcker för den första begränsade användartesten.

För statuskoderna skapar teamet en enkel översättningstabell, men dokumenterar att den är en medveten mellanlösning. Sara markerar beslutet i beslutsloggen eftersom det kan påverka framtida informationsarkitektur.

För den externa myndigheten väljer Erik att inte vänta. Den första versionen får tydligt avgränsas till ärenden där den externa informationen inte behövs.

Resultatet är inte att alla beroenden försvinner. Men teamet går från att vara blockerat till att kunna leverera ett smalare inkrement med tydliga begränsningar.

Sara sammanfattar:

> “Vi har inte löst hela beroendebilden. Men vi har skilt på det som måste vara på plats, det som kan avgränsas bort, det som kan göras tillfälligt och det som behöver ett långsiktigt arkitekturbeslut.”

Det är ett annat sätt att arbeta med beroenden. Mindre fokus på att allt ska vara koordinerat innan utvecklingen fortsätter. Mer fokus på att förstå beroendena tillräckligt väl för att kunna minska väntan och fatta bättre stegvisa beslut.

## Vanliga fallgropar

- **Fallgrop: Att behandla alla beroenden som planeringsfrågor**
  - Varför den uppstår: Det är naturligt att vilja lösa väntan genom bättre koordinering, möten och tidplaner.
  - Vad arkitekten kan göra i stället: Undersök om beroendet också är ett designproblem, ett mandatproblem eller ett informationsproblem.

- **Fallgrop: Att acceptera historiska kopplingar som naturlagar**
  - Varför den uppstår: Äldre systemlandskap har ofta vuxit fram under lång tid, och kopplingarna känns givna.
  - Vad arkitekten kan göra i stället: Fråga vilka kopplingar som faktiskt behövs för värdeskapandet och vilka som bara finns på grund av tidigare designval.

- **Fallgrop: Att minska beroenden genom att skapa nya dolda beroenden**
  - Varför den uppstår: En snabb mellanlösning kan verka frikoppla teamet, men samtidigt skapa ny teknikskuld eller otydligt ansvar.
  - Vad arkitekten kan göra i stället: Dokumentera tillfälliga lösningar, tidsätt dem och följ upp dem som arkitekturbeslut.

- **Fallgrop: Att eskalera för många beslut**
  - Varför den uppstår: När riskerna är oklara känns det tryggt att lyfta frågor till forum eller styrning.
  - Vad arkitekten kan göra i stället: Skilj på beslut som kräver formellt mandat och beslut som kan fattas inom etablerade principer.

- **Fallgrop: Att optimera ett team men glömma helheten**
  - Varför den uppstår: Agila team kan bli starkt fokuserade på sitt eget flöde och sin egen leverans.
  - Vad arkitekten kan göra i stället: Titta på hur lokala förenklingar påverkar andra team, förvaltning, säkerhet och framtida ändringsbarhet.

## Frågor att ställa i situationen

När ett beroende bromsar arbetet kan arkitekten använda följande frågor:

1. Vad är det konkret som teamet väntar på?
2. Är beroendet tekniskt, organisatoriskt, informationsmässigt, beslutsmässigt eller kompetensmässigt?
3. Är beroendet nödvändigt, eller ett resultat av tidigare design- eller organisationsval?
4. Kan beroendet minskas genom ett tydligare gränssnitt eller en annan ansvarsfördelning?
5. Kan teamet lära något värdefullt genom ett smalare inkrement?
6. Vilken risk uppstår om vi går vidare utan att beroendet är helt löst?
7. Vem behöver fatta beslut om avgränsning, risk eller prioritering?
8. Hur dokumenterar vi beroendet så att det inte försvinner ur sikte?
9. Är detta ett enstaka hinder eller ett återkommande mönster?
10. Vad skulle göra nästa liknande leverans mindre beroende?

## Reflektionsfrågor

1. Vilka beroenden bromsar oftast utvecklingsflödet i din organisation?
2. Vilka av dessa beroenden brukar beskrivas som planeringsproblem, men kan egentligen vara arkitekturproblem?
3. När har du sett ett team vara lokalt effektivt men ändå fastna i helhetens beroenden?
4. Vilka beroenden är rimliga och nödvändiga i din myndighetskontext?
5. Vilka beroenden skulle kunna minska genom tydligare gränssnitt, ansvar eller principer?
6. Hur brukar du som arkitekt agera när ett team väntar på andra?
7. Vilken fråga skulle du kunna börja ställa oftare: “Hur koordinerar vi detta?” eller “Varför är vi beroende på det här sättet?”
8. Vilket beroende borde lyftas som ett långsiktigt arkitekturbeslut snarare än som ett återkommande leveranshinder?

## Snabb sammanfattning

Beroenden är inte bara något som ska kartläggas. De påverkar teamens möjlighet att leverera, lära och anpassa sig.

I en fasorienterad logik hanteras beroenden ofta genom planering, samordning och beslutspunkter. I en mer agil logik behöver arkitekten också fråga om beroendena kan minskas, frikopplas eller hanteras på ett sätt som stödjer flöde.

Alla beroenden ska inte tas bort. Vissa är nödvändiga, särskilt i myndighetsmiljöer med säkerhet, juridik, förvaltning och externa aktörer. Men beroenden behöver förstås tillräckligt väl för att organisationen ska kunna avgöra vilka som ska accepteras, vilka som ska göras synliga, vilka som ska reduceras och vilka som kräver långsiktiga arkitekturbeslut.

Arkitektens bidrag är att hjälpa organisationen se skillnaden mellan:

- beroenden som måste samordnas,
- beroenden som kan minskas genom design,
- beroenden som kan hanteras genom avgränsade inkrement,
- beroenden som kräver tydligare mandat,
- beroenden som visar att arkitekturen behöver förändras.

## Nästa steg

När beroenden hanteras mer aktivt blir dokumentationen viktig på ett nytt sätt. Det räcker inte att dokumentera lösningen som den borde se ut i slutet. Organisationen behöver också kunna förstå vilka beslut som har fattats, varför vissa beroenden accepterats, vilka mellanlösningar som finns och vilka risker som ska följas upp.

Nästa kapitel handlar därför om **dokumentation som stöd för lärande och ansvar**. Där flyttas fokus från dokumentation som leverans eller godkännande till dokumentation som ett praktiskt stöd för beslut, samordning, spårbarhet och fortsatt utveckling.
