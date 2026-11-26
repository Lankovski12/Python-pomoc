# Python pomoč

Repozitorij je namenjen učencem Digital School pri tečaju Python. Tukaj najdeš razlago snovi, ki smo jo predelali, in naloge za vajo.

---

## Kazalo

**Snov**

1. [Spremenljivke](#spremenljivke)
2. [Print](#print)
3. [Matematične operacije](#matematične-operacije)
4. [IF stavki](#if-stavki)
5. [Input](#input)
6. [While zanka](#while-zanka)
7. [For zanka](#for-zanka)
8. [Seznami](#seznami)

**Naloge**

1. [Naloge: IF stavki in input](#naloge-if-stavki-in-input)
2. [Naloge: samo while zanka](#naloge-samo-while-zanka)
3. [Naloge: for in while zanka](#naloge-for-in-while-zanka)
4. [Naloge: samo for zanka](#naloge-samo-for-zanka)
5. [Težje naloge: for zanka](#težje-naloge-for-zanka)
6. [Naloge: seznami](#naloge-seznami)

---

# Snov

## Spremenljivke

Vse vrednosti itd. moramo shraniti.

```python
prvo = 5
drugo = 7
vsota = prvo + drugo
print("To je vsota", vsota)
```

## Print

Možna uporaba funkcije print. Print na konec sam doda novo vrstico.

```python
print("Hello world!")
# Hello world!

print("Hej,", "to", "je", "print")
# Hej, to je print

pozdrav = "Živjo"
print(pozdrav)
# Živjo
```

### Ne želiš nove vrstice?

```python
print("Živjo", end=" ")
print("ti")
# Živjo ti
```

Parameter **end** določi, kaj se izpiše na koncu printa (namesto nove vrstice).

```python
print("Živjo", end="---")
print("ti")
# Živjo---ti
```

## Matematične operacije

| Operacija | Znak | Primer |
|-----------|------|--------|
| Vsota | `+` | `vsota = prvi + drugi` |
| Odštevanje | `-` | `razlika = prvi - drugi` |
| Množenje | `*` | `zmnozek = prvi * drugi` |
| Deljenje | `/` | `deljenje = prvi / drugi` |
| Modulo (ostanek) | `%` | `modulo = prvi % drugi` |

**Modulo** predstavlja vrednost, ki ostane pri deljenju dveh števil (ostanek).

```python
modulo = prvi % drugi
# 15 % 7 = 1
```

## IF stavki

Včasih se nam lahko zgodi več različnih dogodkov in potrebujemo vsakega posebej obravnavati. Zato uporabimo IF stavke, kjer lahko v vsakem pogoju ločimo med različnimi dogodki, ki so se zgodili, in njihovim obravnavanjem.

```python
if pogoj:
    posledica
elif pogoj:
    posledica
else:
    posledica
```

V pogojih uporabljamo operatorje:

| Operator | Pomen |
|----------|-------|
| `==` | Preveri, če sta leva in desna stran enaki. (Ne mešaj z `=`, ki levi strani priredi desno stran!) |
| `<`, `>`, `<=`, `>=` | Preverjajo, ali je nekaj manjše, večje ali enako |
| `!=` | Obratno od `==`. Preveri, če sta leva in desna stran različni. |

## Input

V programih moramo sprejeti uporabniški vnos, to naredimo s sledečo kodo.

> **Pazi!** Pred funkcijo input moraš za števila dati `int` (cela števila) ali `float` (decimalna števila).

```python
ime = input("Vnesi svoje ime: ")

prvo_stevilo = int(input("Vnesi prvo število: "))
```

## While zanka

Včasih želimo, da se del kode izvede večkrat zaporedoma, vse dokler velja določen pogoj. Zato uporabimo WHILE zanko, ki na začetku preveri pogoj, in če je resničen (True), izvede kodo. To ponavlja toliko časa, dokler pogoj ne postane neresničen (False).

```python
while pogoj:
    posledica (koda, ki se ponavlja)
```

> **Pazi!** V zanki moraš nujno poskrbeti, da se pogoj slej ko prej spremeni (npr. povečaš števec, spremeniš spremenljivko). Če tega ne narediš, se bo zanka vrtela v neskončnost! (Če se ti to zgodi, pritisni `CTRL + C`.)

Primer:

```python
odstevanje = 5

while odstevanje > 0:
    print(odstevanje)
    odstevanje = odstevanje - 1
    # ali pa
    # odstevanje -= 1

print("Vzlet")
```

## For zanka

Včasih že vnaprej vemo, kolikokrat natančno želimo ponoviti del kode (na primer: izpiši številke od 1 do 10, ali pa ponovi kodo 5-krat). Takrat namesto while zanke raje uporabimo FOR zanko.

Zelo pogosto jo uporabljamo skupaj s funkcijo `range()`, ki nam ustvari zaporedje števil.

```python
for spremenljivka in zaporedje:
    posledica (koda, ki se ponavlja)
```

> **Pazi!** Funkcija `range(n)` začne šteti pri 0 in konča tik pred n. To pomeni, da `range(5)` ustvari števila: 0, 1, 2, 3, 4 (skupaj natanko 5 števil, a brez petice!).

| Zapis | Števila |
|-------|---------|
| `range(5)` | 0, 1, 2, 3, 4 |
| `range(zacetek, konec)`, npr. `range(2, 6)` | 2, 3, 4, 5 |
| `range(zacetek, konec, korak)`, npr. `range(10, 0, -1)` | 10, 9, 8, ..., 1 (brez 0) |

```python
print("Začenjam štetje:")
for i in range(5):
    print(i)
print("Konec!")

# izpis je
# Začenjam štetje:
# 0
# 1
# 2
# 3
# 4
# Konec!
```

## Seznami

### Kaj je seznam?

Do sedaj smo v eno spremenljivko shranili samo eno vrednost. Včasih pa želimo shraniti več vrednosti skupaj, na primer vse ocene v razredu ali točke iz vseh iger. Takrat uporabimo **seznam**.

Seznam je kot škatla s predalčki. V vsakem predalčku je ena vrednost, predalčki pa so postavljeni po vrsti.

### Kako naredimo seznam?

Seznam zapišemo z oglatimi oklepaji `[ ]`, vrednosti pa ločimo z vejicami.

```python
ocene = [5, 3, 4, 5, 2]
print(ocene)
# [5, 3, 4, 5, 2]

prazen = []
print(prazen)
# []
```

Na konec seznama lahko dodamo novo vrednost z `append`:

```python
tocke = []
tocke.append(10)
tocke.append(25)
tocke.append(7)
print(tocke)
# [10, 25, 7]
```

### Kako štejemo v seznamu?

Vsaka vrednost v seznamu ima svojo številko mesta, ki ji rečemo **indeks**.

> **Pazi!** Tako kot pri `range()` tudi v seznamu začnemo šteti pri **0**, ne pri 1!

```python
stevila = [8, 3, 12, 5]
#  indeks:  0  1   2  3
```

Do vrednosti pridemo tako, da za imenom seznama v oglatih oklepajih napišemo indeks:

```python
stevila = [8, 3, 12, 5]

print(stevila[0])   # 8  (prva vrednost)
print(stevila[2])   # 12 (tretja vrednost)

stevila[1] = 100    # vrednost na mestu 1 zamenjamo
print(stevila)
# [8, 100, 12, 5]
```

Koliko vrednosti je v seznamu, nam pove funkcija `len()`:

```python
stevila = [8, 3, 12, 5]
print(len(stevila))
# 4
```

Ker začnemo šteti pri 0, je zadnji indeks vedno `len(seznam) - 1`. V seznamu s 4 vrednostmi je zadnji indeks 3.

### Kako se sprehodimo čez seznam?

Najlažje se čez seznam sprehodimo s for zanko. Spremenljivka v zanki dobi vsakič naslednjo vrednost iz seznama.

```python
stevila = [8, 3, 12, 5]

for stevilo in stevila:
    print(stevilo)

# izpis je
# 8
# 3
# 12
# 5
```

Če potrebujemo tudi indeks (mesto), uporabimo `range(len(seznam))`:

```python
stevila = [8, 3, 12, 5]

for i in range(len(stevila)):
    print("Na mestu", i, "je število", stevila[i])

# izpis je
# Na mestu 0 je število 8
# Na mestu 1 je število 3
# Na mestu 2 je število 12
# Na mestu 3 je število 5
```

Primer: seštejemo vsa števila v seznamu.

```python
stevila = [8, 3, 12, 5]
vsota = 0

for stevilo in stevila:
    vsota = vsota + stevilo

print("Vsota je", vsota)
# Vsota je 28
```

---

# Naloge

## Naloge: IF stavki in input

**1. Kalkulator**

Dokončaj kalkulator. Moraš imeti vseh 5 operacij. Lahko nadgradiš kalkulator tako, da izpiše kot rezultat celoten račun, torej:

```text
3 + 4 = 7
15 / 3 = 5
20 % 3 = 2
```

**2. Popust v trgovini**

Napiši program, ki uporabnika vpraša po končnem znesku nakupa in njegovi starosti. Program naj izračuna končno ceno s popustom po naslednjih pravilih:

- Če je uporabnik star manj kot 15 let, dobi 20% popust.
- Če je znesek nakupa večji od 50 EUR, dobi 10% popust.
- Če je uporabnik star več kot 65 let in zapravi več kot 30 EUR, dobi 15% popust.
- V vseh ostalih primerih ni popusta.

Na koncu naj program izpiše: "Vaš končni znesek za plačilo je: [znesek] EUR."

**3. Vstopnica za kino**

Program naj vpraša po starosti obiskovalca in času (uri) predstave (vpiše naj samo celo uro, npr. 14 ali 20).

Film ima oznako 15+. Če je oseba mlajša od 15 let, ji program izpiše: "Oprostite, film je samo za starejše od 15 let." in se zaključi.

Če je oseba dovolj stara, program preveri uro:

- Za predstave pred 17. uro je cena vstopnice 5 EUR.
- Za predstave od 17. ure naprej je cena vstopnice 7 EUR.

Če obiskovalec kupi VIP sedež (program naj vpraša z "da" ali "ne"), se ceni prišteje še 3 EUR.

Program naj izpiše končno ceno vstopnice.

## Naloge: samo while zanka

**1. Skrito geslo**

Napiši program, ki uporabnika sprašuje "Vnesi geslo: ", dokler ne vnese besede "python". Ko ugane, naj program izpiše "Vstop dovoljen".

*Namig:* uporabi funkcijo `input()` in preverjaj, če je geslo različno (`!=`) od skrivne besede.

**2. Zbiranje točk v igri**

Igraš igro, kjer zbiraš točke. Začneš z 0 točkami. V vsakem koraku zanke naj te program vpraša "Koliko točk si dobil?" in jih prišteje k tvojemu skupnemu številu točk. Zanka naj teče, dokler nimaš vsaj 20 točk. Na koncu izpiši "Zmagal si!".

**3. Nakupovanje v trgovini**

Uporabnik ima v denarnici 50 evrov. Napiši program, ki ga v zanki sprašuje "Koliko stane izdelek, ki ga želiš kupiti? ". Ceno odštej od njegovega denarja in mu izpiši, koliko mu je še ostalo. Zanka naj teče toliko časa, dokler ima v denarnici več kot 0 evrov. Če želi kupiti izdelek, ki je dražji od preostalega denarja, mu izpiši "Nimaš dovolj denarja za ta izdelek!".

**4. Bankomat in varnostni PIN**

Skrita PIN koda je "1234". Uporabnik ima na voljo samo 3 poskuse, da vnese pravilen PIN. Napiši program, ki ga v zanki sprašuje "Vnesi PIN: ". Zanka naj teče, dokler PIN ni pravilen IN dokler ima uporabnik še kaj poskusov. Če vnese pravilen PIN, naj se izpiše "Uspešna prijava!". Če porabi vse 3 poskuse in ne ugane, naj se izpiše "Kartica je blokirana!".

**5. Igra ugibanja števil**

Računalnik si je "zamislil" število 42. Uporabnik mora to število uganiti. V zanki ga program sprašuje po številu. Če uporabnik vnese manjše število, program izpiše "Moje število je večje.". Če vnese večje, program izpiše "Moje število je manjše.". Zanka se konča, ko uporabnik število ugane, na koncu pa se izpiše "Bravo, uganil si!".

## Naloge: for in while zanka

Vsako nalogo poskusi rešiti dvakrat: enkrat z while in enkrat s for zanko.

**1. Ponavljanje besede**

Napiši program, ki uporabnika vpraša: "Katero besedo naj ponavljam?". Nato naj program to besedo izpiše natanko 5-krat.

- *Namig za while:* Ustvari števec, ki se začne pri 0 in povečuje do 5.
- *Namig za for:* Uporabi `range(5)`.

*Bonus:* 5 spremeni na uporabnikov vnos.

**2. Odštevanje do novega leta**

Napiši program, ki odšteva od 10 do 1. Na koncu naj izpiše "Srečno novo leto!".

- *Namig za while:* Začni spremenljivko pri 10 in v vsakem koraku odštej 1 (`-= 1`).
- *Namig za for:* Poskusi `range(10, 0, -1)`.

**3. Soda števila**

Napiši program, ki izpiše samo soda števila od 2 do 10 (torej: 2, 4, 6, 8, 10).

- *Namig za while:* Števec začni pri 2 in ga v vsakem koraku zanke povečaj za dve (`+= 2`).
- *Namig za for:* Ali veš, da ima funkcija range lahko tudi tretjo številko, ki določa korak? Poskusi `range(2, 11, 2)`.

**4. Kvadrati števil**

Napiši program, ki izračuna in izpiše kvadrate prvih petih števil (od 1 do 5). Kvadrat števila dobiš tako, da ga pomnožiš samega s seboj (npr. `2 * 2`). Program naj izpiše: 1, 4, 9, 16, 25.

- *Namig za while:* Števec naj gre od 1 do 5. V zanki izpiši vrednost `stevec * stevec`.
- *Namig za for:* Uporabi `for i in range(1, 6):` in znotraj zanke izpiši `i * i`.

## Naloge: samo for zanka

**1. Poštevanka**

Uporabnik naj vnese poljubno število (npr. 7). Program naj s pomočjo for zanke izpiše celotno poštevanko tega števila do 10.

**Primer izpisa:**

```text
1 x 7 = 7
2 x 7 = 14
...
```

**2. Sedežni red v kinu**

Kino dvorana ima **3 vrste** (oštevilčene od 1 do 3) in v vsaki vrsti **4 sedeže** (oštevilčene od 1 do 4). Napiši program z dvojno `for` zanko, ki bo natisnil vse vstopnice za dvorano.

**Primer izpisa:**

```text
Vrsta 1, Sedež 1
Vrsta 1, Sedež 2
Vrsta 1, Sedež 3
Vrsta 1, Sedež 4
Vrsta 2, Sedež 1
...
```

**3. Igralni kocki**

Predstavljaj si, da vržeš dve igralni kocki (vsaka ima številke od 1 do 6). Napiši program, ki bo z dvojno for zanko izpisal vse možne kombinacije, ki jih lahko vržeš.

*Bonus:* Program naj poleg kombinacije preveri, ali je vsota obeh kock enaka 7. Če je, naj poleg kombinacije izpiše še "Srečna sedmica".

**Primer izpisa:**

```text
1-1
1-2
1-3
1-4
...
```

**4. Koda za sef**

Pozabil si 3-mestno kodo za svoj sef. Veš le to, da so vse tri številke med 0 in 9. Napiši program, ki s tremi for zankami preizkusi vse kombinacije in izpiše pravo.

Spodnje vrstice prilepi čisto na začetek programa, da ti vsakič generira tri naključna števila, ki jih iščeš. Če želiš, da je geslo daljše od treh števil, samo dodaj še več vrstic spodnje kode. Pazi, kako boš preverjal if pogoj!

```python
import random

s1 = random.randint(0, 9)
s2 = random.randint(0, 9)
s3 = random.randint(0, 9)
```

**5. Tabela poštevanke**

Naredimo 10x10 tabelo. V vsaki vrstici imamo poštevanko od 1 do 10.

<img width="450" height="388" alt="slika" src="https://github.com/user-attachments/assets/40c491ad-bc92-4473-8d21-23f8d37d5ba5" />

**6. Piramidi**

Naredimo dve piramidi. Na sliki bomo naredili Full Pyramid in Half Pyramid.

*Bonus:* naredi še katerokoli drugo.

<img width="700" alt="slika" src="https://github.com/user-attachments/assets/f7928d04-6880-449f-baad-aa33106df776" />

## Težje naloge: for zanka

**1. Praštevilo**

Uporabnik naj vnese poljubno število. Program naj preveri, ali je to število praštevilo (praštevila so deljiva samo z 1 in sama s seboj, npr. 2, 3, 5, 7, 11...). Zanka naj gre skozi vsa števila od 2 do nekaj manj kot vneseno število. Če med potjo najde število, ki ga deli brez ostanka, to ni praštevilo!

*Namig:* Uporabi operator za ostanek pri deljenju `%`. Če velja `stevilo % i == 0`, se deli brez ostanka.

## Naloge: seznami

**1. Nakupovalna košarica**

V trgovini si v košarico dal nekaj izdelkov. Njihove cene so shranjene v seznamu `cene = [3, 12, 5, 8, 2]`. Napiši program, ki se s for zanko sprehodi čez košarico in za vsak izdelek izpiše, koliko stane. Na koncu naj izpiše, koliko moraš plačati skupaj.

V denarnici imaš 25 EUR. Če je skupni znesek večji od tega, naj program izpiše "Nimaš dovolj denarja, nekaj moraš vrniti na polico!", sicer pa "Lahko plačaš!".

**Primer izpisa:**

```text
Izdelek 1 stane 3 EUR
Izdelek 2 stane 12 EUR
Izdelek 3 stane 5 EUR
Izdelek 4 stane 8 EUR
Izdelek 5 stane 2 EUR
Skupaj: 30 EUR
Nimaš dovolj denarja, nekaj moraš vrniti na polico!
```

*Namig:* Za številko izdelka uporabi `for i in range(len(cene)):` in izpiši `i + 1`, saj indeksi začnejo pri 0.

*Bonus:* Program naj izpiše še, koliko denarja ti ostane oziroma koliko ti ga manjka.

**2. Lov na zaklad**

Pred tabo je 8 skrinj, oštevilčenih od 0 do 7. V nekaterih je zlato, nekatere pa so prazne. Kaj je v skrinjah, je shranjeno v seznamu (0 pomeni prazno skrinjo):

```python
skrinje = [0, 0, 50, 0, 100, 0, 20, 0]
```

Igralec ima 3 poskuse. Program naj ga vsakič vpraša "Katero skrinjo odpreš (0-7)? ". Če je skrinja prazna, naj izpiše "Prazna skrinja!", sicer pa "Našel si [število] zlatnikov!". Na koncu izpiši, koliko zlatnikov je igralec zbral skupaj.

*Namig:* Vrednost v izbrani skrinji dobiš s `skrinje[izbira]`.

*Bonus:* Ko igralec skrinjo odpre, jo izprazni (vrednost nastavi na 0), da istega zlata ne more pobrati dvakrat.

**3. Vremenska postaja**

Postal si vremenar. Vsak dan v tednu izmeriš temperaturo. Naredi prazen seznam in uporabnika sedemkrat vprašaj "Temperatura za dan [številka dneva]: ". Vsako temperaturo dodaj v seznam.

Ko so vse temperature vnesene, naj program:

- izpiše celoten seznam,
- izpiše, kateri dnevi so bili ledeni (temperatura pod 0),
- na koncu izpiše, koliko ledenih dni je bilo.

**Primer izpisa:**

```text
Temperatura za dan 1: 3
Temperatura za dan 2: -2
Temperatura za dan 3: 1
Temperatura za dan 4: -5
Temperatura za dan 5: 4
Temperatura za dan 6: 0
Temperatura za dan 7: -1
[3, -2, 1, -5, 4, 0, -1]
Dan 2 je bil leden!
Dan 4 je bil leden!
Dan 7 je bil leden!
Ledenih dni: 3
```

*Namig:* Za dodajanje uporabi `temperature.append(t)`. Ne pozabi na `int()` pri inputu!

**Težja naloga: Najboljši rezultat**

Imaš seznam točk, ki so jih igralci dosegli v igri: `tocke = [34, 78, 12, 91, 56, 91, 23]`.

Napiši program, ki:

1. poišče največje število točk **brez** uporabe funkcije `max()`,
2. izpiše, na katerem mestu (indeksu) v seznamu je to število,
3. izračuna in izpiše povprečje vseh točk.

*Namig:* Ustvari spremenljivko `najvecje = tocke[0]`. Nato se sprehodi čez seznam in vsakič preveri, ali je trenutno število večje od `najvecje`. Če je, ga shrani. Za povprečje najprej seštej vse točke in vsoto deli z `len(tocke)`.

*Bonus:* Število 91 se v seznamu pojavi dvakrat. Ali lahko program izpiše obe mesti?
