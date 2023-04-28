# Filius-Router
COME COLLEGARE I DISPOSITIVI DI DUE RETI DIVERSE:<br>
Prima cosa selezionare gli host necessari, gli switch e un router centrale<br>




In questo caso specifico abbiamo due notebook,due server che fungono anche da dhcp server,due switch e un router con due schede di rete.
la netmask sarà uguale per tutti i dispositivi ossia: 255.255.255.0 , in questo  caso ci basta un ottetto per gli host.





Inizialmente gli indirizzi ip saranno impostati automaticamente dall’applicazione ma se vogliamo rendere automatico questo processo con un server dhcp bisogna:



Selezionare sul server la voce “dhcp server setup” e poi impostare la porzione di indirizzi ip che possono essere assegnati a un dispositivo. una volta assegnati tutti gli ip anche allo stesso router per fare comunicare i dispositivi di diversi reti bisogna inserire il gateway in tutti i dispositivi. il gateway è l’indirizzo che ci permette di fare uscire un pacchetto da una rete e farlo accedere ad un altra in poche parole è l’indirizzo di uscita e di ingresso ad una rete. il gateway da inserire sarà l’indirizzo ip del router di quella sottorete.
Ora per verificare che le due connessioni funzionino bisogna inserire in tutti e due i notebook una command-line. successivamente si scrive il comando “ipconfig”  per scoprire gli indirizzi ip
con l'istruzione “ping (indirizzo ip)” possiamo verificare se abbiamo perdite di pacchetti lungo la strada e se effettivamente si può comunicare tra computer di diverse reti.
Risposte alle domande:

1-il DHCP è un protocollo di rete che consente di assegnare automaticamente gli indirizzi IP e altre informazioni di configurazione di rete ai dispositivi che si collegano a una rete.  Quando un dispositivo si connette a una rete che utilizza il DHCP, il server DHCP  assegna automaticamente un indirizzo IP al dispositivo, insieme ad altre informazioni come il gateway, il server DNS.
2-inizialmente il tutto non funzionava perchè il pacchetto una volta arrivato al router si fermava se non impostato bene il gateway. oppure una volta arrivato dall’altra rete non riusciva a tornare indietro.
3-Il comando ping utilizza il protocollo ICMP. Quando si esegue il comando ping  il sistema invia una richiesta  al dispositivo di destinazione, che a sua volta invia una risposta  al dispositivo sorgente. In questo modo, il comando ping consente di verificare la connessione di rete tra i due dispositivi, identificando eventuali problemi di connessione o di latenza sulla rete.








