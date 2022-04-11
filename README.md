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

Le collezioni di dati sono `liste`, `tuple`, `set` e `dictionary`
- Liste: collezioni ordinate e modificabili e permettono duplicati.
- Tuple: collezioni ordinate ma immutabili e permettono duplicati.
- Set: collezioni non ordinate e quindi non indicizzate e non permettono duplicati.
- Dictionary: collezioni ordinate e modificabili non permettono duplicati.
Con `ordinato` si intende che la collezione ha ordine ben definito e l'aggiunta di elementi non incide.
Con `indicizzato` si intende che possiamo accedere agli elementi tramite un indice.
`modificabile` significa che si può modificare che è poi il contrario di `immutabile`.
`permette duplicati` significa che possono esserci più elementi con lo stesso valore.

La lista è la cosa più simile all'array per il momento come flessibilità, e si scrivono per esempio
```py
x = ['milano','roma','napoli']
y = ['montagna', 505, False]
z = list(('pianura','mare','montagna')) #costruttore
```
possono accogliere più dati contemporaneamente. Con la funzione `len()` possiamo prendere la lunghezza, quindi il numero di elementi.
Se usiamo `list` che è un costruttore, dobbiamo usare le parentesi tonde.
Nelle liste è possibile accedere agli elementi a ritroso quindi facendo `x[-1]` andiamo a prendere l'ultimo elemento della lista.

Se voglio sostituire un elemento farò `x[0]='firenze'` così facendo al posto di 'milano' avrò 'firenze'.
`append()`aggiunge in coda alla lista, posso inserire con `insert(1,'firenze')` cosi facendo aggiungo al posto 1 la stringa 'firenze'.

Facendo `x.extend(y)` aggiungo al fondo di x tutto il contenuto di y. `x.remove('milano')` serve per rimuovere un elemento specifico, mentre `x.pop()` serve per rimuovere l'ultimo elemento della lista.
Con `del x[0]` posso rimuovere l'elemento specificato e con `x.clear()` svuoto la lista.

La ***list comprension*** è una shorthand e si fa:
```py
lista_citta = ['udine','bologna','napoli']
[print(citta) for citta in lista_citta]
```
Per ordinare una lista si usa `lista_citta.sort()`, caso in cui serva cambiare l'ordinamento si usa `lista_citta.sort(reverse=True)`.
Per copiare una lista è necessario usare il comando `x=lista_citta.copy()`.oppure `x=list(lista_citta)`.

La cosa è che se io penso di copiare una lista in un altra facendo `y=x` sbaglio,  perché in realtà cosi facendo ne sto facendo solo un puntatore e tutto quello che farò a y succederà anche a x. Gli unici modi per non farne un' istanza ma per farne una copia sono quelli citati sopra.

Per unire due liste basta fare `x+y` oppure uso `append()` e verso il contenuto di uno dentro l'altro con un for:
```py
for citta in x:
    y.append(citta)
```
Oppure posso usare `y.extend(x)`. 

## Tuple 

