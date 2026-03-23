<div align="center">

<img src="screenshots/logo.png" alt="Hamsa Logo" width="120" />

# Hamsa 🌸

### Multi-Market Beauty & Makeup E-Commerce App

A large-scale beauty and makeup shopping platform serving **4 regional markets** — Saudi Arabia, Yemen, Oman, and UAE.  
Each market operates with its own independent data, currency, and catalog.

<br/>

[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-3.x-0175C2?logo=dart&logoColor=white)](https://dart.dev)
[![BLoC](https://img.shields.io/badge/State-BLoC-4CAF50)](https://bloclibrary.dev)
[![REST API](https://img.shields.io/badge/Backend-REST%20API-FF6B35)](https://restfulapi.net)
[![Private](https://img.shields.io/badge/Source-Private-red)](https://github.com/AhmeedGamil)

</div>

---

## 📸 Screenshots

<div align="center">
<table>
  <tr>
    <td align="center">
      <img src="screenshots/market_select.png" width="200" alt="Market Selection"/>
      <br/><sub><b>Market Selection</b></sub>
    </td>
    <td align="center">
      <img src="screenshots/home.png" width="200" alt="Home"/>
      <br/><sub><b>Home</b></sub>
    </td>
    <td align="center">
      <img src="screenshots/categories.png" width="200" alt="Categories"/>
      <br/><sub><b>Categories</b></sub>
    </td>
    <td align="center">
      <img src="screenshots/product.png" width="200" alt="Product Detail"/>
      <br/><sub><b>Product Detail</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="screenshots/product.png" width="200" alt="Product Detail"/>
      <br/><sub><b>Product Detail</b></sub>
    </td>
    <td align="center">
      <img src="screenshots/cart.png" width="200" alt="Cart"/>
      <br/><sub><b>Cart (Guest)</b></sub>
    </td>
    <td align="center">
      <img src="screenshots/checkout.png" width="200" alt="Checkout"/>
      <br/><sub><b>Checkout</b></sub>
    </td>
    <td align="center">
      <img src="screenshots/orders.png" width="200" alt="Orders"/>
      <br/><sub><b>Orders</b></sub>
    </td>
  </tr>
</table>
</div>

---

## 🎬 Demo

<div align="center">
  <img src="screenshots/demo.gif" width="280" alt="Hamsa App Demo"/>
</div>

> *Record your screen and convert to GIF using [ScreenToGif](https://www.screentogif.com/) (Windows) or [Gifox](https://gifox.app/) (Mac)*

---

## ✨ Features

- 🌍 **4 Regional Markets** — Saudi Arabia, Yemen, Oman, and UAE each with fully isolated data, products, pricing, and currency
- 🛒 **Guest Cart** — Add to cart without requiring login, with seamless account merge on sign-in
- 🔐 **Auth Flow** — Secure user authentication
- 💳 **Checkout** — Secure multi-step checkout with market-specific payment options
- 🎨 **Glass UI** — Custom blur and glass morphism effects throughout the interface
- 🎬 **Animations** — Smooth transitions, hero animations, and micro-interactions
- 🔔 **Push Notifications** — Order status updates and promotional alerts
- 🌐 **RTL Support** — Full Arabic right-to-left layout support
- 📦 **Order Tracking** — Real-time order status per market

---

## 🏗️ Architecture

Clean Architecture with BLoC state management — fully decoupled presentation, domain, and data layers.

```
lib/
├── core/
│   ├── api/                # API client setup
│   ├── config/             # App configuration
│   ├── constants/          # Market configs (SA, YE, OM, UAE)
│   ├── database/           # Local database setup
│   ├── di/                 # Dependency injection
│   ├── error/              # Error handling & failures
│   ├── l10n/               # Localization (Arabic/English)
│   ├── network/            # Network layer & interceptors
│   ├── registry/           # Service registry
│   ├── routing/            # App navigation & routes
│   ├── storage/            # Local storage abstraction
│   ├── theme/              # Glass UI theme, colors, text styles
│   ├── usecases/           # Base usecase definitions
│   ├── utils/              # Helpers & extensions
│   └── widgets/            # Shared UI components
│
└── features/               # Each feature is fully self-contained
    ├── cart/
    │   ├── data/           # Models, repositories, datasources
    │   ├── di/             # Feature-level dependency injection
    │   ├── domain/         # Entities, usecases, abstract repos
    │   ├── presentation/   # BLoC, pages, widgets
    │   ├── cart_registry.dart
    │   └── cart.dart
    ├── products/           # Same structure
    ├── orders/             # Same structure
    ├── auth/               # Same structure
    └── ...
```

---

## 🌍 Multi-Market Architecture

One of the core technical challenges was making a single codebase support 4 fully independent markets cleanly.

```
MarketConfig
├── Saudi Arabia 🇸🇦  → SAR · Arabic/English · SA catalog
├── Yemen 🇾🇪         → YER · Arabic · YE catalog  
├── Oman 🇴🇲          → OMR · Arabic/English · OM catalog
└── UAE 🇦🇪           → AED · Arabic/English · UAE catalog
```

- Each market has its own **currency**, **language defaults**, and **product catalog**
- Switching markets resets the relevant BLoC state and re-fetches market-specific data
- Guest cart is stored locally and scoped per market

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| Framework | Flutter 3.x |
| Language | Dart |
| State Management | BLoC + Cubit |
| Architecture | Clean Architecture |
| Backend | REST API (external team) |
| Local Storage | Shared Preferences + SQLite |
| UI Effects | BackdropFilter · Glass morphism |
| Animations | Flutter Animations + Hero |
| Notifications | Firebase Cloud Messaging |
| RTL | Full Arabic support |

---

## 👨‍💻 Developer

**Ahmed Gamil** — Flutter Developer & AI Systems Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ahmed%20Gamil-0077B5?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ahmed-gamil-630980218/)

---

<div align="center">
  <sub>This repository contains screenshots and documentation only. Source code is proprietary.</sub>
</div>
