# Pedagogisk canon

## Bok

**Arbetstitel:**  
*Från XLPM till agil IT-utveckling: arkitektens nya arbetssätt i statlig myndighet*

**Boktyp:**  
Praktisk lärobok / handbok.

**Språk:**  
Svenska, med etablerade engelska termer när de är tydligare eller mer vedertagna än svenska alternativ.

**Svårighetsgrad:**  
Erfaren.

**Målgrupp:**  
Lösningsarkitekter, IT-arkitekter och närliggande roller i statlig myndighet som är vana vid tidig behovsanalys, kravarbete, arkitektur, design och beslutsunderlag.

**Pedagogisk stil:**  
Kollegial, reflekterande, praktisk och situationsbaserad.

**Övningar:**  
Boken ska inte innehålla traditionella övningar. I stället används reflektionsfrågor, samtalsfrågor och praktiska frågor att ställa i verkliga situationer.

## Grundbudskap

Arkitektens ansvar försvinner inte i agil IT-utveckling. Det förändras.

I en mer fasorienterad utvecklingslogik har arkitekten ofta stort värde genom att skapa riktning, struktur och beslutsunderlag tidigt. I en mer agil utvecklingslogik behövs fortfarande riktning och struktur, men arkitektens bidrag behöver oftare ske genom närvaro, dialog, successiva beslut, tydliga principer och stöd till teamens lärande.

Bokens centrala tanke:

> Arkitekten går från att främst skapa färdiga arkitekturprodukter före utveckling till att utveckla organisationens förmåga att fatta bra arkitektur- och designbeslut över tid.

## Syn på XLPM och fasorienterat arbete

Boken ska beskriva XLPM och fasorienterade arbetssätt neutralt.

- XLPM ska inte framställas som fel, omodernt eller inkompetent.
- Fasorienterat arbete ska beskrivas som ett arbetssätt som kan ge tydlighet, ansvar, beslutsstruktur och kontroll.
- Friktionen ska beskrivas som något som uppstår när arbetssätt, förväntningar och beslutspunkter inte passar den typ av osäker, iterativ IT-utveckling som organisationen försöker bedriva.
- Fokus ska ligga på vad arkitekten behöver göra annorlunda, inte på att kritisera tidigare styrmodeller.

Återanvändbar formulering:

> Det tidigare arbetssättet var inte nödvändigtvis fel. Men när utvecklingen blir mer iterativ behöver arkitektens sätt att skapa trygghet, riktning och kvalitet förändras.

## Återkommande scenario

### Myndigheten för samhällstjänster

Myndigheten för samhällstjänster ansvarar för digitala tjänster som används av både medborgare och handläggare. Den hanterar ärenden där rättssäkerhet, spårbarhet, informationssäkerhet och tillgänglighet är viktiga.

Myndigheten har flera äldre IT-stöd, bland annat ett centralt handläggningssystem. Systemet fungerar, men är svårt att förändra, har många integrationer och kräver mycket samordning vid ändringar.

Myndigheten vill modernisera handläggningsstödet och samtidigt utveckla nya digitala medborgartjänster. Organisationen rör sig från tydligt fasindelade projekt mot mer iterativ utveckling med tätare leveranser och mer teamnära ansvar.

Återkommande spänningar:

- behovet av kontroll kontra behovet av lärande,
- krav på dokumentation kontra behovet av flöde,
- säkerhet och regelefterlevnad kontra kortare utvecklingscykler,
- arkitekturens helhetsperspektiv kontra teamens självständighet,
- långsiktighet kontra stegvisa leveranser,
- styrning kontra lokalt beslutsmandat.

## Återkommande personer

### Sara – erfaren lösningsarkitekt

Sara är lösningsarkitekt på Myndigheten för samhällstjänster. Hon är van att arbeta tidigt i projekt, analysera behov, identifiera beroenden, ta fram lösningsbeskrivningar, formulera arkitekturbeslut och bidra till beslutsunderlag.

Styrkor:

- ser helhet och beroenden,
- förstår både verksamhet och IT,
- kan skapa struktur i otydliga situationer,
- är van att dokumentera och förankra beslut,
- har respekt för myndighetens ansvar, risker och krav.

Utmaning:

Sara behöver inte bli “mindre arkitekt”. Hon behöver bli arkitekt på ett annat sätt: mer närvarande, mer dialogbaserad, mer iterativ och mer inriktad på att hjälpa team och organisation att fatta bra beslut över tid.

### Erik – produktägare eller verksamhetsnära ansvarig

Erik representerar behovet av snabbare återkoppling, tydligare nytta, prioritering och stegvis leverans.

### Lina – teamrepresentant eller utvecklingsledare

Lina representerar teamets perspektiv: behov av tydlighet, självständighet, snabb återkoppling och mindre väntan.

### Amir – säkerhets- och regelefterlevnadsperspektiv

Amir representerar myndighetens ansvar för säkerhet, integritet, regelverk, risk och spårbarhet.

## Kapitelstruktur

Kommande kapitel bör använda denna anpassade mall:

```markdown
# Kapitel X: [Titel]

## Varför detta kapitel finns

## Situationen: [konkret arkitektdilemma]

## Det invanda sättet att agera

## Varför det kan skapa friktion i agil utveckling

## Ett mer agilt förhållningssätt

## Exempel: Myndigheten för samhällstjänster

## Vanliga fallgropar

## Frågor att ställa i situationen

## Reflektionsfrågor

## Snabb sammanfattning

## Nästa steg
```

## Stilregler

- Använd tydlig svensk sakprosa.
- Förklara engelska termer första gången de används.
- Håll stycken relativt korta.
- Börja gärna i konkreta situationer före abstrakta resonemang.
- Använd “I en fasorienterad logik …” och “I en mer agil logik …” för att visa skillnader utan att värdera.
- Var kollegial, inte tillrättavisande.

## Introduktionsordning för centrala begrepp

1. Kapitel 1: fasorienterad utvecklingslogik, agil utvecklingslogik, lärandebaserad styrning.
2. Kapitel 2: kontinuerligt arkitekturarbete, teamnära arkitektur, arkitekt som möjliggörare.
3. Kapitel 3: beslutsförmåga, reversibla och svårreversibla beslut, lagom sena beslut.
4. Kapitel 4: lösningsrymd, hypotesdriven behovsanalys, arkitektoniska konsekvenser av behov.
5. Kapitel 5: löpande kravförfining, icke-funktionella krav, krav som beslutsunderlag.
6. Kapitel 6: tillräcklig arkitektur, arkitektoniska startvillkor, utforskande implementation.
7. Kapitel 7: kontinuerlig design, designprinciper, gemensamt designansvar.
8. Kapitel 8: flödeshämmande beroenden, arkitektur som beroendehantering, beroendereducerande design.
9. Kapitel 9: levande dokumentation, dokumentation för användning, beslutslogg.
10. Kapitel 10: inbyggd kontroll, kontinuerlig riskdialog, säkerhet som designbegränsning.
11. Kapitel 11: beslutsflöde, mandat nära kunskap, arkitekturforum som stödstruktur.
12. Kapitel 12: arkitektonisk närvaro, reflekterande arkitektpraktik, situationsbaserat arkitektledarskap.
