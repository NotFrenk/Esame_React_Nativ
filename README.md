# ProgettoNativConGrafica

## Descrizione
ProgettoNativConGrafica è un'applicazione mobile sviluppata con **React Native** ed **Expo** per la gestione delle informazioni sui voli e sugli aeroporti. L'app comunica con un backend **Flask** che fornisce dati sugli aeroporti e sui voli, recuperati da un database **PostgreSQL**.

## Tecnologie Utilizzate
- **Frontend**: React Native, Expo
- **Backend**: Flask, psycopg2
- **Database**: PostgreSQL

## Requisiti
Assicurati di avere installati i seguenti strumenti:
- **Node.js** (versione più recente consigliata)
- **Expo CLI** (`npm install -g expo-cli`)
- **Python 3** e **Flask** (`pip install flask flask-cors psycopg2`)
- **PostgreSQL**

## Installazione

### 1. Clonare il repository
```sh
 git clone <URL_DEL_REPOSITORY>
 cd progettoNativConGrafica
```

### 2. Avviare il backend Flask
1. Configura il database PostgreSQL con le credenziali nel file `query.py`.
2. Esegui il backend:
   ```sh
   python query.py
   ```

Il server Flask sarà avviato su `http://127.0.0.1:5001` (o `http://10.0.2.2:5001` su emulatori Android).

### 3. Installare le dipendenze del frontend
```sh
npm install
```

### 4. Avviare l'app mobile
```sh
npm start
```
Scegli il target di avvio:
- **Android**: `npm run android`
- **iOS** (Mac con Xcode): `npm run ios`
- **Web**: `npm run web`

## API disponibili
Il backend fornisce le seguenti API:
- `GET /aeroporti` → Restituisce l'elenco dei voli fuori L'italia.
- `GET /vol.sopra.med` → Restituisce l'elenco dei voli in L'italia.
- `GET /serv.api` → Restituisce l'elenco di tutti i voli.

## Struttura del Progetto
```
progettoNativConGrafica/
│── assets/              # Immagini e icone
│── comp/                # Componenti React Native
│   ├── VisTab.js        # Componente per la visualizzazione tabellare
│── query.py             # Backend Flask
│── App.js               # Entry point del frontend
│── index.js             # Inizializzazione Expo
│── app.json             # Configurazione Expo
│── package.json         # Dipendenze e script
│── package-lock.json    # Blocco delle versioni npm
```

