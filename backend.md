# Documentazione del Backend

## Indice

1. [Introduzione](#1-introduzione)
2. [Tecnologie Utilizzate](#2-tecnologie-utilizzate)
3. [Architettura del Backend](#3-architettura-del-backend)
4. [Modelli dei Dati](#4-modelli-dei-dati)
5. [API](#5-api)
6. [Autenticazione e Autorizzazione](#6-autenticazione-e-autorizzazione)
7. [Logging e Monitoraggio](#7-logging-e-monitoraggio)
8. [Gestione delle Eccezioni](#8-gestione-delle-eccezioni)
9. [Testing](#9-testing)
10. [Deployment](#10-deployment)
11. [Conclusione](#11-conclusione)

## 1. Introduzione
La documentazione seguente fornisce una panoramica dettagliata del backend dell'applicazione, che gestisce le operazioni relative alla registrazione degli utenti, al login, alla gestione dei clienti e alla comunicazione con il database. Il backend è sviluppato utilizzando il framework ASP.NET Core.

## 2. Tecnologie Utilizzate

Il backend utilizza diverse tecnologie per implementare le sue funzionalità:

- **ASP.NET Core:** È il framework utilizzato per lo sviluppo dell'applicazione web.
- **Entity Framework Core:** È un ORM (Object-Relational Mapping) utilizzato per interagire con il database relazionale.
- **Microsoft SQL Server:** È il database relazionale utilizzato per memorizzare i dati dell'applicazione.
- **DotNetEnv:** È una libreria utilizzata per caricare le variabili d'ambiente da un file .env.

## 3. Architettura del Backend

### Struttura dei File in un Albero di Path

Di seguito la descrizione della struttura delle cartelle e dei file del frontend inclusi componenti:

- **Server**

   _Directory principale del progetto con il resto dei file generati automaticamente in fase di creazione del progetto react ._
  - <a id="App"></a>`App.cs`: _Contiene il gestore dei componenti funzionali e gestisce i reindirizzamenti alle pagine con un sistema di [routing](#5-routing)._

  - **src/**
    
     _Directory principale del codice sorgente._
   - **Server/**
     
       _Contiene tutti gli script cs sviluppati per il server._
     - **Requests/**
     
       _Contiene tutti gli script cs sviluppati per l'elaborazione delle richieste al server._
   - **Database/**
     
       _Contiene tutti gli script cs sviluppati per il database._
        - **Table/**
     
       _Contiene tutti gli script cs sviluppati per il riferimento alle tabelle del database._

## 4. Modelli dei Dati

Il backend utilizza due modelli principali:

### Utente
- **UtenteId:** Identificatore univoco dell'utente.
- **Username:** Nome utente dell'utente.
- **Password:** Password non crittografata dell'utente.
- **HashedPassword:** Password crittografata dell'utente.

### Cliente
- **alias:** Alias univoco del cliente.
- **ragioneSociale:** Ragione sociale del cliente.
- **codiceFiscale:** Codice fiscale del cliente.
- **partitaIVA:** Partita IVA del cliente.
- **pec:** Indirizzo PEC (Posta Elettronica Certificata) del cliente.
- **indirizzo:** Indirizzo del cliente.
- **citta:** Città del cliente.
- **stato:** Stato del cliente.
- **email:** Indirizzo email del cliente.
- **telefono:** Numero di telefono del cliente.
  
## 5. API

Il backend espone diverse API per consentire al client di interagire con le risorse del sistema:

- **/register (POST):** Gestisce la registrazione di un nuovo cliente.
- **/login (POST):** Gestisce il processo di login dell'utente.
- **/list (GET):** Restituisce l'elenco dei clienti memorizzati nel database.

## 6. Autenticazione e Autorizzazione

Il backend implementa un meccanismo di autenticazione basato su username e password. Le credenziali degli utenti vengono verificate nel database e, se corrette, viene restituito un token di accesso per le successive richieste.

## 7. Logging e Monitoraggio

Il backend utilizza i registri per registrare eventi importanti e informazioni di debug. I registri vengono salvati in file di log per consentire il monitoraggio delle attività e la risoluzione dei problemi.

## 8. Gestione delle Eccezioni

Il backend gestisce le eccezioni in modo appropriato, restituendo codici di stato HTTP appropriati e fornendo informazioni dettagliate sugli errori al client. Ciò aiuta a garantire una gestione sicura e robusta delle richieste.

## 9. Testing

Il backend è stato ampiamente testato utilizzando diverse tecniche, tra cui test unitari, test di integrazione e test di accettazione. Ciò garantisce un'alta qualità del software e una maggiore affidabilità del sistema nel suo complesso.

## 10. Deployment

Per il deployment del backend, è necessario seguire una serie di passaggi che includono la compilazione del codice, la creazione dei pacchetti di distribuzione e la configurazione dell'ambiente di produzione. Sono disponibili diverse opzioni di deployment, tra cui il deployment su server fisici, server virtuali o servizi cloud.

## 11. Conclusione

La documentazione fornita offre una panoramica completa del backend dell'applicazione, illustrando le sue funzionalità, la sua architettura e le tecnologie utilizzate. Il backend è progettato per essere robusto, sicuro e scalabile, garantendo un'esperienza utente ottimale e una gestione efficiente dei dati dell'applicazione.
