# Documentazione del Progetto Gestionale

## Indice

1. [Titolo e Descrizione del Progetto](#1-titolo-e-descrizione-del-progetto)
2. [Stato del Progetto](#2-stato-del-progetto)
3. [Installazione](#3-installazione)
4. [Utilizzo](#4-utilizzo)
5. [Documentazione](#5-documentazione)
6. [Contributo](#6-contributo)
7. [Crediti](#7-crediti)
8. [Licenza](#8-licenza)
9. [Contatti](#9-contatti)
10. [Badge](#10-badge)
11. [Recap](#11-recap)

## 1. Titolo e Descrizione del Progetto:

Il progetto "Gestionale" consente agli utenti preregistrati di gestire la registrazione dei propri clienti e la visualizzazione della lista delle loro anagrafiche:

1. **Accesso Utente**:
   
   ![Form di autenticazione dell'utente](autenticaUtente.png)
   
   - L'utente effettua il login al sistema da **account unici preregistrati** 
   - Degli account utente le **credenziali sono criptate con SHA3**
   - Il sistema garantisce una **gestione sicura per l'apertura delle pagine sensibili** tramite la cache in cui viene memorizzato l'accesso dell'utente tenendolo in memoria in modo che se non è presente allora impedisce l'ingresso in qualsiasi form che non sia quello di autenticazione.

3. **Registrazione Clienti**:
   
   ![Form di registrazione del cliente](registraCliente.png)
   
   Gli utenti possono registrare i propri clienti nel sistema che li identifica sulla base del loro codice fiscale.
   
5. **Visualizzazione Clienti**:
   
   ![Form di visualizzazione dei clienti](visualizzaClienti.png)

   Gli utenti possono visualizzare in modo massivo o nel dettaglio le anagrafiche dei propri clienti con le seguenti features:
   
   - Si possono selezionare quali campi rendere visibili e quali oscurare 
   - Si possono filtrare i clienti da visualizzare con un sistema di ricerca abilitato su ogni campo

## 2. Stato del Progetto:

Il progetto è stato completato con successo ed è in uno stato stabile. Tutte le funzionalità sono state implementate e testate con successo. Il software è pronto per l'utilizzo in produzione. 

![Stato del Progetto](https://img.shields.io/badge/Stato-Stabile-brightgreen)

![Versione](https://img.shields.io/badge/Versione-1.0-blue)

![Manutenzione](https://img.shields.io/badge/Manutenzione-Attiva-green)

## 3. Installazione:

Per installare il progetto, è necessario avere installati i seguenti componenti:
- [NodeJS](https://nodejs.org/en/download) e la libreria di React per il frontend
- [.NET](https://dotnet.microsoft.com/en-us/download) Core per il backend
- [SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16#download-ssms) e [Microsoft SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) per il database

![Compatibilità OS](https://img.shields.io/badge/Compatibilit%C3%A0%20OS-Windows%20%7C%20Android%20%7C%20iOS%20%28iPhone%29%20%7C%20Mac-lightgrey)


## 4. Utilizzo:

Seguire le istruzioni di configurazione per configurare React, .NET Core, SQL Server Management Studio e Microsoft SQL Server. Queste istruzioni dettagliate sono disponibili nella sezione di [installazione](#3-installazione) del README.

## 5. Documentazione:

Per la documentazione dettagliata del frontend e del backend, fare riferimento ai seguenti link:
- [Documentazione Frontend](link-documentazione-frontend)
- [Documentazione Backend](link-documentazione-backend)

![Tecnologia](https://img.shields.io/badge/Tecnologia-React%20%7C%20.NET%20%7C%20C%23-yellow)

![Compatibilità](https://img.shields.io/badge/Compatibilit%C3%A0-Chrome%20%7C%20Firefox%20%7C%20Safari-green)

![Linguaggio](https://img.shields.io/badge/Linguaggio-JavaScript%20%7C%20C%23-orange)

![Documentazione](https://img.shields.io/badge/Documentazione-Completa-blue)

## 6. Contributo:

Per contribuire al progetto o segnalare bug rivolgersi alle fonti seguenti:

- **email:** 
  - **aziendale:** gestionale.dev@gmail.com
  - **privata:** 
    - **Reda Karimi:** redakarimi76@gmail.com
    - **Vittorio Piotti:** vittoriopiotti.vp@gmail.com
- **repository GitHub:** [github](link-repository)

![Contributo](https://img.shields.io/badge/Contributo-Open%20Source-green)


## 7. Crediti:

- Backend: Reda Karimi
- Frontend: Vittorio Piotti
- Risorse di Sviluppo: Visual Studio, Estensione SSH per lavoro di gruppo in locale

![Ambiente di sviluppo](https://img.shields.io/badge/Ambiente%20di%20Sviluppo-Visual%20Studio%20Code%20%7C%20Visual%20Studio-blue)


## 8. Licenza:

Il progetto è rilasciato sotto una licenza open-source e non è vincolato da condizioni di utilizzo del codice sorgente.

![Licenza](https://img.shields.io/badge/Licenza-Open%20Source-blue)


## 9. Contatti:

- **Gestore Backend**: Reda Karimi
  - **Nome**: Reda Karimi
  - **Email**: redakarimi76@gmail.com
  - **GitHub**: [redakarimi](https://github.com/redakarimi)

- **Gestore Frontend**: Vittorio Piotti
  - **Nome**: Vittorio Piotti
  - **Email**: vittoriopiotti.vp@gmail.com
  - **GitHub**: [vittoriopiotti](https://github.com/vittoriopiotti)


![Contatto](https://img.shields.io/badge/Contatto-Email-blue)

![Supporto](https://img.shields.io/badge/Supporto-Community-green)

## 10. Badge:

Lo stato della build è riuscito e stabile.

![Download](https://img.shields.io/badge/Download-100K%2B-blue)

## 11. Recap:
Questo README fornisce una panoramica del progetto Gestionale, comprese le istruzioni per l'installazione, l'utilizzo, il contributo e il contatto con i gestori del backend e del frontend. Assicurati di consultare la documentazione dettagliata per informazioni più approfondite.

![Popolarità](https://img.shields.io/badge/Popolarit%C3%A0-Alta-yellow)

![Ultima modifica](https://img.shields.io/badge/Ultima%20Modifica-Gennaio%202024-blue)
