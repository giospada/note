---
tags: [Computer]
title: Python
created: '2020-04-11T09:29:33.578Z'
modified: '2020-05-30T17:01:52.670Z'
---

# Python

# Virtual Environments

servono per gestire contemporaneamente più progetti con più pacchetti anche di versioni diverse
il virtual environment contiene una serie di directory che contengono python + i pacchetti

## creare un ve

il modulo per creare un enviromnent è vent `pip3 install venv`
per creare un ve nella directory corrente `python3 -m venv nomedelprogetto`
crearà la directory "nomedelprogetto" che conterrà l'interprete di python e stdlib
per attivare il virtual envirorment 
windows:
`nomedelprogetto\Scripts\activate.bat`
unix:
`source nomedelprogetto/bin/activate`

## usare i pacchetti

ora puoi installare tutti i pacchetti che vuoi con pip

## Python
sono contenute nel modulo **re**
> per definire una regual expression è meglio usare una row string (non fanno l'ascape dei caratteri) ex. st=r"prova" #row string

- re.match(pattern,st2)
usata per determinare se c'è un match all'**inizio**, ritorna l'oggetto che rappresenta il match di pattern su st2 se non c'è ritorna none 
- re.search(pattern,st2)
cerca un match in qualunque punto della stringa
- re.findall(pattern,st2)
fa la lista di tutte le substring che matchano
- re.sub(patten,repl,st)
ripiazza tutte i match con repl 
r"\1" #questa string a in sub mette il primo greuppo al posto do \1

# Py Cui

[Documentazione](https://jwlodek.github.io/py_cui-docs/writing/)

un modulo per la grafica da terminale
concetti:
tre modi di operare:
- **overview** mode: serve per scorrere tra i widget e si puo interagire con loro e cliccando `enter` si può andare in focus mode del widget
- **focus** mode: quando si entra si appliaca un diverso key bindings e `Esc` per uscire 
- **popup** mode: non ci sono keybinding predefiniti è accessibile solo il popup e il widget che aveva il focus lo perde

## Widget 

sono pochi 
- Label
- Block Label
- Button
- Scroll Menu
- Checkbox Menux
- Text Block
- text Box

# argparse

È una libreria per gestire i args
per creare un istanza
```python
import argparse
parser = argparse.ArgumentParser()
# add argument
parser.parse_args()
```
per aggungere un arg is usa la funzione parser.add_argument("nome",help="cosa fa questa opzione",type=tipo)




# Human Request

> pip install requests
 import requests

request ha i metodi statici:
- get 
- post
- put
- delete
- head
- options
che supportano vari parametri:
- params : i parametri es `request.get("www.l.com",params={'k':'v'})#www.l.com?k=v` 
- data : i dati in post 
- headers : gli headers

# json

> import json

json.dump : json to string
json.loads : load json
