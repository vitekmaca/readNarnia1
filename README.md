# Lev, čarodějnice a skříň 🦁

Interaktivní průvodce první knihou Letopisů Narnie, pro předčítání dětem. Stejná appka jako [readHP](https://github.com/vitekmaca/readHP) a [readHP2](https://github.com/vitekmaca/readHP2) — stejná struktura a chování, nový obsah. Fanouškovský projekt, žádná oficiální appka.

## Aktuální stav

- **Postavy:** 19 v appce, zatím **bez portrétů** (viz seznam níže).
- **Ilustrace kapitol:** zatím žádná ze 17.
- **Audio:** zatím žádné namluvené kapitoly.

Appka funguje i bez obrázků a audia — postavy mají místo portrétu ikonku, kapitoly bez nahrávky mají vlastní hlášku a ilustrace prostě chybí.

## Co appka umí

- 🎧 **Namluvené kapitoly** — audiopřehrávač u každé kapitoly (soubory v `assets/audio/`).
- 🦁 **Postavy** s portréty a „příběhem zatím", který se dopisuje podle toho, co už bylo přečteno.
- 🖼️ **Malovaná ilustrace** klíčového momentu ke každé ze 17 kapitol.
- 📖 **Dva režimy**: *Rodiče* (shrnutí, na co se zaměřit, otázky pro děti, „metr strašidelnosti") a *Děti* (bez spoilerů — jen „co bylo minule" a kvízy, postavy se odemykají čtením).
- 🌍 **Svět** — Narnie, Bílá čarodějnice, Aslan, Hluboké kouzlo, Cair Paravel, národy Narnie a časová osa.
- 🌗 Světlý/tmavý motiv v hlavičce.
- Body se tu sbírají „pro Aslana" (za správné odpovědi v kvízu).

Appka je jen česky. Má **vlastní, nezávislý postup čtení** (localStorage klíč `narnia_lev_v1`).

## ⚠️ Autorská práva

Kniha Lev, čarodějnice a skříň je stále chráněné dílo. Appka obsahuje jen **vlastní parafráze a shrnutí** (ne text knihy). Až přibydou portréty a ilustrace, použij jen obrázky, které smíš použít (vlastní, licencované nebo vygenerované); u obrázků z knižních vydání platí stejné opatrnosti jako u readHP — viz [README readHP](https://github.com/vitekmaca/readHP#️-autorská-práva--proč-musí-repo-zůstat-soukromé).

## Struktura projektu

- `index.html` — **sestavená appka** (jeden soubor).
- `lev-carodejnice-skrin.template.html` — **zdrojová šablona** (HTML/CSS/JS + veškerý text). Tady se edituje obsah.
- `assets/` — `portraits/<id>.jpg`, `scenes/<n>.jpg` (1–17), `audio/<n>.m4a` (audio se do HTML nevkládá).
- `build.mjs` — build skript (Node): `node build.mjs`. Chybějící obrázky jen vypíše, build neselže.

---

## Co přesně potřebuju od tebe (obrázky)

Celkem **36 souborů** (17 scén + 19 portrétů), `build.mjs` ale běží i s částí chybějící.

### 17 ilustrací kapitol

`assets/scenes/1.jpg` … `assets/scenes/17.jpg` — scéna na šířku. Přesné popisky jsou v šabloně (proměnná `ILLUS`).

| # | Klíčový moment |
|---|---|
| 1 | Čtyři sourozenci na prahu obrovského domu profesora Kirkea |
| 2 | Lucie vychází ze skříně do zasněženého lesa k faunovi pod lampou |
| 3 | Edmund se plíží skříní do zasněženého lesa, kde ho čeká čarodějnice |
| 4 | Bílá čarodějnice podává Edmundovi turecký med v saních |
| 5 | Lucie utíká uražená, Edmund se jí posmívá |
| 6 | Čtyři děti v kožiších v zasněženém lese za lampou |
| 7 | U Bobrů — tabule jídla a šeptané jméno Aslan |
| 8 | Útěk z hráze, Edmund zmizel |
| 9 | Edmund v temném sále plném soch zkamenělých tvorů |
| 10 | Tání sněhu a první ptáčci, čarodějnice uvízla v blátě |
| 11 | Aslan se zlatou hřívou ve stanu před dětmi |
| 12 | Petr s mečem zasáhne vlka Maugrima |
| 13 | Čarodějnice žádá Edmunda podle starého zákona, Aslan naslouchá |
| 14 | Zuzana a Lucie vedle Aslana na cestě ke Kamennému stolu |
| 15 | Rozlomený Kamenný stůl a živý Aslan za úsvitu |
| 16 | Aslan dýchá do zkamenělých tvorů v nádvoří zámku |
| 17 | Čtyři vládci Narnie na trůnech v Cair Paravelu, bílý jelen v lese |

### 19 portrétů postav

`assets/portraits/<id>.jpg` — na výšku (poměr 3:4).

| soubor | postava |
|---|---|
| `lucie.jpg` | Lucie Pevensieová |
| `petr.jpg` | Petr Pevensie |
| `zuzana.jpg` | Zuzana Pevensieová |
| `edmund.jpg` | Edmund Pevensie |
| `kirke.jpg` | Profesor Kirke |
| `macready.jpg` | Paní Macreadyová |
| `tumnus.jpg` | Pan Tumnus (faun) |
| `jadis.jpg` | Bílá čarodějnice |
| `trpaslik.jpg` | Čarodějnicin trpaslík |
| `pbobr.jpg` | Pan Bobr |
| `pbobrova.jpg` | Paní Bobrová |
| `maugrim.jpg` | Maugrim (vlčí velitel) |
| `vanoce.jpg` | Otec Vánoc |
| `aslan.jpg` | Aslan |
| `oreius.jpg` | Oreius (kentaur) |
| `rumblebuffin.jpg` | Obr Rumblebuffin |
| `mysi.jpg` | Myši |
| `lesni.jpg` | Dryády a Naiády |
| `jelen.jpg` | Bílý jelen |

### Jména k ověření

České překlady jmen se mezi vydáními liší — zkontroluj prosím podle svého výtisku:
- **Pevensieovi** (Petr, Zuzana, Edmund, Lucie) — jména dětí
- **Pan Tumnus**, **Maugrim** (někde Fenris Ulf), **Oreius**, **Obr Rumblebuffin**
- **Pan a paní Bobrovi**, **Otec Vánoc**, **Kamenný stůl**, **Cair Paravel**

Názvy kapitol v appce jsou moje vlastní parafráze (ne doslovný text knihy) — pokud chceš, aby seděly s tvým výtiskem, řekni a upravím.
