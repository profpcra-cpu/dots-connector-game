# 🧠 Brain Flow Master

O **Brain Flow Master** é uma aplicação web interativa desenvolvida com JavaScript e integrada ao **Google Firebase Realtime Database** para armazenamento e sincronização de dados em tempo real[cite: 10].

---

## 🚀 Funcionalidades

- **Sincronização em Tempo Real:** Leitura e escrita instantânea de dados utilizando o Realtime Database[cite: 10].
- **Arquitetura Modular:** Estruturado com módulos ES6 e suporte nativo ao SDK v10+ do Firebase.
- **Suporte a Analytics:** Integração nativa com o Google Analytics para monitorização de métricas de utilização.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 & CSS3**
- **JavaScript (ES6+)**
- **Firebase Realtime Database** (v10.x+)
- **Firebase Analytics**

---

## 📋 Pré-requisitos

Para rodar ou contribuir com o projeto, você precisará de:

1. Um navegador moderno com suporte a módulos ES6 (Chrome, Firefox, Edge, Safari).
2. Uma conta no [Google Firebase Console](https://console.firebase.google.com/)[cite: 1, 6].

---

## ⚙️ Configuração do Firebase

1. **Criar o Projeto no Firebase:**
   - Aceda ao console do Firebase e crie um projeto com o nome `brain-flow-master`[cite: 1, 4].
   - Ative o **Realtime Database** na região `us-central1` (ou na região de sua preferência)[cite: 7, 8].
   - Defina as Regras de Segurança iniciais (ex.: Modo de Teste durante o desenvolvimento).

2. **Obter Credenciais:**
   - Vá em **Configurações do Projeto** > **Geral** > **Seus aplicativos**[cite: 5, 9, 10].
   - Adicione um app Web (`brain-flow-web`)[cite: 5, 11].

3. **Arquivo de Configuração (`firebase-config.js`):**
   Crie um arquivo para gerenciar a inicialização da aplicação:

```javascript
import { initializeApp } from "firebase/app";
import { getAnalytics } from "firebase/analytics";
import { getDatabase } from "firebase/database";

const firebaseConfig = {
  apiKey: "AIzaSyBiP8g18Ev_7yv05-etUcKRLa-P6xOsh8I",
  authDomain: "brain-flow-master.firebaseapp.com",
  databaseURL: "[https://brain-flow-master-default-rtdb.firebaseio.com](https://brain-flow-master-default-rtdb.firebaseio.com)",
  projectId: "brain-flow-master",
  storageBucket: "brain-flow-master.firebasestorage.app",
  messagingSenderId: "137353474062",
  appId: "1:137353474062:web:b53db8e1cde4c341740c5f",
  measurementId: "G-XHCEYHY37W"
};

// Inicializa o Firebase
const app = initializeApp(firebaseConfig);
export const analytics = getAnalytics(app);
export const db = getDatabase(app);
