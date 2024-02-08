# Documentazione del Frontend

## Indice

1. [Introduzione](#1-introduzione)
2. [Tecnologie Utilizzate](#2-tecnologie-utilizzate)
3. [Struttura del Progetto](#3-struttura-del-progetto)
4. [Componenti Principali](#4-componenti-principali)
5. [Routing](#5-routing)
6. [Gestione dello Stato](#6-gestione-dello-stato)
7. [Chiamate API](#7-chiamate-api)
8. [Stili](#8-stili)
9. [Testing](#9-testing)
10. [Avvio e Sviluppo Locale](#10-avvio-e-sviluppo-locale)
11. [Distribuzione](#11-distribuzione)
12. [Conclusione](#12-conclusione)

## 1. Introduzione

Il frontend del progetto "Gestionale" offre un interfaccia userfriendly che consente agli utenti preregistrati di gestire la registrazione dei propri clienti e la visualizzazione della lista delle loro anagrafiche:

### Indice

1. [Accesso Utente](#accesso-utente)
2. [Registrazione Clienti](#registrazione-clienti)
3. [Visualizzazione Clienti](#visualizzazione-clienti)

---

### Accesso Utente

![Form di autenticazione dell'utente](autenticaUtente.png)

- L'utente effettua il login al sistema da **account unici preregistrati** 
- Degli account utente le **credenziali sono criptate con SHA3**
- Il sistema garantisce una **gestione sicura per l'apertura delle pagine sensibili** tramite la cache in cui viene memorizzato l'accesso dell'utente tenendolo in memoria in modo che se non è presente allora impedisce l'ingresso in qualsiasi form che non sia quello di autenticazione.

### Registrazione Clienti

![Form di registrazione del cliente](registraCliente.png)

Gli utenti possono registrare i propri clienti nel sistema che li identifica sulla base del loro codice fiscale.

### Visualizzazione Clienti

![Form di visualizzazione dei clienti](visualizzaClienti.png)

Gli utenti possono visualizzare in modo massivo o nel dettaglio le anagrafiche dei propri clienti con le seguenti features:

- Si possono selezionare quali campi rendere visibili e quali oscurare 
- Si possono filtrare i clienti da visualizzare con un sistema di ricerca abilitato su ogni campo

## 2. Tecnologie Utilizzate

### Indice


1. [React Router DOM](#React)
2. [Ant Design ](#ReactDOM)
3. [Axios ](#ReactRouterDOM)
4. [React Toastify](#AntDesign)
5. [React Toastify](#Axios)
6. [Sha3 ](#ReactToastify)
7. [Bootstrap ](#Sha3)
8. [Web Vitals ](#Bootstrap)
9. [Web Vitals ](#WebVitals)
10. [Testing Library](#TestingLibrary)
11. [ESLint ](#ESLint)
12. [TypeScript Types for Bootstrap ](#TypeScriptTypesBootstrap)


---

Il frontend del progetto utilizza una serie di tecnologie per lo sviluppo dell'interfaccia utente e la gestione delle dipendenze. Di seguito sono elencate le principali tecnologie utilizzate:

- <a id="React"></a>**[React](https://reactjs.org/)**: React è il framework JavaScript utilizzato per lo sviluppo dell'interfaccia utente rendendo più semplice la gestione dello stato e il rendering dinamico dei dati.

- <a id="ReactDOM"></a>**[React DOM](https://reactjs.org/docs/react-dom.html)**: React DOM è una libreria utilizzata per il rendering di React all'interno del DOM del browser. Questa libreria è responsabile della manipolazione del DOM e dell'aggiornamento dell'interfaccia utente in base allo stato dell'applicazione.

- <a id="ReactRouterDOM"></a>**[React Router DOM](https://reactrouter.com/en/6.22.0)**: React Router DOM è una libreria utilizzata per gestire il routing dell'applicazione React. Permette di definire rotte all'interno dell'applicazione e di associare componenti React a percorsi specifici.

- <a id="AntDesign"></a>**[Ant Design](https://ant.design/)**: Ant Design è una libreria di componenti UI per React. Offre una vasta gamma di componenti predefiniti pronti per l'uso, che facilitano la creazione di un'interfaccia utente intuitiva e ben progettata.

- <a id="Axios"></a>**[Axios](https://axios-http.com/)**: Axios è una libreria utilizzata per effettuare richieste HTTP dall'applicazione frontend al backend. Fornisce un'interfaccia semplice e intuitiva per l'invio e la gestione delle richieste e delle risposte HTTP.

- <a id="ReactToastify"></a>**[React Toastify](https://github.com/fkhadra/react-toastify)**: React Toastify è una libreria utilizzata per mostrare notifiche toast nell'applicazione React. Queste notifiche sono utili per informare gli utenti su eventi importanti o messaggi di errore senza interrompere l'esperienza utente.

- <a id="Sha3"></a>**[Sha3](https://www.npmjs.com/package/sha3)**: Sha3 è una libreria utilizzata per calcolare l'hash SHA-3 delle stringhe. Questa libreria è utile per la crittografia e la sicurezza dei dati all'interno dell'applicazione.

- <a id="Bootstrap"></a>**[Bootstrap](https://getbootstrap.com/)**: Bootstrap è un framework CSS utilizzato per la progettazione e lo stile dell'interfaccia utente. Offre una serie di componenti UI predefiniti, griglie responsive e stili CSS pronti per l'uso, che semplificano la creazione di un'interfaccia utente accattivante e moderna.

- <a id="WebVitals"></a>**[Web Vitals](https://web.dev/vitals/)**: Web Vitals è una libreria utilizzata per misurare le prestazioni web. Fornisce metriche standard per valutare la velocità di caricamento, la reattività e l'esperienza utente complessiva del sito web.

- <a id="TestingLibrary"></a>**[Testing Library](https://testing-library.com/)**: Testing Library è una libreria utilizzata per i test unitari e di integrazione nell'ambiente di sviluppo React. Fornisce un'API semplice e intuitiva per testare i componenti React e le loro interazioni con l'utente.

- <a id="ESLint"></a>**[ESLint](https://eslint.org/)**: ESLint è uno strumento utilizzato per il linting del codice JavaScript e React. Aiuta a identificare e correggere gli errori nel codice, nonché a mantenere uno stile di codifica uniforme all'interno del progetto.

- <a id="TypeScriptTypesBootstrap"></a>**[TypeScript Types for Bootstrap](https://www.npmjs.com/package/@types/bootstrap)**: Questa libreria fornisce tipi TypeScript per Bootstrap, che consentono di utilizzare Bootstrap in modo più sicuro e affidabile all'interno di un progetto React con TypeScript.

Queste sono le principali tecnologie utilizzate nel frontend del progetto, che contribuiscono a creare un'interfaccia utente funzionale, intuitiva e ben progettata.



## 3. Struttura del Progetto

### Indice

1. [Organizzazione dei Componenti Grafici](#organizzazione-dei-componenti-grafici)
2. [Struttura dei File in un Albero di Path](#struttura-dei-file-in-un-albero-di-path)

---

### Organizzazione dei Componenti Grafici

La struttura del progetto frontend segue un'organizzazione ben definita per garantire una chiara separazione delle responsabilità e una maggiore manutenibilità del codice.

Ogni componente grafico funzionale è organizzato in quattro file distinti:

1. **View**: Questo file contiene solo la parte grafica del componente, ovvero la struttura HTML e la presentazione CSS. La View non ha alcuna logica di business o gestione dello stato.

2. **Manager**: Il file Manager contiene la logica di business del componente, inclusa l'elaborazione dei dati e la gestione dello stato. Qui vengono definiti i metodi e gli attributi necessari per il funzionamento del componente.

3. **Main**: Questo file istanzia il Manager e la View del componente, passando come parametri a View i metodi e gli attributi strettamente necessari all'interfaccia grafica definiti nel Manager.

4. **App**: Infine, il file App istanzia il Main del componente, garantendo una maggiore pulizia del codice e facilitando la gestione dei componenti all'interno dell'applicazione.

La scelta di questa struttura organizzativa dei componenti grafici è motivata dalla separazione dei compiti e dalla chiarezza del codice. Separando la parte grafica dalla logica di business, è più semplice comprendere e mantenere ciascun componente in modo isolato. Inoltre, questa organizzazione facilita il riutilizzo dei componenti e favorisce una migliore scalabilità dell'applicazione nel tempo.

### Struttura dei File in un Albero di Path

Di seguito la descrizione della struttura delle cartelle e dei file del frontend inclusi componenti:

- **Client**

   _Directory principale del progetto con il resto dei file generati automaticamente in fase di creazione del progetto react ._
  - **src/**
    
     _Directory principale del codice sorgente._
    - **script/**

       _Contiene tutti gli script js sviluppati._
      - **extra/**

         _Contiene gli script secondari utilizzati nei file principali._
        - **design/**

           _Contiene gli script dei componenti grafici secondari riutilizzati in più schermate._
          - **FloatButton/**

             _Contiene gli script per il funzionamento del menu di navigazione del sito._
            - `FloatButtonApp.js`: _Script che istanzia ed usa il main al fine di migliorare la visibilità e la coerenza del codice._
            - `FloatButtonMain.js`: _Script che istanzia ed usa il manager e la view unendo la parte logica e quella grafica del componente cosi da garantirne il funzionamento ed una corretta separazione dei compiti mantenendo la parte logica e quella grafica separate._
            - `FloatButtonManager.js`: _Script che gestisce la logica e l'elaborazione dei dati della view._
            - `FloatButtonView.js`: _Script che contiene la vista del componente e ne gestisce solo la grafica._
        - **utility/**

           _Contiene gli script che sono i gestori per l'elaborazione dei dati e vengono riutilizzati nei componenti principali._
          - `RequestManager.js`: _Componente per la gestione delle richieste GET e POST dal frontend al server._
          - `WindowLoader.js`: _Gestisce l'animazione di caricamento delle pagine web._

      - **features/**

         _Contiene i componenti funzionali del progetto._
        - **autenticaCliente/**
          
             _Contiene gli script per il form di autenticazione dell'utente._
            - <a id="AutenticaClienteApp"></a>`AutenticaClienteApp.js`: _Script che istanzia ed usa il main al fine di migliorare la visibilità e la coerenza del codice._
            - `AutenticaClienteMain.js`: _Script che istanzia ed usa il manager e la view unendo la parte logica e quella grafica del componente cosi da garantirne il funzionamento ed una corretta separazione dei compiti mantenendo la parte logica e quella grafica separate._
            - `AutenticaClienteManager.js`: _Script che gestisce la logica e l'elaborazione dei dati della view._
            - `AutenticaClienteView.js`: _Script che contiene la vista del componente e ne gestisce solo la grafica._
              
        - **registraCliente/**
        
             _Contiene gli script per il form di registrazione del cliente._
            - <a id="RegistraClienteApp"></a>`RegistraClienteApp.js`: _Script che istanzia ed usa il main al fine di migliorare la visibilità e la coerenza del codice._
            - `RegistraClienteMain.js`: _Script che istanzia ed usa il manager e la view unendo la parte logica e quella grafica del componente cosi da garantirne il funzionamento ed una corretta separazione dei compiti mantenendo la parte logica e quella grafica separate._
            - `RegistraClienteManager.js`: _Script che gestisce la logica e l'elaborazione dei dati della view._
            - `RegistraClienteView.js`: _Script che contiene la vista del componente e ne gestisce solo la grafica._
              
        - **visualizzaClienti/**
          
             _Contiene gli script per il form di visualizzazione delle anagrafiche dei clienti._
            - <a id="VisualizzaClientiApp"></a>`VisualizzaClientiApp.js`: _Script che istanzia ed usa il main al fine di migliorare la visibilità e la coerenza del codice._
            - `VisualizzaClientiMain.js`: _Script che istanzia ed usa il manager e la view unendo la parte logica e quella grafica del componente cosi da garantirne il funzionamento ed una corretta separazione dei compiti mantenendo la parte logica e quella grafica separate._
            - `VisualizzaClientiManager.js`: _Script che gestisce la logica e l'elaborazione dei dati della view._
            - `VisualizzaClientiView.js`: _Script che contiene la vista del componente e ne gestisce solo la grafica._
    
      - **UI/**

         _Contiene il gestore dei componenti funzionali e gestisce i reindirizzamenti alle pagine con un sistema di [routing](#5-routing)._
         - `UIApp.js`: _Script che istanzia ed usa il main al fine di migliorare la visibilità e la coerenza del codice._
         - `UIMain.js`: _Script che istanzia ed usa il manager e la view unendo la parte logica e quella grafica del componente cosi da garantirne il funzionamento ed una corretta separazione dei compiti mantenendo la parte logica e quella grafica separate._
         - `UIManager.js`: _Script che gestisce la logica e l'elaborazione dei dati della view._
         - <a id="UIView"></a>`UIView.js`: _Script che contiene la vista del componente e ne gestisce solo la grafica, qui è organizzato il sistema di [routing](#5-routing)._

    - **style/**

       _Contiene tutti i fogli di stile css sviluppati._
       - `global.css`: _Foglio di stile con gli stili globali per tutto il progetto._
      - `autenticaUtente.css`: _Foglio di stile con gli stili relativi alla schermata di autenticazione dell'utente._
      - `registraCliente.css`: _Foglio di stile con gli stili relativi alla schermata di registrazione del cliente._
      - `visualizzaClienti.css`: _Foglio di stile con gli stili relativi alla schermata di visualizzazione dei clienti._
      - `menuLaterale.css`: _Foglio di stile con gli stili relativi al componente del menu di navigazione._



## 4. Componenti Principali
Elenco e descrizione dei componenti principali utilizzati nel frontend, con eventuali screenshot e descrizione.

| Nome Form                                | Descrizione Form                                                                                                                                                                                                                                                                                                                                                                                  | Immagine Form                                |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Form di autenticazione utente            | <ul><li>L'utente effettua il login al sistema da <strong>account unici preregistrati</strong></li><li>Degli account utente le <strong>credenziali sono criptate con SHA3</strong></li><li>Il sistema garantisce una <strong>gestione sicura per l'apertura delle pagine sensibili</strong> tramite la cache in cui viene memorizzato l'accesso dell'utente tenendolo in memoria in modo che se non è presente allora impedisce l'ingresso in qualsiasi form che non sia quello di autenticazione.</li></ul> | ![Form di autenticazione utente](autenticaUtente.png) |
| Form di registrazione cliente           | Gli utenti possono registrare i propri clienti nel sistema che li identifica sulla base del loro codice fiscale.                                                                                                                                                                                                                                                               | ![Form di registrazione cliente](registraCliente.png) |
| Form di visualizzazione anagrafiche cliente | Gli utenti possono visualizzare in modo massivo o nel dettaglio le anagrafiche dei propri clienti con le seguenti features:<ul><li>Si possono selezionare quali campi rendere visibili e quali oscurare</li><li>Si possono filtrare i clienti da visualizzare con un sistema di ricerca abilitato su ogni campo</li></ul>                                                                                                                                                        | ![Form di visualizzazione anagrafiche cliente](visualizzaClienti.png) |

## 5. Routing

### Indice

1. [Spiegazione del sistema di routing](#spiegazione-del-sistema-di-routing)
2. [Descrizione delle rotte principali dell'applicazione](#descrizione-delle-rotte-principali-dellapplicazione)
3. [Routing Sicuro e Reindirizzamento](#routing-sicuro-e-reindirizzamento)

---

### Spiegazione del sistema di routing

Nel progetto si ha utilizzato **React Router per gestire il routing** dell'applicazione.

I **componenti importati** da React Router sono i seguenti:

- `BrowserRouter`: Questo componente fornisce il contesto del routing per i componenti figlio. È avvolto intorno all'intera struttura delle rotte.
- `Routes`: Questo componente contiene una serie di `Route` componenti che definiscono le rotte dell'applicazione.
- `Route`: Questo componente definisce una singola rotta dell'applicazione, associando un percorso URL a un componente React.

Il sistema di routing è configurato all'interno del componente `UIView` [(vedi)](#UIView). Le rotte principali dell'applicazione sono definite come seguenti:

### Descrizione delle rotte principali dell'applicazione

- **Rotte Principali**:
  - La rotta principale (`"/"`) è associata al componente `autenticaUtenteApp` [(vedi)](#AutenticaUtenteApp). Questa rotta gestisce l'autenticazione dell'utente e viene visualizzata come pagina di accesso.
  - La rotta `"/registraCliente"` è associata al componente `registraClienteApp` [(vedi)](#RegistraClienteApp). Questa rotta gestisce il processo di registrazione del cliente.
  - La rotta `"/visualizzaClienti"` è associata al componente `visualizzaClientiApp` [(vedi)](#VisualizzaClientiApp). Questa rotta gestisce la visualizzazione dei clienti registrati.

### Routing Sicuro e Reindirizzamento

Il sistema implementa il routing sicuro per garantire che l'utente venga reindirizzato alle pagine appropriate solo dopo l'autenticazione. Questo viene fatto salvando nella cache i dati di accesso dell'utente. Se un utente prova ad accedere direttamente a una pagina senza essere autenticato, viene reindirizzato automaticamente alla pagina di accesso.




## 6. Gestione dello Stato

Per la gestione dello stato dell'applicazione, sono stati principalmente utilizzati gli Hooks di React, in particolare `useState`, `useEffect`, `useRef`, e `useMemo`, ciascuno con un preciso scopo e utilizzo all'interno dei componenti.

### Indice

1. [Utilizzo degli Hooks](#utilizzo-degli-hooks)
2. [Motivazioni di Utilizzo](#motivazioni-di-utilizzo)

---

### Utilizzo degli Hooks

- **useState**: Questo Hook è stato utilizzato per definire e gestire lo stato locale all'interno dei componenti funzionali. Ad esempio, è stato utilizzato `useState` per gestire lo stato di variabili dinamiche come il testo di un input, lo stato di un modale, o il conteggio di un contatore.

- **useEffect**: È stato impiegato `useEffect` per gestire gli effetti collaterali nelle componenti funzionali, come le richieste HTTP, la sottoscrizione agli eventi, o la gestione del ciclo di vita del componente. Questo Hook è utile per eseguire codice aggiuntivo dopo il rendering del componente o per ripulire le risorse quando il componente viene smontato.

- **useRef**: È stato utilizzato `useRef` per mantenere riferimenti a elementi DOM o valori persistenti tra i render dei componenti. Questo Hook è stato prezioso quando è stato necessario manipolare direttamente elementi DOM o mantenere riferimenti a valori che non devono essere re-inizializzati ad ogni renderizzazione del componente.

- **useMemo**: È stato fatto uso di `useMemo` per memorizzare valori calcolati all'interno dei componenti funzionali. Questo Hook è stato utile quando è stato necessario calcolare valori derivati da altri stati o proprietà del componente, evitando il ricalcolo ad ogni renderizzazione a meno che le dipendenze non cambino.

### Motivazioni di Utilizzo

L'adozione di questi Hooks ha consentito di gestire in modo efficiente lo stato all'interno dei singoli componenti, senza dover ricorrere a librerie esterne come Redux. La scelta di utilizzare Hooks di React anziché librerie esterne è stata guidata dalla semplicità, dalla leggibilità e dalla scalabilità del codice.

Utilizzare Hooks direttamente all'interno dei componenti ha semplificato la gestione dello stato, evitando la complessità aggiuntiva introdotta da librerie esterne. Questo approccio è stato particolarmente adatto per la gestione dello stato di piccoli componenti UI o di logica di visualizzazione semplice, mantenendo allo stesso tempo un codice chiaro e facilmente manutenibile.


## 7. Chiamate API
Spiegazione di come vengono effettuate le chiamate API dal frontend, con esempi di utilizzo di librerie come Axios.

## 8. Stili
Descrizione di come vengono gestiti gli stili nel frontend, ad esempio tramite CSS, CSS-in-JS, o librerie come Styled Components.

## 9. Testing
Breve panoramica dei test effettuati sul frontend, inclusi test unitari, di integrazione e di utilizzo di strumenti come Jest e React Testing Library.

## 10. Avvio e Sviluppo Locale
Istruzioni su come avviare il frontend in modalità di sviluppo locale, con eventuali prerequisiti e comandi necessari.

## 11. Distribuzione
Breve guida su come distribuire il frontend in un ambiente di produzione, con eventuali configurazioni o passaggi aggiuntivi necessari.

## 12. Conclusione
Ringraziamenti, riferimenti aggiuntivi e informazioni per il supporto o la collaborazione futura.

