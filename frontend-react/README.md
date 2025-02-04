# Runnare il docker
---

# **POC LLM Ergon**

Questo progetto utilizza Docker per eseguire e distribuire l'applicazione **POC LLM Ergon** in modo facile e consistente.

---

## **Requisiti**

- **Docker** (versione 20.10 o superiore)
- **Docker Compose** (opzionale, per una gestione più semplice dei servizi)

---

## **Costruzione e Avvio del Container**

### **1. Clonare il Repository**

Clona il repository del progetto sul tuo sistema locale:

```bash
git clone https://github.com/username/poc-llm-ergon.git
cd poc-llm-ergon
```

---

### **2. Creare l'Immagine Docker**

Esegui il comando per creare l'immagine Docker:

```bash
docker build -t poc-llm-ergon .
```

oppure con docker-compose

```bash
docker-compose up -d
```

---

### **3. Avviare il Container**

Esegui il container con il comando:

```bash
docker run -d --name poc-llm-ergon -p 3000:80 poc-llm-ergon
```

- `-d`: Esegue il container in modalità detached (in background).
- `--name`: Imposta il nome del container come `poc-llm-ergon`.
- `-p 3000:80`: Mappa la porta `80` del container alla porta `3000` sul sistema host.

Puoi accedere all'applicazione in un browser all'indirizzo:  
[http://localhost:3000](http://localhost:3000)

---

## **Gestione del Container**

### **Visualizzare i Container in Esecuzione**

```bash
docker ps
```

### **Fermare il Container**

```bash
docker stop poc-llm-ergon
```

### **Riavviare il Container**

```bash
docker start poc-llm-ergon
```

### **Rimuovere il Container**

```bash
docker rm -f poc-llm-ergon
```

---

oppure con docker-compose, fermalo con:

```bash
docker-compose down
```

---

## **Aggiornamento del Container**

Per aggiornare il container all'ultima versione:

1. Ricostruisci l'immagine:

   ```bash
   docker build --no-cache -t poc-llm-ergon .
   ```

2. Riavvia il container:

   ```bash
   docker stop poc-llm-ergon
   docker rm poc-llm-ergon
   docker run -d --name poc-llm-ergon -p 3000:80 poc-llm-ergon
   ```

---

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
