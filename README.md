## Project Overview

SismoSafe è un sistema embedded progettato per rilevare vibrazioni e generare automaticamente un’allerta.
Il sistema è basato su un’architettura distribuita composta da due nodi STM32 che collaborano tra loro per monitorare l’ambiente e reagire in caso di movimento anomalo.

## 🎥 Project Presentation Video

[![Watch the presentation video](thumbnail_video.png)](video_presentazione.mp4)

Click on the image above to watch the project presentation.

### Punti principali del progetto

**Architettura a due nodi**

* **Nodo A** controlla un motore DC tramite driver L298N.
* **Nodo B** monitora le vibrazioni tramite il sensore MPU6050.

**Rilevamento vibrazioni**

* Il Nodo B acquisisce continuamente i dati dal sensore e verifica la presenza di movimenti anomali.

**Comunicazione tra i nodi**

* In caso di vibrazione significativa, il Nodo B invia un messaggio `"STOP"` al Nodo A tramite comunicazione **UART**, interrompendo il funzionamento del motore.

**Notifica remota**

* Il Nodo B comunica con un modulo **ESP8266**, che invia una notifica **Telegram** allo smartphone dell’utente.

**Uso di protocolli embedded**

* **UART** per la comunicazione tra nodi e con il modulo Wi-Fi.
* **I2C** per la comunicazione con il sensore **MPU6050**.

## Authors

* **Matteo Cuomo**
* **Antonio Tufo**

Project developed for the course **Architettura e Progetto dei Calcolatori**

University of Naples Federico II

Academic Year 2024/2025

Professor: Nicola Mazzocca

## License

This project is licensed under the MIT License.
