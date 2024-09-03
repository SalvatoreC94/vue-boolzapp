# vue-boolzapp

## Descrizione
**vue-boolzapp** è un'applicazione che replica una semplice chat simile a WhatsApp. L'obiettivo del progetto è esercitarsi con Vue.js, implementando varie funzionalità come la visualizzazione dinamica dei messaggi e dei contatti, l'invio di messaggi e la ricerca di utenti.

## Milestone

### Milestone 1: Struttura Grafica e Messaggi di Base
- **Replica della Grafica**: Implementare la grafica della chat con messaggi inviati dall'utente (verdi) e dall'interlocutore (bianchi), utilizzando classi CSS diverse per i due tipi di messaggi.
- **Visualizzazione Dinamica della Lista Contatti**: Utilizzare la direttiva `v-for` per visualizzare dinamicamente nome e immagine di ogni contatto nella lista.

### Milestone 2: Visualizzazione dei Messaggi
- **Visualizzazione Dinamica dei Messaggi**: Utilizzare la direttiva `v-for` per mostrare tutti i messaggi relativi al contatto attivo all'interno del pannello della conversazione.
- **Clic sul Contatto**: Implementare la funzionalità per cui, cliccando su un contatto, viene mostrata la relativa conversazione.

### Milestone 3: Aggiunta e Risposta ai Messaggi
- **Aggiunta di un Messaggio**: Permettere all'utente di scrivere un messaggio nella parte bassa della chat e aggiungerlo al thread premendo "Enter". Il messaggio verrà visualizzato in verde.
- **Risposta Automatica dell'Interlocutore**: Implementare una risposta automatica "ok" da parte dell'interlocutore, che apparirà dopo 1 secondo dall'invio di un messaggio da parte dell'utente.

### Milestone 4: Ricerca Utenti
- **Ricerca Utenti**: Implementare una funzionalità di ricerca che, scrivendo nell'input a sinistra, visualizza solo i contatti il cui nome contiene le lettere inserite (es. scrivendo "mar" rimangono visibili solo Marco e Martina).

### Milestone 5 (Opzionale): Funzionalità Aggiuntive
- **Cancella Messaggio**: Implementare una funzionalità per cancellare un messaggio cliccando su di esso, che farà apparire un menu a tendina con l'opzione per eliminare il messaggio selezionato.
- **Visualizzazione Ora e Ultimo Messaggio**: Mostrare l'ora dell'ultimo messaggio inviato/ricevuto nella lista dei contatti.

## Consigli Utili
- **Scrollbar Verticali**: Le scrollbar verticali possono essere trascurate sia nel pannello dei messaggi che nella lista dei contatti.
- **Pulsanti e Icone**: Non è necessario implementare la funzionalità dei pulsanti e delle icone (eccetto l'invio del messaggio).
- **Gestione delle Date**: Può essere utile utilizzare la libreria Luxon per gestire le date.
  
## Struttura dell'Array dei Contatti
Esempio di come potrebbe essere strutturato l'array dei contatti:

```javascript
contacts: [
    {
        name: 'Michele',
        avatar: './img/avatar_1.png',
        visible: true,
        messages: [
            {
                date: '10/01/2020 15:30:55',
                message: 'Hai portato a spasso il cane?',
                status: 'sent'
            },
            {
                date: '10/01/2020 15:50:00',
                message: 'Ricordati di stendere i panni',
                status: 'sent'
            },
            {
                date: '10/01/2020 16:15:22',
                message: 'Tutto fatto!',
                status: 'received'
            }
        ],
    },
    // Altri contatti...
]
