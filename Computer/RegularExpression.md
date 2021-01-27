---
tags: [Computer]
title: RegularExpression
created: '2020-04-01T10:19:59.139Z'
modified: '2020-05-30T17:01:46.861Z'
---

# RegularExpression

**principalmente usate per**:
- verificare che delle stringhe rispettino dei pattern
- sobstituire alle stringhe
## General
**Metacaratteri**
sono caratteri che hanno coportamenti particolari nelle re:
- `.`: matcha un qulsiasi altro carattere
- `^`: matcha l'inizio della stringa( con m flag l'inizio delle righe)
- `$`: matcha la fine della stringa( con m flag la fine delle righe)
- `*`: zero o più ripetizioni della cosa precedente (prova sempre a matcharne il più possibile)
- `+`: una ripeticione  della cosa precedente
- `?`: zero o una repietizione della cosa precedente
- `{x,y}`: tra le x e le y ripetizioni della cosa precedente (se il primo numero manca è 0)(se il secondo numero manca è infinito)
- `\d`:i numeri(la versione maiuscola fa l'opposto)
- `\s`:gli spazi (la versione maiuscola fa l'opposto)
- `\w`:una parola (la versione maiuscola fa l'opposto)
- `()`: qullo che è mecchato dentro le () diventa un gruppo è puo essere richamato in vari modi  
- `[]`: le parentesi graffe matchano un qualsiasi carattere che all'interno di esse (si possono defninire un insieme di caratteri con "-" es 0-9)
- `[^]` :inverte il match 

 





