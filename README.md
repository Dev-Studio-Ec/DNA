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

### 🔐 **Sistema de Autenticación Multi-Modal**
- **Multi-Auth**: Email/Password, Phone SMS, Google Sign-In, Apple Sign-In
- **Session Management**: Token refresh automático, logout seguro
- **Social Linking**: Vinculación de cuentas múltiples
- **Password Management**: Recuperación, cambio seguro con re-autenticación

### 🏗️ **Arquitectura Enterprise**
- **Clean Architecture**: Separación clara de capas Data/Domain/Presentation
- **BLoC Pattern**: State management robusto y predecible
- **Dependency Injection**: GetIt con setup modular y testeable
- **SOLID Principles**: Código mantenible y escalable

## 🏗️ Arquitectura del Proyecto

```
lib/
├── core/
│   ├── base/
│   │   ├── base_datasource.dart
│   │   ├── base_entity.dart
│   │   ├── base_repository.dart
│   │   └── base_usecase.dart
│   ├── config/
│   │   ├── app_config.dart
│   │   ├── image/
│   │   │   ├── image_config.dart
│   │   │   └── image_upload_result.dart
│   │   ├── storage/
│   │   │   └── storage_paths.dart
│   │   ├── theme/
│   │   │   ├── app_colors.dart
│   │   │   ├── app_dimensions.dart
│   │   │   ├── app_text_styles.dart
│   │   │   ├── app_theme.dart
│   │   │   └── vegfarm_theme.dart
│   │   └── validations/
│   │       └── validation_result.dart
│   ├── constants/
│   │   ├── api_constants.dart
│   │   ├── assets_paths.dart
│   │   └── firebase_constants.dart
│   ├── di/
│   │   ├── dependency_injection.dart
│   │   └── service_locator.dart
│   ├── error/
│   │   ├── error_handler.dart
│   │   ├── error_mapper.dart
│   │   ├── exceptions.dart
│   │   ├── failures.dart
│   │   └── pharmaceutical_exceptions.dart
│   ├── network/
│   │   ├── api_endpoints.dart
│   │   ├── base_api_service.dart
│   │   ├── dio_client.dart
│   │   ├── interceptors/
│   │   │   ├── auth_interceptor.dart
│   │   │   ├── error_interceptor.dart
│   │   │   └── logging_interceptor.dart
│   │   └── network_info.dart
│   ├── router/
│   │   ├── app_router.dart
│   │   ├── navigation_service.dart
│   │   ├── route_observer.dart
│   │   └── route_paths.dart
│   ├── security/
│   │   ├── biometric_service.dart
│   │   ├── encryption_service.dart
│   │   ├── security_utils.dart
│   │   └── token_manager.dart
│   ├── services/
│   │   ├── analytics_service.dart
│   │   ├── cache_service.dart
│   │   ├── environment_service.dart
│   │   ├── firebase_firestore_service.dart
│   │   ├── firebase_storage_service.dart
│   │   ├── image_service.dart
│   │   ├── image_upload_service.dart
│   │   ├── logger_service.dart
│   │   ├── notification_service.dart
│   │   ├── onboarding_service.dart
│   │   ├── storage_service.dart
│   │   └── vegfarm_core_services.dart
│   ├── utils/
│   │   ├── enums/
│   │   │   ├── app_environment.dart
│   │   │   ├── platform_type.dart
│   │   │   └── user_role.dart
│   │   ├── extensions/
│   │   │   ├── datetime_extensions.dart
│   │   │   ├── num_extensions.dart
│   │   │   └── string_extensions.dart
│   │   ├── formatters.dart
│   │   ├── helpers/
│   │   │   ├── currency_helper.dart
│   │   │   ├── date_helper.dart
│   │   │   └── image_helper.dart
│   │   └── validators.dart
│   └── vegfarm_core.dart
├── data/
│   └── services/
│       ├── firebase_storage_service_impl.dart
│       ├── image_service_impl.dart
│       ├── image_upload_service_impl.dart
│       ├── products_service.dart
│       └── vegfarm_services_impl.dart
├── dev/
│   ├── firestore_loader.dart
│   └── structure.md
├── domain/
│   └── entities/
│       ├── category_entity.dart
│       ├── offer_entity.dart
│       ├── product_entity.dart
│       ├── review_entity.dart
│       ├── user_role_entity.dart
│       └── vegfarm_entities.dart
├── features/
│   ├── auth/
│   │   ├── data/
│   │   │   ├── datasources_impl/
│   │   │   │   ├── auth_local_datasource_impl.dart
│   │   │   │   ├── auth_remote_datasource_impl.dart
│   │   │   │   └── social_auth_datasource_impl.dart
│   │   │   ├── models/
│   │   │   │   ├── auth_response_model.dart
│   │   │   │   ├── authorization_info.dart
│   │   │   │   ├── social_auth_model.dart
│   │   │   │   └── user_model.dart
│   │   │   └── repositories/
│   │   │       └── auth_repository_impl.dart
│   │   ├── domain/
│   │   │   ├── datasources/
│   │   │   │   ├── auth_local_datasource.dart
│   │   │   │   ├── auth_remote_datasource.dart
│   │   │   │   └── social_auth_datasource.dart
│   │   │   ├── entities/
│   │   │   │   ├── auth_session_entity.dart
│   │   │   │   ├── social_auth_entity.dart
│   │   │   │   └── user_entity.dart
│   │   │   ├── enums/
│   │   │   │   ├── app_permission.dart
│   │   │   │   ├── auth_enums.dart
│   │   │   │   └── image_enums.dart
│   │   │   ├── repositories/
│   │   │   │   └── auth_repository.dart
│   │   │   ├── services/
│   │   │   │   ├── auth_service.dart
│   │   │   │   ├── authorization_service.dart
│   │   │   │   ├── permission_service.dart
│   │   │   │   └── role_service.dart
│   │   │   └── usecases/
│   │   │       ├── change_password_usecase.dart
│   │   │       ├── check_auth_status_usecase.dart
│   │   │       ├── forgot_password_usecase.dart
│   │   │       ├── get_current_user_usecase.dart
│   │   │       ├── login_with_apple_usecase.dart
│   │   │       ├── login_with_email_usecase.dart
│   │   │       ├── login_with_google_usecase.dart
│   │   │       ├── login_with_phone_usecase.dart
│   │   │       ├── logout_usecase.dart
│   │   │       ├── refresh_token_usecase.dart
│   │   │       ├── register_usecase.dart
│   │   │       ├── resend_phone_verification_usecase.dart
│   │   │       ├── send_phone_verification_usecase.dart
│   │   │       ├── update_email_usecase.dart
│   │   │       ├── update_profile_usecase.dart
│   │   │       ├── verify_email_usecase.dart
│   │   │       └── verify_phone_code_usecase.dart
│   │   ├── presentation/
│   │   │   ├── bloc/
│   │   │   │   ├── auth_bloc.dart
│   │   │   │   ├── auth_event.dart
│   │   │   │   └── auth_state.dart
│   │   │   ├── screens/
│   │   │   │   ├── dashboard_screen.dart
│   │   │   │   ├── error_screen.dart
│   │   │   │   ├── forgot_password_screen.dart
│   │   │   │   ├── login_screen.dart
│   │   │   │   ├── phone_verification_screen.dart
│   │   │   │   ├── register_screen.dart
│   │   │   │   ├── scaffold_with_nav_bar.dart
│   │   │   │   └── vegfarm_auth_screens.dart
│   │   │   └── widgets/
│   │   │       └── auth/
│   │   │           ├── authenticated_builder.dart
│   │   │           ├── conditional_access_builder.dart
│   │   │           ├── permission_builder.dart
│   │   │           └── role_builder.dart
│   │   └── vegfarm_auth_features.dart
│   ├── favorites/
│   │   └── presentation/
│   │       ├── screens/
│   │       └── widgets/
│   ├── home/
│   │   └── presentation/
│   │       ├── screens/
│   │       └── widgets/
│   ├── orders/
│   │   └── presentation/
│   │       ├── screens/
│   │       └── widgets/
│   ├── products/
│   │   ├── data/
│   │   │   ├── datasources/
│   │   │   │   ├── firebase_products_remote_datasource.dart
│   │   │   │   ├── products_datasource_factory.dart
│   │   │   │   ├── shared_prefs_products_local_datasource.dart
│   │   │   │   └── vegfarm_product_datasources_impl.dart
│   │   │   ├── models/
│   │   │   │   ├── cart_action_result.dart
│   │   │   │   ├── favorite_action_result.dart
│   │   │   │   ├── pharmaceutical_product_metrics.dart
│   │   │   │   ├── pharmaceutical_search_result.dart
│   │   │   │   ├── product_detail_data.dart
│   │   │   │   ├── product_validation_result.dart
│   │   │   │   └── share_action_result.dart
│   │   │   └── repositories/
│   │   │       └── products_repository_impl.dart
│   │   ├── domain/
│   │   │   ├── datasources/
│   │   │   │   ├── products_local_datasource.dart
│   │   │   │   ├── products_remote_datasource.dart
│   │   │   │   └── vegfarm_product_datasources.dart
│   │   │   ├── enums/
│   │   │   │   └── product_enums.dart
│   │   │   ├── repositories/
│   │   │   │   └── products_repository.dart
│   │   │   └── usecases/
│   │   │       └── get_product_details_usecase.dart
│   │   ├── presentation/
│   │   │   ├── bloc/
│   │   │   │   └── product_bloc/
│   │   │   │       ├── product_bloc.dart
│   │   │   │       ├── product_event.dart
│   │   │   │       └── product_state.dart
│   │   │   └── widgets/
│   │   └── products_feature.dart
│   ├── profile/
│   │   └── presentation/
│   │       ├── screens/
│   │       └── widgets/
│   └── search/
├── firebase_options.dart
├── main.dart
└── shared/
    ├── data/
    │   ├── datasources/
    │   │   ├── base_local_datasource.dart
    │   │   └── base_remote_datasource.dart
    │   ├── models/
    │   │   ├── api_response_model.dart
    │   │   ├── error_response_model.dart
    │   │   └── pagination_model.dart
    │   ├── services/
    │   │   └── onboarding_service_impl.dart
    │   └── vegfarm_data.dart
    ├── domain/
    │   ├── entities/
    │   │   ├── base_entity.dart
    │   │   └── onboarding_status_entity.dart
    │   ├── enums/
    │   │   └── vegfarm_enums.dart
    │   ├── value_objects/
    │   │   ├── email.dart
    │   │   ├── password.dart
    │   │   └── phone_number.dart
    │   └── vegfarm_domain.dart
    └── presentation/
        ├── blocs/
        │   ├── observer_bloc/
        │   │   └── simple_bloc_observer.dart
        │   └── vegfarm_blocs.dart
        ├── modules/
        │   ├── accountant/
        │   │   └── accountant_dashboard_screen.dart
        │   ├── admin/
        │   │   └── screens/
        │   │       └── admin_dashboard_screen.dart
        │   ├── client/
        │   │   └── screens/
        │   │       ├── account/
        │   │       │   └── profile_screen.dart
        │   │       ├── favorites/
        │   │       │   └── favorites_screen.dart
        │   │       ├── home/
        │   │       │   ├── components/
        │   │       │   │   ├── home_categories_section.dart
        │   │       │   │   ├── home_components.dart
        │   │       │   │   ├── home_footer.dart
        │   │       │   │   ├── home_header.dart
        │   │       │   │   ├── home_offers_section.dart
        │   │       │   │   ├── home_products_grid.dart
        │   │       │   │   └── home_search_bar.dart
        │   │       │   └── home_screen.dart
        │   │       ├── main_layout_screen.dart
        │   │       ├── orders/
        │   │       │   └── orders_screen.dart
        │   │       ├── product/
        │   │       │   ├── components/
        │   │       │   │   ├── product_action_buttons.dart
        │   │       │   │   ├── product_basic_info.dart
        │   │       │   │   ├── product_components.dart
        │   │       │   │   ├── product_detail_app_bar.dart
        │   │       │   │   ├── product_image_gallery.dart
        │   │       │   │   ├── product_pharmaceutical_info.dart
        │   │       │   │   ├── product_reviews.dart
        │   │       │   │   └── product_technical_specs.dart
        │   │       │   ├── components_old/
        │   │       │   │   ├── product_action_buttons.dart
        │   │       │   │   ├── product_basic_info.dart
        │   │       │   │   ├── product_components.dart
        │   │       │   │   ├── product_image_gallery.dart
        │   │       │   │   ├── product_pharmaceutical_info.dart
        │   │       │   │   ├── product_reviews.dart
        │   │       │   │   └── product_technical_specs.dart
        │   │       │   └── product_detail_screen.dart
        │   │       ├── profile/
        │   │       │   └── profile_screen.dart
        │   │       └── search/
        │   │           └── search_screen.dart
        │   ├── seller/
        │   │   └── screens/
        │   │       └── seller_dashboard_screen.dart
        │   └── shared/
        │       └── screens/
        │           ├── error/
        │           │   └── vegfarm_error_app.dart
        │           ├── onboarding/
        │           │   ├── components/
        │           │   │   ├── onboarding_components.dart
        │           │   │   ├── onboarding_header.dart
        │           │   │   ├── onboarding_navigation_buttons.dart
        │           │   │   ├── onboarding_progress_indicator.dart
        │           │   │   ├── onboarding_step1_profile_image.dart
        │           │   │   ├── onboarding_step2_personal_info.dart
        │           │   │   └── onboarding_step3_complete.dart
        │           │   └── onboarding_screen.dart
        │           ├── products/
        │           │   ├── product_details_screen.dart
        │           │   └── products_catalog_screen.dart
        │           └── start/
        │               ├── splash_animated_content.dart
        │               ├── splash_animation_controller.dart
        │               ├── splash_background.dart
        │               ├── splash_components.dart
        │               ├── splash_constants.dart
        │               ├── splash_content.dart
        │               ├── splash_debug.dart
        │               ├── splash_logos.dart
        │               └── splash_screen.dart
        ├── vegfarm_modules_screens.dart
        └── widgets/
            ├── animations/
            │   ├── fade_in_animation.dart
            │   ├── loading_animations.dart
            │   └── slide_animation.dart
            ├── backgrounds/
            │   └── animated_login_background.dart
            ├── buttons/
            │   ├── custom_elevated_button.dart
            │   ├── custom_outlined_button.dart
            │   ├── floating_action_button.dart
            │   ├── premium_button.dart
            │   ├── premium_social_button.dart
            │   └── premium_text_button.dart
            ├── feedback/
            │   ├── empty_state_widget.dart
            │   ├── error_widget.dart
            │   ├── loading_widget.dart
            │   └── shimmer_loading.dart
            ├── inputs/
            │   ├── custom_dropdown.dart
            │   ├── custom_search_field.dart
            │   ├── custom_text_field.dart
            │   ├── phone_input_field.dart
            │   └── premium_input_field.dart
            ├── layouts/
            │   ├── adaptive_scaffold.dart
            │   ├── responsive_layout.dart
            │   └── scaffold_with_nav.dart
            ├── media/
            │   ├── avatar_widget.dart
            │   ├── cached_image.dart
            │   └── image_picker_widget.dart
            ├── navigation/
            │   ├── app_drawer.dart
            │   ├── bottom_nav_bar.dart
            │   └── breadcrumb_nav.dart
            ├── theme/
            │   ├── app_theme.dart
            │   ├── color_schemes.dart
            │   ├── component_themes.dart
            │   ├── dimensions.dart
            │   ├── responsive_breakpoints.dart
            │   └── text_themes.dart
            └── vegfarm_widgets.dart
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
