# Progetto-Programmazione-Java
Si richiedeva di creare una catena di negozi di articoli sportivi di 29 sedi dislocate sul territorio nazionale. Ogni sede è identificata da un campo descrittivo ed ha associato l’elenco dei 100 prodotti in vendita; tale elenco contiene due informazioni: il codice del prodotto ed il numero di pezzi disponibili in giacenza.

PARTE 1:
Progettare e implementare in Java un sistema per la gestione delle vendite della una catena di negozi di articoli sportivi. 
Il programma deve leggere da un file l’elenco dei negozi. Questi possono essere di due tipi: city store oppure super store. 
Ogni negozio possiede tali informazioni: 
tipo del negozio (“city-store” oppure “super-store”), codice (o ID), indirizzo (stringa con spazi). 
Per i city store , sappiamo anche nome e cognome del responsabile,  codice fiscale del responsabile, a capo. 
Per i super store, sappiamo la ragione sociale o la partita iva, numero di casse, superficie del negozio (metri quadri)
Per ogni negozio sappiamo la disponibilità di prodotti. I prodotti sono suddivisi in categorie. Ogni prodotto ha delle sue caratteristiche.

Abbiamo fatto il DB "centro commerciale" con collegate diverse tabelle:
"shop": tabella principale, contiene tutti i 29 negozi con tutte le varie info, con attributi ID, indirizzo e tipo;
"infoc": contiene le info associate ai city-store (attributi: nome, cognome, CF del responsabile),
	 inoltre è presente lo shopID per poter fare il join con la tab principale sull'ID dei negozi;
"infos": contiene le info associate ai super-store(partitaIVA, ID Negozio, superficie del negozio (in metri quadri))

In più, per tutte e 29 le sedi abbiamo inserito un campo descrittivo ed associato l’elenco dei 100 prodotti in vendita; 
tale elenco contiene informazioni/attributi: prezzo, categoria, quantità disponibile in giacenza, 
il codice del prodotto ID univoco per ognuno di essi (che è CHIAVE PRIMARIA).

Usiamo php.myadmin per collegare mySQL con Java e facilitarci il lavoro, quindi scarichiamo XAMPP vado su internet e 
inserisco localhost/dashboard e clicco su phpmyadmin.
Inseriamo tutto il DB, 29 negozi con 100 prodotti in ognuno di essi.

Il programma deve poter mostrare con un sistema di interfaccia grafica l’elenco dei negozi con le seguenti informazioni: 
Tipo, ID, Indirizzo, Superficie, Nome e Cognome Responsabile, Codice Fiscale, Partita Iva.
Per gli attributi che non si applicano ad un negozio (Responsabile e CodiceFiscale per i super store e PartitaIva per i city store).

Si apre una finestra e abbiamo il titolo "BENVENUTI A SPORT CENTER", poi c'è una label/etichetta in cui sono riportati tutti i negozi.
Questi ultimi si differenziano tra loro tramite l'indirizzo (sono delle comuni vie di enna), si è scelta un'unica città per facilitarne l'ambientazione.
Il programma chiede "dove vuoi comprare?", si seleziona la via e appare la finestra principale vera e propria:
La Finestra ci sono 3 metodi di ricerca, metti la spunta in quella che confermi tu, ci sono tutti prodotti, categoria o ricerca manuale cioè personalizzata, 
nel quale ti spunta la barra di ricerca (text field) dove puoi inserire quello che vuoi cercare. Già con 3 lettere ti spuntano i prodotti associati.

I Prodotti sono suddivisi con ID, con numeri da 100 a 200, da 200 a 300, e per categoria: ovviamente suddivisi per sport, calcio, basket, pallavolo, 
tennis, pesca, abbigliamento, attrezzi vari (oggetti tipo per palestra, i pesi), accessori sortivi come polsini e ciclismo (sono 9 in totale.)

Il programma mantiene l’elenco degli scontrini di acquisto memorizzati su un file che ha le seguenti informazioni per ciascuno scontrino: 
Il codice dello scontrino e il codice del negozio 
la data (giorno, mese e anno) 
l’elenco dei prodotti acquistati con la transazione (righe della transazione), con descrizione, quantità venduta, prezzo per unità 
l’elenco dei prodotti termina con un END
