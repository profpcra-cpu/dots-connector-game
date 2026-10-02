import { initializeApp } from "firebase/app";
import { getDatabase, ref, set, get, child, onValue } from "firebase/database";

// A sua configuração do Firebase
const firebaseConfig = {
  apiKey: "AIzaSyBiP8g18Ev_7yv05-etUcKRLa-P6xOsh8I",
  authDomain: "brain-flow-master.firebaseapp.com",
  databaseURL: "https://brain-flow-master-default-rtdb.firebaseio.com",
  projectId: "brain-flow-master",
  storageBucket: "brain-flow-master.firebasestorage.app",
  messagingSenderId: "137353474062",
  appId: "1:137353474062:web:b53db8e1cde4c341740c5f",
  measurementId: "G-XHCEYHY37W"
};

// Inicializar o Firebase
const app = initializeApp(firebaseConfig);

// Inicializar e exportar a instância do Realtime Database
export const db = getDatabase(app);
