---
tags: [Compiti]
title: Info
created: '2020-05-28T14:15:38.170Z'
modified: '2020-05-28T14:15:50.695Z'
---

# Info

## HTML
è un sistema LIFI (last in first out) 
attributi:
id: marchio che dovrebbe essere univoco
class: marchio che si da a più tag se ne possono dichiarare multipli

Ereditarietà: i tag contenuti (in assenza di attributi specifici) ereditano le caratteristiche indicate per i tag contenitori.
Polimorfismo: lo stesso attributo può comportarsi in modo diverso a seconda del tag in cui è inserito.
Logica LIFO: se lo stesso attributo è presente con valori diversi in più tag, in ciascuno prevale quello più vicino cioè l’ultimo dichiarato.

tags:
- html:tag iniziale
- head:tag contenente le informazioni
- title: titolo 
- style: contine i fogli di stile css
- link: serve per collegare ad un foglio di stile / un foglio contenente uno script
- body: contiene gli elementi visualizzabili
- p: paragrafo diplay block (va a capo)
- br: line break
- pre preformatted text
- i: italico
- b: blod
- del: linea sopra
- ins: linea sotto
- sub: pedice
- sup: apice
- a: serve per creare un link
- img : serve per mostrare un immagine
- table: tabella
- tr: riga
- th: titolo
- td cella

## CSS
per assegnare a un tag nel css scrivere il nome del tag prima
per assegnare a un id mettere \# e poi l'id
per assegnare a una classe mettere il . e poi il nome della classe 
(le assegnazioni possono essere concatenate

definizione del css:
inline: in riga utilizzando l'attributo style
internal: di solito messo nell'head sotto il tag style viene definito il css
external: sempre nell'head utilizzando il tab link

definizione colori:
rgb(rosso,verde,blue) si sostituiscono con valori da 0 a 255
\#rrggbb si sostituiscono con valori esadecimali
attributi:
background-color: colore di background
color:colore del testo
border-color: colore del contorno
font-size: definisce la larghezza del testo
font-family: famiglia del testo
border: il bordo
padding: il padding attoeno 
margin:il margine



## Interrogazione


una **relazione** è un sotto insieme di tutte le n-uple che si possono costituire da n insiemi<br>
il **grado** è il numero numero di colonne <br>
un **attributo** è una colonna<br>
un **dominio** sono i valori che un attributo può avere<br>
la **carinalità** sono le n-uple che compongono la tabella<br>


**chiave** è un attributo (o un insieme)che identifica univocamente le n-uple all'interno di una relazione

**chiave esterna** è un attributo (o un insieme)che identifica univocamente una riga di una altra tabella 


Operazioni relazionali:
- selezione:selezione u-uple della relazione di partenza che soddisfano una condizione:
    - grado uguale alla relazione di partenza
    - cardinalità è minore uguale alla cardinalità della tabella di partenza
- proiezione: genera una relazione estraendo solo alcune colone dalla tabella iniziale.:
    - grado minore o uguale alla relazione di partenza
    - caridnalità minore uguale(perchè può essere che eliminando una colonna possono diminuire essendo che non ci possono essere n-uple uguali nel modello relazionale)
- congiunzione: combina due relazioni generando una nuova relazione le cui righe contengono gli attributi abbinati attraverso una determinata proprietà:
    - grado è la somma dei gradi delle relazioni
    - la cardinalità è minore uguale al prodotto al numero di righe

**normalizzazione**

serve sopratutto per prevenire le anomalie conseguite dalla **ridondanza**:
- anomalia di aggiornamento 
- anomalia di cancellazione
- anomalia d'inserimento

termini:<br>
**chiave candidata**: è un attributo (o più) che identificano una n-upla<br>
**chiave primaria** è la chiave candita scelta dal progettista per identificare in modo univoco una riga<br>
**chiave alternativa**: chiave candidata diversa dalla primaria<br>
**attributo non chiave** è un attributo che non fa parte della chiave<br>

**dipendenza funzionale** quando un valore o un insieme  di attributi determino un altro attributo<br>
**dipendenza transitiva** quando X detrmina Y che a sua volta determina Z allora X determina Z<br>

**prima forma normale**:
- gli attributi rappresentano le informazioni elemantari
- righe univoche
- tutte contengono lo stesso numero di colonne
- tutti i valori di una colonna appartengono ad un dominio

**seconda forma normale** deve essere in prima forma normale e tutti gli attribti non chiave dipendono dall'intera chiae , cioè non possiede attributi che dipendono da soltanto una parte della chiave

**terza forma normale** deve esere in seconda tutti gli attributi non-chiave dipendono direttamente
dalla chiave(la terza forma elimia la dipendenza transitiva)


integrità referenziale: insieme delle regole del modello che garantiscono l'integrità deidati



erp :software per gestire in modo integrato le risorse aziendali (enterprise resource planning)

vantaggi:
- semplicità d'uso
- la comunicazioni tra i soggetti (l'intergrazione dei dati)
- non dublica i dati
- si sviluppano intorno a dei moduli per gestire le diverse aree funzionali
- e hanno un sistema di gestione di diritti d'accesso

sistemi disgunti:
- è più personalizzabile


