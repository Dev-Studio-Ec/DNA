🧬 DNA - Enterprise Encrypted Messaging Platform






EN: Enterprise-grade encrypted messaging system with paranoid-level security. Biometric login, decoy chats, vulnerability alerts, and military-grade encryption.

ES: Sistema de mensajería encriptada a nivel empresarial con seguridad de grado paranoico. Inicio con biometría, chats señuelo, alertas de vulnerabilidad y cifrado de nivel militar.

🔐 Security That Goes Beyond
Feature	Description
Triple Factor Authentication	Face Recognition + Fingerprint + Passcode
Emergency Access Code	Alternate passcode that launches a decoy environment
Decoy Chats	Fake interface & messages when under threat
Biometric Lockdown	Face or fingerprint required for critical operations
Tamper Detection	Alerts when device integrity or SIM is compromised
Offline Encryption	End-to-end AES-256 + RSA + Salting, even without internet
Cloud & Local Protection	Double encryption in Firestore + local secure storage
Zero-Knowledge Architecture	Not even admins can read your messages

✨ Features Overview
🧬 Core Messaging
End-to-End Encryption

Chat with Attachments (photos, docs, voice notes)

Self-Destructing Messages

Biometric Protected Conversations

Message Backup & Recovery

🕵️‍♂️ Decoy & Intrusion Management
Emergency Code Entry

Fake Contact Lists & Threads

Intruder Detection with Silent Alerts

Vulnerability Notifications to User

🔐 User Security
Face & Fingerprint Auth

Passcode & Emergency Access

Security Log History

Session Timeout & Auto-Lock

⚙️ Additional Capabilities
Push Notifications

Multi-device Sync (coming soon)

Dark Mode

Language Selector (English & Spanish)

🏗️ Project Structure (Clean Architecture)
pgsql
Copiar
dna/
├── lib/
│   ├── config/           → App initialization, theme, locale, env
│   ├── core/             → Constants, errors, helpers, encryption
│   ├── data/             → DTOs, repositories, datasources
│   ├── domain/           → Entities, repositories, services
│   ├── infrastructure/   → Firebase, biometric, storage impls
│   └── presentation/     → UI, Blocs, Screens, Widgets
📊 Technical Metrics
Metric	Value
📄 Dart Files	350+
🔐 Auth Factors	3
👥 Roles	1 (User)
🧱 Layers	5 (Clean)
📦 Dependencies	40+
🌐 Offline Ready	Yes

🔧 Dependencies
yaml
Copiar
flutter_bloc: ^9.1.1
get_it: ^8.0.3
firebase_auth: ^5.4.2
cloud_firestore: ^5.6.3
flutter_secure_storage: ^9.0.0
local_auth: ^2.1.6
flutter_local_notifications: ^17.0.0
encrypt: ^5.0.1
screen_util: ^5.9.3
📱 Platform Support
Feature	iOS	Android
Face Auth	✅	✅
Fingerprint	✅	✅
Secure Storage	✅	✅
Emergency Code	✅	✅
Local Notifications	✅	✅

🔐 Security Workflow
User Launches App

Biometric Verification

Passcode Auth

Optional Emergency Code (if under threat)

Access to Real or Decoy Environment

All Messages Encrypted Locally & Remotely

Auto Logout on Inactivity

🚧 Roadmap
Feature	Status
Biometric Login	✅ Completed
Decoy Chats	✅ Completed
Offline Encryption	✅ Completed
Push Notifications	✅ Completed
Multi-device Sync	🚧 In Dev
End-to-End Encryption	✅ Completed
Secure Message Recovery	🚧 Planned
Intruder Selfie Detection	🧪 Testing

👨‍💻 Credits
Role	Name
Lead Developer	Ing. Sergio Ron
Organization	Dev Studio EC
Design & UX	Sergio Ron & Team
Security Lead	Sergio Ron

📄 License
MIT License – see LICENSE file.

🌐 Contact
Channel	Info
Email	sron@dev-studio.tech
GitHub	Dev-Studio-Ec
WhatsApp	(+593) 983748341

🇪🇸 Versión en Español
Si deseas leer este README completamente en español, desplázate hacia README_ES.md (próximamente se incluirá como archivo separado).
O bien puedes traducir esta página directamente desde GitHub con un clic derecho → “Traducir al español”.

💡 Disclaimer
This app is under active development. Security protocols are extremely strict and might block access in non-compliant devices (rooted/jailbroken, emulators, custom ROMs). Please test in production devices.

🙌 Built with Paranoia, Dart & Flutter
“If you're not paranoid, you're not paying attention.”
— Sergio Ron

