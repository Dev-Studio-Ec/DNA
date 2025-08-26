# 🧬 DNA — Encrypted Messaging App / Aplicación de Mensajería Encriptada

![DNA Logo](assets/images/dna_logo.png)

> **EN**: **DNA** is a **paranoia-grade secure messaging platform** built with **Flutter** and **end-to-end encryption**, offering **multi-factor authentication**, **biometric access**, and **military-level privacy protocols**.  
> **ES**: **DNA** es una plataforma de mensajería **hipersegura de nivel paranoico** desarrollada con **Flutter** y cifrado extremo a extremo, con **autenticación multifactor**, **acceso biométrico** y protocolos de privacidad a nivel militar.

---

## 🔐 Security System / Sistema de Seguridad

| Feature | Descripción |
|--------|-------------|
| ✅ **Triple Factor Authentication** / Autenticación de Triple Factor | Password, fingerprint, face recognition. |
| ✅ **Emergency Escape Code** / Clave de Emergencia | Triggers fake session (decoy chats). |
| ✅ **End-to-End Encryption (E2EE)** | Based on Signal Protocol, with per-user key generation. |
| ✅ **Public & Master Key System** / Sistema de Claves Públicas y Maestras | Enables controlled access & future self-recovery. |
| ✅ **Biometric Authentication** / Autenticación Biométrica | Face ID / Touch ID fully integrated. |
| ✅ **Offline Secure Key Storage** / Claves guardadas localmente | Keys never leave the device. |
| ✅ **Fake Chat Mode** / Modo Chat Falso | Decoy environment if user feels threatened. |
| ✅ **Intrusion Alerts** / Alertas de Vulnerabilidad | Notifies trusted contacts if breach is suspected. |

---

## ✨ Features / Funcionalidades

- 💬 Real-time secure messaging with encryption.
- 📞 Voice & video calling (planned).
- 🖼 Media sharing (photos, audio, video).
- 🔐 Disappearing messages & secret chats.
- 👥 Group chats with encrypted moderation.
- 🟢 Online status & activity presence.
- 🧠 AI-suggested replies (optional).
- 📱 Adaptive UI, dark/light themes.

---

## 🧠 Architecture / Arquitectura

### Frontend
| Tech | Uso |
|------|-----|
| Flutter + BLoC | State management & UI |
| GoRouter | Navigation |
| flutter_screenutil | Responsive layout |
| formz | Form validation |
| Firebase Auth | Phone auth with OTP |

### Backend
| Servicio | Función |
|---------|---------|
| Firebase Firestore | Real-time chat DB |
| Firebase Storage | Encrypted media storage |
| Firebase Cloud Messaging (FCM) | Push notifications |
| Cloud Functions | Auth + Security rules |
| WebSocket (custom) | Live presence system |
| Signal Protocol | End-to-end encryption engine |

---

## 📁 Project Structure / Estructura del Proyecto

dna/
├── lib/
│ ├── core/ # Constants, themes, helpers
│ ├── data/ # Repositories, services, models
│ ├── domain/ # Entities and use cases
│ ├── presentation/ # UI: Screens and Widgets
│ ├── bloc/ # State management (BLoCs)
│ └── main.dart # Entry point
├── assets/
│ ├── images/
│ ├── animations/
│ └── logo_purple.png
├── pubspec.yaml
└── README.md

yaml
Copiar

---

## ⚙️ Dependencies / Dependencias

```yaml
dependencies:
  flutter_bloc: ^9.1.1
  equatable: ^2.0.7
  go_router: ^16.0.0
  formz: ^0.8.0
  firebase_core: ^4.0.0
  firebase_auth: ^6.0.0
  cloud_firestore: ^6.0.0
  firebase_storage: ^13.0.0
  firebase_messaging: ^16.0.0
  encrypt: ^5.0.3
  pointycastle: ^4.0.0
  flutter_secure_storage: ^9.2.4
  flutter_screenutil: ^5.9.3
  lottie: ^3.3.1
  cached_network_image: ^3.4.1
  intl: ^0.20.2
  image_picker: ^1.1.2
  just_audio: ^0.10.4
  record: ^6.0.0
  video_player: ^2.10.0
🚀 Getting Started / Primeros Pasos
Prerequisites
Flutter 3.22+

Dart 3.4+

Firebase CLI

Installation
bash
Copiar
git clone https://github.com/Dev-Studio-Ec/dna.git
cd dna
flutter pub get
firebase init
flutter run
🧪 Roadmap
Estado	Tarea
✅	Project scaffolding with Clean Architecture
✅	Phone authentication with Firebase
✅	Biometric + emergency code auth
✅	E2EE Signal Protocol integration
⏳	Real-time messaging w/ media
⏳	Decoy chats + intrusion alerts
🔜	Secure voice/video calls
🔜	Group chat with roles
🔜	Desktop and web support

🖌 UI/UX Philosophy
🖤 Dark-first elegant design

🧩 Modular widget system

📱 Fully responsive across devices

✨ Micro-interactions & smooth animations

🎯 Clean, minimalist layout hierarchy

📜 License / Licencia
MIT License
This project is licensed under the MIT License. See LICENSE for more details.

🙌 Credits / Créditos
Developed with ❤️ by:
Ing. Sergio Ron
Dev Studio — Ecuador
