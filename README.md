# 🌱 Ecosphere

**A mobile application that promotes environmental sustainability by connecting users to tree sponsorship opportunities and waste management initiatives.**

Ecosphere empowers individuals to make a direct environmental impact by sponsoring trees, tracking waste collection schedules, and managing their contribution to a greener planet. Built with Flutter and powered by Firebase, the app provides a seamless experience across Android and iOS platforms.

---

## ✨ Features

- **🔐 User Authentication** - Secure sign-up and login with Firebase Authentication
- **🌳 Tree Sponsorship** - Browse and sponsor trees, view sponsorship details and payment options
- **📅 Waste Collection Calendar** - Track local waste collection schedules based on your city
- **👤 User Profiles** - Manage personal information including name, email, city, and phone
- **🔍 Tree Discovery** - Search and explore available trees to sponsor
- **💰 Payment Integration** - Secure sponsorship payment flow
- **🎨 Beautiful UI** - Modern Material Design with green-themed aesthetics
- **📱 Multi-platform** - Native support for Android and iOS

---

## 🛠️ Tech Stack

- **Language:** Dart 3.5.3+
- **Framework:** Flutter
- **State Management:** Provider 6.1.2
- **Backend & Database:** Firebase (Authentication, Cloud Firestore)
- **UI Libraries:**
  - Material Design 3
  - Google Fonts 6.2.1
  - Flutter SVG 2.0.10+1
  - Cupertino Icons 1.0.8
- **Authentication:** Firebase Auth, Google Sign-In 6.2.1
- **Additional Tools:**
  - Table Calendar 3.1.2 (waste schedule management)
  - GoRouter 14.3.0 (navigation)
  - Flutter Toast 8.2.8 (notifications)

---

## 📁 Project Structure

```
lib/
  ├── main.dart                 App entry point, Firebase initialization, routing
  ├── models/                   Data models for the application
  │   ├── activity.dart         Activity/task model with city and collection time
  │   └── schedule.dart         Waste collection schedule model
  ├── pages/                    UI screens and pages
  │   ├── login.dart            Authentication login screen
  │   ├── signup.dart           User registration screen
  │   ├── home.dart             Main home dashboard with navigation
  │   ├── calendar.dart         Waste schedule calendar view
  │   ├── user_profile.dart     User profile display
  │   ├── edit_user_profile.dart Profile editing functionality
  │   ├── my_trees.dart         User's sponsored trees collection
  │   ├── sponsor.dart          Browse available trees to sponsor
  │   ├── sponsor_tree.dart     Individual tree sponsorship details
  │   ├── sponsor_overview_page.dart  Sponsorship summary and overview
  │   ├── sponsor_payment.dart  Payment processing for sponsorship
  │   ├── tree_details.dart     Detailed tree information
  │   └── search.dart           Search functionality for trees and activities
  ├── services/                 Business logic and data services
  │   ├── auth_service.dart     Firebase authentication (sign up, sign in, sign out)
  │   └── firestore_service.dart Cloud Firestore database operations
  ├── src/                      Reusable widgets and utilities
  └── assets/                   Images, icons, and custom fonts

android/                        Android platform-specific code
ios/                           iOS platform-specific code
web/                           Web platform support

pubspec.yaml                   Project dependencies and configuration
firebase.json                  Firebase project configuration
```

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (3.5.3 or higher)
- Dart SDK (included with Flutter)
- Firebase project with credentials configured
- Git

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/BilalR4M/ecosphere.git
   cd ecosphere
   ```

2. **Install dependencies:**
   ```bash
   flutter pub get
   ```

3. **Configure Firebase:**
   - Update Firebase credentials in `firebase.json`
   - Ensure Firestore database and Authentication are enabled in Firebase Console
   - Download and place `google-services.json` for Android and `GoogleService-Info.plist` for iOS

4. **Run the app:**
   ```bash
   # For Android
   flutter run -d android
   
   # For iOS
   flutter run -d ios
   
   # For Web
   flutter run -d chrome
   ```

### Development

- **Run with hot reload:**
  ```bash
  flutter run
  ```

- **Build for release:**
  ```bash
  # Android
  flutter build apk --release
  
  # iOS
  flutter build ios --release
  ```

- **Run tests:**
  ```bash
  flutter test
  ```

---

## 📱 App Flow

1. **Launch** → User starts at Login screen
2. **Authentication** → Sign up with email/password or sign in to existing account
3. **Home Dashboard** → Main hub with options to:
   - View profile
   - Sponsor a tree
   - Check waste schedule
   - Sign out
4. **Tree Sponsorship** → Browse trees → View details → Process payment → Track sponsored trees
5. **Waste Schedule** → View calendar with collection dates by city
6. **User Profile** → Manage personal information and settings

---

## 🔒 Authentication

The app uses Firebase Authentication with the following flows:

- **Sign Up:** Collects email, password, name, city, and phone number. User data stored in Firestore `users` collection.
- **Sign In:** Authenticates user and navigates to home dashboard
- **Sign Out:** Safely logs out user and returns to login screen
- **Google Sign-In:** Built-in support for authentication with Google accounts

---

## 🗄️ Firebase Database Structure

### Firestore Collections:

- **`users/`** - User profile data
  - Fields: `name`, `email`, `city`, `phone`
  
- **`activities/`** - Waste collection activities
  - Fields: `activity`, `city`, `collectionTime`
  
- **`trees/`** - Available trees for sponsorship
  - Fields: Tree details, sponsorship info
  
- **`sponsorships/`** - User sponsorships tracking

---

## 🎨 Design

- **Color Scheme:** Green-themed (primary: `#185519`)
- **Typography:** Poppins font family throughout
- **Design System:** Material Design 3
- **Responsive Layout:** Optimized for various screen sizes

---

## 📚 Key Components

### Services
- **AuthService** - Handles user authentication operations (sign up, sign in, sign out, user data retrieval)
- **FirestoreService** - Manages Cloud Firestore database interactions

### Navigation
- Bottom Navigation Bar with 4 main sections: Home, Calendar, Notifications, Profile
- Named routes for direct page access
- GoRouter for advanced routing capabilities

### UI Widgets
- Custom theme with green color palette
- Material buttons and cards
- Calendar widgets for schedule display
- Profile management components

---

## 🐛 Troubleshooting

### Firebase Initialization Issues
- Ensure Firebase credentials are properly configured
- Check internet connectivity
- Verify Firebase project permissions in Console

### Build Errors
- Run `flutter clean` and `flutter pub get`
- Check Flutter and Dart versions
- Update to latest dependencies: `flutter pub upgrade`

### Authentication Failures
- Verify email/password requirements
- Check Firestore security rules
- Ensure user data exists in `users` collection

---

## 📝 Environment Configuration

Create a `.env` file if needed for configuration:
```
FIREBASE_PROJECT_ID=ecosphere-20f5d
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is currently not licensed. Please contact the owner for usage terms.

---

## 👤 Author

**Bilal R4M**
- GitHub: [@BilalR4M](https://github.com/BilalR4M)
- Repository: [ecosphere](https://github.com/BilalR4M/ecosphere)

---

## 🌍 Support & Contact

For issues, questions, or feature requests, please open an [issue](https://github.com/BilalR4M/ecosphere/issues) on GitHub.

---

<div align="center">

**🌱 Help protect our planet, one tree at a time! 🌍**

</div>
