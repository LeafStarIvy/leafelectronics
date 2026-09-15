---
{"dg-publish":true,"permalink":"/jaar-1/semester-1/circuit-analysis-and-electronics-1/college-1-voedingen-en-ohm/","noteIcon":"","created":"2026-09-15T09:42:39.003+02:00","updated":"2026-09-15T11:33:02.058+02:00","dg-note-properties":{}}
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

Voorbeeld: als de temperatuur van 15°C naar 22°C gaat, is ΔT = 22 - 15 = 7°C.

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

























































