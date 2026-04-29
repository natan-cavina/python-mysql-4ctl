
## Domande
- Qual è la differenza tra una query scritta direttamente nel codice e una query parametrizzata?
```text

```La query diretta inserisce direttamente i dati mentre la query parametrizzata usa dei simboli e li passa separatamente 

- Qual è il vantaggio di avere funzioni di supporto come esegui_select() ed esegui_dml()?
```text

```Oltre a una gestione degli errori più efficace, select serve per leggere e dml per modificare 

- In che senso i tre file non sono alternative equivalenti, ma evoluzioni progressive dello stesso codice?
```text

```File 1 serve per verificare la presenza della connesione, file 2 serve per dividere il lavoro in funzioni e il file 3 divide in dati in sezioni 


## Esercizi
Esercizi a partire dal **terzo file Python**.

### 1. Selezionare tutti i modelli di prodotto
Scrivere una funzione:

```python
seleziona_tutti_modelli(connection)
```

La funzione deve restituire tutte le righe della tabella `modelli_prodotto`

---
### 2. Visualizzare gli acquisti di un utente a partire dalla sua email

Scrivere una funzione:

```python

seleziona_acquisti_cliente(connection, email)
```

La query deve restituire almeno i seguenti campi:

* nome
* cognome
* email
* id_ordine
* data_ordine
* cod_seriale
* nome del modello
* categoria
* prezzo_vendita_effettivo
---

### 3. Contare quanti prodotti di un modello sono presenti a magazzino
Scrivere una funzione:

```python
conta_prodotti_modello(connection, cod_modello)
```

La funzione deve restituire il numero di prodotti presenti a magazzino associati a un determinato modello, identificato tramite il campo cod_modello.

---

### 4. Inserire un nuovo modello di prodotto
Scrivere una funzione:

```python
inserisci_modello(connection, cod_modello, nome, descrizione, categoria, prezzo_listino)
```
La funzione deve permettere di inserire un nuovo modello di prodotto

---

### 5. Aggiornare il prezzo di listino di un modello
Scrivere una funzione:

```python
aggiorna_prezzo_modello(connection, cod_modello, nuovo_prezzo)
```
La funzione deve permettere di modificare il prezzo di listino di un modello di prodotto, a partire dal suo codice

## Indicazioni operative

Per scegliere la funzione di supporto corretta:
- usare `esegui_select(...)` per le query `SELECT`;
- usare `esegui_dml(...)` per le query `INSERT`, `UPDATE` e `DELETE`.

Testare la funzione all'interno del main() e stampare a video il risultato
