# Vefforritun 1, 2024, hópverkefni 2

## Verkefnalýsing

Verkefnið felst í að birta gefið efni um vefforritun á mismunandi síðum.

Verkefninu er skipt upp í verkefni sem verður að útfæra og verkefni þar sem hægt er að velja mismunandi virkni til að útfæra. Útfrá stærð hóps þarf að útfæra ákveðið mörg af þessum verkefnum. Ekki er gefið að hvert af þessum verkefnum séu jafn flókin eða tímafrek.

Hægt er að spyrja spurninga um verkefnið á rásinni `#vef1-2024-h2`.

Vefur skal vera prófaður og virka í nýjustu útgáfum af Firefox og Chrome.

### Gefin gögn

Gefin eru gögn fyrir:

- Heildaryfirlit síðu, `index.json`.
- Yfirlit fyrir hvert efni: `html/index.json`, `css/index.json`, `js/index.json`.
- Námsefni fyrir hvert efni: `html/content.json`, `css/content.json`, `js/content.json`.
- Lykilhugtök fyrir hvert efni: `html/keywords.json`, `css/keywords.json`, `js/keywords.json`.
- Spurningar fyrir hvert efni: `html/questions.json`, `css/questions.json`, `js/questions.json`.
- Myndir sem efni getur vísað í: `img/`.

Gögnin sjálf og nánari skilgreining munu koma vonbráðar.

### Forsíða og heildar útlit

Útbúa skal einfalt útlit fyrir forsíðu (`index.html`) sem inniheldur það efni sem er gefið í `index.json`:

- Haus með titli síðu.
- Valmynd með hlekkjum á forsíðu og það efni sem vísað er í (útbúa þarf gildan hlekk út frá útfærslu).
- Fótur með gefnum upplýsingum.

Þetta útlit fylgir sér síðan í gegnum aðrar síður. Athugið að útlit er ekki aðalatriði í þessu verkefni og skal vera einfalt.

Útlit skal vera skalanlegt frá `320px` upp í að minnsta kost `1600px` breidd.

Allt efni skal útbúið í JavaScript við keyrslu.

### Síður fyrir hvert efni

Fyrir hvert efni skal útbúa síðu sem birtir efnið sem gefið er í `html/index.json`, `css/index.json`, `js/index.json`, þetta getur síðan verið breytilegt eftir því hvaða auka virkni er ákveðið að útfæra.

Allt það sama gildir um þessar síður og um forsíðu.

### Slóðir

Þegar farið er á milli forsíðu og flokka skal ekki sækja nýja síðu, heldur skal yfirskrifa virkni `<a href>` og nota [History API](https://developer.mozilla.org/en-US/docs/Web/API/History_API) til að útfæra skiptingu á milli síða. Sérstaklega þarf að passa upp á að back takkinn virki með því að hlusta á [`popstate`](https://developer.mozilla.org/en-US/docs/Web/API/WindowEventHandlers/onpopstate) atburðinn.

Forsíða (`/`) sýnir yfirlit. Fyrir hvern flokk skal nota querystring (hægt að sækja úr `window.location.search` og með `URLSearchParams`), t.d. `/?type=html`, `/?type=html&content=material`, `/?type=html&content=keywords`.

### Önnur virkni

#### Birting á námsefni

Efnið sem gefið er í `html/content.json`, `css/content.json`, `js/content.json` skal birta á sérstakri síðu.

#### Birting á lykilhugtökum

Efnið sem gefið er í `html/keywords.json`, `css/keywords.json`, `js/keywords.json` skal birta á sérstakri síðu.

#### Birting á spurningum

Efnið sem gefið er í `html/questions.json`, `css/questions.json`, `js/questions.json` skal birta á sérstakri síðu.

#### Staða vistuð

Fyrir það efni sem er birt er staða á því vistað í `localStorage` og þegar síða er opnuð aftur skal sú staða vera birt, t.d.:

- Eftir að notandi hefur skoðað mismunandi námsefni er hægt að haka við að því námsefni sé lokið.
- Eftir að notandi hefur svarað spurningum er hægt að sjá svörin.

Aðeins er hægt að fá þetta metið sem ein auka virkni þó útfært sé fyrir fleiri en eitt efni.

#### Yfirlitssíða

Bæta við á forsíðu yfirliti yfir allt efni sem hefur verið vistað í `localStorage`. T.d.

- Hvaða námsefni er lokið, og hvað er eftir.
- Hvaða lykilhugtök hafa verið skoðuð.
- Hvaða spurningum hefur verið svarað og hversu margar af þeim voru réttar.

#### „Flashcards“

Útfæra fyrir lykilhugtök „flashcard“ virkni þar sem birt er lykilhugtak og notandi getur smellt á til að sjá skilgreiningu.

#### Eitthvað sem ykkur dettur í hug

Það er hægt að útfæra þau verkefni nánar og með meiri nákvæmni en skilgreint er hér að ofan. Það er mikilvægt að það sem útfært er sé skýrt tekið fram í `README.md` skrá.

Að auki er hægt að eitthvað allt annað sem ykkur dettur í hug og er í samræmi við verkefnalýsingu. Heyrið í Óla áður en farið út í það.

## Efni

Nánar um uppsetningu á efni í JSON skrám kemur seinna.

## Hópavinna

Verkefnið skal unnið í hóp með 3-4 einstaklingum. Hafið samband við kennara ef ekki er mögulegt að vinna í hóp. Hægt er að leita að félögum á slack á rásinni `#vef1-2024-h2-vantar-hop`. Ekki er krafa að vera í sama hóp og í hópverkefni 1.

Notast skal við Git og GitHub. Engar zip skrár með kóða ættu að ganga á milli í hópavinnu, heldur á að „committa“ allan kóða og vinna gegnum Git.

Sjást ætti á _commit history_ að allir meðlimir hóps hafi tekið þátt í verkefni.

Útbúa þarf a.m.k. fimm Pull Request (PR) þar sem búið er að fara yfir af öðrum meðlim í hóp og yfirferð ásamt gagnrýni sést á GitHub.

## Lýsing á verkefni

`README.md` skrá skal vera í rót verkefnis og innihalda:

- Upplýsingar um hvernig keyra skuli verkefnið:
  - `npm run dev` eða `npm start`.
  - `npm run lint` skal vera til staðar og keyra eslint og stylelint.
- Létt lýsing á uppsetningu verkefnis, hvernig því er skipt í möppur, hvernig CSS/Sass er skipulagt og fleira sem á við.
- Nákvæm útlistun á því hvað er útfært.
- Upplýsingar um alla sem unnu verkefni, nöfn, HÍ notendanöfn og GitHub notendanöfn.

## Tæki og tól

Verkefnið skal innihalda `package.json` og `package-lock.json` sem innihalda öll notuð tól.

Þegar verkefnið er sótt verður `npm install` keyrt á undan öllum öðrum skipunum.

Setja skal upp Sass og stylelint með `stylelint-config-sass-guidelines` og `stylelint-config-standard` fyrir verkefnið.

Setja skal upp eslint.

Leyfilegt er að nota öll tól sem við höfum notað í haust.

## Hýsing

Setja skal verkefnið upp á Netlify, tengt GitHub.

## Mat

- 10% README eftir forskrift, tæki og tól uppsett, vefur keyrir á Netilfy. Lint fyrir CSS/Sass og JavaScript.
- 10% Git notað og PR eftir forskrift.
- 10% Almennt útlit og skalanleiki útfært fyrir forsíðu og efnissíður.
- 10% Slóðir og `History` API útfært.
- 60% Valið efni útfært.

Fyrir valið efni er metið:

- Einstaklingsverkefni: tvö auka verkefni útfært.
- Tveggja manna hópverkefni: þrjú auka verkefni útfærð.
- Þriggja manna hópverkefni: fjögur auka verkefni útfærð.
- Fjögurra manna hópverkefni: fimm auka verkefni útfærð.

## Sett fyrir

Verkefni fyrst sett fyrir í fyrirlestri mánudaginn 21. október 2024.

Sett fyrir að öllu leiti í fyrirlestri mánudaginn 28. október 2024.

## Skil

Tilnefna skal hópstjóra sem skráir sig í ákveðinn hóp undir „Hópverkefni 2“ í Canvas. Aðrir nemendur skrá sig í framhaldinu í sama hóp, hópstjóri getur líka skráð aðra nemendur í hópinn.

**Útbúa skal hóp jafnvel ef verkefnið er unnið sem einstaklingsverkefni**.

Hópstjóri skal skila fyrir hönd allra í Canvas í seinasta lagi föstudaginn 22. nóvember 2024.

**Mikilvægt er að öll skil séu gerð í hóp annars munu ekki allir nemendur fá einkunn.**

Skil skulu innihalda:

- GitHub notendanöfn allra (passa þarf að allir nemendur séu í hópnum!)
- Slóð á verkefnið keyrandi í hýsingu
- Slóð á GitHub repo fyrir verkefni. Dæmatímakennurum skal hafa verið boðið í repo. Notendanöfn þeirra eru:
  - `digitalsigga`
  - `ofurtumi`
  - `osk`
  - `polarparsnip`
  - `reynirjr`

## Einkunn

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 5% hvert, samtals 40% af lokaeinkunn.

Sett verða fyrir tvö hópverkefni þar sem hvort um sig gildir 10%, samtals 20% af lokaeinkunn.

> Útgáfa 0.1
