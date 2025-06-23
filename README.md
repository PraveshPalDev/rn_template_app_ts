
# React Native Boilerplate

![React Native](https://img.shields.io/badge/React_Native-0.78.2-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0.4-blue)
![Redux](https://img.shields.io/badge/Redux-5.0.1-purple)
![React Navigation](https://img.shields.io/badge/React_Navigation-7.0-orange)

## Project Overview

A modern, production-ready React Native boilerplate with TypeScript support, focusing on best practices, scalability, and developer experience. This boilerplate includes authentication flows, theming support, RTL handling, and a robust project structure.

---

## ✅ Why This Boilerplate?

This boilerplate is built with a **robust and thoughtfully organized folder structure**, making it easy for any developer to get started quickly. Whether building a scalable app or learning React Native, this setup offers a strong foundation with essential tools and structure in place.

### ✅ Easy to Use and Extend

- **Well-organized architecture**: Clean separation of logic, UI, configuration, and business logic.
- **Plug-and-play**: Clone → Install → Run.
- **Out-of-the-box features** like theming, localization, authentication, Redux Toolkit setup, and secure storage.
- **Developer-friendly tools**: ESLint, Prettier, TypeScript, and testing setup already integrated.

---

## 📁 Folder Structure

```
.
├── android/                  # Android native code
├── ios/                     # iOS native code
├── src/
│   ├── assets/             # Images, fonts, etc.
│   ├── components/         # Reusable UI components
│   ├── config/             # App configuration
│   ├── context/            # React Context providers
│   ├── hooks/              # Custom React hooks
│   ├── lang/               # i18n translations
│   ├── models/             # TypeScript interfaces
│   ├── navigation/         # Navigation setup
│   ├── redux/              # State management
│   ├── screens/            # Screen components
│   ├── styles/             # Global styles
│   ├── typings/            # Global TypeScript types
│   └── utils/              # Utility functions
├── patches/                # Patch files for dependencies
├── vendor/                 # Vendor files
├── .eslintrc.js            # ESLint configuration
├── .prettierrc.js          # Prettier configuration
├── babel.config.js         # Babel configuration
├── metro.config.js         # Metro bundler configuration
├── tsconfig.json           # TypeScript configuration
└── package.json            # Project dependencies
```

---

## 🚀 Features

- 🔐 **Authentication Flow**: Complete login and OTP verification using `react-native-otp-entry`
- 🌓 **Theme Support**: Dynamic light/dark theme switching with context
- 🌐 **Multi-language Support**: RTL/LTR with `i18next` integration
- 📱 **Responsive Design**: Scales well on different screen sizes
- 🧩 **Modular Architecture**: Clean, maintainable folder structure
- 🔄 **State Management**: Redux Toolkit with async support
- 🎨 **SVG Support**: Vector graphics with `react-native-svg`
- 🔒 **Secure Storage**: Encrypted storage using `rn-secure-storage`
- 💫 **Animations**: Smooth transitions with `react-native-reanimated`
- 🛠 **Developer Tools**: Pre-configured ESLint, Prettier, Jest
- 🛡️ **Type Safety**: Complete TypeScript support
- 🎯 **Navigation**: React Navigation v7 with native stack and bottom tabs

---

## 🧱 Technology Stack

### Core
- **React Native**: 0.78.2
- **TypeScript**: 5.0.4
- **React**: 19.0.0

### State Management
- **Redux**: 5.0.1
- **React Redux**: 9.2.0
- **Redux Toolkit**: 2.6.1

### Navigation
- **@react-navigation/native**: 7.1.5
- **@react-navigation/native-stack**: 7.3.9
- **@react-navigation/bottom-tabs**: 7.3.9

### UI & Animation
- **react-native-reanimated**: 3.17.2
- **react-native-svg**: 15.11.2
- **react-native-modal**: 14.0.0-rc.1
- **react-native-bootsplash**: 6.3.4

### Internationalization
- **i18next**: 24.2.3
- **react-i18next**: 15.4.1
- **intl-pluralrules**: 2.0.1

### Security & Storage
- **rn-secure-storage**: 3.0.1

### Development Tools
- **Jest**: 29.6.3
- **ESLint**: 8.19.0
- **Prettier**: 2.8.8
- **babel-plugin-module-resolver**: 5.0.2

---

## ⚙️ Setup and Installation

### Prerequisites

- Node.js >= 18
- Ruby (for iOS build)
- CocoaPods (for iOS)
- Xcode (for iOS)
- Android Studio (for Android)

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd rn_boilerplate
   ```

2. **Install dependencies:**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Install CocoaPods (for iOS):**
   ```bash
   cd ios
   pod install
   cd ..
   ```

4. **Run the app:**
   ```bash
   # Start Metro
   npm start

   # Run on iOS
   npm run ios

   # Run on Android
   npm run android
   ```

---

## 🔌 Feature Implementations

### 🌙 Theme System

```ts
// Usage in component
const { theme } = useTheme();
const colors = Colors[theme];
```

### 🌍 Internationalization

```ts
import { useTranslation } from 'react-i18next';

const { t } = useTranslation();
<TextComp text={t('WELCOME')} />
```

### 🧭 Navigation Setup

```ts
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';

const Stack = createNativeStackNavigator();
```

### 🧠 Redux Toolkit

```ts
import { configureStore } from '@reduxjs/toolkit';

const store = configureStore({
  reducer: rootReducer,
  middleware: (getDefaultMiddleware) => 
    getDefaultMiddleware({ serializableCheck: false }),
});
```

### 🔐 Secure Storage

```ts
import SecureStorage from 'rn-secure-storage';

await SecureStorage.setItem('token', '12345');
const token = await SecureStorage.getItem('token');
```

---

## 🧭 Development Guidelines

- ✅ Use **functional components** and **React hooks**
- ✅ Follow **TypeScript** best practices
- ✅ Keep components small and focused
- ✅ Use **ESLint** and **Prettier** for code consistency
- ✅ Use **React Navigation** and **Redux Toolkit** as structured

---

## 📜 Available Scripts

- `npm start` – Start Metro bundler
- `npm run ios` – Run the app on iOS simulator
- `npm run android` – Run the app on Android emulator
- `npm run lint` – Lint the codebase
- `npm run test` – Run Jest unit tests
