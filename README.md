# Python 🐍
## Variabili 🐅
In python è possibile usare le collezioni di dati in questa maniera

```py
citta = ['roma','milano','napoli']
x,y,z = citta
print(x)
print(y)
print(z)
```

## Tipi di dati
- str = 'ciao'
- int = 200
- float = 1.3
- bool = True 
    > con la prima sempre maiuscola
- list = ['roma','milano','napoli']               
  > le liste non sono array, ma sono simili a livello sintattico, sono collezioni di dati
- tuple = ('roma','milano','napoli')              
- range = range(6)
- dict = {'nome':'Luca','età':24}
  > sono di ti po dizzionario
- set = {'alpha','beta','gamma'}
```py
x = 5
print(type(x))
x = 5.5
print(type(x))
x = 'ciao'
print(type(x))
```

E' possibile usare il casting in python, quindi cambiare il tipo di dato di una variabile
```py
x = '5'
y = 5
print(int(x)+y)
x = '5'
y = 5
print(x+str(y))
```

> il cast per il float è float()

## Stringhe 👲
usare ' o " non fa differenza, per creare stringhe multilinea si fa con tripli ' o "
in python gli array non esistono, ma le stringhe sono array di char, o meglio collezioni di caratteri
```py
x = 'prova'
print(x[0])
print(x[1])
print(x[2])
print(x[3])
print(x[4])
```
posso anche prendere fino ad un carattere specifico `print(x[:3])`, possiamo anche prendere un range di caratteri `print(x[3:5])` o semplicemente da un carattere in poi `print(x[3:])`.

Esiste un metodo per l'uppercase ed uno per il lowercase
```py
x.upper()
x.lowercase()
```
- il metodo `x.strip()` rimuove gli spazi inutili dalle stringe.
- il metodo `x.replace('o','P')` rimpiazzaerà tutte le o con delle P.

```py
x = 23
prova = 'Ciao sono Luca e sono nato il {}'
print(prova.format(x))
```
il metodo `format()` aggiunge una variabile al contenuto di una stringa, c'è anche possibilità di fare cosi usando degli indici per le varie variabili.
```py
prova = 'Ciao sono Luca e sono nato il {0}, peso {1} e altezza {2}'
print(prova.format(15,65,1.70))
```
Se i valori seguono l'ordine di inserimento, non serve specificare gli indici nelle graffe.

Il carattere di escape per le stringhe è `\`, esempio: `prova = 'Ciao sono Luca e sono \'figo\''`.

## Boolean 🐓
I valori booleani vanno sempre messi con la maiuscola `x=True` o `y=False`.

Con la funzione `bool()` si può verificare lo stato di una variabile, un array vuoto, una stringa vuota o una lista vuota ritornerà sempre `False`.

## Operazioni Aritmetiche :dog:

Non sto a scriverli tutti che senso ha! se servono sono [qui](http://www.helldragon.eu/marcello/galli_python/05-Operatori.html)

## If Statement :cat:
gli If si fanno cosi, è ssenziale indentare, altrimenti non funziona nulla.
```py
if condizione: 
    #codice
else: 
    #codice
```
Ci sono poi diversi comparatori `==`, `!=`, `>=`, `<=`, `<`, `>`.  

L' elseif si scrive `elif`.  

Gli operatori logigi sono `and`, `or` e `not()`.  

Esiste una versione shorthand di if che è `if x > 10 : #singolo statement`.

## Ciclo while 🩰
Velocissimo esempio di un while che cicla per vero
```py
x = ['milano','roma','napoli']
i=0
while i<3:
    print(x[i])
    i+=1
```
`break` permette di uscire prima del verificarsi della condizione, `continue` salta un indice del ciclo ed `else` da un istruzione da fare alla fine del ciclo stesso.

## Ciclo For 🈺
```py
lista_citta = ['milano','roma','napoli']

for citta in lista_citta:
    print(citta)

stringa = 'anguria'
for lettera in stringa:
    print(lettera)

for x in range(6):
    print(x)
```
anche qui posso usare `break`, il `continue` e `else`.

## Collezioni di dati 🗼

