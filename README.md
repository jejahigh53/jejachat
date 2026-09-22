# 🔒 Chat Privata E2EE by JeJa

[![Live Demo](https://img.shields.io/badge/Live_Demo-chat.jjplz.party-2e7d32?style=for-the-badge&logo=rocket)](https://chat.jjplz.party)
[![Security](https://img.shields.io/badge/Security-E2EE_AES--GCM-1a3c34?style=for-the-badge&logo=shield)](https://chat.jjplz.party)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

> **La tua privacy non è un'opzione, è il punto di partenza.**  
> Una web app di messaggistica istantanea ultra-sicura, leggera e completamente cifrata **End-to-End (E2EE)**. Provala subito senza registrarti su 🚀 **[chat.jjplz.party](https://chat.jjplz.party)**.

---

## 🌟 Perché usare questa chat? (I Punti di Forza)

La maggior parte delle app di chat tradizionali conserva i tuoi messaggi sui propri server o richiede numeri di telefono e email per registrati. Questa chat è progettata con un approccio **Zero-Trust**:

* 🔐 **Crittografia Client-Side Reale (E2EE):** Messaggi di testo, immagini e video vengono cifrati **prima** di lasciare il tuo dispositivo.
* 🙈 **Zero-Knowledge Server:** Il server passa semplicemente i pacchetti cifrati tra gli utenti. Non possiede le chiavi di decifratura, non può leggere il contenuto dei messaggi né visualizzare i media scambiati.
* 🚫 **Nessun Account o Dato Personale:** Non serve registrarsi, non servono email né numeri di telefono. Nessuna tracciabilità.
* 📱 **Mobile-First & Ultra Compatibile:** Ottimizzata per girare al massimo delle prestazioni su iOS (Safari) e Android (Chrome) senza crash di memoria durante la cifratura di file video.
* ⚡ **Streaming Video Cifrato:** Gestione avanzata dei file multimediali pesanti con decifratura al volo direttamente nella RAM del browser.

---

## 🛡️ Come funziona la Sicurezza?

La chat sfrutta le **Web Crypto API** native del browser per garantire uno standard crittografico di livello militare:

1. **Derivazione della Chiave (PBKDF2):** Quando inserisci la tua *Passphrase Crittografica*, viene generata una chiave locale **AES-GCM a 256-bit** combinata con un salt univoco.
2. **Cifratura Locale:** 
   * **Testo e Immagini:** Vengono cifrati con Vettore di Inizializzazione (IV) casuale e inviati via WebSocket.
   * **Video:** Vengono letti a blocchi di memoria (`ArrayBuffer`), cifrati in locale e caricati temporaneamente sotto forma di Blob cifrato non leggibile.
3. **Decifratura Locale:** Solo gli utenti all'interno della stanza che possiedono la **stessa passphrase** possono decifrare i dati in tempo reale.

---

## 🚀 Come Usarla (Guida Rapida)

Usare la chat è facilissimo e richiede pochi secondi:

1. Collegati su **[chat.jjplz.party](https://chat.jjplz.party)**.
2. Inserisci il tuo **Nickname** (come vuoi essere visto dagli altri).
3. Inserisci la **Password d'accesso** della stanza.
4. Inserisci la **Passphrase per la crittografia** *(Condividila previamente con i tuoi interlocutori tramite un canale sicuro)*.
5. Clicca su **Entra** e inizia a chattare in totale riservatezza!

> ⚠️ **Nota Importante:** Chiunque inserisca una *Passphrase* errata vedrà solo messaggi e media illeggibili (`[impossibile decifrare]`).

---

## 💻 Tech Stack

* **Frontend:** HTML5, CSS3, JavaScript Vanilla (Web Crypto API)
* **Backend:** Node.js, Express
* **Real-time Engine:** Socket.IO
* **Media Handling:** Multer (upload temporaneo di payload cifrati)
* **Hosting:** Render (con Dominio e SSL gestito)

---

## 🛠️ Installazione Locale

Se vuoi eseguire la tua istanza privata sul tuo computer:

1. **Clona la repository:**
   ```bash
   git clone [https://github.com/tuo-username/tuo-repo.git](https://github.com/tuo-username/tuo-repo.git)
   cd tuo-repo
