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

## Liste 🦍

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

## Tuple 🦝
Le tuple si creano con le parentesi tonde quidi cosi `x = ('roma','milano','napoli')` anche qui possiamo fare valori mischiati, stringhe, numeri, boolean etc etc...

Le tuple di un solo valore sono stringhe infatti `x = ('roma')` sarà una stringa a meno che non si scriva `x = ('roma',)`. Come per gli altri tipi di dato si stampano con i costruttori, quindi o col metodo `z = tuple(x) print(z)` oppure con i costruttori, quindi `x= tuple(('roma','milano','napoli')) print(x)`.

Si accedono con indici e range come per le liste.
Per verificare se un elemento esiste basta fare un semplice:
```py
if 'venezia' in x:
    print('presente')
else
    print('assente')
```
non è possibile modificare gli elementi delle tuple infatti se faccio:
```py
x = tuple(('roma','milano','napoli'))
x[0]='venezia'
```
mi darà errore e non funzionerà, per aggiungere o modificare una tupla esiste un workaround:
```py
x=('roma','milano','napoli')
y=list(x)
y[0]='venezia'
x=tuple(y)
```
in caso si voglia rimuovere un elemento si fa `y.remove('milano')`.
Esiste la possibilità di scompattare una tupla in diverse variabili:
```py
citta=('roma','milano','napoli')
(x,y,z) = citta
```
caso in qui ci siano più valori che variabili ad esempio `citta = ('roma','milano','napoli','venezia')` è possibile usare una lista all'interno delle variabili disponibili, dichiarandola con un * cosi `(x,y,*z)= citta` a questo punto la z sarà una lista contenente due valori.

Per cicla basta fare `for elemeno in citta: print(elemento)`.
E' possibile unire due tuple con il `+`.
Ci sono diversi metodi utili un paio tra tutti sono `count('milano')` per contare quante volte è presente un elemento nella tupla e `index('milano')` per vedere che indice ha un dato elemento.

## Set 🦓
I set si creano con le graffe quindi `x={'roma','milano','napoli'}` anche i set possono avere valori misti.
Esiste il costruttore che sarà `y = set(('roma','milano','napoli'))`.

I set non sono indicizzati quindi `x[0]` non funziona, è possibile però prendere i dati con il classico `for citta in x: print(citta)` solo che tutte le volte citta avrà un valore random di quelli disponibili.

Nei set non è possibile modificare, ma posso aggiungere e rimuovere con `x.add('venezia')` oppure `x.remove('milano')` o `x.discard('milano')`.
La differenza tra remove e discard è che remove restituisce un errore se non trova l'elemento da cancellare, mentre discard no.

Un altro modo per aggiungere è:
```py
x={'roma','milano','napoli'}
y={'venezia','firenze'}
x.update(y)
```

`x.clear()` cancella il contenuto del set, mentre `del x` cancella completamente il set.
Esiste la possibilità di unire due liste in una terza, con il comando `z = x.union(y)`.
Il comando `x.intersection_update(y)` restituisce solo gli elementi duplicati tra x e y.
Se voglio assegnare l'intersezione uso `z=x.intersection(y)`.
Se uso `x.symmetric_difference_update(y)` ottengo un array senza i duplicati contenuti in y e se voglio fare un assegnazione faccio `z=x.symmetric_difference(y)`.

## Dict
I dictionary sono collezioni di dati ordinate e modificabili ma che non permettono duplicati, sono un po l'equivalente degli oggetti in JavaScript.
Sono formati alla maniera chiave/valore e si creano facendo:
```py
persona = {
    "nome":"Luca",
    "cognome":"Rossi",
    "eta":35
}
```
il fatto che non ammette dublicati è relativo alla sua natura chiavev valore, infatti se provassi ad mettere una nuova chiave e la chiamassi sempre "eta", andrei a sostituire quella precedente.

Per accedere ai dict basta fare: `persona["cognome"]` oppure posso prendere con la get, quindi `persona.get("nome")` o con le chiavi quindi `persona.keys()` cosi ne ottengo una lista che sarà `dict_keys(['nome','cognome','eta'])` se invece facessi `persona.values()` otterrei i valori `dict_values(['Luca','Rossi','35'])` se facessi `persona.items()` otterrei una lista di tuple che rappresenta un oggetto chiave valore `dict_items([('nome','Luca'), ('cognome','Rossi'), ('eta',35)])` in questo caso sono 3 tuple racchiuse in una lista.

Posso controllare se una chiave esiste all'interno del Dict facendo `print("stringa" in persona)` ed otterrò un boolean.

Per modificare gli elementi si usano:
```py
persona["nome"] = "marco"
```
oppure
```py
persona.update({"nome":"Anna"})
```
stesso discorso per aggiungere degli elementi, per rimuovere invece si usano `persona.pop("nome")` oppure `persona.popitem()` per rimuovere l'ultimo item, oppure ancora `persona.clear()` che pulisce completamente il dict e per ultimo `del persona["nome"]` che serve per eliminare la chiave in questione.
Volendo si può anche eliminare l'intero dict facendo `del persona`.

Per ciclare gli elementi uso:
```py
for x in persona:
    print(x)
```
se voglio mandare a schermo le chiavi, se invece voglio stampare i valori farò:
```py
for x in persona:
    print(persona[x])
```
oppure ce possibilità di far riferimento direttamente ad i valori usando `persona.values()` nel for, oppure `persona.keys()` per le chiavi appunto.
Posso scorrerlo generando una tupla facendo:
```py
for x,y in persona.items():
    print(x,y)
```
cosi avrò la risposta direttamente in chiave valore.
Posso copiare un dict usando `x = persona.copy()` se facessi `x = persona` ne farei soltanto una reference, quindi quando cambio il valore di una cambio anche il valore dell'altra.
Un altro modo per copiare è `x = dict(persona)`
I dict possono essera annidati uno dentro l'altro ad esempio:
```py
persona = {
    "nome":"Luca",
    "cognome":"Rossi",
    "eta":35,
    "indirizzo":{
        "citta": "Trieste",
        "cap": "00000",
        "civico": 33
    }
}
```
Per stampare i dict annidati si fa `print(persona["indirizzo"]["civico"])`.

## Funzioni
Le funzioni si definisco con:
```py
def nome_funzione(parametro):
    print("Hello world"+ parametro)
```
per richiamarle si fa `nome_funzione(argomento)`. 

Esistono dei parametri standard che sono:
- Arbitrary Arguments
  si usa quando non si sa quanti argomenti ci sono e si scrive:

  ```py
  def nome_funzione(*opzioni):
      print(opzioni[0])
      print(opzioni[1])
  ```
  e poi richiamo la funzione ad esempio con `nome_funzione("argomento",false)`e lui anche se non ho definito il numero di parametri, funzionerà ugualmente.

- Keyword Arguments
  si usa quando voglio passare un argomento chiave valore (keyword) quindi ad esempio:

  ```py
  def nome_funzione(opzioni,boolean):
      print(opzioni)
      print(boolean)
  ```
  dove chiamerò la funzione `nome_funzione(opzioni="carlo", boolean=True)`.

Si possono usare i parametri di default nella maniera classica, cioè assegnando il parametro da un valore, ad esempio `def nome_funzione(opzioni = "default")`.

```py
def somma(n1,n2):
    somma = n1 + n2
    return somma

x = somma(2,2)
print(x)
```
come in altri linguaggi, se non ho un return non ottendo un valore di ritornod alla funzione.

## Classi ed Oggetti
Le classi si dichiarano:
```py
class Persona:
    nome = "Luca"
    cognome = "Rossi"
```
e possono essere istanziate con `persona1 = Persona()`, i metodi sono sempre nel solito modo, quindi `persona1.nome` e avanti cosi. 
Per far si che le istanze siano diversificate si usa il costruttore in dichiarazione della classe stessa, cosi:
```py
class Persona:
    def __init__(self, nome, cognome):
        self. nome = nome
        self.cognome = cognome
```
Il costruttore è una funzione che viene chiamata automaticamente, ed usa self per identificare se stessa come istanza, assegnando a se i parametri inseriti come argomento.
Per istanziare gli oggetti si fa `persona1 = Persona("Luca","Rossi")` e `persona1 = Persona("Marco","Verdi")`.
Per aggiungere i metodi alla classe si fa:
```py
class Persona:
    def __init__(self, nome, cognome):
        self. nome = nome
        self.cognome = cognome
    def saluta(self):
        print("Ciao! sono "+ self.nome)
```
Chiaramente il metodo è utilizzabile su tutte le istanze della classe e si richiama con `persona1.saluta()`.
Il parametro self identifica l'istanza.

## Ereditarietà
Creare una classe figlia che eredita tutta la struttura della classe madre, ad esempio la classe figlia di `Persona` sarà:
```py
class Insegnante(Persona):
    pass
```
quindi attualmente potrò definire `insegnate1 = Insegnante("Anna","Neri")` che erediterà tutto da `Persona`, quindi posso fare `insegnante1.saluta()`.

Per estendere la classe faccio:
```py
class Insegnante(Persona):
    def __init__(self, nome, cognome, materia):
        super().__init__(nome, cognome)
        self.materia = materia
```
super() serve per definire i campi ereditati da persona.

Posso assegnare i valori alla classe facendo `insegnante1 = Insegnante("Anna","Neri","Matematica")`.
Esiste la possibilità di sovrascrivere i metodi e la roba ereditatà dalla classe madre, per esempio se dichiaro nuovamente il metodo saluta con delle differenze e lo richiamo dopo la dichiarazione, avrò a tutti gli effetti un nuovo metodo saluta che sovrascrive il precedente.
```py
def saluta(self):
    print("buongiorno sono "+ self.nome + " " + self.cognome)
```
questo metodo è della classe ed è stato sovrascritto, quindi ad uso di Insegnante. Se creo un nuovo metodo dentro Insegnante sarà esclusivo di Insegnante e non di Persona.
esempio:
```py
def dai_voto(self):
    print("bravo 8")
```
questo sarà solo di Insegnante.

## Scope delle variabili
Si possono dichiarare variabili globali e non, per esempio all'interno di funzioni.
Se all'interno di una funzione, voglio usare una variabile globale senza averne solo un istanza per quella specifica funzione, dovrò utilizzare la parola `global` davanti. Cosi facendo quando cambierà il valore di quella variabile nella funzione, avrò cambiato anche la funzione globale, diversamente senza l'uso del `global` cambierà il contenuto della variabile solo per quella funzione.

## Moduli
Un modulo è un po come se fosse una libreria e si creano come file `nomemodulo.py` normalissimi, ad esempio:
```py
def saluta(nome):
    print("Ciao "+ nome 
```
per includerlo dentro un programma dovrò fare `import nomemodulo` e poi per richiamarne le funzioni/metodi farò `nomemodulo.saluta(nome)`