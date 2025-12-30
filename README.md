# Gulf Sky Provider

A comprehensive Flutter mobile application for property management and maintenance services in the Gulf region. This client-facing app enables tenants and property owners to manage their properties, request maintenance services, subscribe to packages, and process payments seamlessly.

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Stripe](https://img.shields.io/badge/Stripe-008CDD?style=for-the-badge&logo=stripe&logoColor=white)

## Features

### 🏠 Property Management
- Browse buildings by type (residential, commercial, etc.)
- View and manage rental contracts
- Access property information and details

### 🔧 Maintenance Requests
- Submit maintenance requests with detailed descriptions
- Select service types and sections
- Attach images to describe issues
- Schedule visit dates
- Pin location on map for accurate service delivery

### 📦 Package Subscriptions
- Browse available maintenance packages
- Subscribe/unsubscribe from packages
- View package benefits and pricing

### 💳 Payment Integration
- Secure payment processing via Stripe
- Pay for one-time services
- Pay for package subscriptions
- Contract cancellation support

### 🚪 Evacuation Requests
- Submit evacuation/move-out requests
- Track request status

### 📱 Additional Features
- Push notifications via Firebase Cloud Messaging
- Order history and tracking
- Multi-language support (Arabic & English)
- User authentication (Login/Register)

## Tech Stack

| Category | Technology |
|----------|------------|
| Framework | Flutter |
| State Management | BLoC / Cubit |
| Architecture | Clean Architecture |
| Dependency Injection | GetIt |
| Navigation | GoRouter |
| Networking | Dio |
| Local Storage | SharedPreferences |
| Push Notifications | Firebase Cloud Messaging |
| Analytics | Firebase Analytics |
| Payments | Stripe |
| Maps | Google Maps Flutter |
| Localization | Flutter Intl (ARB) |

## Architecture

The project follows **Clean Architecture** principles with three main layers:

```
lib/
├── config/
│   └── routes/              # App routing configuration
├── core/
│   ├── api/                 # API services, endpoints, error handling
│   ├── error/               # Failure classes
│   ├── services/            # FCM, dependency injection
│   └── utils/               # Colors, styles, validators, extensions
└── features/
    ├── data/
    │   ├── data_sources/    # Remote data sources
    │   ├── models/          # Data models (JSON serialization)
    │   └── repositories/    # Repository implementations
    ├── domain/
    │   ├── entities/        # Business entities
    │   ├── repositories/    # Repository contracts
    │   └── usecases/        # Business logic use cases
    └── presentation/
        ├── blocs/           # BLoC state management
        ├── cubits/          # Cubit state management
        ├── shared_widgets/  # Reusable UI components
        └── views/           # Screen implementations
```

## Getting Started

### Prerequisites

- Flutter SDK (>=2.19.1 <3.0.0)
- Dart SDK
- Android Studio / Xcode (for mobile development)
- Firebase project configured
- Stripe account for payments
- Google Maps API key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/jaafar-shiha/gulf-sky-provider.git
   cd gulf-sky-provider
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Configure Firebase**
   - Add your `google-services.json` (Android) to `android/app/`
   - Add your `GoogleService-Info.plist` (iOS) to `ios/Runner/`

4. **Configure Google Maps**
   - Add your API key to:
     - `android/app/src/main/AndroidManifest.xml`
     - `ios/Runner/AppDelegate.swift`

5. **Run the app**
   ```bash
   flutter run
   ```

### Generate Localization Files

```bash
flutter gen-l10n
```

## Screenshots

*Add screenshots of your app here*

## API Endpoints

The app communicates with a backend API for:
- User authentication
- Building and property information
- Maintenance and evacuation requests
- Package management
- Payment processing
- Notifications

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Contact

For any inquiries, please contact the development team.

---

*Built with ❤️ using Flutter*
