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
  - `App.cs`: _Contiene il gestore del server_

  - **src/**
    
     _Directory principale del codice sorgente._
      - **Server/**
        
          _Contiene tutti gli script cs sviluppati per il server._
          - `Server.cs`: _Contiene il server._

        - **Requests/**
        
          _Contiene tutti gli script cs sviluppati per l'elaborazione delle richieste al server._
          - `ListHandler.cs`: _Contiene il gestore della richiesta relativa alla visualizzazione delle anagrafiche dei clienti._
          - `Loginhandler.cs`: _Contiene il gestore della richiesta relativa all'autenticazione dell'utente._
          - `RegisterHandler.cs`: _Contiene il gestore della richiesta relativa alla registrazione di un nuovo cliente._
      - **Database/**

          _Contiene tutti gli script cs sviluppati per il database._
          - `Database.cs`: _Contiene il database._

           - **Table/**
      
             _Contiene tutti gli script cs sviluppati per il riferimento alle tabelle del database._
             - `Utente.cs`: _Contiene la tabella utente._
             - `Cliente.cs`: _Contiene la tabella cliente._


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

Breve panoramica dei test unitari e di integrazione effettuati sul frontend 

### Indice

1. [Test Effettuati](#test-effettuati)
2. [Benefici dei Test](#benefici-dei-test)
3. [Esito dei Test](#esito-dei-test)

---


### Test Effettuati

- **Test Unitari**: Sono stati sviluppati test unitari per verificare il corretto funzionamento dei singoli componenti e delle funzioni utilizzate nell'applicazione. Questi test hanno consentito di individuare eventuali bug e garantire che ogni componente si comporti come previsto in condizioni specifiche.

- **Test di Integrazione**: Sono stati eseguiti test di integrazione per verificare l'interazione tra diversi componenti e le varie parti dell'applicazione. Questi test sono stati utili per assicurare che le varie parti dell'applicazione funzionino correttamente insieme e che non vi siano problemi di compatibilità o conflitti tra di esse.

> [!NOTE]
> - La complessità del progetto non ha richiesto l'utilizzo di framework esterni per il testing come Jest o React Testing Library.
> 
> - La [struttura del progetto](#3-struttura-del-progetto) in termini di organizzazione del codice ha facilitato la manutenibilità a livello di test, consentendo di scrivere e mantenere i test in modo efficiente.
   


### Benefici dei Test

- **Miglioramento della Qualità**: I test hanno contribuito a migliorare la qualità complessiva dell'applicazione, individuando e risolvendo bug e problemi prima che possano influenzare gli utenti finali.

- **Riduzione dei Rischi**: Effettuando test regolari, si è ridotto il rischio di errori e malfunzionamenti nell'applicazione, garantendo un'esperienza utente più fluida e priva di problemi.

- **Aumento della Fiducia**: L'utilizzo di test ha aumentato la fiducia nello sviluppo e nel rilascio dell'applicazione, fornendo una valida garanzia che ogni cambiamento o aggiornamento non provochi regressioni o problemi imprevisti.



### Esito dei Test

Tutti i test finali hanno dato esito positivo, confermando la stabilità della build.


![Stato del Progetto](https://img.shields.io/badge/Stato-Stabile-brightgreen)

![Versione](https://img.shields.io/badge/Versione-1.0-blue)

![Manutenzione](https://img.shields.io/badge/Manutenzione-Attiva-green)

## 10. Deployment

Per il deployment del backend, è necessario seguire una serie di passaggi che includono la compilazione del codice, la creazione dei pacchetti di distribuzione e la configurazione dell'ambiente di produzione. Sono disponibili diverse opzioni di deployment, tra cui il deployment su server fisici, server virtuali o servizi cloud.

## 11. Conclusione

La documentazione fornita offre una panoramica completa del backend dell'applicazione, illustrando le sue funzionalità, la sua architettura e le tecnologie utilizzate. Il backend è progettato per essere robusto, sicuro e scalabile, garantendo un'esperienza utente ottimale e una gestione efficiente dei dati dell'applicazione.

### Indice

1. [Ringraziamenti](#ringraziamenti)
2. [Riferimenti aggiuntivi](#riferimenti-aggiuntivi)
3. [Supporto e collaborazione futura](#supporto-e-collaborazione-futura)

---

### Ringraziamenti

Desideriamo ringraziare il team di sviluppo per il loro impegno e dedizione nel portare avanti questo progetto. 

| Ruolo          | Nome            | Email                        | GitHub                                           |
|----------------|-----------------|------------------------------|-----------------------------------------------|
| Gestore Backend| Reda Karimi     | redakarimi76@gmail.com      | [redakarimi](https://github.com/redakarimi)  |
| Gestore Frontend| Vittorio Piotti| vittoriopiotti.vp@gmail.com | [vittoriopiotti](https://github.com/vittoriopiotti) |


### Riferimenti aggiuntivi

Per contribuire al progetto, ricevere informazioni o segnalare bug fare riferimento ai seguenti link:


| Issues Repository GitHub                        | Email Aziendale                  | Email Privata                  |
|------------------------------------------|---------------------------------|--------------------------------|
| [Repository](https://github.com/pub) | gestionale.dev@gmail.com                | redakarimi76@gmail.com                        |
|  |                |                           vittoriopiotti.vp@gmail.com     |

![Contatto](https://img.shields.io/badge/Contatto-Email%20%7C%20GitHub-blue)


### Supporto e collaborazione futura

Siamo aperti a nuove collaborazioni e siamo disponibili a offrire supporto per l'implementazione del progetto in altri contesti o per eventuali miglioramenti futuri. Non esitate a contattarci per ulteriori dettagli o proposte di collaborazione.

Grazie ancora a tutti coloro che hanno reso possibile il successo di questo progetto!

![Supporto](https://img.shields.io/badge/Supporto-Community%20%7C%20Aziendale-green)
> [!NOTE]
> Consultare il [readme](readme.md) per ulteriori informazioni.


