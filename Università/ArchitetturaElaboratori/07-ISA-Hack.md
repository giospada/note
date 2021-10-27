
# ISA del processore Hack


> **Instruction Set Architeture**:(rappresenta l'interfaccia fra l'hardware e il software) sono la serie di istruzioni che il processore esegue

- Memoria dati: RAM – una sequenza di registri a 16 bit che contiene dati
- Memoria istruzioni: ROM – una sequenza di registri a 16 bit che contiene istruzioni da eseguire
- **Registri**: D, A (**registri interni** del processore), M (registro attualmente puntato da A in memoria RAM, **RAM[A]**) 
- Elaborazione: ALU, la conosciamo già
- **PC**: contiene l’indirizzo della prossima istruzione da eseguire (ROM[PC]). Inizialmente PC vale 0 (i programmi da eseguire inizieranno quindi da ROM[0])

**Tipi di Istruzioni**:

## Istruzioni

- **A-instructions:** istruzioni che si limitano a caricare un valore all'interno del registro A 
- **C-instructions:** istruzini che eseguono una computazione prelevando i due operandi A,D,M oppure le costanti 0,1 o -1, e memorizzano il risultato in A,D,M

<details>
<summary>
esempio di C instruction
</summary>

- Le computazioni che si possono eseguire sono: 0 , 1 , -1 , D , A , !D , !A , -D , -A , D+1 , A+1 , D-1 , A-1 , D+A , D-A , A-D , D&A , D|A , M , !M , -M , M+1 , M-1 , D+M , D-M , M-D , D&M , D|M
- D e A sono i registri interni, M coincide con RAM[A] 
</details>

### Sintassi A-Instruction

**A-instruction**: ` @valore //A <- valore`

<details>
<summary>
esempi
</summary>

Caricare una costante ( D = value)
```asm
@17 // A = 17
D = A // D = 17
```

Caricare un valore da RAM ( D = RAM[A])
```asm
@17 // A = 17
D = M // D = RAM[17]
```


 Selezionare una locazione ROM ( PC = A )
```asm
@17   // A = 17
0;JMP // mette 17 in PC, la prossima
       // istruzione sara’ ROM[17]
```
</details>

### Sintassi C-Instruction

**C-Instruction**: `dist= comp;jump` (`dist =` e `jump` sono opzionali)

**comp** = 0 , 1 , -1 , D , A , !D , !A , -D , -A , D+1 , A+1 , D-1, A-1 , D+A , D-A , A-D , D&A , D|A , M , !M , -M ,M+1, M-1 , D+M , D-M , M-D , D&M , D|M
**dest** = M , D , MD , A , AM , AD , AMD, o nullo (in questo caso viene omesso)
**jump** = JGT , JEQ , JGE , JLT , JNE , JLE , JMP, o nullo (omesso)


## Esercizi



> memoria[2]=memoria[1]-memoria[0]-2
```asm
@1
D=M
@0
D=D-M
@2
M=D-A
```

> memoria[2]=memoria[1]-memoria[0]-2

```asm
@1
D=M
@0
D=D&M
@
M=!D
```

> Mettere il valore 1 in tutte le celle di memoria con indirizzo compreso tra RAM[0] e RAM[1] assumendo RAM[1] > RAM[0] > 1

```asm
//essendo che RAM[1]>RAM[0] possiamo scrivere già il primo valore in RAM[0] e possiamo occupare come vogliamo RAM[0] e RAM[1]
(while)
@0
A=M
M=1
@0
MD=M+1
@1
D=M-D
@while
D;JGE
```

> RAM[2] = RAM[1] * (2^RAM[0])  

```asm
//; questo designe supporta RAM[0]=0
//; come prima cosa si scrive RAM[1] in RAM[2]{
@1
D=M
@2
M=D
//; }
(top)
//; decrementa RAM[0] e se è minore di zero va alla fine {
@0
MD=M-1
@end
D;JLE
//; }
//; allora se non è RAM[0] minore di zero fa RAM[2]+=RAM[2] e riparte dal check e decremtnto{
@2
D=M
M=D+M
@top
D;JMP
//;}
(end)
```
> RAM[2] = RAM[1] / RAM[0], RAM[3] = RAM[1] mod RAM[0] 

```asm
//;mettiamo RAM[1] in RAM[3] e settiamo RAM[2]=0
@2
M=0
@1
D=M
@3
M=D
//; checkiamo che RAM[3] sia maggiore di RAM[0] e se è minore andiamo a end
(top)
@end
@3
D=M
@0
D=D-M
@end
D;JLT
// se RAM[3] è maggiore di RAM decrementeiamo RAM[3] di RAM[0] e aggingiamo uno a RAM[2]
@3
M=D
@2
M=M+1
@top
D;JMP
(end)

```

## Simboli nel linguaggio HACK

### Etichette


- **Etichette**: Usate per fare riferimento ad indirizzi della ROM; Dichiarate tramite direttiva `(XXX)` che definisce il simbolo XXX che farà riferimento all’indirizzo di ROM dell’istruzione successiva alla dichiarazione
- **variabili**: Usate per far riferimento ad indirizzi in memoria RAM. Ci sono due tipi di variabili:
    - pre-definite: ad esempio `SCREEN` e `KBD` che fanno riferimento agli indirizzi RAM 16384 e 24576 (indicano rispettivamente l’inizio della memoria per gestire lo schermo e la locazione dove viene inserito il tasto premuto )
    - definite dall’utente: ogni simbolo non predefinito xxx che appare in un programma Hack senza essere dichiarato usando(xxx)viene trattato come una variabile, e gli viene assegnato in automatico un valore (a partire dal valore 16, da 0 a 15 sono usati dalle variabili predefinite R0..R15)
    
