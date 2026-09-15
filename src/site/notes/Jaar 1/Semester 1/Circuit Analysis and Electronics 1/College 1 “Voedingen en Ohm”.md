---
{"dg-publish":true,"permalink":"/jaar-1/semester-1/circuit-analysis-and-electronics-1/college-1-voedingen-en-ohm/","noteIcon":"","created":"2026-09-15T09:42:39.003+02:00","updated":"2026-09-15T12:00:49.404+02:00","dg-note-properties":{}}
---

## Over deze les
Onderwerpen:
• [[Definities/Stroomsterkte\|Stroomsterkte]]
• [[Definities/Spanning\|Spanning]]
• [[Definities/Weerstand\|Weerstand]]
• [[Definities/Wet van Ohm\|Wet van Ohm]]

# Elektronica — Spanning, Stroom, Weerstand & Condensator

## 0. Waarom Δ (delta) overal staat

Voordat we beginnen: bijna elke formule hieronder bevat een Δ. Dat symbool duikt zo vaak op dat het de moeite waard is 'm eerst apart vast te zetten.

**Δ = "verandering in"**. Het is geen getal, het is een instructie: _neem de eindwaarde, trek er de beginwaarde van af._

$$\Delta X = X_{eind} - X_{begin}$$

Voorbeeld: als de temperatuur(T) van 15°C naar 22°C gaat, is ΔT = 22 - 15 = 7°C.

Je ziet het steeds terug omdat elektrische grootheden (lading, spanning, tijd) zelden interessant zijn als los getal — het gaat om **hoeveel iets verandert**, en vaak specifiek om **hoe snel** iets verandert (verandering gedeeld door tijd).

---

## 1. Stroomsterkte (I)

**Elektrische stroom = de lading die per tijdseenheid door een oppervlak (dwarsdoorsnede van een draad) stroomt.**

Stel je een draad voor als een buis. Er lopen elektrisch geladen deeltjes (elektronen) doorheen. Stroomsterkte zegt niets anders dan: _hoeveel lading passeert een bepaald punt, per seconde._

$$I = \frac{\Delta q}{\Delta t}$$

Waarbij:

- **Δq** = de hoeveelheid lading die verplaatst is, in **Coulomb (C)**
- **Δt** = de tijdsduur waarin dat gebeurt, in **seconden (s)**
- **I** = de stroomsterkte, in **Ampere (A)**

**1 Ampere = 1 Coulomb per seconde.** Dat is dus letterlijk de eenheid: A = C/s.

### Wat beweegt er nou eigenlijk?

In een geleider (bijvoorbeeld koperdraad) zit een rooster van atomen (ionen) die vastzitten op hun plek. Daartussen bewegen vrije elektronen. **De elektronen bewegen van de negatieve pool naar de positieve pool** van de bron.

> **Let op — een klassiek verwarringspunt:** de _technische stroomrichting_ (die je in schema's tekent, met de pijl) is gedefinieerd van + naar −, dus **tegengesteld** aan de daadwerkelijke beweging van de elektronen. Dit is historisch zo afgesproken (vóór men wist dat elektronen negatief geladen zijn) en is nooit meer aangepast. Voor het rekenen maakt dit niets uit — maar het is goed om te weten dat "stroomrichting op papier" en "waar de elektronen echt heen gaan" twee verschillende dingen zijn.

---

## 2. Spanning (U)

**Spanning = het verschil in elektrische potentiële energie tussen twee punten.**

Denk aan spanning als een soort "elektrische hoogte". Net zoals water van hoog naar laag stroomt door een hoogteverschil, stroomt lading tussen twee punten door een _spanningsverschil_. Hoe groter het verschil, hoe harder de "drang" om te stromen.

### Waar komt de eenheid Volt vandaan?

De officiële definitie: een spanning is **1 Volt** als het verplaatsen van **1 Coulomb** lading van het ene naar het andere punt een **arbeid (energie)** kost van **1 Joule**.

$$U = \frac{\Delta W}{\Delta q}$$

Waarbij:

- **ΔW** = de verrichte arbeid (energie), in **Joule (J)**
- **Δq** = de verplaatste lading, in **Coulomb (C)**
- **U** = de spanning, in **Volt (V)**

$$1\ V = 1\ \frac{J}{C}$$

_(Vernoemd naar Alessandro Volta — geldt ook zo bij natuurkunde, dus deze definitie is niet elektronica-specifiek.)_

### Het verband tussen spanning, stroom en vermogen

Als je de twee formules hierboven combineert (Δq/Δt komt in beide voor), zie je een derde grootheid ontstaan: **vermogen (P)**.

$$U = \frac{\Delta W}{\Delta q} \quad\text{en}\quad I = \frac{\Delta q}{\Delta t} \quad\Rightarrow\quad \frac{\Delta W}{\Delta t} = P$$

Dit laat zien waarom spanning en stroom altijd samen opduiken: energie per tijd (vermogen) hangt af van beide.

### Spanning bestaat alleen tússen twee punten

Dit is een cruciaal punt: **je kunt niet zeggen "dit punt heeft een spanning van 5V"** zonder erbij te zeggen _ten opzichte van wat_. Spanning is altijd een verschil, nooit een absolute waarde op zich.

In de praktijk kies je daarom een **referentiepunt** (ook wel "common point" of "nulpunt" genoemd) — een vast punt waar je alle andere spanningen mee vergelijkt. **Het is gebruikelijk om de negatieve pool van de spanningsbron als dit referentiepunt te kiezen.**

> **Correctie op eigen aantekening:** in je notities stond "zwart/min is geen ground, het is een zwevend 0-punt." Dat klopt niet helemaal met wat de sheet zegt — de negatieve pool wordt juist **gekozen als vast referentiepunt** (nulpunt), niet als iets "zwevends". "Zwevend" (floating) zou betekenen dat een punt geen vaste relatie met de rest van het circuit heeft — dat is hier niet het geval. De min-pool ligt hier per afspraak vast op 0V, en alle andere spanningen in het circuit worden daaraan gerelateerd.

_(Zoek zelf een afbeelding op van een voedingsapparaat met + en − aansluitingen, zoals op de sheet — dat maakt dit concept meteen visueel duidelijk.)_

---

## 3. De Wet van Ohm

Nu je spanning en stroom apart snapt, komt de vraag: **hoe hangen ze samen in een geleider (bijvoorbeeld een weerstand)?**

**De Wet van Ohm zegt: de stroom door een geleider is recht evenredig met de spanning erover.** De verhouding tussen die twee heet **weerstand (R)**.

$$I = \frac{U}{R} \qquad\text{ofwel ook geschreven als}\qquad U = I \times R$$

Waarbij:

- **I** = stroomsterkte door de geleider, in **Ampere (A)**
- **U** = spanning gemeten over de geleider, in **Volt (V)**
- **R** = weerstand van de geleider, in **Ohm (Ω)**

### Wat betekent "recht evenredig" hier visueel?

Als je stroom (I) tegen spanning (U) uitzet in een grafiek, krijg je een rechte lijn door de oorsprong. **De helling van die lijn is de weerstand R.** Een grotere R betekent een minder steile lijn (meer spanning nodig voor dezelfde stroom); een kleinere R betekent een steilere lijn.

_(Zoek een "spanning-stroom karakteristiek" grafiek op als visueel voorbeeld — dit is een standaardplaatje in elk elektronicaboek.)_

**Rekenvoorbeeld uit de les:** bij een lijn waarbij 10V hoort bij 0.1A geldt: $$R = \frac{U}{I} = \frac{10\ V}{0.1\ A} = 100\ \Omega$$

---

## 4. Weerstand (R)

Een **weerstand** is de eigenschap van een materiaal die aangeeft hoe moeilijk het is voor stroom om erdoorheen te lopen. Fysiek is het vaak ook een apart component (het "weerstandje") dat je in een circuit plaatst om de stroom te beperken.

- Eenheid: **Ohm (Ω)**
- Hoe hoger R, hoe minder stroom er loopt bij eenzelfde spanning (zie de wet van Ohm hierboven — R staat in de noemer).

_(De Hooverdam-analogie op de sheet is een mooi visueel beeld: een dam die de waterstroom afremt, vergelijkbaar met hoe een weerstand de stroom afremt. Zoek een schema-symbool van een weerstand op om te combineren met deze analogie.)_

---

## 5. Referentierichting: $U_{ab}$ en $I_{ab}$

Dit bouwt direct voort op wat je bij spanning leerde: spanning bestaat alleen tussen twee punten. Hier maken we dat concreet met notatie.

$$U_{ab} = U_a - U_b$$

**$U_{ab}$ geeft aan hoeveel de spanning in punt $a$ hoger is dan in punt $b$.** Je kunt het ook lezen als: hoeveel de spanning _daalt_ als je van $a$ naar $b$ beweegt.

Op dezelfde manier is $I_{ab}$ de stroom die **van $a$ naar $b$** loopt (de volgorde van de letters geeft de richting aan).

**Let op:** deze waarden kunnen **negatief** zijn. Een negatieve $U_{ab}$ betekent simpelweg dat punt $b$ juist hoger ligt dan punt $a$ — niet dat er iets "fout" is. Uit de les: een voorbeeldopgave gaf $U_{ab} = -12\ V$ en $I_{ab} = -1\ A$ — dat is een volkomen geldig antwoord, het zegt alleen dat de werkelijke richting van spanning/stroom tegengesteld is aan de richting die je had aangenomen (van a naar b).

---

## 6. Condensator

Dit onderdeel combineert alles hierboven: lading, spanning, stroom én de Δ-notatie komen hier samen.

### Wat is het, fysiek?

Een condensator bestaat uit twee platen dicht bij elkaar, met een niet-geleidend materiaal (isolator) ertussen. Als je er spanning op zet:

- de ene plaat wordt **positief** geladen (tekort aan elektronen)
- de andere plaat wordt **negatief** geladen (overschot aan elektronen)

De twee tegengesteld geladen platen trekken elkaar aan — hierdoor ontstaat een **elektrisch veld** tussen de platen. Op deze manier **slaat de condensator energie op** in dat veld (zie verderop).

### De basisformule: lading en spanning

$$q = C \cdot u$$

Waarbij:

- **q** = de lading op elke plaat, in **Coulomb (C)** — let op: op de ene plaat +q, op de andere -q, maar de hoeveelheid is gelijk
- **C** = de **capaciteit** van de condensator, in **Farad (F)** — dit is een vaste eigenschap van de condensator zelf (hoe groot de platen zijn, hoe dicht ze bij elkaar zitten, welk materiaal ertussen zit)
- **u** = de spanning over de condensator, in **Volt (V)**

Hoe hoger de capaciteit C, hoe meer lading er bij eenzelfde spanning wordt opgeslagen.

### De stroom door een condensator

Door wiskundig af te leiden hoe lading verandert over tijd (Δq/Δt — precies de definitie van stroom uit hoofdstuk 1!), volgt:

$$i = \frac{\Delta q}{\Delta t} = C \cdot \frac{\Delta u}{\Delta t}$$

**Dit is de belangrijkste formule van dit onderdeel.** Vertaling in woorden: _de stroom door een condensator is evenredig met hoe snel de spanning erover verandert._

Dit is meteen ook iets fundamenteel anders dan bij een gewone weerstand: bij een weerstand hangt de stroom af van de spanning zélf (Wet van Ohm). Bij een condensator hangt de stroom af van **hoe snel de spanning verandert** — staat de spanning stil (constant), dan loopt er dus geen stroom, ook al staat er wel spanning op.

### Energie-opslag

$$W = \frac{1}{2} C u^2$$

Waarbij **W** de opgeslagen energie is, in **Joule (J)**.

**Belangrijk gevolg van het kwadraat:** als de spanning **verdubbelt**, neemt de opgeslagen energie toe met een factor **4** (want 2² = 4), niet met een factor 2. Dit is een veelgemaakte denkfout — energie schaalt niet lineair met spanning bij een condensator.

### Rekenvoorbeeld uit de les

Gegeven: $C = 100\ \mu F = 100 \times 10^{-6}\ F$ _(Let op: op je rekenmachine voer je dit in als `100 EXP -6` of `100E-6`, niet als "100 Ω F" — dat laatste stond los in de aantekeningen maar is geen eenheid; de eenheid van C is altijd Farad.)_

**Vraag 1: stroom tussen 0 en 4 ms** Antwoord: **0,5 A** → In dit interval steeg de spanning gelijkmatig; met $i = C \cdot \frac{\Delta u}{\Delta t}$ vind je 0,5 A.

**Vraag 2: stroom tussen 4 en 6 ms** Antwoord: **−1 A** → Het negatieve teken betekent dat de spanning in dit interval **daalde** in plaats van steeg (vergelijk met $U_{ab}$ hierboven: een negatief teken is geen fout, het geeft richting/afname aan).

**Vraag 3: opgeslagen energie op t = 4 ms** Antwoord: **20 mJ** → Bereken de spanning $u$ op t=4ms uit de grafiek, vul in bij $W = \frac{1}{2}Cu^2$.

---

## Samenvattend overzicht

|Grootheid|Symbool|Eenheid|Kernformule|
|---|---|---|---|
|Lading|q|Coulomb (C)|—|
|Stroomsterkte|I|Ampere (A) = C/s|$I = \Delta q / \Delta t$|
|Spanning|U|Volt (V) = J/C|$U = \Delta W / \Delta q$|
|Weerstand|R|Ohm (Ω)|$R = U / I$|
|Capaciteit|C|Farad (F)|$q = C u$|
|Vermogen|P|Watt (W) = J/s|$P = \Delta W / \Delta t$|
|Energie (condensator)|W|Joule (J)|$W = \frac{1}{2}Cu^2$|

**De rode draad:** stroom is lading-per-tijd, spanning is energie-per-lading, en de meeste "geavanceerde" formules (Ohm, condensator) zijn simpelweg deze twee basisdefinities die met elkaar gecombineerd worden.

---

## Suggesties voor visuele voorbeelden om zelf op te zoeken

- Schema van een spanningsbron met + en − aansluitpunten (en waarom een voeding soms 3 aansluitpunten heeft)
- Spanning-stroom karakteristiek grafiek (rechte lijn, helling = R)
- Doorsnede van een condensator met elektrisch veld tussen de platen
- Rooster van ionen met bewegende elektronen in een geleider (om stroomrichting vs. elektronenrichting te visualiseren)















---

## dg-publish: true title: Spanning, Stroom & Weerstand — Interactieve Uitleg

# Wat er echt gebeurt in een stroomkring

Sleep aan de knoppen hieronder. Elke animatie is live gekoppeld aan de formule erboven.

<div class="el-sim"> <style> .el-sim{ --bg: #12161c; --bg-panel: #1a2029; --bg-panel-raised: #212836; --border: #2c3444; --text: #dfe4ea; --text-dim: #8b93a3; --text-faint: #5c6376; --copper: #c9803d; --copper-bright: #e6a25c; --blue: #5b8dd9; --blue-bright: #7ba7ea; --green: #7fb069; --green-bright: #99c980; --red: #d9705b; --mono: 'SF Mono', 'JetBrains Mono', Consolas, 'Courier New', monospace; --sans: -apple-system, 'Segoe UI', 'Inter', Roboto, sans-serif; } .el-sim *{ box-sizing: border-box; } .el-sim{ scroll-behavior: smooth; } .el-sim{ margin:0; background: var(--bg); color: var(--text); font-family: var(--sans); line-height: 1.6; font-size: 16px; } .el-sim .wrap{ max-width: 760px; margin: 0 auto; padding: 24px 16px 60px; } .el-sim header.hero{ padding: 8px 0 40px; border-bottom: 1px solid var(--border); margin-bottom: 40px; } .el-sim .hero-kicker{ font-family: var(--mono); font-size: 13px; color: var(--copper); letter-spacing: 0.02em; margin-bottom: 14px; } .el-sim h1{ font-size: 2.1rem; line-height: 1.2; margin: 0 0 16px; font-weight: 650; letter-spacing: -0.01em; } .el-sim .hero-sub{ color: var(--text-dim); font-size: 1.05rem; max-width: 58ch; } .el-sim section{ margin: 64px 0; } .el-sim section.first{ margin-top: 0; } .el-sim h2{ font-size: 1.5rem; font-weight: 650; margin: 0 0 6px; display:flex; align-items:baseline; gap:10px; } .el-sim .section-num{ font-family: var(--mono); font-size: 0.85rem; color: var(--text-faint); font-weight: 500; } .el-sim h3{ font-size: 1.05rem; font-weight: 650; margin: 28px 0 10px; color: var(--text); } .el-sim p{ margin: 12px 0; color: var(--text); } .el-sim p.lead{ color: var(--text-dim); margin-bottom: 22px; } .el-sim .formula-box{ background: var(--bg-panel); border: 1px solid var(--border); border-left: 3px solid var(--copper); border-radius: 4px; padding: 18px 22px; margin: 18px 0; font-family: var(--mono); font-size: 1.15rem; text-align: center; color: var(--copper-bright); overflow-x: auto; } .el-sim .formula-box.blue{ border-left-color: var(--blue); color: var(--blue-bright); } .el-sim .formula-box.green{ border-left-color: var(--green); color: var(--green-bright); } .el-sim .var-key{ font-family: var(--mono); font-size: 0.9rem; background: var(--bg-panel); border: 1px solid var(--border); border-radius: 4px; padding: 14px 18px; margin: 14px 0; color: var(--text-dim); } .el-sim .var-key div{ padding: 3px 0; } .el-sim .var-key b{ color: var(--text); font-weight: 600; } .el-sim .panel{ background: var(--bg-panel); border: 1px solid var(--border); border-radius: 8px; padding: 24px; margin: 20px 0; } .el-sim .panel-label{ font-family: var(--mono); font-size: 12px; color: var(--text-faint); margin-bottom: 16px; text-transform: none; } .el-sim svg.diagram{ width: 100%; height: auto; display: block; } .el-sim .controls{ display: flex; flex-direction: column; gap: 18px; margin-top: 20px; } .el-sim .control{ display:flex; flex-direction: column; gap: 6px; } .el-sim .control-row{ display:flex; justify-content: space-between; align-items: baseline; font-family: var(--mono); font-size: 13px; } .el-sim .control-row .label{ color: var(--text-dim); } .el-sim .control-row .value{ color: var(--copper-bright); font-weight: 600; } .el-sim .control-row .value.blue{ color: var(--blue-bright); } .el-sim .control-row .value.green{ color: var(--green-bright); } .el-sim input[type="range"]{ -webkit-appearance: none; width: 100%; height: 4px; border-radius: 2px; background: var(--border); outline: none; } .el-sim input[type="range"]::-webkit-slider-thumb{ -webkit-appearance: none; width: 16px; height: 16px; border-radius: 50%; background: var(--copper-bright); cursor: pointer; border: 2px solid var(--bg); box-shadow: 0 0 0 1px var(--copper); } .el-sim input[type="range"]::-moz-range-thumb{ width: 16px; height: 16px; border-radius: 50%; background: var(--copper-bright); cursor: pointer; border: 2px solid var(--bg); } .el-sim .control.blue input[type="range"]::-webkit-slider-thumb{ background: var(--blue-bright); box-shadow: 0 0 0 1px var(--blue); } .el-sim .control.green input[type="range"]::-webkit-slider-thumb{ background: var(--green-bright); box-shadow: 0 0 0 1px var(--green); } .el-sim .readout{ display:flex; gap: 14px; margin-top: 18px; flex-wrap: wrap; } .el-sim .readout-item{ flex: 1; min-width: 130px; background: var(--bg-panel-raised); border: 1px solid var(--border); border-radius: 6px; padding: 12px 14px; } .el-sim .readout-item .rlabel{ font-family: var(--mono); font-size: 11px; color: var(--text-faint); margin-bottom: 4px; } .el-sim .readout-item .rvalue{ font-family: var(--mono); font-size: 1.3rem; font-weight: 600; color: var(--text); } .el-sim .readout-item.highlight .rvalue{ color: var(--copper-bright); } .el-sim .callout{ background: var(--bg-panel-raised); border: 1px solid var(--border); border-radius: 6px; padding: 16px 18px; margin: 18px 0; font-size: 0.95rem; } .el-sim .callout .ctitle{ font-family: var(--mono); font-size: 12px; color: var(--blue-bright); margin-bottom: 6px; font-weight: 600; } .el-sim .callout.warn{ border-left: 3px solid var(--red); } .el-sim .callout.warn .ctitle{ color: var(--red); } .el-sim .callout.correction{ border-left: 3px solid var(--copper); } .el-sim .callout.correction .ctitle{ color: var(--copper-bright); } .el-sim .divider{ border: none; border-top: 1px solid var(--border); margin: 56px 0; } .el-sim .footer-note{ font-family: var(--mono); font-size: 12px; color: var(--text-faint); margin-top: 60px; padding-top: 24px; border-top: 1px solid var(--border); } .el-sim .analogy-label{ display:inline-block; font-family: var(--mono); font-size: 11px; color: var(--green-bright); background: rgba(127,176,105,0.1); border: 1px solid rgba(127,176,105,0.3); padding: 3px 9px; border-radius: 3px; margin-bottom: 10px; } @media (max-width: 600px){.el-sim h1{ font-size: 1.7rem; } .el-sim .wrap{ padding: 32px 16px 100px; } .el-sim .panel{ padding: 18px; } } @media (prefers-reduced-motion: reduce){.el-sim *{ animation-duration: 0.01ms !important; animation-iteration-count: 1 !important; } } </style> <div class="wrap"> <header class="hero"> <div class="hero-kicker">ELEKTRONICA — INTERACTIEVE UITLEG</div> <h1>Wat er echt gebeurt in een stroomkring</h1> <p class="hero-sub">Sleep aan de knoppen. Elke animatie hieronder is live gekoppeld aan de formule erboven — verander een waarde en zie wat er werkelijk fysiek gebeurt, niet alleen welk getal er verandert.</p> </header> <section class="first"> <h2><span class="section-num">01</span> Coulomb — wat is lading eigenlijk?</h2> <p class="lead">Voordat spanning of stroom iets betekenen, moet je weten wat er stroomt. Dat is <b>lading</b>.</p> <p>Elk elektron heeft een piepklein beetje elektrische lading. Die lading is zó klein dat rekenen in "aantal elektronen" onwerkbaar is — je zou getallen krijgen als 6.242.000.000.000.000.000 elektronen voor iets simpels. Daarom is er een grotere, praktische eenheid afgesproken: de <b>Coulomb (C)</b>.</p> <div class="var-key"> <div><b>1 Coulomb</b> = de lading van ongeveer 6,24 × 10¹⁸ elektronen bij elkaar</div> </div> <p>Een Coulomb is dus geen "ding" dat je kunt aanraken — het is een <b>hoeveelheidsmaat</b>, net zoals een "dozijn" een hoeveelheidsmaat is voor 12 stuks. Alleen dan voor elektrische lading in plaats van eieren.</p> <div class="panel"> <div class="panel-label">SIMULATIE — elektronen optellen tot 1 Coulomb</div> <svg class="diagram" viewBox="0 0 680 200" id="els_coulombSvg"> <rect x="0" y="0" width="680" height="200" fill="none"/> <text x="340" y="24" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="12">elektronen verzameld in de "emmer"</text> <!-- bucket --> <path d="M 260 60 L 250 170 L 430 170 L 420 60" fill="none" stroke="#2c3444" stroke-width="2"/> <g id="els_electronDots"></g> <text x="340" y="192" text-anchor="middle" fill="#dfe4ea" font-family="monospace" font-size="13" id="els_coulombCounter">0 × 10¹⁸ elektronen</text> </svg> <div class="controls"> <div class="control green"> <div class="control-row"><span class="label">verzamelde lading</span><span class="value green" id="els_coulombVal">0.00 C</span></div> <input type="range" id="els_coulombSlider" min="0" max="100" value="0" step="1"> </div> </div> <div class="readout"> <div class="readout-item highlight"> <div class="rlabel">q (lading)</div> <div class="rvalue" id="els_coulombQOut">0.00 C</div> </div> </div> </div> <div class="callout"> <div class="ctitle">WAAROM DIT BELANGRIJK IS</div> Elke formule hierna — stroom, spanning, condensator — draait om lading (q). Coulomb is de "munteenheid" waarin je die lading afrekent. Zonder dit begrip is een Ampere of een Volt gewoon een willekeurig woord. </div> </section> <hr class="divider"> <section> <h2><span class="section-num">02</span> Δ (Delta) — "verandering in"</h2> <p class="lead">Je ziet dit symbool in bijna elke formule hieronder. Het is geen getal, het is een instructie.</p> <div class="formula-box">Δ X &nbsp;=&nbsp; X<sub>eind</sub> − X<sub>begin</sub></div> <div class="panel"> <div class="panel-label">SIMULATIE — Δ met temperatuur als voorbeeld</div> <svg class="diagram" viewBox="0 0 680 160" id="els_deltaSvg"> <line x1="80" y1="130" x2="600" y2="130" stroke="#2c3444" stroke-width="2"/> <text x="60" y="134" fill="#8b93a3" font-family="monospace" font-size="11" text-anchor="end">begin</text> <text x="620" y="134" fill="#8b93a3" font-family="monospace" font-size="11" text-anchor="start">eind</text> <circle id="els_deltaStart" cx="120" cy="120" r="6" fill="#5b8dd9"/> <circle id="els_deltaEnd" cx="560" cy="60" r="6" fill="#c9803d"/> <line id="els_deltaBracket" x1="120" y1="120" x2="560" y2="60" stroke="#e6a25c" stroke-width="1.5" stroke-dasharray="4 3"/> <text id="els_deltaLabel" x="340" y="40" text-anchor="middle" fill="#e6a25c" font-family="monospace" font-size="14" font-weight="600">ΔT = 0°C</text> </svg> <div class="controls"> <div class="control blue"> <div class="control-row"><span class="label">begin-temperatuur</span><span class="value blue" id="els_deltaStartVal">15°C</span></div> <input type="range" id="els_deltaStartSlider" min="0" max="40" value="15" step="1"> </div> <div class="control"> <div class="control-row"><span class="label">eind-temperatuur</span><span class="value" id="els_deltaEndVal">22°C</span></div> <input type="range" id="els_deltaEndSlider" min="0" max="40" value="22" step="1"> </div> </div> </div> <p>In de elektronica gaat het bijna nooit om een absolute waarde, maar om <b>hoeveel iets verandert</b> — en vaak specifiek om <b>hoe snel</b> (verandering gedeeld door tijd, Δt). Dat is precies wat Δt/Δq/Δu in de volgende hoofdstukken betekenen.</p> </section> <hr class="divider"> <section> <h2><span class="section-num">03</span> Stroomsterkte (I) — hoeveel lading passeert per seconde</h2> <span class="analogy-label">WATER-ANALOGIE</span> <p class="lead">Stroomsterkte is <b>niet</b> "hoe hard elektronen bewegen" — het is <b>hoeveel lading een punt in de draad passeert, per seconde</b>. Vergelijk het met water door een pijp: stroomsterkte is niet de snelheid van een individueel watermolecuul, het is het <i>debiet</i> — hoeveel liter per seconde er door de pijp gaat.</p> <div class="formula-box">I &nbsp;=&nbsp; Δq / Δt</div> <div class="var-key"> <div><b>Δq</b> = verplaatste lading, in Coulomb (C)</div> <div><b>Δt</b> = tijdsduur waarin dat gebeurt, in seconden (s)</div> <div><b>I</b> = stroomsterkte, in Ampere (A)</div> <div style="margin-top:8px; color:#dfe4ea;"><b>1 Ampere = 1 Coulomb per seconde</b> — dat is letterlijk wat de eenheid betekent: A = C/s</div> </div> <div class="panel"> <div class="panel-label">SIMULATIE — draad met stromende lading</div> <svg class="diagram" viewBox="0 0 680 140" id="els_currentSvg"> <rect x="40" y="55" width="600" height="30" rx="4" fill="#1a2029" stroke="#2c3444" stroke-width="2"/> <!-- gate marking the measurement point --> <line x1="400" y1="40" x2="400" y2="100" stroke="#e6a25c" stroke-width="2" stroke-dasharray="3 3"/> <text x="400" y="30" text-anchor="middle" fill="#e6a25c" font-family="monospace" font-size="11">meetpunt</text> <g id="els_chargeDots"></g> <text x="340" y="122" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="12" id="els_currentCaption">elektronen bewegen door de draad →</text> </svg> <div class="controls"> <div class="control"> <div class="control-row"><span class="label">stroomsterkte I</span><span class="value" id="els_currentVal">1.0 A</span></div> <input type="range" id="els_currentSlider" min="0.2" max="4" value="1" step="0.1"> </div> </div> <div class="readout"> <div class="readout-item"> <div class="rlabel">Δq per seconde</div> <div class="rvalue" id="els_currentQOut">1.0 C/s</div> </div> <div class="readout-item highlight"> <div class="rlabel">I</div> <div class="rvalue" id="els_currentIOut">1.0 A</div> </div> </div> </div> <h3>Wat beweegt er nou echt?</h3> <p>In een geleider (bijvoorbeeld koperdraad) zit een vast rooster van atoomkernen. Daartussen bewegen vrije elektronen — die bewegen van de <b>negatieve pool naar de positieve pool</b> van de bron.</p> <div class="callout warn"> <div class="ctitle">KLASSIEK VERWARRINGSPUNT</div> De <i>technische stroomrichting</i> die je in schema's tekent (de pijl) loopt van + naar −, dus <b>tegengesteld</b> aan de daadwerkelijke beweging van de elektronen. Dit is historisch zo afgesproken — vóór men wist dat elektronen negatief geladen zijn — en is nooit veranderd. Voor het rekenen maakt dit niets uit, maar "stroomrichting op papier" en "waar de elektronen echt heen gaan" zijn twee verschillende dingen. </div> </section> <hr class="divider"> <section> <h2><span class="section-num">04</span> Spanning (U) — elektrische "hoogte"</h2> <span class="analogy-label">WATER-ANALOGIE</span> <p class="lead">Spanning is geen "hoeveelheid elektriciteit" — het is een <b>verschil in potentiële energie</b> tussen twee punten. Zoals water van hoog naar laag stroomt door een hoogteverschil, stroomt lading door een spanningsverschil.</p> <div class="formula-box blue">U &nbsp;=&nbsp; ΔW / Δq</div> <div class="var-key"> <div><b>ΔW</b> = verrichte arbeid (energie), in Joule (J)</div> <div><b>Δq</b> = verplaatste lading, in Coulomb (C)</div> <div><b>U</b> = spanning, in Volt (V)</div> <div style="margin-top:8px; color:#dfe4ea;"><b>1 Volt = 1 Joule per Coulomb</b> — de energie die vrijkomt (of nodig is) om 1 Coulomb lading tussen twee punten te verplaatsen</div> </div> <div class="panel"> <div class="panel-label">SIMULATIE — waterreservoir op hoogte</div> <svg class="diagram" viewBox="0 0 680 220" id="els_voltageSvg"> <line x1="60" y1="200" x2="620" y2="200" stroke="#2c3444" stroke-width="2"/> <!-- reservoir --> <rect id="els_reservoirTank" x="120" y="40" width="90" height="140" fill="none" stroke="#2c3444" stroke-width="2"/> <rect id="els_reservoirWater" x="122" y="120" width="86" height="58" fill="#5b8dd9" opacity="0.5"/> <text x="165" y="30" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="11">reservoir A</text> <!-- pipe --> <path id="els_voltagePipe" d="M 210 175 Q 350 175 430 175" stroke="#5b8dd9" stroke-width="4" fill="none" opacity="0.7"/> <!-- ground level --> <rect x="430" y="150" width="90" height="50" fill="none" stroke="#2c3444" stroke-width="2"/> <rect x="432" y="170" width="86" height="28" fill="#5b8dd9" opacity="0.3"/> <text x="475" y="140" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="11">punt B (referentie)</text> <text id="els_voltageDropLabel" x="330" y="90" text-anchor="middle" fill="#7ba7ea" font-family="monospace" font-size="13" font-weight="600">U = 5 V</text> </svg> <div class="controls"> <div class="control blue"> <div class="control-row"><span class="label">spanning U (hoogteverschil)</span><span class="value blue" id="els_voltageVal">5 V</span></div> <input type="range" id="els_voltageSlider" min="0" max="12" value="5" step="0.5"> </div> </div> <div class="readout"> <div class="readout-item highlight"> <div class="rlabel">U</div> <div class="rvalue" id="els_voltageUOut">5 V</div> </div> <div class="readout-item"> <div class="rlabel">"drang" om te stromen</div> <div class="rvalue" id="els_voltageDescOut">gemiddeld</div> </div> </div> </div> <h3>Spanning bestaat alleen tussen twee punten</h3> <p>Dit is cruciaal: je kunt niet zeggen "dit punt heeft een spanning van 5V" zonder erbij te zeggen <i>ten opzichte van wat</i>. Net zoals "dit reservoir staat op 5 meter hoogte" alleen betekenis heeft als je weet ten opzichte van welk referentieniveau (zeeniveau? straatniveau?).</p> <p>Daarom kies je een <b>referentiepunt</b> — ook wel "common point" of "nulpunt" genoemd — een vast punt waar je alle andere spanningen mee vergelijkt. <b>Het is gebruikelijk om de negatieve pool van de spanningsbron als dit referentiepunt te kiezen.</b></p> <div class="callout correction"> <div class="ctitle">CORRECTIE OP EIGEN AANTEKENING</div> Eerdere notitie zei: "zwart/min is geen ground, het is een zwevend 0-punt." Dat klopt niet — de negatieve pool wordt juist <b>gekozen als vast referentiepunt</b>. "Zwevend" (floating) zou betekenen dat een punt géén vaste relatie heeft met de rest van het circuit — dat is hier niet het geval. De min-pool ligt hier per afspraak vast op 0V. </div> </section> <hr class="divider"> <section> <h2><span class="section-num">05</span> De Wet van Ohm — hoe U, I en R samenhangen</h2> <p class="lead">Nu spanning en stroom apart duidelijk zijn: hoe hangen ze samen in een geleider?</p> <div class="formula-box">I &nbsp;=&nbsp; U / R &nbsp;&nbsp;&nbsp;&nbsp;ofwel&nbsp;&nbsp;&nbsp;&nbsp; U &nbsp;=&nbsp; I × R</div> <div class="var-key"> <div><b>I</b> = stroomsterkte, in Ampere (A)</div> <div><b>U</b> = spanning over de geleider, in Volt (V)</div> <div><b>R</b> = weerstand van de geleider, in Ohm (Ω)</div> </div> <p><b>Waarom werkt het zo?</b> Denk aan een pijp met een vernauwing (de weerstand). Bij een gegeven hoogteverschil (U) geldt: hoe nauwer de vernauwing (hoe hoger R), hoe minder water er per seconde doorheen kan (hoe lager I). R is de "moeite" die het kost voor stroom om te lopen.</p> <div class="panel"> <div class="panel-label">SIMULATIE — pijp met instelbare vernauwing</div> <svg class="diagram" viewBox="0 0 680 160" id="els_ohmSvg"> <path d="M 40 70 L 260 70" stroke="#2c3444" stroke-width="30" fill="none"/> <path id="els_ohmNeck" d="M 260 70 L 420 70" stroke="#2c3444" stroke-width="30" fill="none"/> <path d="M 420 70 L 640 70" stroke="#2c3444" stroke-width="30" fill="none"/> <g id="els_ohmFlow"></g> <text x="340" y="35" text-anchor="middle" fill="#99c980" font-family="monospace" font-size="12">weerstand R</text> <text x="120" y="120" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="12">spanning (druk) duwt de stroom</text> </svg> <div class="controls"> <div class="control blue"> <div class="control-row"><span class="label">spanning U</span><span class="value blue" id="els_ohmUVal">10 V</span></div> <input type="range" id="els_ohmUSlider" min="1" max="20" value="10" step="0.5"> </div> <div class="control green"> <div class="control-row"><span class="label">weerstand R</span><span class="value green" id="els_ohmRVal">100 Ω</span></div> <input type="range" id="els_ohmRSlider" min="10" max="500" value="100" step="10"> </div> </div> <div class="readout"> <div class="readout-item highlight"> <div class="rlabel">I = U / R</div> <div class="rvalue" id="els_ohmIOut">0.100 A</div> </div> </div> </div> <h3>Wat betekent de grafiek visueel?</h3> <p>Zet je stroom (I) uit tegen spanning (U), dan krijg je een rechte lijn door de oorsprong. <b>De helling van die lijn is de weerstand R.</b> Grotere R = minder steile lijn (meer spanning nodig voor dezelfde stroom).</p> <div class="panel"> <div class="panel-label">I-U GRAFIEK — helling verandert live mee met R hierboven</div> <svg class="diagram" viewBox="0 0 400 260" id="els_ohmGraphSvg"> <line x1="50" y1="220" x2="370" y2="220" stroke="#2c3444" stroke-width="1.5"/> <line x1="50" y1="220" x2="50" y2="20" stroke="#2c3444" stroke-width="1.5"/> <text x="370" y="240" text-anchor="end" fill="#8b93a3" font-family="monospace" font-size="11">U (V) →</text> <text x="20" y="30" text-anchor="start" fill="#8b93a3" font-family="monospace" font-size="11">I (A)</text> <line id="els_ohmGraphLine" x1="50" y1="220" x2="370" y2="150" stroke="#99c980" stroke-width="2.5"/> <circle id="els_ohmGraphDot" cx="290" cy="180" r="5" fill="#e6a25c"/> </svg> </div> </section> <hr class="divider"> <section> <h2><span class="section-num">06</span> Weerstand (R) — waarom het de stroom afremt</h2> <p>Op atomair niveau: elektronen die door een materiaal bewegen botsen voortdurend tegen het rooster van atomen. Hoe meer/vaker dat gebeurt, hoe hoger de weerstand. Dit is ook waarom weerstanden <b>warm worden</b> — de botsingen zetten bewegingsenergie om in warmte.</p> <div class="var-key"> <div>Eenheid: <b>Ohm (Ω)</b></div> <div>Hoe hoger R → hoe minder stroom bij dezelfde spanning (zie de Wet van Ohm hierboven, R staat in de noemer)</div> </div> <div class="callout"> <div class="ctitle">ANALOGIE — DE HOOVERDAM</div> Een dam remt de waterstroom af en zet het hoogteverschil (de "spanning" van het water) om in gecontroleerde doorstroom. Een weerstand doet precies hetzelfde met elektrische stroom: het beperkt hoeveel er per seconde doorheen kan bij een gegeven spanning. </div> </section> <hr class="divider"> <section> <h2><span class="section-num">07</span> Referentierichting — U<sub>ab</sub> en I<sub>ab</sub></h2> <p class="lead">Dit bouwt direct voort op spanning: het bestaat alleen tussen twee punten. Hier maken we dat concreet met notatie.</p> <div class="formula-box blue">U<sub>ab</sub> &nbsp;=&nbsp; U<sub>a</sub> − U<sub>b</sub></div> <p><b>U<sub>ab</sub></b> geeft aan hoeveel de spanning in punt <i>a</i> hoger is dan in punt <i>b</i>. Je kunt het ook lezen als: hoeveel de spanning <i>daalt</i> als je van <i>a</i> naar <i>b</i> beweegt. Op dezelfde manier is <b>I<sub>ab</sub></b> de stroom die van <i>a</i> naar <i>b</i> loopt — de volgorde van de letters geeft de richting aan.</p> <div class="panel"> <div class="panel-label">SIMULATIE — twee punten, richting bepaalt het teken</div> <svg class="diagram" viewBox="0 0 680 140" id="els_uabSvg"> <circle cx="150" cy="70" r="30" fill="#1a2029" stroke="#5b8dd9" stroke-width="2"/> <text x="150" y="76" text-anchor="middle" fill="#7ba7ea" font-family="monospace" font-size="16" font-weight="600">a</text> <circle cx="530" cy="70" r="30" fill="#1a2029" stroke="#5b8dd9" stroke-width="2"/> <text x="530" y="76" text-anchor="middle" fill="#7ba7ea" font-family="monospace" font-size="16" font-weight="600">b</text> <line x1="180" y1="70" x2="500" y2="70" stroke="#2c3444" stroke-width="2"/> <path id="els_uabArrow" d="M 480 60 L 500 70 L 480 80" fill="none" stroke="#e6a25c" stroke-width="2.5"/> <text id="els_uabResultLabel" x="340" y="45" text-anchor="middle" fill="#e6a25c" font-family="monospace" font-size="14" font-weight="600">U_ab = 6 V</text> </svg> <div class="controls"> <div class="control blue"> <div class="control-row"><span class="label">U in punt a</span><span class="value blue" id="els_uaVal">8 V</span></div> <input type="range" id="els_uaSlider" min="-12" max="12" value="8" step="1"> </div> <div class="control blue"> <div class="control-row"><span class="label">U in punt b</span><span class="value blue" id="els_ubVal">2 V</span></div> <input type="range" id="els_ubSlider" min="-12" max="12" value="2" step="1"> </div> </div> <div class="readout"> <div class="readout-item highlight"> <div class="rlabel">U_ab = U_a − U_b</div> <div class="rvalue" id="els_uabOut">6 V</div> </div> </div> </div> <p>Deze waarden kunnen <b>negatief</b> zijn. Sleep punt b hoger dan punt a hierboven — dan wordt U<sub>ab</sub> negatief. Dat is geen fout: het betekent simpelweg dat b hoger ligt dan a, dus de spanning "stijgt" in plaats van "daalt" als je van a naar b gaat.</p> <div class="callout"> <div class="ctitle">VOORBEELD UIT DE LES</div> Een opgave gaf U_ab = −12 V en I_ab = −1 A als antwoord — een volkomen geldig resultaat. Het zegt alleen dat de werkelijke richting tegengesteld is aan de richting die was aangenomen (van a naar b). </div> </section> <hr class="divider"> <section> <h2><span class="section-num">08</span> Condensator — energie opslaan in een elektrisch veld</h2> <p class="lead">Dit onderdeel combineert alles hierboven: lading, spanning, stroom én Δ komen hier samen.</p> <p>Een condensator bestaat uit twee platen dicht bij elkaar met een isolator ertussen. Zet je er spanning op, dan wordt de ene plaat <b>positief</b> geladen (tekort aan elektronen) en de andere <b>negatief</b> (overschot aan elektronen). De tegengesteld geladen platen trekken elkaar aan — er ontstaat een <b>elektrisch veld</b> tussen de platen, en daarin wordt energie opgeslagen.</p> <div class="formula-box green">q &nbsp;=&nbsp; C · u</div> <div class="var-key"> <div><b>q</b> = lading op elke plaat, in Coulomb (C)</div> <div><b>C</b> = capaciteit van de condensator, in Farad (F) — een vaste eigenschap (plaatgrootte, afstand, materiaal ertussen)</div> <div><b>u</b> = spanning over de condensator, in Volt (V)</div> </div> <div class="panel"> <div class="panel-label">SIMULATIE — condensator opladen</div> <svg class="diagram" viewBox="0 0 680 200" id="els_capSvg"> <rect id="els_capPlatePos" x="280" y="40" width="14" height="120" fill="#c9803d"/> <rect id="els_capPlateNeg" x="386" y="40" width="14" height="120" fill="#5b8dd9"/> <text x="287" y="180" text-anchor="middle" fill="#e6a25c" font-family="monospace" font-size="12">+</text> <text x="393" y="180" text-anchor="middle" fill="#7ba7ea" font-family="monospace" font-size="12">−</text> <g id="els_capField"></g> <text x="340" y="25" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="11">elektrisch veld tussen de platen</text> </svg> <div class="controls"> <div class="control blue"> <div class="control-row"><span class="label">spanning u</span><span class="value blue" id="els_capUVal">6 V</span></div> <input type="range" id="els_capUSlider" min="0" max="12" value="6" step="0.5"> </div> <div class="control green"> <div class="control-row"><span class="label">capaciteit C</span><span class="value green" id="els_capCVal">100 µF</span></div> <input type="range" id="els_capCSlider" min="10" max="300" value="100" step="10"> </div> </div> <div class="readout"> <div class="readout-item"> <div class="rlabel">q = C · u</div> <div class="rvalue" id="els_capQOut">600 µC</div> </div> <div class="readout-item highlight"> <div class="rlabel">W = ½Cu²</div> <div class="rvalue" id="els_capWOut">1.80 mJ</div> </div> </div> </div> <h3>De stroom door een condensator</h3> <p>Combineer i = Δq/Δt (stroom-definitie uit hoofdstuk 3) met q = Cu:</p> <div class="formula-box green">i &nbsp;=&nbsp; C · (Δu / Δt)</div> <div class="callout"> <div class="ctitle">DIT IS ANDERS DAN EEN WEERSTAND</div> Bij een weerstand hangt de stroom af van de spanning zélf (Wet van Ohm). Bij een condensator hangt de stroom af van <b>hoe snel</b> de spanning verandert. Staat de spanning stil (constant), dan loopt er dus <b>geen</b> stroom meer — ook al staat er wel spanning op de condensator. </div> <h3>Energie-opslag — let op het kwadraat</h3> <div class="formula-box green">W &nbsp;=&nbsp; ½ · C · u²</div> <p>Sleep hierboven de spanning naar het dubbele en kijk wat er met W gebeurt: het viervoudigt, niet verdubbelt — want 2² = 4. Dit is een veelgemaakte denkfout: energie schaalt <b>kwadratisch</b> met spanning, niet lineair.</p> <h3>Rekenvoorbeeld uit de les</h3> <p>Gegeven: C = 100 µF = 100 × 10⁻⁶ F (rekenmachine: <code>100 EXP -6</code> of <code>100E-6</code>)</p> <div class="var-key"> <div>Stroom tussen 0–4 ms → <b>0,5 A</b> (spanning steeg gelijkmatig)</div> <div>Stroom tussen 4–6 ms → <b>−1 A</b> (negatief teken = spanning daalde in dit interval)</div> <div>Opgeslagen energie op t = 4 ms → <b>20 mJ</b> (spanning op t=4ms invullen in W = ½Cu²)</div> </div> </section> <hr class="divider"> <section> <h2><span class="section-num">09</span> Alles samen</h2> <div class="var-key" style="font-size:0.95rem;"> <div><b>q</b> — lading — Coulomb (C)</div> <div><b>I</b> — stroomsterkte — Ampere (A) = C/s — <span style="color:#8b93a3">I = Δq/Δt</span></div> <div><b>U</b> — spanning — Volt (V) = J/C — <span style="color:#8b93a3">U = ΔW/Δq</span></div> <div><b>R</b> — weerstand — Ohm (Ω) — <span style="color:#8b93a3">R = U/I</span></div> <div><b>C</b> — capaciteit — Farad (F) — <span style="color:#8b93a3">q = Cu</span></div> <div><b>W</b> — energie — Joule (J) — <span style="color:#8b93a3">W = ½Cu²</span></div> </div> <p style="margin-top:20px;"><b>De rode draad:</b> stroom is lading-per-tijd, spanning is energie-per-lading. Bijna elke andere formule in dit vak — Ohm, condensator — is simpelweg deze twee basisdefinities die met elkaar gecombineerd worden.</p> </section> <div class="footer-note"> Interactieve studienotitie · alle simulaties zijn schematisch bedoeld om intuïtie op te bouwen, niet als exacte natuurkundige weergave. </div> </div> </div> <script> (function(){ if (window.__elSimLoaded) return; window.__elSimLoaded = true; // ---------- 01 Coulomb ---------- const coulombSlider = document.getElementById('els_coulombSlider'); const coulombVal = document.getElementById('els_coulombVal'); const coulombQOut = document.getElementById('els_coulombQOut'); const coulombCounter = document.getElementById('els_coulombCounter'); const electronDots = document.getElementById('els_electronDots'); function renderCoulomb(){ const pct = +coulombSlider.value; // 0-100 representing 0-1C const q = pct / 100; coulombVal.textContent = q.toFixed(2) + ' C'; coulombQOut.textContent = q.toFixed(2) + ' C'; coulombCounter.textContent = (q * 6.24).toFixed(2) + ' × 10¹⁸ elektronen'; electronDots.innerHTML = ''; const count = Math.round(pct / 3); // up to ~33 dots for(let i=0;i<count;i++){ const cols = 10; const col = i % cols; const row = Math.floor(i / cols); const cx = 268 + col * 16; const cy = 160 - row * 14; if(cy < 65) continue; const dot = document.createElementNS('http://www.w3.org/2000/svg','circle'); dot.setAttribute('cx', cx); dot.setAttribute('cy', cy); dot.setAttribute('r', 4); dot.setAttribute('fill', '#99c980'); dot.setAttribute('opacity', '0.85'); electronDots.appendChild(dot); } } coulombSlider.addEventListener('input', renderCoulomb); renderCoulomb(); // ---------- 02 Delta ---------- const deltaStartSlider = document.getElementById('els_deltaStartSlider'); const deltaEndSlider = document.getElementById('els_deltaEndSlider'); const deltaStartVal = document.getElementById('els_deltaStartVal'); const deltaEndVal = document.getElementById('els_deltaEndVal'); const deltaStart = document.getElementById('els_deltaStart'); const deltaEnd = document.getElementById('els_deltaEnd'); const deltaBracket = document.getElementById('els_deltaBracket'); const deltaLabel = document.getElementById('els_deltaLabel'); function tempToY(t){ return 125 - (t/40)*100; } function renderDelta(){ const s = +deltaStartSlider.value; const e = +deltaEndSlider.value; deltaStartVal.textContent = s + '°C'; deltaEndVal.textContent = e + '°C'; const sy = tempToY(s), ey = tempToY(e); deltaStart.setAttribute('cy', sy); deltaEnd.setAttribute('cy', ey); deltaBracket.setAttribute('y1', sy); deltaBracket.setAttribute('y2', ey); const diff = e - s; deltaLabel.textContent = 'ΔT = ' + (diff>=0?'+':'') + diff + '°C'; deltaLabel.setAttribute('y', Math.min(sy,ey) - 15); } deltaStartSlider.addEventListener('input', renderDelta); deltaEndSlider.addEventListener('input', renderDelta); renderDelta(); // ---------- 03 Current ---------- const currentSlider = document.getElementById('els_currentSlider'); const currentVal = document.getElementById('els_currentVal'); const currentQOut = document.getElementById('els_currentQOut'); const currentIOut = document.getElementById('els_currentIOut'); const currentCaption = document.getElementById('els_currentCaption'); const chargeDots = document.getElementById('els_chargeDots'); let currentDots = []; function initCurrentDots(){ chargeDots.innerHTML = ''; currentDots = []; for(let i=0;i<8;i++){ const dot = document.createElementNS('http://www.w3.org/2000/svg','circle'); dot.setAttribute('r', 5); dot.setAttribute('fill', '#e6a25c'); dot.setAttribute('cy', 70); const x = 60 + i * 75; dot.setAttribute('cx', x); chargeDots.appendChild(dot); currentDots.push({el:dot, x:x}); } } initCurrentDots(); let currentAnimId = null; function animateCurrent(){ const speed = (+currentSlider.value) * 1.4; currentDots.forEach(d=>{ d.x += speed; if(d.x > 640) d.x = 40; d.el.setAttribute('cx', d.x); }); currentAnimId = requestAnimationFrame(animateCurrent); } animateCurrent(); function renderCurrent(){ const I = +currentSlider.value; currentVal.textContent = I.toFixed(1) + ' A'; currentQOut.textContent = I.toFixed(1) + ' C/s'; currentIOut.textContent = I.toFixed(1) + ' A'; } currentSlider.addEventListener('input', renderCurrent); renderCurrent(); // ---------- 04 Voltage ---------- const voltageSlider = document.getElementById('els_voltageSlider'); const voltageVal = document.getElementById('els_voltageVal'); const voltageUOut = document.getElementById('els_voltageUOut'); const voltageDescOut = document.getElementById('els_voltageDescOut'); const reservoirWater = document.getElementById('els_reservoirWater'); const voltageDropLabel = document.getElementById('els_voltageDropLabel'); function renderVoltage(){ const U = +voltageSlider.value; voltageVal.textContent = U + ' V'; voltageUOut.textContent = U + ' V'; const desc = U < 3 ? 'zwak' : U < 8 ? 'gemiddeld' : 'sterk'; voltageDescOut.textContent = desc; // water height maps to U: higher U = water fills higher in reservoir (more potential) const maxHeight = 140; const waterHeight = 20 + (U/12) * maxHeight * 0.85; const y = 178 - waterHeight; reservoirWater.setAttribute('y', Math.max(y, 42)); reservoirWater.setAttribute('height', Math.min(waterHeight, 136)); voltageDropLabel.textContent = 'U = ' + U + ' V'; } voltageSlider.addEventListener('input', renderVoltage); renderVoltage(); // ---------- 05 Ohm ---------- const ohmUSlider = document.getElementById('els_ohmUSlider'); const ohmRSlider = document.getElementById('els_ohmRSlider'); const ohmUVal = document.getElementById('els_ohmUVal'); const ohmRVal = document.getElementById('els_ohmRVal'); const ohmIOut = document.getElementById('els_ohmIOut'); const ohmNeck = document.getElementById('els_ohmNeck'); const ohmFlow = document.getElementById('els_ohmFlow'); const ohmGraphLine = document.getElementById('els_ohmGraphLine'); const ohmGraphDot = document.getElementById('els_ohmGraphDot'); let ohmFlowDots = []; function initOhmFlow(){ ohmFlow.innerHTML = ''; ohmFlowDots = []; for(let i=0;i<10;i++){ const dot = document.createElementNS('http://www.w3.org/2000/svg','circle'); dot.setAttribute('r', 4); dot.setAttribute('fill', '#7ba7ea'); dot.setAttribute('cy', 70); const x = 50 + i * 60; dot.setAttribute('cx', x); ohmFlow.appendChild(dot); ohmFlowDots.push({el:dot, x:x}); } } initOhmFlow(); function ohmAnimate(){ const U = +ohmUSlider.value; const R = +ohmRSlider.value; const I = U / R; const speed = Math.max(0.3, Math.min(I * 25, 8)); ohmFlowDots.forEach(d=>{ d.x += speed; if(d.x > 640) d.x = 40; d.el.setAttribute('cx', d.x); }); requestAnimationFrame(ohmAnimate); } ohmAnimate(); function renderOhm(){ const U = +ohmUSlider.value; const R = +ohmRSlider.value; const I = U / R; ohmUVal.textContent = U.toFixed(1) + ' V'; ohmRVal.textContent = R + ' Ω'; ohmIOut.textContent = I.toFixed(3) + ' A'; // neck width narrows as R increases (R range 10-500 -> stroke 30 down to 6) const neckWidth = Math.max(6, 30 - (R/500)*24); ohmNeck.setAttribute('stroke-width', neckWidth); // graph line slope = 1/R, scaled for display const scale = 4000; // scales R to fit graph nicely const dx = 320; // U axis pixel span const maxUdisp = 20; const dispI = maxUdisp / R * scale / 100; const y2 = Math.max(20, 220 - dispI * 8); ohmGraphLine.setAttribute('x1',50); ohmGraphLine.setAttribute('y1',220); ohmGraphLine.setAttribute('x2',370); ohmGraphLine.setAttribute('y2', y2); // dot position for current U value along the line const frac = U / maxUdisp; const dotX = 50 + frac * dx; const dotY = 220 - frac * (220 - y2); ohmGraphDot.setAttribute('cx', dotX); ohmGraphDot.setAttribute('cy', dotY); } ohmUSlider.addEventListener('input', renderOhm); ohmRSlider.addEventListener('input', renderOhm); renderOhm(); // ---------- 07 Uab ---------- const uaSlider = document.getElementById('els_uaSlider'); const ubSlider = document.getElementById('els_ubSlider'); const uaVal = document.getElementById('els_uaVal'); const ubVal = document.getElementById('els_ubVal'); const uabOut = document.getElementById('els_uabOut'); const uabArrow = document.getElementById('els_uabArrow'); const uabResultLabel = document.getElementById('els_uabResultLabel'); function renderUab(){ const ua = +uaSlider.value; const ub = +ubSlider.value; const uab = ua - ub; uaVal.textContent = ua + ' V'; ubVal.textContent = ub + ' V'; uabOut.textContent = uab + ' V'; uabResultLabel.textContent = 'U_ab = ' + uab + ' V'; if(uab >= 0){ uabArrow.setAttribute('d','M 480 60 L 500 70 L 480 80'); uabArrow.setAttribute('stroke', '#e6a25c'); uabResultLabel.setAttribute('fill', '#e6a25c'); } else { uabArrow.setAttribute('d','M 200 60 L 180 70 L 200 80'); uabArrow.setAttribute('stroke', '#d9705b'); uabResultLabel.setAttribute('fill', '#d9705b'); } } uaSlider.addEventListener('input', renderUab); ubSlider.addEventListener('input', renderUab); renderUab(); // ---------- 08 Capacitor ---------- const capUSlider = document.getElementById('els_capUSlider'); const capCSlider = document.getElementById('els_capCSlider'); const capUVal = document.getElementById('els_capUVal'); const capCVal = document.getElementById('els_capCVal'); const capQOut = document.getElementById('els_capQOut'); const capWOut = document.getElementById('els_capWOut'); const capField = document.getElementById('els_capField'); function renderCap(){ const u = +capUSlider.value; const C = +capCSlider.value; // µF capUVal.textContent = u + ' V'; capCVal.textContent = C + ' µF'; const q_uC = C * u; // microcoulomb capQOut.textContent = q_uC.toFixed(0) + ' µC'; const C_F = C * 1e-6; const W_J = 0.5 * C_F * u * u; capWOut.textContent = (W_J*1000).toFixed(2) + ' mJ'; // field lines density scales with u capField.innerHTML = ''; const numLines = Math.max(1, Math.round(u)); for(let i=0;i<numLines;i++){ const y = 50 + (i * (110/Math.max(numLines,1))); const line = document.createElementNS('http://www.w3.org/2000/svg','line'); line.setAttribute('x1', 296); line.setAttribute('x2', 384); line.setAttribute('y1', y); line.setAttribute('y2', y); line.setAttribute('stroke', '#99c980'); line.setAttribute('stroke-width', '1.5'); line.setAttribute('opacity', '0.6'); capField.appendChild(line); const arrow = document.createElementNS('http://www.w3.org/2000/svg','path'); arrow.setAttribute('d', `M 378 ${y-3} L 384 ${y} L 378 ${y+3}`); arrow.setAttribute('stroke', '#99c980'); arrow.setAttribute('fill', 'none'); arrow.setAttribute('stroke-width', '1.5'); arrow.setAttribute('opacity', '0.6'); capField.appendChild(arrow); } } capUSlider.addEventListener('input', renderCap); capCSlider.addEventListener('input', renderCap); renderCap(); })(); </script>







<div class="el-sim">
<style>
.el-sim{
    --bg: #12161c;
    --bg-panel: #1a2029;
    --bg-panel-raised: #212836;
    --border: #2c3444;
    --text: #dfe4ea;
    --text-dim: #8b93a3;
    --text-faint: #5c6376;
    --copper: #c9803d;
    --copper-bright: #e6a25c;
    --blue: #5b8dd9;
    --blue-bright: #7ba7ea;
    --green: #7fb069;
    --green-bright: #99c980;
    --red: #d9705b;
    --mono: 'SF Mono', 'JetBrains Mono', Consolas, 'Courier New', monospace;
    --sans: -apple-system, 'Segoe UI', 'Inter', Roboto, sans-serif;
  }
.el-sim *{ box-sizing: border-box; }
.el-sim{ scroll-behavior: smooth; }
.el-sim{
    margin:0;
    background: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    line-height: 1.6;
    font-size: 16px;
  }
.el-sim .wrap{
    max-width: 760px;
    margin: 0 auto;
    padding: 24px 16px 60px;
  }
.el-sim header.hero{
    padding: 8px 0 40px;
    border-bottom: 1px solid var(--border);
    margin-bottom: 40px;
  }
.el-sim .hero-kicker{
    font-family: var(--mono);
    font-size: 13px;
    color: var(--copper);
    letter-spacing: 0.02em;
    margin-bottom: 14px;
  }
.el-sim h1{
    font-size: 2.1rem;
    line-height: 1.2;
    margin: 0 0 16px;
    font-weight: 650;
    letter-spacing: -0.01em;
  }
.el-sim .hero-sub{
    color: var(--text-dim);
    font-size: 1.05rem;
    max-width: 58ch;
  }
.el-sim section{
    margin: 64px 0;
  }
.el-sim section.first{ margin-top: 0; }
.el-sim h2{
    font-size: 1.5rem;
    font-weight: 650;
    margin: 0 0 6px;
    display:flex;
    align-items:baseline;
    gap:10px;
  }
.el-sim .section-num{
    font-family: var(--mono);
    font-size: 0.85rem;
    color: var(--text-faint);
    font-weight: 500;
  }
.el-sim h3{
    font-size: 1.05rem;
    font-weight: 650;
    margin: 28px 0 10px;
    color: var(--text);
  }
.el-sim p{ margin: 12px 0; color: var(--text); }
.el-sim p.lead{ color: var(--text-dim); margin-bottom: 22px; }
.el-sim .formula-box{
    background: var(--bg-panel);
    border: 1px solid var(--border);
    border-left: 3px solid var(--copper);
    border-radius: 4px;
    padding: 18px 22px;
    margin: 18px 0;
    font-family: var(--mono);
    font-size: 1.15rem;
    text-align: center;
    color: var(--copper-bright);
    overflow-x: auto;
  }
.el-sim .formula-box.blue{ border-left-color: var(--blue); color: var(--blue-bright); }
.el-sim .formula-box.green{ border-left-color: var(--green); color: var(--green-bright); }
.el-sim .var-key{
    font-family: var(--mono);
    font-size: 0.9rem;
    background: var(--bg-panel);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 14px 18px;
    margin: 14px 0;
    color: var(--text-dim);
  }
.el-sim .var-key div{ padding: 3px 0; }
.el-sim .var-key b{ color: var(--text); font-weight: 600; }
.el-sim .panel{
    background: var(--bg-panel);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 24px;
    margin: 20px 0;
  }
.el-sim .panel-label{
    font-family: var(--mono);
    font-size: 12px;
    color: var(--text-faint);
    margin-bottom: 16px;
    text-transform: none;
  }
.el-sim svg.diagram{
    width: 100%;
    height: auto;
    display: block;
  }
.el-sim .controls{
    display: flex;
    flex-direction: column;
    gap: 18px;
    margin-top: 20px;
  }
.el-sim .control{
    display:flex;
    flex-direction: column;
    gap: 6px;
  }
.el-sim .control-row{
    display:flex;
    justify-content: space-between;
    align-items: baseline;
    font-family: var(--mono);
    font-size: 13px;
  }
.el-sim .control-row .label{ color: var(--text-dim); }
.el-sim .control-row .value{ color: var(--copper-bright); font-weight: 600; }
.el-sim .control-row .value.blue{ color: var(--blue-bright); }
.el-sim .control-row .value.green{ color: var(--green-bright); }
.el-sim input[type="range"]{
    -webkit-appearance: none;
    width: 100%;
    height: 4px;
    border-radius: 2px;
    background: var(--border);
    outline: none;
  }
.el-sim input[type="range"]::-webkit-slider-thumb{
    -webkit-appearance: none;
    width: 16px; height: 16px;
    border-radius: 50%;
    background: var(--copper-bright);
    cursor: pointer;
    border: 2px solid var(--bg);
    box-shadow: 0 0 0 1px var(--copper);
  }
.el-sim input[type="range"]::-moz-range-thumb{
    width: 16px; height: 16px;
    border-radius: 50%;
    background: var(--copper-bright);
    cursor: pointer;
    border: 2px solid var(--bg);
  }
.el-sim .control.blue input[type="range"]::-webkit-slider-thumb{ background: var(--blue-bright); box-shadow: 0 0 0 1px var(--blue); }
.el-sim .control.green input[type="range"]::-webkit-slider-thumb{ background: var(--green-bright); box-shadow: 0 0 0 1px var(--green); }
.el-sim .readout{
    display:flex;
    gap: 14px;
    margin-top: 18px;
    flex-wrap: wrap;
  }
.el-sim .readout-item{
    flex: 1;
    min-width: 130px;
    background: var(--bg-panel-raised);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 12px 14px;
  }
.el-sim .readout-item .rlabel{
    font-family: var(--mono);
    font-size: 11px;
    color: var(--text-faint);
    margin-bottom: 4px;
  }
.el-sim .readout-item .rvalue{
    font-family: var(--mono);
    font-size: 1.3rem;
    font-weight: 600;
    color: var(--text);
  }
.el-sim .readout-item.highlight .rvalue{ color: var(--copper-bright); }
.el-sim .callout{
    background: var(--bg-panel-raised);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 16px 18px;
    margin: 18px 0;
    font-size: 0.95rem;
  }
.el-sim .callout .ctitle{
    font-family: var(--mono);
    font-size: 12px;
    color: var(--blue-bright);
    margin-bottom: 6px;
    font-weight: 600;
  }
.el-sim .callout.warn{ border-left: 3px solid var(--red); }
.el-sim .callout.warn .ctitle{ color: var(--red); }
.el-sim .callout.correction{ border-left: 3px solid var(--copper); }
.el-sim .callout.correction .ctitle{ color: var(--copper-bright); }
.el-sim .divider{
    border: none;
    border-top: 1px solid var(--border);
    margin: 56px 0;
  }
.el-sim .footer-note{
    font-family: var(--mono);
    font-size: 12px;
    color: var(--text-faint);
    margin-top: 60px;
    padding-top: 24px;
    border-top: 1px solid var(--border);
  }
.el-sim .analogy-label{
    display:inline-block;
    font-family: var(--mono);
    font-size: 11px;
    color: var(--green-bright);
    background: rgba(127,176,105,0.1);
    border: 1px solid rgba(127,176,105,0.3);
    padding: 3px 9px;
    border-radius: 3px;
    margin-bottom: 10px;
  }
@media (max-width: 600px){.el-sim h1{ font-size: 1.7rem; }
.el-sim .wrap{ padding: 32px 16px 100px; }
.el-sim .panel{ padding: 18px; }
  }
@media (prefers-reduced-motion: reduce){.el-sim *{ animation-duration: 0.01ms !important; animation-iteration-count: 1 !important; }
  }
</style>
<div class="wrap">
  <header class="hero">
    <div class="hero-kicker">ELEKTRONICA — INTERACTIEVE UITLEG</div>
    <h1>Wat er echt gebeurt in een stroomkring</h1>
    <p class="hero-sub">Sleep aan de knoppen. Elke animatie hieronder is live gekoppeld aan de formule erboven — verander een waarde en zie wat er werkelijk fysiek gebeurt, niet alleen welk getal er verandert.</p>
  </header>
  <section class="first">
    <h2><span class="section-num">01</span> Coulomb — wat is lading eigenlijk?</h2>
    <p class="lead">Voordat spanning of stroom iets betekenen, moet je weten wat er stroomt. Dat is <b>lading</b>.</p>
    <p>Elk elektron heeft een piepklein beetje elektrische lading. Die lading is zó klein dat rekenen in "aantal elektronen" onwerkbaar is — je zou getallen krijgen als 6.242.000.000.000.000.000 elektronen voor iets simpels. Daarom is er een grotere, praktische eenheid afgesproken: de <b>Coulomb (C)</b>.</p>
    <div class="var-key">
      <div><b>1 Coulomb</b> = de lading van ongeveer 6,24 × 10¹⁸ elektronen bij elkaar</div>
    </div>
    <p>Een Coulomb is dus geen "ding" dat je kunt aanraken — het is een <b>hoeveelheidsmaat</b>, net zoals een "dozijn" een hoeveelheidsmaat is voor 12 stuks. Alleen dan voor elektrische lading in plaats van eieren.</p>
    <div class="panel">
      <div class="panel-label">SIMULATIE — elektronen optellen tot 1 Coulomb</div>
      <svg class="diagram" viewBox="0 0 680 200" id="els_coulombSvg">
        <rect x="0" y="0" width="680" height="200" fill="none"/>
        <text x="340" y="24" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="12">elektronen verzameld in de "emmer"</text>
        <!-- bucket -->
        <path d="M 260 60 L 250 170 L 430 170 L 420 60" fill="none" stroke="#2c3444" stroke-width="2"/>
        <g id="els_electronDots"></g>
        <text x="340" y="192" text-anchor="middle" fill="#dfe4ea" font-family="monospace" font-size="13" id="els_coulombCounter">0 × 10¹⁸ elektronen</text>
      </svg>
      <div class="controls">
        <div class="control green">
          <div class="control-row"><span class="label">verzamelde lading</span><span class="value green" id="els_coulombVal">0.00 C</span></div>
          <input type="range" id="els_coulombSlider" min="0" max="100" value="0" step="1">
        </div>
      </div>
      <div class="readout">
        <div class="readout-item highlight">
          <div class="rlabel">q (lading)</div>
          <div class="rvalue" id="els_coulombQOut">0.00 C</div>
        </div>
      </div>
    </div>
    <div class="callout">
      <div class="ctitle">WAAROM DIT BELANGRIJK IS</div>
      Elke formule hierna — stroom, spanning, condensator — draait om lading (q). Coulomb is de "munteenheid" waarin je die lading afrekent. Zonder dit begrip is een Ampere of een Volt gewoon een willekeurig woord.
    </div>
  </section>
  <hr class="divider">
  <section>
    <h2><span class="section-num">02</span> Δ (Delta) — "verandering in"</h2>
    <p class="lead">Je ziet dit symbool in bijna elke formule hieronder. Het is geen getal, het is een instructie.</p>
    <div class="formula-box">Δ X &nbsp;=&nbsp; X<sub>eind</sub> − X<sub>begin</sub></div>
    <div class="panel">
      <div class="panel-label">SIMULATIE — Δ met temperatuur als voorbeeld</div>
      <svg class="diagram" viewBox="0 0 680 160" id="els_deltaSvg">
        <line x1="80" y1="130" x2="600" y2="130" stroke="#2c3444" stroke-width="2"/>
        <text x="60" y="134" fill="#8b93a3" font-family="monospace" font-size="11" text-anchor="end">begin</text>
        <text x="620" y="134" fill="#8b93a3" font-family="monospace" font-size="11" text-anchor="start">eind</text>
        <circle id="els_deltaStart" cx="120" cy="120" r="6" fill="#5b8dd9"/>
        <circle id="els_deltaEnd" cx="560" cy="60" r="6" fill="#c9803d"/>
        <line id="els_deltaBracket" x1="120" y1="120" x2="560" y2="60" stroke="#e6a25c" stroke-width="1.5" stroke-dasharray="4 3"/>
        <text id="els_deltaLabel" x="340" y="40" text-anchor="middle" fill="#e6a25c" font-family="monospace" font-size="14" font-weight="600">ΔT = 0°C</text>
      </svg>
      <div class="controls">
        <div class="control blue">
          <div class="control-row"><span class="label">begin-temperatuur</span><span class="value blue" id="els_deltaStartVal">15°C</span></div>
          <input type="range" id="els_deltaStartSlider" min="0" max="40" value="15" step="1">
        </div>
        <div class="control">
          <div class="control-row"><span class="label">eind-temperatuur</span><span class="value" id="els_deltaEndVal">22°C</span></div>
          <input type="range" id="els_deltaEndSlider" min="0" max="40" value="22" step="1">
        </div>
      </div>
    </div>
    <p>In de elektronica gaat het bijna nooit om een absolute waarde, maar om <b>hoeveel iets verandert</b> — en vaak specifiek om <b>hoe snel</b> (verandering gedeeld door tijd, Δt). Dat is precies wat Δt/Δq/Δu in de volgende hoofdstukken betekenen.</p>
  </section>
  <hr class="divider">
  <section>
    <h2><span class="section-num">03</span> Stroomsterkte (I) — hoeveel lading passeert per seconde</h2>
    <span class="analogy-label">WATER-ANALOGIE</span>
    <p class="lead">Stroomsterkte is <b>niet</b> "hoe hard elektronen bewegen" — het is <b>hoeveel lading een punt in de draad passeert, per seconde</b>. Vergelijk het met water door een pijp: stroomsterkte is niet de snelheid van een individueel watermolecuul, het is het <i>debiet</i> — hoeveel liter per seconde er door de pijp gaat.</p>
    <div class="formula-box">I &nbsp;=&nbsp; Δq / Δt</div>
    <div class="var-key">
      <div><b>Δq</b> = verplaatste lading, in Coulomb (C)</div>
      <div><b>Δt</b> = tijdsduur waarin dat gebeurt, in seconden (s)</div>
      <div><b>I</b> = stroomsterkte, in Ampere (A)</div>
      <div style="margin-top:8px; color:#dfe4ea;"><b>1 Ampere = 1 Coulomb per seconde</b> — dat is letterlijk wat de eenheid betekent: A = C/s</div>
    </div>
    <div class="panel">
      <div class="panel-label">SIMULATIE — draad met stromende lading</div>
      <svg class="diagram" viewBox="0 0 680 140" id="els_currentSvg">
        <rect x="40" y="55" width="600" height="30" rx="4" fill="#1a2029" stroke="#2c3444" stroke-width="2"/>
        <!-- gate marking the measurement point -->
        <line x1="400" y1="40" x2="400" y2="100" stroke="#e6a25c" stroke-width="2" stroke-dasharray="3 3"/>
        <text x="400" y="30" text-anchor="middle" fill="#e6a25c" font-family="monospace" font-size="11">meetpunt</text>
        <g id="els_chargeDots"></g>
        <text x="340" y="122" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="12" id="els_currentCaption">elektronen bewegen door de draad →</text>
      </svg>
      <div class="controls">
        <div class="control">
          <div class="control-row"><span class="label">stroomsterkte I</span><span class="value" id="els_currentVal">1.0 A</span></div>
          <input type="range" id="els_currentSlider" min="0.2" max="4" value="1" step="0.1">
        </div>
      </div>
      <div class="readout">
        <div class="readout-item">
          <div class="rlabel">Δq per seconde</div>
          <div class="rvalue" id="els_currentQOut">1.0 C/s</div>
        </div>
        <div class="readout-item highlight">
          <div class="rlabel">I</div>
          <div class="rvalue" id="els_currentIOut">1.0 A</div>
        </div>
      </div>
    </div>
    <h3>Wat beweegt er nou echt?</h3>
    <p>In een geleider (bijvoorbeeld koperdraad) zit een vast rooster van atoomkernen. Daartussen bewegen vrije elektronen — die bewegen van de <b>negatieve pool naar de positieve pool</b> van de bron.</p>
    <div class="callout warn">
      <div class="ctitle">KLASSIEK VERWARRINGSPUNT</div>
      De <i>technische stroomrichting</i> die je in schema's tekent (de pijl) loopt van + naar −, dus <b>tegengesteld</b> aan de daadwerkelijke beweging van de elektronen. Dit is historisch zo afgesproken — vóór men wist dat elektronen negatief geladen zijn — en is nooit veranderd. Voor het rekenen maakt dit niets uit, maar "stroomrichting op papier" en "waar de elektronen echt heen gaan" zijn twee verschillende dingen.
    </div>
  </section>
  <hr class="divider">
  <section>
    <h2><span class="section-num">04</span> Spanning (U) — elektrische "hoogte"</h2>
    <span class="analogy-label">WATER-ANALOGIE</span>
    <p class="lead">Spanning is geen "hoeveelheid elektriciteit" — het is een <b>verschil in potentiële energie</b> tussen twee punten. Zoals water van hoog naar laag stroomt door een hoogteverschil, stroomt lading door een spanningsverschil.</p>
    <div class="formula-box blue">U &nbsp;=&nbsp; ΔW / Δq</div>
    <div class="var-key">
      <div><b>ΔW</b> = verrichte arbeid (energie), in Joule (J)</div>
      <div><b>Δq</b> = verplaatste lading, in Coulomb (C)</div>
      <div><b>U</b> = spanning, in Volt (V)</div>
      <div style="margin-top:8px; color:#dfe4ea;"><b>1 Volt = 1 Joule per Coulomb</b> — de energie die vrijkomt (of nodig is) om 1 Coulomb lading tussen twee punten te verplaatsen</div>
    </div>
    <div class="panel">
      <div class="panel-label">SIMULATIE — waterreservoir op hoogte</div>
      <svg class="diagram" viewBox="0 0 680 220" id="els_voltageSvg">
        <line x1="60" y1="200" x2="620" y2="200" stroke="#2c3444" stroke-width="2"/>
        <!-- reservoir -->
        <rect id="els_reservoirTank" x="120" y="40" width="90" height="140" fill="none" stroke="#2c3444" stroke-width="2"/>
        <rect id="els_reservoirWater" x="122" y="120" width="86" height="58" fill="#5b8dd9" opacity="0.5"/>
        <text x="165" y="30" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="11">reservoir A</text>
        <!-- pipe -->
        <path id="els_voltagePipe" d="M 210 175 Q 350 175 430 175" stroke="#5b8dd9" stroke-width="4" fill="none" opacity="0.7"/>
        <!-- ground level -->
        <rect x="430" y="150" width="90" height="50" fill="none" stroke="#2c3444" stroke-width="2"/>
        <rect x="432" y="170" width="86" height="28" fill="#5b8dd9" opacity="0.3"/>
        <text x="475" y="140" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="11">punt B (referentie)</text>
        <text id="els_voltageDropLabel" x="330" y="90" text-anchor="middle" fill="#7ba7ea" font-family="monospace" font-size="13" font-weight="600">U = 5 V</text>
      </svg>
      <div class="controls">
        <div class="control blue">
          <div class="control-row"><span class="label">spanning U (hoogteverschil)</span><span class="value blue" id="els_voltageVal">5 V</span></div>
          <input type="range" id="els_voltageSlider" min="0" max="12" value="5" step="0.5">
        </div>
      </div>
      <div class="readout">
        <div class="readout-item highlight">
          <div class="rlabel">U</div>
          <div class="rvalue" id="els_voltageUOut">5 V</div>
        </div>
        <div class="readout-item">
          <div class="rlabel">"drang" om te stromen</div>
          <div class="rvalue" id="els_voltageDescOut">gemiddeld</div>
        </div>
      </div>
    </div>
    <h3>Spanning bestaat alleen tussen twee punten</h3>
    <p>Dit is cruciaal: je kunt niet zeggen "dit punt heeft een spanning van 5V" zonder erbij te zeggen <i>ten opzichte van wat</i>. Net zoals "dit reservoir staat op 5 meter hoogte" alleen betekenis heeft als je weet ten opzichte van welk referentieniveau (zeeniveau? straatniveau?).</p>
    <p>Daarom kies je een <b>referentiepunt</b> — ook wel "common point" of "nulpunt" genoemd — een vast punt waar je alle andere spanningen mee vergelijkt. <b>Het is gebruikelijk om de negatieve pool van de spanningsbron als dit referentiepunt te kiezen.</b></p>
    <div class="callout correction">
      <div class="ctitle">CORRECTIE OP EIGEN AANTEKENING</div>
      Eerdere notitie zei: "zwart/min is geen ground, het is een zwevend 0-punt." Dat klopt niet — de negatieve pool wordt juist <b>gekozen als vast referentiepunt</b>. "Zwevend" (floating) zou betekenen dat een punt géén vaste relatie heeft met de rest van het circuit — dat is hier niet het geval. De min-pool ligt hier per afspraak vast op 0V.
    </div>
  </section>
  <hr class="divider">
  <section>
    <h2><span class="section-num">05</span> De Wet van Ohm — hoe U, I en R samenhangen</h2>
    <p class="lead">Nu spanning en stroom apart duidelijk zijn: hoe hangen ze samen in een geleider?</p>
    <div class="formula-box">I &nbsp;=&nbsp; U / R &nbsp;&nbsp;&nbsp;&nbsp;ofwel&nbsp;&nbsp;&nbsp;&nbsp; U &nbsp;=&nbsp; I × R</div>
    <div class="var-key">
      <div><b>I</b> = stroomsterkte, in Ampere (A)</div>
      <div><b>U</b> = spanning over de geleider, in Volt (V)</div>
      <div><b>R</b> = weerstand van de geleider, in Ohm (Ω)</div>
    </div>
    <p><b>Waarom werkt het zo?</b> Denk aan een pijp met een vernauwing (de weerstand). Bij een gegeven hoogteverschil (U) geldt: hoe nauwer de vernauwing (hoe hoger R), hoe minder water er per seconde doorheen kan (hoe lager I). R is de "moeite" die het kost voor stroom om te lopen.</p>
    <div class="panel">
      <div class="panel-label">SIMULATIE — pijp met instelbare vernauwing</div>
      <svg class="diagram" viewBox="0 0 680 160" id="els_ohmSvg">
        <path d="M 40 70 L 260 70" stroke="#2c3444" stroke-width="30" fill="none"/>
        <path id="els_ohmNeck" d="M 260 70 L 420 70" stroke="#2c3444" stroke-width="30" fill="none"/>
        <path d="M 420 70 L 640 70" stroke="#2c3444" stroke-width="30" fill="none"/>
        <g id="els_ohmFlow"></g>
        <text x="340" y="35" text-anchor="middle" fill="#99c980" font-family="monospace" font-size="12">weerstand R</text>
        <text x="120" y="120" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="12">spanning (druk) duwt de stroom</text>
      </svg>
      <div class="controls">
        <div class="control blue">
          <div class="control-row"><span class="label">spanning U</span><span class="value blue" id="els_ohmUVal">10 V</span></div>
          <input type="range" id="els_ohmUSlider" min="1" max="20" value="10" step="0.5">
        </div>
        <div class="control green">
          <div class="control-row"><span class="label">weerstand R</span><span class="value green" id="els_ohmRVal">100 Ω</span></div>
          <input type="range" id="els_ohmRSlider" min="10" max="500" value="100" step="10">
        </div>
      </div>
      <div class="readout">
        <div class="readout-item highlight">
          <div class="rlabel">I = U / R</div>
          <div class="rvalue" id="els_ohmIOut">0.100 A</div>
        </div>
      </div>
    </div>
    <h3>Wat betekent de grafiek visueel?</h3>
    <p>Zet je stroom (I) uit tegen spanning (U), dan krijg je een rechte lijn door de oorsprong. <b>De helling van die lijn is de weerstand R.</b> Grotere R = minder steile lijn (meer spanning nodig voor dezelfde stroom).</p>
    <div class="panel">
      <div class="panel-label">I-U GRAFIEK — helling verandert live mee met R hierboven</div>
      <svg class="diagram" viewBox="0 0 400 260" id="els_ohmGraphSvg">
        <line x1="50" y1="220" x2="370" y2="220" stroke="#2c3444" stroke-width="1.5"/>
        <line x1="50" y1="220" x2="50" y2="20" stroke="#2c3444" stroke-width="1.5"/>
        <text x="370" y="240" text-anchor="end" fill="#8b93a3" font-family="monospace" font-size="11">U (V) →</text>
        <text x="20" y="30" text-anchor="start" fill="#8b93a3" font-family="monospace" font-size="11">I (A)</text>
        <line id="els_ohmGraphLine" x1="50" y1="220" x2="370" y2="150" stroke="#99c980" stroke-width="2.5"/>
        <circle id="els_ohmGraphDot" cx="290" cy="180" r="5" fill="#e6a25c"/>
      </svg>
    </div>
  </section>
  <hr class="divider">
  <section>
    <h2><span class="section-num">06</span> Weerstand (R) — waarom het de stroom afremt</h2>
    <p>Op atomair niveau: elektronen die door een materiaal bewegen botsen voortdurend tegen het rooster van atomen. Hoe meer/vaker dat gebeurt, hoe hoger de weerstand. Dit is ook waarom weerstanden <b>warm worden</b> — de botsingen zetten bewegingsenergie om in warmte.</p>
    <div class="var-key">
      <div>Eenheid: <b>Ohm (Ω)</b></div>
      <div>Hoe hoger R → hoe minder stroom bij dezelfde spanning (zie de Wet van Ohm hierboven, R staat in de noemer)</div>
    </div>
    <div class="callout">
      <div class="ctitle">ANALOGIE — DE HOOVERDAM</div>
      Een dam remt de waterstroom af en zet het hoogteverschil (de "spanning" van het water) om in gecontroleerde doorstroom. Een weerstand doet precies hetzelfde met elektrische stroom: het beperkt hoeveel er per seconde doorheen kan bij een gegeven spanning.
    </div>
  </section>
  <hr class="divider">
  <section>
    <h2><span class="section-num">07</span> Referentierichting — U<sub>ab</sub> en I<sub>ab</sub></h2>
    <p class="lead">Dit bouwt direct voort op spanning: het bestaat alleen tussen twee punten. Hier maken we dat concreet met notatie.</p>
    <div class="formula-box blue">U<sub>ab</sub> &nbsp;=&nbsp; U<sub>a</sub> − U<sub>b</sub></div>
    <p><b>U<sub>ab</sub></b> geeft aan hoeveel de spanning in punt <i>a</i> hoger is dan in punt <i>b</i>. Je kunt het ook lezen als: hoeveel de spanning <i>daalt</i> als je van <i>a</i> naar <i>b</i> beweegt. Op dezelfde manier is <b>I<sub>ab</sub></b> de stroom die van <i>a</i> naar <i>b</i> loopt — de volgorde van de letters geeft de richting aan.</p>
    <div class="panel">
      <div class="panel-label">SIMULATIE — twee punten, richting bepaalt het teken</div>
      <svg class="diagram" viewBox="0 0 680 140" id="els_uabSvg">
        <circle cx="150" cy="70" r="30" fill="#1a2029" stroke="#5b8dd9" stroke-width="2"/>
        <text x="150" y="76" text-anchor="middle" fill="#7ba7ea" font-family="monospace" font-size="16" font-weight="600">a</text>
        <circle cx="530" cy="70" r="30" fill="#1a2029" stroke="#5b8dd9" stroke-width="2"/>
        <text x="530" y="76" text-anchor="middle" fill="#7ba7ea" font-family="monospace" font-size="16" font-weight="600">b</text>
        <line x1="180" y1="70" x2="500" y2="70" stroke="#2c3444" stroke-width="2"/>
        <path id="els_uabArrow" d="M 480 60 L 500 70 L 480 80" fill="none" stroke="#e6a25c" stroke-width="2.5"/>
        <text id="els_uabResultLabel" x="340" y="45" text-anchor="middle" fill="#e6a25c" font-family="monospace" font-size="14" font-weight="600">U_ab = 6 V</text>
      </svg>
      <div class="controls">
        <div class="control blue">
          <div class="control-row"><span class="label">U in punt a</span><span class="value blue" id="els_uaVal">8 V</span></div>
          <input type="range" id="els_uaSlider" min="-12" max="12" value="8" step="1">
        </div>
        <div class="control blue">
          <div class="control-row"><span class="label">U in punt b</span><span class="value blue" id="els_ubVal">2 V</span></div>
          <input type="range" id="els_ubSlider" min="-12" max="12" value="2" step="1">
        </div>
      </div>
      <div class="readout">
        <div class="readout-item highlight">
          <div class="rlabel">U_ab = U_a − U_b</div>
          <div class="rvalue" id="els_uabOut">6 V</div>
        </div>
      </div>
    </div>
    <p>Deze waarden kunnen <b>negatief</b> zijn. Sleep punt b hoger dan punt a hierboven — dan wordt U<sub>ab</sub> negatief. Dat is geen fout: het betekent simpelweg dat b hoger ligt dan a, dus de spanning "stijgt" in plaats van "daalt" als je van a naar b gaat.</p>
    <div class="callout">
      <div class="ctitle">VOORBEELD UIT DE LES</div>
      Een opgave gaf U_ab = −12 V en I_ab = −1 A als antwoord — een volkomen geldig resultaat. Het zegt alleen dat de werkelijke richting tegengesteld is aan de richting die was aangenomen (van a naar b).
    </div>
  </section>
  <hr class="divider">
  <section>
    <h2><span class="section-num">08</span> Condensator — energie opslaan in een elektrisch veld</h2>
    <p class="lead">Dit onderdeel combineert alles hierboven: lading, spanning, stroom én Δ komen hier samen.</p>
    <p>Een condensator bestaat uit twee platen dicht bij elkaar met een isolator ertussen. Zet je er spanning op, dan wordt de ene plaat <b>positief</b> geladen (tekort aan elektronen) en de andere <b>negatief</b> (overschot aan elektronen). De tegengesteld geladen platen trekken elkaar aan — er ontstaat een <b>elektrisch veld</b> tussen de platen, en daarin wordt energie opgeslagen.</p>
    <div class="formula-box green">q &nbsp;=&nbsp; C · u</div>
    <div class="var-key">
      <div><b>q</b> = lading op elke plaat, in Coulomb (C)</div>
      <div><b>C</b> = capaciteit van de condensator, in Farad (F) — een vaste eigenschap (plaatgrootte, afstand, materiaal ertussen)</div>
      <div><b>u</b> = spanning over de condensator, in Volt (V)</div>
    </div>
    <div class="panel">
      <div class="panel-label">SIMULATIE — condensator opladen</div>
      <svg class="diagram" viewBox="0 0 680 200" id="els_capSvg">
        <rect id="els_capPlatePos" x="280" y="40" width="14" height="120" fill="#c9803d"/>
        <rect id="els_capPlateNeg" x="386" y="40" width="14" height="120" fill="#5b8dd9"/>
        <text x="287" y="180" text-anchor="middle" fill="#e6a25c" font-family="monospace" font-size="12">+</text>
        <text x="393" y="180" text-anchor="middle" fill="#7ba7ea" font-family="monospace" font-size="12">−</text>
        <g id="els_capField"></g>
        <text x="340" y="25" text-anchor="middle" fill="#8b93a3" font-family="monospace" font-size="11">elektrisch veld tussen de platen</text>
      </svg>
      <div class="controls">
        <div class="control blue">
          <div class="control-row"><span class="label">spanning u</span><span class="value blue" id="els_capUVal">6 V</span></div>
          <input type="range" id="els_capUSlider" min="0" max="12" value="6" step="0.5">
        </div>
        <div class="control green">
          <div class="control-row"><span class="label">capaciteit C</span><span class="value green" id="els_capCVal">100 µF</span></div>
          <input type="range" id="els_capCSlider" min="10" max="300" value="100" step="10">
        </div>
      </div>
      <div class="readout">
        <div class="readout-item">
          <div class="rlabel">q = C · u</div>
          <div class="rvalue" id="els_capQOut">600 µC</div>
        </div>
        <div class="readout-item highlight">
          <div class="rlabel">W = ½Cu²</div>
          <div class="rvalue" id="els_capWOut">1.80 mJ</div>
        </div>
      </div>
    </div>
    <h3>De stroom door een condensator</h3>
    <p>Combineer i = Δq/Δt (stroom-definitie uit hoofdstuk 3) met q = Cu:</p>
    <div class="formula-box green">i &nbsp;=&nbsp; C · (Δu / Δt)</div>
    <div class="callout">
      <div class="ctitle">DIT IS ANDERS DAN EEN WEERSTAND</div>
      Bij een weerstand hangt de stroom af van de spanning zélf (Wet van Ohm). Bij een condensator hangt de stroom af van <b>hoe snel</b> de spanning verandert. Staat de spanning stil (constant), dan loopt er dus <b>geen</b> stroom meer — ook al staat er wel spanning op de condensator.
    </div>
    <h3>Energie-opslag — let op het kwadraat</h3>
    <div class="formula-box green">W &nbsp;=&nbsp; ½ · C · u²</div>
    <p>Sleep hierboven de spanning naar het dubbele en kijk wat er met W gebeurt: het viervoudigt, niet verdubbelt — want 2² = 4. Dit is een veelgemaakte denkfout: energie schaalt <b>kwadratisch</b> met spanning, niet lineair.</p>
    <h3>Rekenvoorbeeld uit de les</h3>
    <p>Gegeven: C = 100 µF = 100 × 10⁻⁶ F (rekenmachine: <code>100 EXP -6</code> of <code>100E-6</code>)</p>
    <div class="var-key">
      <div>Stroom tussen 0–4 ms → <b>0,5 A</b> (spanning steeg gelijkmatig)</div>
      <div>Stroom tussen 4–6 ms → <b>−1 A</b> (negatief teken = spanning daalde in dit interval)</div>
      <div>Opgeslagen energie op t = 4 ms → <b>20 mJ</b> (spanning op t=4ms invullen in W = ½Cu²)</div>
    </div>
  </section>
  <hr class="divider">
  <section>
    <h2><span class="section-num">09</span> Alles samen</h2>
    <div class="var-key" style="font-size:0.95rem;">
      <div><b>q</b> — lading — Coulomb (C)</div>
      <div><b>I</b> — stroomsterkte — Ampere (A) = C/s — <span style="color:#8b93a3">I = Δq/Δt</span></div>
      <div><b>U</b> — spanning — Volt (V) = J/C — <span style="color:#8b93a3">U = ΔW/Δq</span></div>
      <div><b>R</b> — weerstand — Ohm (Ω) — <span style="color:#8b93a3">R = U/I</span></div>
      <div><b>C</b> — capaciteit — Farad (F) — <span style="color:#8b93a3">q = Cu</span></div>
      <div><b>W</b> — energie — Joule (J) — <span style="color:#8b93a3">W = ½Cu²</span></div>
    </div>
    <p style="margin-top:20px;"><b>De rode draad:</b> stroom is lading-per-tijd, spanning is energie-per-lading. Bijna elke andere formule in dit vak — Ohm, condensator — is simpelweg deze twee basisdefinities die met elkaar gecombineerd worden.</p>
  </section>
  <div class="footer-note">
    Interactieve studienotitie · alle simulaties zijn schematisch bedoeld om intuïtie op te bouwen, niet als exacte natuurkundige weergave.
  </div>
</div>
</div>
<script>
(function(){
  if (window.__elSimLoaded) return;
  window.__elSimLoaded = true;
// ---------- 01 Coulomb ----------
  const coulombSlider = document.getElementById('els_coulombSlider');
  const coulombVal = document.getElementById('els_coulombVal');
  const coulombQOut = document.getElementById('els_coulombQOut');
  const coulombCounter = document.getElementById('els_coulombCounter');
  const electronDots = document.getElementById('els_electronDots');
  function renderCoulomb(){
    const pct = +coulombSlider.value; // 0-100 representing 0-1C
    const q = pct / 100;
    coulombVal.textContent = q.toFixed(2) + ' C';
    coulombQOut.textContent = q.toFixed(2) + ' C';
    coulombCounter.textContent = (q * 6.24).toFixed(2) + ' × 10¹⁸ elektronen';
    electronDots.innerHTML = '';
    const count = Math.round(pct / 3); // up to ~33 dots
    for(let i=0;i<count;i++){
      const cols = 10;
      const col = i % cols;
      const row = Math.floor(i / cols);
      const cx = 268 + col * 16;
      const cy = 160 - row * 14;
      if(cy < 65) continue;
      const dot = document.createElementNS('http://www.w3.org/2000/svg','circle');
      dot.setAttribute('cx', cx);
      dot.setAttribute('cy', cy);
      dot.setAttribute('r', 4);
      dot.setAttribute('fill', '#99c980');
      dot.setAttribute('opacity', '0.85');
      electronDots.appendChild(dot);
    }
  }
  coulombSlider.addEventListener('input', renderCoulomb);
  renderCoulomb();
  // ---------- 02 Delta ----------
  const deltaStartSlider = document.getElementById('els_deltaStartSlider');
  const deltaEndSlider = document.getElementById('els_deltaEndSlider');
  const deltaStartVal = document.getElementById('els_deltaStartVal');
  const deltaEndVal = document.getElementById('els_deltaEndVal');
  const deltaStart = document.getElementById('els_deltaStart');
  const deltaEnd = document.getElementById('els_deltaEnd');
  const deltaBracket = document.getElementById('els_deltaBracket');
  const deltaLabel = document.getElementById('els_deltaLabel');
  function tempToY(t){ return 125 - (t/40)*100; }
  function renderDelta(){
    const s = +deltaStartSlider.value;
    const e = +deltaEndSlider.value;
    deltaStartVal.textContent = s + '°C';
    deltaEndVal.textContent = e + '°C';
    const sy = tempToY(s), ey = tempToY(e);
    deltaStart.setAttribute('cy', sy);
    deltaEnd.setAttribute('cy', ey);
    deltaBracket.setAttribute('y1', sy);
    deltaBracket.setAttribute('y2', ey);
    const diff = e - s;
    deltaLabel.textContent = 'ΔT = ' + (diff>=0?'+':'') + diff + '°C';
    deltaLabel.setAttribute('y', Math.min(sy,ey) - 15);
  }
  deltaStartSlider.addEventListener('input', renderDelta);
  deltaEndSlider.addEventListener('input', renderDelta);
  renderDelta();
  // ---------- 03 Current ----------
  const currentSlider = document.getElementById('els_currentSlider');
  const currentVal = document.getElementById('els_currentVal');
  const currentQOut = document.getElementById('els_currentQOut');
  const currentIOut = document.getElementById('els_currentIOut');
  const currentCaption = document.getElementById('els_currentCaption');
  const chargeDots = document.getElementById('els_chargeDots');
  let currentDots = [];
  function initCurrentDots(){
    chargeDots.innerHTML = '';
    currentDots = [];
    for(let i=0;i<8;i++){
      const dot = document.createElementNS('http://www.w3.org/2000/svg','circle');
      dot.setAttribute('r', 5);
      dot.setAttribute('fill', '#e6a25c');
      dot.setAttribute('cy', 70);
      const x = 60 + i * 75;
      dot.setAttribute('cx', x);
      chargeDots.appendChild(dot);
      currentDots.push({el:dot, x:x});
    }
  }
  initCurrentDots();
  let currentAnimId = null;
  function animateCurrent(){
    const speed = (+currentSlider.value) * 1.4;
    currentDots.forEach(d=>{
      d.x += speed;
      if(d.x > 640) d.x = 40;
      d.el.setAttribute('cx', d.x);
    });
    currentAnimId = requestAnimationFrame(animateCurrent);
  }
  animateCurrent();
  function renderCurrent(){
    const I = +currentSlider.value;
    currentVal.textContent = I.toFixed(1) + ' A';
    currentQOut.textContent = I.toFixed(1) + ' C/s';
    currentIOut.textContent = I.toFixed(1) + ' A';
  }
  currentSlider.addEventListener('input', renderCurrent);
  renderCurrent();
  // ---------- 04 Voltage ----------
  const voltageSlider = document.getElementById('els_voltageSlider');
  const voltageVal = document.getElementById('els_voltageVal');
  const voltageUOut = document.getElementById('els_voltageUOut');
  const voltageDescOut = document.getElementById('els_voltageDescOut');
  const reservoirWater = document.getElementById('els_reservoirWater');
  const voltageDropLabel = document.getElementById('els_voltageDropLabel');
  function renderVoltage(){
    const U = +voltageSlider.value;
    voltageVal.textContent = U + ' V';
    voltageUOut.textContent = U + ' V';
    const desc = U < 3 ? 'zwak' : U < 8 ? 'gemiddeld' : 'sterk';
    voltageDescOut.textContent = desc;
    // water height maps to U: higher U = water fills higher in reservoir (more potential)
    const maxHeight = 140;
    const waterHeight = 20 + (U/12) * maxHeight * 0.85;
    const y = 178 - waterHeight;
    reservoirWater.setAttribute('y', Math.max(y, 42));
    reservoirWater.setAttribute('height', Math.min(waterHeight, 136));
    voltageDropLabel.textContent = 'U = ' + U + ' V';
  }
  voltageSlider.addEventListener('input', renderVoltage);
  renderVoltage();
  // ---------- 05 Ohm ----------
  const ohmUSlider = document.getElementById('els_ohmUSlider');
  const ohmRSlider = document.getElementById('els_ohmRSlider');
  const ohmUVal = document.getElementById('els_ohmUVal');
  const ohmRVal = document.getElementById('els_ohmRVal');
  const ohmIOut = document.getElementById('els_ohmIOut');
  const ohmNeck = document.getElementById('els_ohmNeck');
  const ohmFlow = document.getElementById('els_ohmFlow');
  const ohmGraphLine = document.getElementById('els_ohmGraphLine');
  const ohmGraphDot = document.getElementById('els_ohmGraphDot');
  let ohmFlowDots = [];
  function initOhmFlow(){
    ohmFlow.innerHTML = '';
    ohmFlowDots = [];
    for(let i=0;i<10;i++){
      const dot = document.createElementNS('http://www.w3.org/2000/svg','circle');
      dot.setAttribute('r', 4);
      dot.setAttribute('fill', '#7ba7ea');
      dot.setAttribute('cy', 70);
      const x = 50 + i * 60;
      dot.setAttribute('cx', x);
      ohmFlow.appendChild(dot);
      ohmFlowDots.push({el:dot, x:x});
    }
  }
  initOhmFlow();
  function ohmAnimate(){
    const U = +ohmUSlider.value;
    const R = +ohmRSlider.value;
    const I = U / R;
    const speed = Math.max(0.3, Math.min(I * 25, 8));
    ohmFlowDots.forEach(d=>{
      d.x += speed;
      if(d.x > 640) d.x = 40;
      d.el.setAttribute('cx', d.x);
    });
    requestAnimationFrame(ohmAnimate);
  }
  ohmAnimate();
  function renderOhm(){
    const U = +ohmUSlider.value;
    const R = +ohmRSlider.value;
    const I = U / R;
    ohmUVal.textContent = U.toFixed(1) + ' V';
    ohmRVal.textContent = R + ' Ω';
    ohmIOut.textContent = I.toFixed(3) + ' A';
    // neck width narrows as R increases (R range 10-500 -> stroke 30 down to 6)
    const neckWidth = Math.max(6, 30 - (R/500)*24);
    ohmNeck.setAttribute('stroke-width', neckWidth);
    // graph line slope = 1/R, scaled for display
    const scale = 4000; // scales R to fit graph nicely
    const dx = 320; // U axis pixel span
    const maxUdisp = 20;
    const dispI = maxUdisp / R * scale / 100;
    const y2 = Math.max(20, 220 - dispI * 8);
    ohmGraphLine.setAttribute('x1',50); ohmGraphLine.setAttribute('y1',220);
    ohmGraphLine.setAttribute('x2',370); ohmGraphLine.setAttribute('y2', y2);
    // dot position for current U value along the line
    const frac = U / maxUdisp;
    const dotX = 50 + frac * dx;
    const dotY = 220 - frac * (220 - y2);
    ohmGraphDot.setAttribute('cx', dotX);
    ohmGraphDot.setAttribute('cy', dotY);
  }
  ohmUSlider.addEventListener('input', renderOhm);
  ohmRSlider.addEventListener('input', renderOhm);
  renderOhm();
  // ---------- 07 Uab ----------
  const uaSlider = document.getElementById('els_uaSlider');
  const ubSlider = document.getElementById('els_ubSlider');
  const uaVal = document.getElementById('els_uaVal');
  const ubVal = document.getElementById('els_ubVal');
  const uabOut = document.getElementById('els_uabOut');
  const uabArrow = document.getElementById('els_uabArrow');
  const uabResultLabel = document.getElementById('els_uabResultLabel');
  function renderUab(){
    const ua = +uaSlider.value;
    const ub = +ubSlider.value;
    const uab = ua - ub;
    uaVal.textContent = ua + ' V';
    ubVal.textContent = ub + ' V';
    uabOut.textContent = uab + ' V';
    uabResultLabel.textContent = 'U_ab = ' + uab + ' V';
    if(uab >= 0){
      uabArrow.setAttribute('d','M 480 60 L 500 70 L 480 80');
      uabArrow.setAttribute('stroke', '#e6a25c');
      uabResultLabel.setAttribute('fill', '#e6a25c');
    } else {
      uabArrow.setAttribute('d','M 200 60 L 180 70 L 200 80');
      uabArrow.setAttribute('stroke', '#d9705b');
      uabResultLabel.setAttribute('fill', '#d9705b');
    }
  }
  uaSlider.addEventListener('input', renderUab);
  ubSlider.addEventListener('input', renderUab);
  renderUab();
  // ---------- 08 Capacitor ----------
  const capUSlider = document.getElementById('els_capUSlider');
  const capCSlider = document.getElementById('els_capCSlider');
  const capUVal = document.getElementById('els_capUVal');
  const capCVal = document.getElementById('els_capCVal');
  const capQOut = document.getElementById('els_capQOut');
  const capWOut = document.getElementById('els_capWOut');
  const capField = document.getElementById('els_capField');
  function renderCap(){
    const u = +capUSlider.value;
    const C = +capCSlider.value; // µF
    capUVal.textContent = u + ' V';
    capCVal.textContent = C + ' µF';
    const q_uC = C * u; // microcoulomb
    capQOut.textContent = q_uC.toFixed(0) + ' µC';
    const C_F = C * 1e-6;
    const W_J = 0.5 * C_F * u * u;
    capWOut.textContent = (W_J*1000).toFixed(2) + ' mJ';
    // field lines density scales with u
    capField.innerHTML = '';
    const numLines = Math.max(1, Math.round(u));
    for(let i=0;i<numLines;i++){
      const y = 50 + (i * (110/Math.max(numLines,1)));
      const line = document.createElementNS('http://www.w3.org/2000/svg','line');
      line.setAttribute('x1', 296);
      line.setAttribute('x2', 384);
      line.setAttribute('y1', y);
      line.setAttribute('y2', y);
      line.setAttribute('stroke', '#99c980');
      line.setAttribute('stroke-width', '1.5');
      line.setAttribute('opacity', '0.6');
      capField.appendChild(line);
      const arrow = document.createElementNS('http://www.w3.org/2000/svg','path');
      arrow.setAttribute('d', `M 378 ${y-3} L 384 ${y} L 378 ${y+3}`);
      arrow.setAttribute('stroke', '#99c980');
      arrow.setAttribute('fill', 'none');
      arrow.setAttribute('stroke-width', '1.5');
      arrow.setAttribute('opacity', '0.6');
      capField.appendChild(arrow);
    }
  }
  capUSlider.addEventListener('input', renderCap);
  capCSlider.addEventListener('input', renderCap);
  renderCap();
})();
</script>

































