# Python_pomoč
Repozitorji namenjem učencem Digital School pri tečaju Python

### Spremenjlivke
Vse vrednosti itd. moramo shraniti.

```python
prvo = 5
drugo = 7
vsota = prvo + drugo
print("To je vsota", vsota)
```
### Print
Možna uporaba funckije print. Print na konec sam doda novo vrstico.

```python
print("Hello world!")
# Hello world!

print("Hej,", "to", "je", "print")
#Hej, to je print

pozdrav = "Živjo"
print(pozdrav)
#Živjo
```

#### <em>Ne želiš nove vrstice?</em>
```python
print("Živjo", end=" ")
print("ti")
#Živjo ti
```

Parameter <b>end</b> določi ločilo med elementi printa.
```python
print("Živjo", end="---")
print("ti")
#Živjo---ti
```

### Matematične operacije

1. Vsota

```python
vsota = prvi + drugi
```
2. Odštevanje

```python
razlika = prvi - drugi
```
3. Množenje

```python
zmnozek = prvi * drugi
```
4. Deljenje

```python
deljenje = prvi / drugi
```

5. Modulo

Modulo predstavlja vrednost, ki ostane pri deljenju dveh števil (ostanek).

```python
modulo = prvi % drugi
# 15 % 7 = 1
```
### IF stavki

Včasih se nam lahko zgodi več različnih dogotkov in potrebujemo vsakega posebej obravnavati. Zato uporabimo IF stavke, kjer lahko v vsakem pogoji ločimo med različnimi dogotki, ki so se zgodili in njihovo obravnavanje. 

```python
if pogoj:
    posledica
elif pogoj:
    posledica
else:
    posledica
```

V pogojih uporabljamo operatorje:

1. ==
Ki preveri, če sta leva in desna stran enaki. (Ne mešaj z =, ki levi strani priredi desno stran!!!!!)

2. <, >, <=, >=
Preverjata ali je nekaj manjše, večje ali enako

3. !=
Obratno od ==. Ta preveri, če sta leva in desna stran različni.

### Input

V programih moramo sprejeti uporabniški vnos, to naredimo s sledečo kodo. Pazi pred funkcijo input moraš za števila dati int ali float (to so decimalna števila).

```python
ime = input("Vnesi svoje ime: ")

prvo_stevilo = int(input("Vnesi prvo število: "))
```

### While zanka
Včasih želimo, da se del kode izvede večkrat zaporedoma, vse dokler velja določen pogoj. Zato uporabimo WHILE zanko, ki na začetku preveri pogoj, in če je resničen (True), izvede kodo. To ponavlja toliko časa, dokler pogoj ne postane neresničen (False).

```python
while pogoj:
    posledica (koda, ki se ponavlja)
```

Pazi! V zanki moraš nujno poskrbeti, da se pogoj slej ko prej spremeni (npr. povečaš števec, spremeniš spremenljivko). Če tega ne narediš, se bo zanka vrtela v neskončnost!! (Če se ti to zgodi, pritisni CTRL + C).

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

### For zanka

Včasih že vnaprej vemo, kolikokrat natančno želimo ponoviti del kode (na primer: izpiši številke od 1 do 10, ali pa ponovi kodo 5-krat). Takrat namesto while zanke raje uporabimo FOR zanko.

Zelo pogosto jo uporabljamo skupaj s funkcijo range(), ki nam ustvari zaporedje števil.

```python
for spremenljivka in zaporedje:
    posledica (koda, ki se ponavlja)
```

Pazi! Funkcija range(n) začne šteti pri 0 in konča tik pred n. To pomeni, da range(5) ustvari števila: 0, 1, 2, 3, 4 (skupaj natanko 5 števil, a brez petice!). Če želiš začeti pri drugem številu in končati drugje, uporabiš range(zacetek, konec). Lahko poveš tudi s kakšnim korakom se štetje spreminja. range(10,0,-1) bo štel od 10 do vključno 1 in brez 0.

```python
print("Začenjam štetje:")
for i in range(5):
    print(i)
print("Konec!")

# izpis je
0
1
2
3
4
```

## Stare naloge
1. Dokončaj kalkulator. Moraš imeti vseh 5 operaciji. Lahko nadgradiš kalkulator tako, da izpiše kot rezultat celotni račun, torej

```python
3 + 4 = 7
15 / 3 = 5
20 % 3 = 2
```

2. Napiši program, ki uporabnika vpraša po končnem znesku nakupa in njegovi starosti. Program naj izračuna končno ceno s popustom po naslednjih pravilih:
- Če je uporabnik star manj kot 15 let, dobi 20% popust.
- Če je znesek nakupa večji od 50 EUR, dobi 10% popust.
- Če je uporabnik star več kot 65 let in zapravi več kot 30 EUR, dobi 15% popust.
- V vseh ostalih primerih ni popusta.

Na koncu naj program izpiše: "Vaš končni znesek za plačilo je: [znesek] EUR."

3. Program naj vpraša po starosti obiskovalca in času (uri) predstave (npr. vpiše naj samo celo uro, npr. 14 ali 20).
Film ima oznako 15+. Če je oseba mlajša od 15 let, ji program izpiše: "Oprostite, film je samo za starejše od 15 let." in se zaključi.
Če je oseba dovolj stara, program preveri uro:
- Za predstave pred 17. uro je cena vstopnice 5 EUR.
- Za predstave od 17. ure naprej je cena vstopnice 7 EUR.

Če obiskovalec kupi VIP sedež (program naj vpraša z "da" ali "ne"), se ceni prišteje še 3 EUR.

Program naj izpiše končno ceno vstopnice.

## Naloge samo z while

1. Skrito geslo

Napiši program, ki uporabnika sprašuje “Vnesi geslo: “, dokler ne vnese besede “python”. Ko ugane, naj program izpiše “Vstop dovoljen”.
Namig: uporabi funkcijo input() in preverjaj, če je geslo različno (!=) od skrivne besede.

2. Zbiranje točk v igri

Igraš igro, kjer zbiraš točke. Začneš z 0 točkami. V vsakem koraku zanke naj te program vpraša “Koliko točk si dobil?” in jih prišteje k tvojemu skupnemu številu točk. Zanka naj teče, dokler nimaš vsaj 20 točk. Na koncu izpiši “Zmagal si!”.

3. Nakupovanje v trgovini

Uporabnik ima v denarnici 50 evrov. Napiši program, ki ga v zanki sprašuje "Koliko stane izdelek, ki ga želiš kupiti? ". Ceno odštej od njegovega denarja in mu izpiši, koliko mu je še ostalo. Zanka naj teče toliko časa, dokler ima v denarnici več kot 0 evrov. Če želi kupiti izdelek, ki je dražji od preostalega denarja, mu izpiši "Nimaš dovolj denarja za ta izdelek!".

4. Bankomat in varnostni PIN

Skrita PIN koda je "1234". Uporabnik ima na voljo samo 3 poskuse, da vnese pravilen PIN. Napiši program, ki ga v zanki sprašuje "Vnesi PIN: ". Zanka naj teče, dokler PIN ni pravilen IN dokler ima uporabnik še kaj poskusov. Če vnese pravilen PIN, naj se izpiše "Uspešna prijava!". Če porabi vse 3 poskuse in ne ugane, naj se izpiše "Kartica je blokirana!".

5. Igra ugibanja števil

Računalnik si je "zamislil" število 42. Uporabnik mora to število uganiti. V zanki ga program sprašuje po številu. Če uporabnik vnese manjše število, program izpiše "Moje število je večje.". Če vnese večje, program izpiše "Moje število je manjše.". Zanka se konča, ko uporabnik število ugane, na koncu pa se izpiše "Bravo, uganil si!".

## Naloge za for in while

1. Napiši program, ki uporabnika vpraša: "Katero besedo naj ponavljam?". Nato naj program to besedo izpiše natanko 5-krat. Namig za while: Ustvari števec, ki se začne pri 0 in povečuje do 5. Namig za for: Uporabi range(5).

Bonus naloga: 5 spremeni na uporabnikov vnos

2. Napiši program, ki odšteva od 10 do 1. Na koncu naj izpiše "Srečno novo leto!". Namig za while: Začni spremenljivko pri 10 in v vsakem koraku odštej 1 (-= 1).Namig za for: Poskusi range(10, 0, -1).

3. Napiši program, ki izpiše samo soda števila od 2 do 10 (torej: 2, 4, 6, 8, 10). Namig za while: Števec začni pri 2 in ga v vsakem koraku zanke povečaj za dve (+= 2). Namig za for: Ali veš, da ima funkcija range lahko tudi tretjo številko, ki določa korak? Poskusi range(2, 11, 2).

4. Napiši program, ki izračuna in izpiše kvadrate prvih petih števil (od 1 do 5). Kvadrat števila dobiš tako, da ga pomnožiš samega s seboj (npr. 2 * 2). Program naj izpiše: 1, 4, 9, 16, 25. Namig za while: Števec naj gre od 1 do 5. V zanki izpiši vrednost števec * števec. Namig za for: Uporabi for i in range(1, 6): in znotraj zanke izpiši i * i.
   
## Naloge samo za for zanko

1. Uporabnik naj vnese poljubno število (npr. 7). Program naj s pomočjo for zanke izpiše celotno poštevanko tega števila do 10. Primer izpisa:
1 x 7 = 7
2 x 7 = 14

2. Naredimo 10x10 tabelo. V vsaki vrstici imamo poštevanko od 1 do 10.
<img width="450" height="388" alt="slika" src="https://github.com/user-attachments/assets/40c491ad-bc92-4473-8d21-23f8d37d5ba5" />


3. Naredimo dve piramidi. Na sliki bomo naredili Full Pyramid in Half Pyramid. Bonus: naredi še katerokoli drugo.
<img width="1568" height="1244" alt="slika" src="https://github.com/user-attachments/assets/f7928d04-6880-449f-baad-aa33106df776" />

### Težje naloge za for zanko

1. Uporabnik naj vnese poljubno število. Program naj preveri, ali je to število praštevilo (praštevila so deljiva samo z 1 in sama s seboj, npr. 2, 3, 5, 7, 11...). Zanka naj gre skozi vsa števila od 2 do nekaj manj kot vneseno število. Če med potjo najde število, ki ga deli brez ostanka, to ni praštevilo! Namig: Uporabi operator za ostanek pri deljenju %. Če velja stevilo % i == 0, se deli brez ostanka.

### Nujna naloga

Program naj uporabnika vpraša za število. Nato s pomočjo while zanke izpiše vsa števila od 1 do n (n je stevilo, ki ga je vpisal uporabnik).
