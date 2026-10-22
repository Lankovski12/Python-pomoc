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

## Nove naloge

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


