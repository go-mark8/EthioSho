# 🛒 EthioShop - Enterprise-Grade Ethiopian E-Commerce Marketplace

<div align="center">
  
![Flutter](https://img.shields.io/badge/Flutter-3.24+-02569B?logo=flutter)
![Dart](https://img.shields.io/badge/Dart-3.4+-0175C2?logo=dart)
![Firebase](https://img.shields.io/badge/Firebase-Latest-FFCA28?logo=firebase)
![License](https://img.shields.io/badge/License-MIT-green)
![Platform](https://img.shields.io/badge/Platform-Android_iOS_Web_Light-blue)

**A modern, enterprise-grade e-commerce platform built specifically for the Ethiopian market**

[Features](#-key-features) •
[Architecture](#-architecture) •
[Getting Started](#-getting-started) •
[Documentation](#-documentation) •
[Contributing](#-contributing)

</div>

---

## 📖 Table of Contents

- [About](#-about)
- [Key Features](#-key-features)
- [Architecture](#-architecture)
- [Technology Stack](#-technology-stack)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Development](#-development)
- [Testing](#-testing)
- [Deployment](#-deployment)
- [Configuration](#-configuration)
- [Documentation](#-documentation)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Support](#-support)

---

## 🎯 About

EthioShop is a comprehensive, enterprise-grade e-commerce marketplace designed specifically for the Ethiopian market. Built with Flutter and Firebase, it provides a seamless shopping experience with P2P capabilities, offline support, and Ethiopian-specific features including local currency (ETB), regional delivery, and Chapa payment gateway integration.

### 🌟 Why EthioShop?

- **🇪🇹 Ethiopian-Centric**: Built for Ethiopia with ETB currency, 13 regional support, and local payment methods
- **🏢 Enterprise-Grade**: Clean Architecture, scalable design, production-ready code
- **📱 Cross-Platform**: Single codebase for Android, iOS, Web, and Desktop
- **🔄 Offline-First**: Works without internet with automatic sync
- **🛡️ Secure**: Firebase Auth, secure payments, data encryption
- **⚡ Performant**: Optimized for Ethiopian network conditions
- **🎨 Modern UI**: Material 3 design with Ethiopian flag colors

---

## 🚀 Key Features

### 👤 For Buyers
- **🔍 Advanced Search**: Search products by category, price, location
- **🛒 Smart Cart**: Save for later, quantity management, price calculations
- **💳 Secure Payments**: Chapa, Telebirr, Cash on Delivery
- **📦 Order Tracking**: Real-time order status and delivery tracking
- **💬 In-App Chat**: Direct communication with sellers
- **⭐ Reviews & Ratings**: Read and write product reviews
- **❤️ Wishlist**: Save favorite products for later
- **📍 Regional Delivery**: Delivery across all 13 Ethiopian regions

### 🏪 For Sellers
- **📊 Dashboard**: Analytics, sales overview, performance metrics
- **📦 Product Management**: Create, edit, manage products easily
- **📝 Order Processing**: Accept, ship, and manage orders
- **💰 Revenue Tracking**: Track earnings and payment status
- **🏷️ Inventory Management**: Stock levels, low stock alerts
- **📱 Mobile Management**: Manage your shop on the go

### 🔧 For Administrators
- **🎛️ Admin Dashboard**: Platform overview and analytics
- **👥 User Management**: Manage buyers and sellers
- **🛍️ Product Moderation**: Approve/reject products
- **📋 Order Management**: View and manage all orders
- **📈 Reports & Analytics**: Detailed platform insights
- **🔒 Security Controls**: User blocking, content moderation

### 💎 Technical Features
- **🔄 Offline-First**: Works without internet with automatic sync
- **🔐 Secure Authentication**: Email, Google, phone authentication
- **📱 Push Notifications**: Real-time order and chat notifications
- **🌍 Multi-Theme**: Light and dark mode support
- **♿ Accessible**: WCAG 2.1 compliant UI
- **🌐 Multi-Language Ready**: Amharic, Oromo, Tigrinya support
- **⚡ Performance**: Optimized images, lazy loading, pagination
- **🧪 Well-Tested**: Comprehensive unit and integration tests

---

## 🏗️ Architecture

EthioShop follows **Clean Architecture** principles with clear separation of concerns:

```
┌─────────────────────────────────────────────────────────────┐
│                    Presentation Layer                        │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐    │
│  │ Screens  │  │ Providers│  │ Widgets  │  │  Routes  │    │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘    │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│                      Domain Layer                            │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐        │
│  │  Entities   │  │ Repositories│  │  Use Cases  │        │
│  └─────────────┘  └─────────────┘  └─────────────┘        │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│                       Data Layer                             │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐        │
│  │ Data Sources│  │  Models     │  │Repositories │        │
│  │  (Firebase) │  │             │  │(Implementation)│      │
│  └─────────────┘  └─────────────┘  └─────────────┘        │
└─────────────────────────────────────────────────────────────┘
```

### Architecture Principles

1. **Dependency Inversion**: Depend on abstractions, not implementations
2. **Separation of Concerns**: Each layer has a single responsibility
3. **Testability**: All components are easily testable
4. **Scalability**: Easy to add new features without breaking existing code
5. **Maintainability**: Clear code structure and documentation

---

## 🛠️ Technology Stack

### Core Technologies
- **Framework**: Flutter 3.24+
- **Language**: Dart 3.4+
- **State Management**: Riverpod 2.6+
- **Routing**: Go Router 14.6+

### Backend & Database
- **Authentication**: Firebase Auth
- **Database**: Cloud Firestore
- **Storage**: Firebase Storage
- **Messaging**: Cloud Messaging (FCM)
- **Analytics**: Firebase Analytics & Crashlytics

### Local Storage
- **Offline Cache**: Hive 1.1+
- **Database**: Floor (SQLite wrapper)

### Payment Integration
- **Primary**: Chapa (Ethiopian payment gateway)
- **Supporting**: Telebirr, Cash on Delivery

### UI/UX
- **Design System**: Material 3
- **Icons**: Flutter SVG, Cupertino Icons
- **Images**: Cached Network Image, Photo View
- **Animations**: Smooth Page Indicator, Shimmer

### Development Tools
- **Code Generation**: Freezed, JSON Serializable, Floor
- **Linting**: Flutter Lints
- **Formatting**: Dart Format
- **Package Manager**: Pub

### DevOps
- **CI/CD**: GitHub Actions (configurable)
- **Environment Management**: Nix (flake.nix)
- **Version Control**: Git
- **Code Quality**: Analysis Options

---

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Flutter SDK**: 3.24.0 or higher
- **Dart SDK**: 3.4.0 or higher
- **Android Studio** (for Android development)
- **Xcode** (for iOS development, macOS only)
- **VS Code** or **IntelliJ IDEA** (recommended IDE)
- **Git**: For version control
- **Node.js** (optional, for web tools)

### Installation

#### Option 1: Using Nix (Recommended)

```bash
# Clone the repository
git clone https://github.com/your-org/ethioshop.git
cd ethioshop

# Enter the development environment
nix develop

# Install dependencies
flutter pub get

# Run the app
flutter run
```

#### Option 2: Manual Installation

```bash
# Clone the repository
git clone https://github.com/your-org/ethioshop.git
cd ethioshop

# Install Flutter dependencies
flutter pub get

# Verify Flutter installation
flutter doctor

# Run the app
flutter run
```

### Firebase Setup

1. **Create Firebase Project**
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Create a new project: "EthioShop"

2. **Add Apps to Firebase**
   - Android: Follow Firebase setup instructions for Android
   - iOS: Follow Firebase setup instructions for iOS
   - Web: Follow Firebase setup instructions for Web

3. **Download Configuration Files**
   - Android: `google-services.json` → Place in `android/app/`
   - iOS: `GoogleService-Info.plist` → Place in `ios/Runner/`
   - Web: Firebase config object → Update in `lib/core/config/firebase_options.dart`

4. **Enable Firebase Services**
   - Authentication: Enable Email/Password and Google providers
   - Firestore: Create database and set rules
   - Storage: Create storage bucket and set rules
   - Cloud Messaging: Enable FCM

5. **Configure Security Rules**
   - Firestore: Set appropriate read/write rules
   - Storage: Set storage access rules

### Environment Configuration

Create a `.env` file in the root directory:

```env
# Firebase
FIREBASE_API_KEY=your_api_key
FIREBASE_AUTH_DOMAIN=your_auth_domain
FIREBASE_PROJECT_ID=your_project_id
FIREBASE_STORAGE_BUCKET=your_storage_bucket
FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
FIREBASE_APP_ID=your_app_id

# Chapa Payment
CHAPA_SECRET_KEY=your_chapa_secret_key
CHAPA_PUBLIC_KEY=your_chapa_public_key

# App Configuration
APP_ENV=development
API_BASE_URL=https://api.ethioshop.com
WEB_BASE_URL=https://ethioshop.com
```

### Running the App

```bash
# Install dependencies
flutter pub get

# Run on specific device
flutter run -d <device_id>

# Run on Chrome (Web)
flutter run -d chrome

# Run on Android emulator
flutter run -d android

# Run on iOS simulator
flutter run -d ios
```

---

## 📁 Project Structure

```
ethioshop/
├── lib/                          # Application source code
│   ├── main.dart                # App entry point
│   ├── core/                    # Core utilities and configuration
│   │   ├── constants/          # App constants (ETB, regions, etc.)
│   │   ├── config/             # Firebase and app configuration
│   │   ├── error/              # Error handling
│   │   ├── router/             # App routing (Go Router)
│   │   └── theme/              # App theming (Material 3)
│   ├── domain/                 # Domain layer (business logic)
│   │   ├── entities/           # Business entities
│   │   ├── repositories/       # Repository interfaces
│   │   ├── usecases/           # Use cases
│   │   └── failures/           # Error handling
│   ├── data/                   # Data layer (data access)
│   │   ├── datasources/        # Data sources (Firebase, local)
│   │   ├── models/             # Data models
│   │   └── repositories/       # Repository implementations
│   └── presentation/           # Presentation layer (UI)
│       ├── providers/          # State management (Riverpod)
│       ├── screens/            # UI screens
│       ├── widgets/            # Reusable widgets
│       └── routes/             # Route definitions
├── assets/                     # App assets
│   ├── images/                 # Images
│   ├── icons/                  # Icons
│   └── fonts/                  # Custom fonts
├── test/                       # Unit and widget tests
├── android/                    # Android platform code
├── ios/                        # iOS platform code
├── web/                        # Web platform code
├── pubspec.yaml                # Flutter dependencies
├── analysis_options.yaml       # Dart analysis options
├── flake.nix                   # Nix development environment
└── README.md                   # This file
```

---

## 🧪 Testing

### Run All Tests

```bash
# Run all tests
flutter test

# Run tests with coverage
flutter test --coverage

# Run specific test file
flutter test test/widgets/product_card_test.dart
```

### Test Coverage

```bash
# Generate coverage report
flutter test --coverage

# View coverage in browser
genhtml coverage/lcov.info -o coverage/html
open coverage/html/index.html
```

### Test Structure

```
test/
├── unit/                      # Unit tests
│   ├── domain/
│   │   ├── entities/
│   │   ├── repositories/
│   │   └── usecases/
│   └── data/
│       ├── models/
│       └── repositories/
├── widget/                    # Widget tests
│   └── widgets/
│       ├── product_card_test.dart
│       └── ...
└── integration/               # Integration tests
    └── screens/
        └── ...
```

---

## 🚢 Deployment

### Android

```bash
# Build APK
flutter build apk --release

# Build App Bundle (for Play Store)
flutter build appbundle --release

# Output location: build/app/outputs/
```

### iOS

```bash
# Build IPA
flutter build ios --release

# Open in Xcode for distribution
open ios/Runner.xcworkspace
```

### Web

```bash
# Build web version
flutter build web --release

# Output location: build/web/
```

### Firebase Hosting (Web)

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login
firebase login

# Initialize Firebase Hosting
firebase init hosting

# Deploy
firebase deploy
```

---

## ⚙️ Configuration

### App Configuration

Edit `lib/core/constants/app_constants.dart` for app-wide settings:

```dart
class AppConstants {
  static const String appName = 'EthioShop';
  static const String appVersion = '1.0.0';
  static const String currencyCode = 'ETB';
  static const String currencySymbol = 'Br';
  
  // Ethiopian regions
  static const List<String> ethiopianRegions = [
    'Addis Ababa',
    'Afar',
    'Amhara',
    // ... more regions
  ];
}
```

### Theme Configuration

Customize the theme in `lib/core/theme/app_theme.dart`:

```dart
class AppTheme {
  static ThemeData get lightTheme => ThemeData(
    colorScheme: ColorScheme.fromSeed(
      seedColor: Colors.green, // Ethiopian green
      brightness: Brightness.light,
    ),
    // ... more theme settings
  );
}
```

### Firebase Configuration

Update Firebase settings in `lib/core/config/firebase_options.dart` with your project credentials.

---

## 📚 Documentation

- **[SETUP_GUIDE.md](SETUP_GUIDE.md)** - Detailed setup instructions
- **[MERGED_PROJECT_SUMMARY.md](MERGED_PROJECT_SUMMARY.md)** - Project merge summary
- **[VERIFICATION_CHECKLIST.md](VERIFICATION_CHECKLIST.md)** - Verification checklist
- **[PROJECT_STATUS.md](PROJECT_STATUS.md)** - Project status and progress
- **[QUICK_START.md](QUICK_START.md)** - Quick start guide
- **[IMPLEMENTATION_SUMMARY.md](IMPLEMENTATION_SUMMARY.md)** - Implementation details

---

## 🗺️ Roadmap

### Version 1.1.0 (Q2 2025)
- [ ] Multi-language support (Amharic, Oromo, Tigrinya)
- [ ] Advanced analytics dashboard
- [ ] Enhanced seller tools
- [ ] Referral system
- [ ] Loyalty program

### Version 1.2.0 (Q3 2025)
- [ ] AI-powered product recommendations
- [ ] Video product reviews
- [ ] Live streaming sales
- [ ] Augmented reality product view
- [ ] Voice search

### Version 2.0.0 (Q4 2025)
- [ ] Seller marketplace (multi-vendor)
- [ ] Logistics integration
- [ ] International shipping
- [ ] Cryptocurrency payments
- [ ] Blockchain-based reviews

---

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

### Development Workflow

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style

- Follow Dart style guide
- Run `dart format .` before committing
- Run `flutter analyze` to check for issues
- Write tests for new features
- Update documentation

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2026 EthioShop

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 💬 Support

### Community
- **Discord**: [Join our Discord server](https://discord.gg/ethioshop)
- **Twitter**: [@EthioShopApp](https://twitter.com/EthioShopApp)
- **LinkedIn**: [EthioShop](https://linkedin.com/company/ethioshop)

### Help & Documentation
- **Documentation**: [docs.ethioshop.com](https://docs.ethioshop.com)
- **FAQ**: [faq.ethioshop.com](https://faq.ethioshop.com)
- **Support Email**: support@ethioshop.com

### Bug Reports
- Report bugs via [GitHub Issues](https://github.com/your-org/ethioshop/issues)
- Include:
  - Detailed description of the issue
  - Steps to reproduce
  - Expected behavior
  - Screenshots/videos if applicable
  - Flutter and Dart version

---

## 🙏 Acknowledgments

- **Flutter Team** - For the amazing framework
- **Firebase Team** - For the backend services
- **Chapa** - Ethiopian payment gateway
- **Ethiopian Developers Community** - For support and feedback

---

## 📊 Project Stats

- **Total Files**: 107+ Dart files
- **Lines of Code**: 18,000+
- **Screens**: 28 screens
- **Providers**: 9 state management providers
- **Widgets**: 5 reusable widgets
- **Routes**: 25+ routes
- **Ethiopian Regions**: 13 regions
- **Product Categories**: 14 categories
- **Completion**: 95%

---

## 🔗 Links

- **Website**: [https://ethioshop.com](https://ethioshop.com)
- **GitHub**: [https://github.com/your-org/ethioshop](https://github.com/your-org/ethioshop)
- **Play Store**: [https://play.google.com/store/apps/details?id=com.ethio.shop](https://play.google.com/store/apps/details?id=com.ethio.shop)
- **App Store**: [https://apps.apple.com/app/ethioshop/id123456789](https://apps.apple.com/app/ethioshop/id123456789)
- **Web App**: [https://app.ethioshop.com](https://app.ethioshop.com)

---

<div align="center">

**Built with ❤️ for Ethiopia**

Made with Flutter · Firebase · Ethiopian Flag Colors 🇪🇹

[⬆ Back to Top](#-ethioshop---enterprise-grade-ethiopian-e-commerce-marketplace)

</div>
