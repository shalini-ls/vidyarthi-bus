# 🚌 Vidyarthi-Bus

> **Live bus crowd monitoring app for college students in Karnataka**

A real-time Android application that allows students across 5 major Karnataka cities to check live crowd levels of college buses before the bus arrives, report current crowd status with one tap, and find alternative transport contacts.

---

## 📱 Features

| Feature | Description |
|---|---|
| **Splash Screen** | Animated bus logo with app branding |
| **Student Login** | Name, city, college selection with Firebase registration |
| **Home Dashboard** | Personalized greeting, college routes, live stats |
| **Route Browser** | Filter by city, see all active routes with crowd levels |
| **Live Crowd Meter** | Green/Yellow/Red real-time crowd indicators |
| **One-Tap Reporting** | Report Empty/Medium/Full with a single tap |
| **Real-Time Sync** | Firebase Realtime Database for instant updates across all users |
| **Auto Refresh** | Status updates every 10 seconds |
| **Alt Transport** | City-specific alternative transport contacts with tap-to-call |
| **Admin Panel** | Add/edit/delete routes, toggle active status |
| **Bottom Navigation** | Home, Routes, Contacts, Profile tabs |
| **Location Support** | Location permissions for future GPS features |
| **Share Feature** | Share bus status via WhatsApp, etc. |
| **Material Design** | Modern Material Components UI throughout |

---

## 🏙️ Supported Cities & Colleges

- **Mysore**: JSS College, University of Mysore, NIE, SJCE, Mysore Medical College
- **Shivamogga**: Kuvempu University, Sahyadri College, JNNCE, PES College
- **Davanagere**: Bapuji Institute, SDM College, DBIT, Davanagere University
- **Hassan**: HIMS, PESIT, VTU Hassan, Hassan Engineering College
- **Mangalore**: St Aloysius, NITK Surathkal, Manipal University, SDM Medical

---

## 🔧 Setup Instructions

### 1. Firebase Setup (Required)

1. Go to [Firebase Console](https://console.firebase.google.com)
2. Create a new project named **"Vidyarthi-Bus"**
3. Add an Android app with package name: `com.vidyarthi.bus`
4. Download the `google-services.json` file
5. Replace the placeholder file at `app/google-services.json`
6. Enable **Realtime Database** in Firebase Console
7. Set database rules from `firebase-database-rules.json`

### 2. Open in Android Studio

1. Open Android Studio
2. Select **File → Open** and navigate to the `Vidyarthi-Bus/` folder
3. Wait for Gradle sync to complete
4. Click **Run** (▶️) to build and deploy

### 3. Admin Access

- On the login screen, tap **"Admin? Login here"**
- Password: `admin@vbus2024`
- Admin can add/edit/delete routes

---

## 📁 Project Structure

```
Vidyarthi-Bus/
├── app/
│   ├── build.gradle
│   ├── google-services.json
│   ├── proguard-rules.pro
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── java/com/vidyarthi/bus/
│       │   ├── activities/
│       │   │   ├── SplashActivity.kt
│       │   │   ├── LoginActivity.kt
│       │   │   ├── MainActivity.kt
│       │   │   ├── BusDetailActivity.kt
│       │   │   └── AdminActivity.kt
│       │   ├── adapters/
│       │   │   ├── BusRouteAdapter.kt
│       │   │   └── ContactAdapter.kt
│       │   ├── fragments/
│       │   │   ├── HomeFragment.kt
│       │   │   ├── RoutesFragment.kt
│       │   │   ├── ContactsFragment.kt
│       │   │   └── ProfileFragment.kt
│       │   ├── models/
│       │   │   ├── BusRoute.kt
│       │   │   ├── Student.kt
│       │   │   ├── CrowdReport.kt
│       │   │   └── TransportContact.kt
│       │   └── utils/
│       │       ├── Constants.kt
│       │       ├── Extensions.kt
│       │       ├── FirebaseSeeder.kt
│       │       └── PrefsManager.kt
│       └── res/
│           ├── layout/          (12 XML layouts)
│           ├── drawable/        (vector icons, shapes, gradients)
│           ├── navigation/      (nav_graph.xml)
│           ├── menu/            (bottom_nav_menu.xml)
│           ├── anim/            (animations)
│           ├── values/          (colors, strings, themes)
│           ├── font/            (Inter Regular/Bold)
│           └── xml/             (backup rules)
├── build.gradle
├── settings.gradle
├── gradle.properties
├── gradlew.bat
├── firebase-database-rules.json
└── README.md
```

---

## 🎨 Crowd Level Colors

| Level | Color | Emoji | Meaning |
|---|---|---|---|
| Empty | 🟢 `#10B981` | 🟢 | Seats freely available |
| Medium | 🟡 `#F59E0B` | 🟡 | Filling up, some seats left |
| Full | 🔴 `#EF4444` | 🔴 | No seats, bus is full |
| Unknown | ⚪ `#9CA3AF` | ⚪ | No reports yet |

---

## 🛠 Tech Stack

- **Language**: Kotlin
- **UI**: Material Design Components
- **Backend**: Firebase Realtime Database
- **Navigation**: Jetpack Navigation Component
- **Architecture**: View Binding + SharedPreferences
- **Min SDK**: 24 (Android 7.0)
- **Target SDK**: 34 (Android 14)

---

## 📝 License

This project is for educational purposes. Built for Karnataka college students.
