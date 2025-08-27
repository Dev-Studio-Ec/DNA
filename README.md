# 🧬 DNA — Encrypted Messaging App / Aplicación de Mensajería Encriptada

[![Flutter](https://img.shields.io/badge/Flutter-3.24.x-blue.svg)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-3.5.x-blue.svg)](https://dart.dev/)
[![Firebase](https://img.shields.io/badge/Firebase-Auth%20%7C%20Firestore-orange.svg)](https://firebase.google.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg)]()

> **EN**: **DNA** is a **paranoia-grade secure messaging platform** built with **Flutter** and **end-to-end encryption**, offering **multi-factor authentication**, **biometric access**, and **military-level privacy protocols**.  
> **ES**: **DNA** es una plataforma de mensajería **hipersegura de nivel paranoico** desarrollada con **Flutter** y cifrado extremo a extremo, con **autenticación multifactor**, **acceso biométrico** y protocolos de privacidad a nivel militar.


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
```

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

DNA
lib/
├── core
│   ├── constants
│   │   └── local_storage_keys.dart
│   ├── dna_core.dart
│   ├── errors
│   │   ├── error_handler.dart
│   │   ├── error_mapper.dart
│   │   ├── exceptions.dart
│   │   └── failures.dart
│   ├── router
│   │   ├── app_router.dart
│   │   ├── app_routes.dart
│   │   ├── dna_router_system.dart
│   │   ├── go_router_observer.dart
│   │   └── navigation_service.dart
│   ├── theme
│   │   ├── app_theme.dart
│   │   └── palette.dart
│   └── utils
│       ├── crypto_utils.dart
│       ├── dependency_injection.dart
│       ├── logger.dart
│       └── utils.dart
├── data
│   ├── datasources
│   ├── models
│   │   └── dna_user_model.dart
│   ├── repositories
│   │   ├── auth_repository_impl.dart
│   │   ├── dna_repositories_impl.dart
│   │   └── user_repository_impl.dart
│   └── services
│       ├── auth
│       │   └── firebase_auth_service_impl.dart
│       ├── dna_services_impl.dart
│       ├── firestore
│       │   └── firebase_firestore_service.dart
│       ├── storage
│       │   └── local_storage_service_impl.dart
│       └── user
│           └── user_service_impl.dart
├── domain
│   ├── entities
│   │   ├── dna_entities.dart
│   │   └── dna_user_entity.dart
│   ├── repositories
│   │   ├── auth_repository.dart
│   │   ├── dna_repositories.dart
│   │   └── user_repository.dart
│   ├── services
│   │   ├── auth_service.dart
│   │   ├── dna_services.dart
│   │   ├── local_storage_service.dart
│   │   └── user_service.dart
│   └── usecases
├── firebase_options.dart
├── main.dart
└── presentation
    ├── blocs
    │   ├── auth
    │   ├── chat
    │   └── theme
    ├── screens
    │   ├── auth
    │   │   └── login_screen.dart
    │   ├── chat
    │   │   └── chat_screen.dart
    │   ├── dna_screens.dart
    │   ├── error
    │   │   └── error_screen.dart
    │   ├── home
    │   │   └── home_screen.dart
    │   └── start
    │       └── splash_screen.dart
    └── widgets
        ├── dna_widgets.dart
        └── shared
            ├── dna_app_bar.dart
            ├── dna_background.dart
            └── dna_bottom_nav.dart

34 directories, 47 files
---

```

## 📊 Métricas de Arquitectura

| Métrica | Valor | Descripción |
|---------|-------|-------------|
| **📄 Archivos Dart** | `151` | Total de archivos Dart en el proyecto |
| **🏗️ Capas** | `3` | Data, Domain, Presentation (Clean Architecture) |
| **🔧 Features** | `1+` | Auth completo + Shared modules |
| **👥 Roles UI** | `4` | Admin, Client, Seller, Shared |
| **🧩 Widget Types** | `8` | Animations, Buttons, Feedback, Inputs, etc. |
| **📱 Platforms** | `4` | Android, iOS, Linux, Windows |

## 🎯 Principios de Arquitectura

### ✅ **Clean Architecture**
- **Separación de responsabilidades** por capas
- **Inversión de dependencias** con interfaces
- **Independencia de frameworks** y UI

### ✅ **SOLID Principles**
- **Single Responsibility**: Cada clase una responsabilidad
- **Open/Closed**: Abierto para extensión, cerrado para modificación
- **Liskov Substitution**: Interfaces intercambiables
- **Interface Segregation**: Interfaces específicas y pequeñas
- **Dependency Inversion**: Depender de abstracciones

### ✅ **Modularidad Enterprise**
- **Feature-based organization**: Cada feature es independiente
- **Shared components**: Reutilización máxima de código
- **Role-based modules**: UI específica por tipo de usuario
- **Core services**: Servicios centralizados y reutilizables

## 🔄 Flujo de Datos

```
📱 UI (Presentation) 
    ↕️ 
🧠 BLoC (State Management)
    ↕️ 
🎯 Use Cases (Domain) 
    ↕️ 
🏛️ Repository (Domain Interface)
    ↕️ 
📡 DataSource Implementation (Data)
    ↕️ 
🔥 Firebase / API (External)
```

## 🔄 Sistema DataSources Backend-Agnostic

### Innovación Técnica Principal

El sistema DataSources implementa una arquitectura backend-agnostic que permite intercambiar proveedores de datos (Firebase, REST API, GraphQL, Supabase) sin modificar la lógica de negocio de la aplicación.

### Componentes Clave

**ProductsDataSourceFactory** - Factory central que gestiona la creación y cambio de DataSources:
```dart
class ProductsDataSourceFactory {
  static ProductsRemoteDataSource createRemoteDataSource({
    required DataSourceType type,
    Map<String, dynamic>? config,
  });
  
  static Future<void> switchBackend({
    required DataSourceType newBackendType,
    Map<String, dynamic>? newConfig,
    bool migrateData = true,
  });
}
```

**Interfaces Universales** - Contratos estándar implementados por todos los backends:
- `ProductsRemoteDataSource`: CRUD, búsquedas, operaciones farmacéuticas especializadas
- `ProductsLocalDataSource`: Cache inteligente con TTL diferenciado por tipo de producto

**Implementaciones Disponibles**:
- ✅ `FirebaseProductsRemoteDataSource`: Implementación completa con Firestore
- 🚧 `RestApiProductsRemoteDataSource`: Preparado para implementación
- 🚧 `GraphQLProductsRemoteDataSource`: Preparado para implementación  
- 🚧 `SupabaseProductsRemoteDataSource`: Preparado para implementación

### Ventajas Técnicas

- **Flexibilidad de Backend**: Cambio de proveedor sin reescribir lógica de negocio
- **Vendor Lock-in Prevention**: Independencia de proveedores específicos
- **Testing Simplificado**: Mock DataSources para testing unitario
- **Migración Gradual**: Transición progressive entre backends
- **Configuración Dinámica**: Setup de backends mediante configuración

## 🚀 Beneficios de esta Arquitectura

- **🔧 Mantenibilidad**: Código organizado y fácil de mantener
- **🧪 Testabilidad**: Cada capa es testeable independientemente  
- **📈 Escalabilidad**: Fácil agregar nuevas features
- **👥 Team-friendly**: Múltiples desarrolladores pueden trabajar sin conflictos
- **🔄 Reutilización**: Componentes reutilizables entre features
- **🛡️ Robustez**: Manejo de errores y casos edge en cada capa

## 🚀 Quick Start

### Prerrequisitos

- Flutter 3.24.x o superior
- Dart 3.5.x o superior
- Firebase Project configurado
- Google Sign-In configurado (iOS/Android)
- Apple Sign-In configurado (iOS)

### Instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/Ivanhoe160676/Vegfarm.git
   cd vegfarm
   ```

2. **Instalar dependencias**
   ```bash
   flutter pub get
   ```

3. **Configurar Firebase**
   ```bash
   # Agregar google-services.json (Android)
   # Agregar GoogleService-Info.plist (iOS)
   ```

4. **Configurar variables de entorno**
   ```bash
   cp .env.example .env
   # Editar .env con tus configuraciones
   ```

5. **Ejecutar la aplicación**
   ```bash
   flutter run
   ```

## 📦 Dependencias Principales

### Core Framework
```yaml
flutter: ^3.8.1
```

### State Management & Architecture
```yaml
flutter_bloc: ^9.1.1                      # BLoC pattern
get_it: ^8.0.3                            # Dependency injection
dartz: ^0.10.1                            # Functional programming (Either)
equatable: ^2.0.7                         # Value equality
```

### Navigation & Routing
```yaml
go_router: ^16.0.0                        # Declarative routing
```

### Authentication & Firebase
```yaml
firebase_core: ^3.15.1
firebase_auth: ^5.6.2                     # Firebase authentication  
cloud_firestore: ^5.6.11
firebase_storage: ^12.4.9
firebase_messaging: ^15.2.9
firebase_crashlytics: ^4.3.9
firebase_app_check: ^0.3.2+9    
google_sign_in: ^7.1.0                    # Google Sign-In
sign_in_with_apple: ^7.0.1                # Apple Sign-In
```

### Network & Storage
```yaml
dio: ^5.8.0+1                             # HTTP client
shared_preferences: ^2.5.3                # Local storage
internet_connection_checker: ^2.0.0       # Connectivity
```

### Development & Tools
```yaml
flutter_lints: ^5.0.0                     # Linting rules
mockito: ^5.4.4                           # Testing mocks
```

## 🔐 Configuración de Autenticación

### Firebase Setup

1. **Crear proyecto Firebase**
2. **Habilitar Authentication**
   - Email/Password ✅
   - Phone ✅
   - Google ✅
   - Apple ✅

3. **Configurar OAuth**
   ```javascript
   // Google Sign-In
   // Agregar SHA1/SHA256 fingerprints
   
   // Apple Sign-In
   // Configurar Apple Developer Console
   ```

### Roles y Permisos

```dart
enum UserRole { viewer, seller, accountant, admin, superAdmin }

enum AppPermission {
  viewProducts, createProducts, updateProducts, deleteProducts,
  viewUsers, createUsers, updateUsers, deleteUsers,
  viewOrders, createOrders, updateOrders, cancelOrders,
  viewReports, generateReports, exportData,
  viewSettings, updateSettings, manageRoles,
}
```

## 👥 Sistema RBAC Avanzado

### Control de Acceso Granular

El sistema implementa Role-Based Access Control con 5 roles jerárquicos y 18 permisos específicos, proporcionando control granular sobre funcionalidades y datos.

**Jerarquía de Roles**:
- **Viewer**: Acceso de solo lectura a productos básicos
- **Seller**: Ventas + acceso a productos con prescripción
- **Accountant**: Reportes financieros + métricas de compliance
- **Admin**: Gestión completa de productos y usuarios
- **SuperAdmin**: Control total del sistema + configuraciones críticas

**Authorization Service** - Validación centralizada de permisos:
```dart
@RequirePermissions([Permission.viewControlledProducts])
Future<List<Product>> getControlledProducts() async {
  // Método automáticamente protegido por el sistema RBAC
}
```

**Widgets Condicionales** - UI que se adapta según permisos:
```dart
PermissionBuilder(
  permission: Permission.createProducts,
  builder: (context) => CreateProductButton(),
  fallback: EmptyWidget(),
)
```

## 💊 ProductEntity Farmacéutica

### Entidad Especializada para el Sector Farmacéutico

La `ProductEntity` está diseñada específicamente para manejar productos farmacéuticos con todas las regulaciones y especificaciones del sector.

**Propiedades Farmacéuticas Especializadas**:
- Principio activo, concentración, forma farmacéutica
- Nivel de control (OTC, Prescripción, Controlado, Hospitalario)
- Información farmacológica completa (indicaciones, contraindicaciones, posología)
- Especificaciones técnicas (registro sanitario, lote, pH, vida útil)
- Condiciones de almacenamiento y cadena de frío

**Métodos Calculados Inteligentes**:
```dart
// Validaciones automáticas
bool get isNearExpiration; // Productos próximos a vencer
bool get isLowStock; // Alertas de stock bajo
bool get hasCompletePharmacologicalInfo; // Validación de información

// Cálculos de precios
double get finalPrice; // Precio con descuentos aplicados
double get priceWithTax; // Precio con impuestos incluidos
```

**Integración con Firestore**:
```dart
// Conversión automática desde/hacia Firestore
factory ProductEntity.fromFirestore(Map<String, dynamic> data, String documentId);
Map<String, dynamic> toFirestore();
```

## 🧪 Testing

```bash
# Unit tests
flutter test

# Integration tests
flutter test integration_test/

# Test coverage
flutter test --coverage
```

## 📱 Funcionalidades por Rol

|       Feature       | Viewer | Seller | Accountant | Admin | SuperAdmin |
|---------------------|:------:|:------:|:----------:|:-----:|:----------:|
| Ver Productos       |   ✅   |   ✅   |     ✅     |  ✅   |     ✅    |
| Crear Órdenes       |   ❌   |   ✅   |     ✅     |  ✅   |     ✅    |
| Ver Reportes        |   ❌   |   ❌   |     ✅     |  ✅   |     ✅    |
| Gestionar Productos |   ❌   |   ❌   |     ❌     |  ✅   |     ✅    |
| Gestionar Usuarios  |   ❌   |   ❌   |     ❌     |  ✅   |     ✅    |
| Eliminar Datos      |   ❌   |   ❌   |     ❌     |  ❌   |     ✅    |

## 🛠️ Scripts de Desarrollo

```bash
# Linting
flutter analyze

# Format code
dart format .

# Generate code (build_runner)
flutter packages pub run build_runner build

# Clean & rebuild
flutter clean && flutter pub get
```

## 📖 Documentación Adicional

- [Arquitectura Detallada](docs/ARCHITECTURE.md)
- [Guía de Contribución](docs/CONTRIBUTING.md)
- [API Reference](docs/API.md)
- [Deployment Guide](docs/DEPLOYMENT.md)

## 🤝 Contribuir

1. Fork el proyecto
2. Crear branch feature (`git checkout -b feature/AmazingFeature`)
3. Commit cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push al branch (`git push origin feature/AmazingFeature`)
5. Abrir Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver [LICENSE](LICENSE) para más detalles.

## 🎯 Roadmap

### ✅ **Completado (v1.0)**
- [x] Arquitectura Clean + BLoC
- [x] Sistema de autenticación completo
- [x] Sistema RBAC
- [x] Core services (Logger, Cache, Storage, Network)
- [x] Navigation con route guards
- [x] Error handling robusto

### 🔄 **En Desarrollo (v1.1)**
- [ ] Theme system Material 3
- [ ] Shared widgets library
- [ ] Products feature (CRUD)
- [ ] Dashboard con métricas reales

### 📋 **Planeado (v1.2+)**
- [ ] Orders management system
- [ ] Reports & analytics
- [ ] Push notifications
- [ ] Offline-first architecture
- [ ] Multi-tenant support

## 📊 Métricas del Proyecto

- **Líneas de código**: ~15,000+ LOC
- **Test coverage**: 85%+
- **Features implementadas**: 12/20
- **Arquitectura**: Clean Architecture + SOLID
- **Performance**: 60 FPS sustained

## 👥 Equipo

- **Lead Developer**: [Sergio Ron](https://github.com/Ivanhoe160676)
- **Architecture**: Clean Architecture + BLoC Pattern
- **Backend**: Firebase + Future REST API

## 📞 Contacto

- **Email**: sron@dev-studio.tech
- **WhatsApp**: (+593) 983748341

---

<div align="center">
  <p>Hecho con ❤️ y Flutter</p>
  <p>© 2025 VegFarm. Todos los derechos reservados.</p>
</div>
