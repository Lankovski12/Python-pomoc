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

Včasih se potrebujemo vprašati

```python
if pogoj:
    posledica
elif pogoj:
    posledica
else:
    posledica
```


