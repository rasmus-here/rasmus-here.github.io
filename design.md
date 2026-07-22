---
version: 1.0.0
status: active
name: HERE Digital Growth System
description: Design specification for HERE's public website. The system balances a confident growth-agency identity with readable, accessible and work-focused interfaces.
language: sv-SE
sourceOfTruth: /src/styles.css
colors:
  brand-dark: "#041f1f"
  brand-primary: "#0b3535"
  brand-secondary: "#195a58"
  brand-line: "#2c8c89"
  accent-primary: "#dd9d1d"
  accent-bright: "#f0b53d"
  surface-primary: "#eff0f1"
  surface-raised: "#ffffff"
  surface-muted: "#e9eded"
  text-on-dark: "#eff0f1"
  text-on-dark-muted: "rgba(239, 240, 241, 0.78)"
  text-primary: "#000000"
  text-secondary: "rgba(0, 0, 0, 0.72)"
  border-on-dark: "rgba(239, 240, 241, 0.14)"
  border-on-light: "rgba(11, 53, 53, 0.14)"
  focus: "#f0b53d"
typography:
  family-sans: "Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
  family-mono: "ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace"
  display:
    fontSize: "clamp(3.2rem, 5.5vw, 5.8rem)"
    fontWeight: 850
    lineHeight: 1.02
    letterSpacing: 0
  page-title:
    fontSize: "clamp(2.8rem, 6vw, 5.5rem)"
    fontWeight: 850
    lineHeight: 1.02
    letterSpacing: 0
  section-title:
    fontSize: "clamp(2.2rem, 4.5vw, 4.5rem)"
    fontWeight: 850
    lineHeight: 1.06
    letterSpacing: 0
  card-title:
    fontSize: "1.35rem"
    fontWeight: 800
    lineHeight: 1.18
    letterSpacing: 0
  body-large:
    fontSize: "clamp(1.08rem, 1.7vw, 1.36rem)"
    fontWeight: 400
    lineHeight: 1.62
    letterSpacing: 0
  body:
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: 0
  eyebrow:
    fontSize: "0.78rem"
    fontWeight: 850
    lineHeight: 1.2
    letterSpacing: 0
    textTransform: uppercase
  button:
    fontSize: "1rem"
    fontWeight: 800
    lineHeight: 1.2
    letterSpacing: 0
spacing:
  1: 4px
  2: 8px
  3: 12px
  4: 16px
  5: 20px
  6: 24px
  8: 32px
  10: 40px
  12: 48px
  16: 64px
  20: 80px
  24: 96px
  base: 4px
rounded:
  control: 8px
  card: 8px
  form-embed: 18px
  pill: 999px
layout:
  contentMaxWidth: 1280px
  readingMaxWidth: 780px
  desktopGutter: 24px
  mobileGutter: 16px
  breakpoints:
    mobile: 720px
    compact-desktop: 1080px
components:
  button-primary:
    backgroundColor: "{colors.accent-primary}"
    textColor: "#ffffff"
    typography: "{typography.button}"
    rounded: "{rounded.control}"
    minHeight: 48px
    padding: "0 20px"
  button-secondary:
    backgroundColor: "rgba(239, 240, 241, 0.08)"
    textColor: "#ffffff"
    borderColor: "rgba(239, 240, 241, 0.34)"
    typography: "{typography.button}"
    rounded: "{rounded.control}"
    minHeight: 48px
    padding: "0 20px"
  focus-ring:
    outline: "3px solid {colors.focus}"
    outlineOffset: 3px
  card:
    backgroundColor: "{colors.surface-primary}"
    textColor: "{colors.text-primary}"
    rounded: "{rounded.card}"
    padding: 24px
  navigation:
    backgroundColor: "rgba(4, 31, 31, 0.96)"
    textColor: "rgba(239, 240, 241, 0.90)"
    activeTextColor: "{colors.accent-bright}"
    minHeight: 76px
  input:
    backgroundColor: "#ffffff"
    textColor: "{colors.text-primary}"
    borderColor: "{colors.accent-primary}"
    rounded: "{rounded.control}"
    minHeight: 44px
motion:
  fast: 150ms
  standard: 240ms
  easing: ease
  reducedMotion: disable-nonessential
imagery:
  preferredFormats:
    - webp
    - svg
  cardAspectRatio: "4 / 3"
  editorialAspectRatio: "16 / 9"
  portraitObjectPosition: "center 24%"
  defaultTreatment: natural
  optionalTeamTreatment: grayscale
---

# HERE Digital Growth System

## Översikt

HEREs webbdesign ska kännas tydlig, kunnig och mänsklig. Den mörkgröna identiteten skapar kontinuitet genom hela upplevelsen, medan ljusa innehållsytor används för längre texter, jämförelser och arbetsintensiva vyer. Guld är en signal för prioritet och handling, inte en dekorationsfärg.

Systemet är framtaget för den publika webbplatsen på `here.se`. Tokens ovan är maskinläsbara. Riktlinjerna nedan beskriver hur de ska tillämpas. Den implementerade källan finns i `/src/styles.css`; denna fil dokumenterar och stabiliserar besluten.

## Varumärkesprinciper

- Sätt faktisk information och faktisk funktion före marknadsföringsdekor.
- Låt mörkgröna ytor bära varumärket och ljusa ytor bära längre läsning.
- Använd guld för primära CTA-knappar, aktiva tillstånd, små kapitelmarkörer och fokus.
- Skapa variation med fotografi, typografisk hierarki och tonala ytor, inte med dekorativa former.
- Prioritera en lugn, professionell byråkänsla framför en lekfull produkt- eller startup-estetik.

## Färger

`brand-primary` är den huvudsakliga sidbakgrunden. `brand-dark` används i header, footer och ytor som behöver starkare kontrast. `brand-secondary` kan separera mörka sektioner och bära resultatblock.

`surface-primary` är standard för läsytor och kort. `surface-raised` används sparsamt för FAQ, formulär och andra element som behöver separeras från en ljus omgivning. `surface-muted` är en fullbreddssektion för exempelvis längre FAQ-innehåll.

Brödtext på mörk bakgrund använder `text-on-dark` eller `text-on-dark-muted`. Brödtext på ljus bakgrund använder `text-primary` eller `text-secondary`. Använd aldrig guld för längre textstycken.

Alla kombinationer för löptext ska hålla minst WCAG AA-kontrast. Färg får inte ensam kommunicera status, val eller fel.

## Typografi

Inter är förstahandsval och systemets sans-serif-stack är alltid fallback. Monospace används endast för kod, hashvärden och annan teknisk data.

Rubriker är kompakta, tunga och vänsterställda. Letter spacing är alltid `0`; textstorlek ska inte styras direkt av viewportens bredd. Använd `clamp()` mellan stabila typografiska nivåer när rubriker behöver svara på tillgängligt utrymme.

Brödtext ska normalt ligga mellan 60 och 78 tecken per rad. Längre case och artiklar använder en läsbredd på högst 780px och en radhöjd mellan 1.65 och 1.76. Undvik centrerad löptext.

Eyebrows är korta kategorietiketter i versaler. De får aldrig bära information som saknas i huvudrubriken.

## Layout och rytm

Spacing bygger på 4px. Vanliga avstånd är 8px inom en liten grupp, 16–24px mellan relaterade element, 32–48px mellan innehållsgrupper och 64–112px mellan större sektioner.

Sidans huvudsakliga maxbredd är 1280px med 24px sidmarginal på desktop och 16px på mobil. Layouten går från flera kolumner till en kolumn vid 1080px eller 720px beroende på innehållstyp.

Använd fullbreddsband för större sidsektioner. Kort används för upprepade objekt, formulär, FAQ-poster och tydligt avgränsade verktyg. Lägg inte kort inuti kort och gör inte varje textsektion till en fristående ruta.

## Djup och ytor

Hierarki skapas i första hand genom bakgrundston, kantlinje och spacing. Skuggor används sparsamt på upprepade kort och överlägg. Artikelkapitel och vanliga sidsektioner ska normalt vara plana.

Standardkort använder 8px radie. Formulärets externa embed använder 18px eftersom dess interna form följer samma rundning. Piller reserveras för status, kompakta taggar och segmenterade val.

## Knappar och länkar

En vy ska normalt ha en tydlig primär handling. Primärknappen är gul med vit text. Sekundärknappen på mörk yta är transparent med en ljus kantlinje. Textlänkar använder beskrivande länktext, till exempel `Läs caset om Eleiko`, inte `Klicka här`.

Ikoner kommer från Lucide när en lämplig ikon finns. Bekanta verktygskommandon kan vara ikonknappar med tooltip. Viktiga navigations- och CTA-länkar använder ikon plus text när ikonen förbättrar förståelsen.

Alla klickbara kontroller ska vara minst 44px höga eller ha en motsvarande träffyta. Alla interaktiva element ska visa systemets guldfärgade fokusmarkering vid `:focus-visible`.

## Navigation

Headern är sticky och använder `brand-dark` med lätt transparens. Aktiv sida och hover markeras med `accent-bright`. Desktopnavigationen får innehålla en dropdown för Affärsområden; vägen från trigger till meny ska vara sammanhängande så att menyn inte stängs när pekaren flyttas.

På mindre skärmar ersätts huvudmenyn av en tydlig menyknapp. Mobilmenyn ska vara tangentbordsåtkomlig, kunna scrollas och aldrig täcka viktig information utan möjlighet att stängas.

## Kort och informationsblock

Kort ska ha en tydlig uppgift och en stabil höjd inom samma grupp. Bild, rubrik, beskrivning och handling ska följa samma ordning mellan kort. Länken placeras längst ned när korten jämförs i ett grid.

Ojämna antal ska lösas genom avsiktlig komposition, exempelvis tre framhävda affärsområden följt av en balanserad sekundär rad. Lämna inte en tom simulerad kortplats.

## Case och artiklar

Case ska bevara hela berättelsen men göra den lätt att skanna. Använd ett kompakt resultatband, en innehållsnavigering, numrerade kapitel, en läsbredd på högst 780px och visuella avbrott med relevanta originalbilder.

Citat placeras nära det avsnitt de styrker och innehåller namn, roll och bild när den finns. Bilder ska använda beskrivande alt-text. Dekorativa porträtt inne i ett semantiskt citerat block kan ha tom alt-text när samma person redan namnges direkt bredvid.

FAQ används bara när frågorna tillför sök- eller användarvärde. Synliga frågor och svar ska motsvara eventuell `FAQPage`-schema markup exakt.

## Bilder

Alla produktionsbilder lagras lokalt i `/public/assets`. Externa hotlinks används inte. WebP är standard för fotografi och SVG för logotyper och enkla vektorer.

Visa det faktiska företaget, arbetet, personen eller resultatet. Undvik generiska stockbilder och atmosfäriska bilder som inte tillför information. Teamfotografier ska visa tillräckligt av personens höjd och får inte beskäras hårt kring ansiktet.

Använd `object-fit: cover` endast när en stabil kortyta kräver det. Redaktionsbilder och skärmbilder använder normalt `object-fit: contain` så att information inte beskärs. Ange stabil `aspect-ratio`, bredd eller höjd för att undvika layoutskiften.

## Formulär

Kontaktformuläret är en Kitsu-embed. HERE-sidan ansvarar för dess placering, responsiva bredd och omgivande layout. Kitsu ansvarar för fält, validering, formulärbakgrund och intern spacing.

Formuläret ska visuellt linjera med kontaktinformationen och inte ha en extra mörk ram. Resize-meddelanden accepteras endast från `https://kitsu.se` och endast när `formId` matchar det förväntade formuläret.

## Rörelse

Rörelse ska förklara förändring eller hjälpa orientering. Vanliga hover- och stateövergångar ligger mellan 150 och 240ms. Långa loopar undviks med undantag för den avsiktliga hero-animationen och kundlogotypbandet.

`prefers-reduced-motion` ska stoppa eller förenkla icke-nödvändig rörelse. Animation får inte flytta kontroller, orsaka layoutskift eller göra text svårare att läsa.

## Responsivitet

Varje komponent ska fungera från 320px och uppåt. Text får inte överlappa andra element eller klippas i knappar och kort. Typografi ska byta nivå vid brytpunkter eller via begränsad `clamp()`, inte skala fritt med viewporten.

Grids blir en kolumn på mobil. Horisontell scroll används endast för avsiktliga, svepbara samlingar där varje objekt fortfarande har en stabil bredd. Inga sidor får skapa oavsiktlig horisontell overflow.

## Tillgänglighet

- Använd semantiska landmarks, en unik `h1` och logisk rubrikhierarki.
- Erbjud skip-link till huvudinnehållet.
- Bevara synlig fokusmarkering på länkar, knappar, formulärfält och `summary`.
- Skriv alt-text som beskriver bildens relevanta innehåll och sammanhang.
- Använd `details` och `summary` för FAQ när beteendet är en enkel accordion.
- Visa inte information enbart genom färg, position eller animation.
- Säkerställ minst 44px träffyta för centrala touchkontroller.
- Testa tangentbord, skärmläsarstruktur, zoom och reduced motion.

## SEO och innehåll

Alla publika sidor ska vara förgenererade så att centralt innehåll finns i HTML utan att JavaScript måste köras. Varje indexerbar sida ska ha unik meta title, meta description och canonical URL.

Använd relevant schema.org-markup för organisation, tjänster, personer, artiklar, case, breadcrumbs och FAQ. Synlig text och strukturerad data måste överensstämma.

Länkar ska beskriva destinationen. Bilder ska ha kontextspecifika alt-texter. Nya indexerbara routes ska läggas till i sitemap och tillåtas i `robots.txt` om det inte finns ett uttryckligt skäl att använda `noindex`.

## Röst och innehåll

Språket är svenska om sidan inte uttryckligen riktar sig till en annan marknad. Tonen ska vara kunnig, rak och pedagogisk. Förklara facktermer första gången de används och koppla tekniska aktiviteter till affärsnytta.

- Rubriker ska säga vad avsnittet faktiskt handlar om.
- CTA-texter börjar helst med ett tydligt verb eller beskriver destinationen.
- Undvik tomma superlativ, intern jargong och onödigt långa introduktioner.
- Skriv HERE med versaler när namnet avser byrån.
- Behåll kundcitat ordagrant när de publiceras som citat.

## Gör

- Använd mörkgrönt, ljusa läsytor och guld i tydliga roller.
- Begränsa långa textrader och skapa tydliga visuella pauser.
- Återanvänd etablerade komponenter och Lucide-ikoner.
- Låt faktisk data, riktiga case och riktiga personer bära designen.
- Kontrollera desktop och mobil efter varje större layoutändring.

## Undvik

- Använd inte guld som stor bakgrundsyta eller för längre text.
- Lägg inte text ovanpå bilder när kontrasten varierar okontrollerat.
- Skapa inte dekorativa gradientformer, bokeh eller fristående färgblobbar.
- Blanda inte många radier eller skuggor i samma vy.
- Beskär inte skärmbilder, personalbilder eller casebilder så att viktig information försvinner.
- Dölj inte viktig information bakom hover eller JavaScript-only rendering.
