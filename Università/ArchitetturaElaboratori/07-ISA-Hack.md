
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


<details>
<summary>
Esercizi
</summary>



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

</details>