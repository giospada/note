
# Network


modelli di canale
- simplex monodirezionali
- half-duplex: entrambe le direzione ma non contemporaneamente
- full-duplex: contemporaneamente

destinazione:
- Unicast:sinsolo destinatario
- Broadcast: tutti i frame
- Multicast: alcuni frame

comunicazione livello link:
- punto punto: unicast
- multi-accesso: che veicolano un messaggio a tutti i destinatari

LAN: un insime di terminali che comunicano tra di loro in modalità boradcast

serve metodo trasmissivo multi accesso e con un protocollo opportuno
possiamo dare ad ogni dispositivo un indirizzo creare comunicazione unicast broadcas
multicast

WAN: connessioni punto punto (fibra ottica per esempio)

internet è la interconnessione di reti locali e geografiche

le comunicazini utilizzano questi canali è standardizzato con il modello ISO
hanno standardizzato l'architettura 

ISO crea 7 livelli( dal fisico fino al'applicazione)

TCP/IP: è a strati ma in 4 (application,trasport,network,lik)

i protocolli ricevono dei payload dal livello rete che imbustano in una frame in cui
viene aggiuntauna una Header

quindi il paccetto ha il il messggio più tutte le intestazioni

Ethernet connessione senza riscontro:
il servizio è inaffidabilie non ha nessuna garanzie dell'effettiva consegna dei dati

## Ethernet

indirizzo 6 byte che definisce il computer all'interno della rete

il tuo computer riceve se :

- broadcast
- unicast
- multicast

il tuo computer è messo in modalità promisqua:riceve tutti i pacchetti della rete


**dispositivi ethernet**

repeter riceve e ripete i bit

Hub ripetitore che riceve su più interfacce

Bridge: lavora a livello due quindi lavora con l'indirizzo MAC
I Bridge creano la loro tabello attraverso l'autoapprendimento
quando arriva un frame si memorizza chi lo manda e da dove lo manda


switch la differenza dal bridge ha la possibilità di realizzarare la
comunicazioni in hardware e quindi avere più comunicazioni contemporaneamente


un router ha due interfacce che lo collegano a più LAN o WAN

TCP/IP assegna degli indirizzi ip i bit che lo compongono sono divisi in due parti
la prima denomina la network comune alla stessa LAN mentre la seconda determina l'hosto all'interno della lan

la maschera fa capire quanti bit sono per la rete e quanti per gli host

per fare il broad cast si usa come indirizzo la parte host più tutti gli indirizzi host
a 255

indirizzi a suso privato
- classe a 1 indirizzo 10.x.x.x
- classe b 16 indirizzi 172.16.x.x
- classe c 255 indirizzi 192.168.0.x

subnetting conesnte di suddividere i bit della parte host

CIDR classless inter domain routing 

con le classi a,b,c c'era uno spreco di indirizzi
così viene introdotto il CIDR così hanno potuto frammentare le reti in base alle 
richieste



routing e router

tabella di routing: ogni oggetto nella rete ip ha un indirizzo ip e ha una singola 
tabella di routing (`ip route` linux)


con l'ip forwrding possiamo far diventare il nostro computer un router 
gestendo tutti i pacchetti

nat tre host connessi e un host centrale fa da router 

nat è un dispositivo che permette a indirizzi privati di comunicare con degli indirizzi 
pubblici





