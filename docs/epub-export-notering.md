# EPUB-export – status och kompletteringar

Projektet är förberett för EPUB-export på underlagsnivå.

## Finns i paketet

- Författare: Erland Lindmark
- Språk: svenska (`sv`)
- Titel i exportmetadata
- Kapitelordning i `docs/export-metadata.yaml`
- Inledning i `chapters/00-inledning.md`
- 12 kapitel i `chapters/`
- Markdown som källformat

## Saknas inte, men kan kompletteras

Följande är inte nödvändigt för att skapa en enkel EPUB, men rekommenderas inför slutlig publicering:

- omslagsbild,
- slutlig undertitel,
- förlagsnamn,
- slutlig rättighetstext,
- ISBN om boken ska publiceras formellt,
- redaktionell språkgranskning,
- eventuell EPUB-specifik CSS eller mall.

## Möjligt exportflöde

En EPUB kan skapas med ett verktyg som Pandoc genom att använda kapitelordningen i `docs/export-metadata.yaml`.

Exempel på princip:

```bash
pandoc chapters/00-inledning.md chapters/01-*.md chapters/02-*.md chapters/03-*.md chapters/04-*.md chapters/05-*.md chapters/06-*.md chapters/07-*.md chapters/08-*.md chapters/09-*.md chapters/10-*.md chapters/11-*.md chapters/12-*.md \
  --metadata-file=docs/export-metadata.yaml \
  -o exports/fran-xlpm-till-agil-it-utveckling.epub
```

Kommandot kan behöva justeras beroende på lokalt verktyg, önskad mall och omslagsbild.
