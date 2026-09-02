# Matix the Math Club — Workspace & Multi-Platform Project Structure

This workspace contains the complete codebase, assets, multi-platform native client projects, and standalone web application for **Matix the Math Club**.

---

## 📁 Repository & Directory Layout

```text
├── app.html                  # Main Web Application & core frontend UI (Single-Page App)
├── temp/                     # Shared distribution & staging folder
│   └── app.html              # Synchronized snapshot used during multi-platform builds
│
├── Matix the Math Club Android/
│   ├── app/
│   │   └── src/main/
│   │       ├── assets/       # Embedded web assets (app.html sync destination)
│   │       └── java/club/matix/mathclub/
│   │           ├── ai/       # Matix AI Engine (MatixAi.kt)
│   │           └── ui/       # Design tokens, theme system (MatixTheme.kt)
│   ├── build.gradle.kts      # Gradle build configuration
│   └── settings.gradle.kts
│
├── Matix the Math Club iOS/
│   ├── Matix the Math Club/
│   │   ├── Ai/               # Matix AI Engine (MatixAI.swift)
│   │   ├── Ui/               # SwiftUI Design System & Theme (MatixTheme.swift)
│   │   └── WebShell.swift    # WebKit container loading app.html
│   ├── Matix the Math Club.xcodeproj
│   └── sync-app.js           # Build synchronization script
│
├── Matix the Math Club macOS/
│   ├── .github/workflows/    # CI/CD Workflows (build-mac.yml)
│   ├── Matix the Math Club/
│   │   ├── Ai/               # Matix AI Engine (MatixAI.swift)
│   │   └── Ui/               # App theme & native UI tokens
│   ├── Matix the Math Club.xcodeproj
│   └── package.json          # Electron / packaging configuration
│
└── Matix the Math Club Windows/
    ├── .github/workflows/    # CI/CD Workflows (build-installer.yml)
    ├── MatixTheMathClub/
    │   ├── Ai/               # Matix AI Engine (MatixAi.cs)
    │   ├── Ui/               # WPF / XAML theme & styling (MatixTheme.cs)
    │   ├── App.xaml / MainWindow.xaml
    │   └── MatixTheMathClub.csproj
    ├── installer-config.iss  # Inno Setup Windows installer config
    └── Matix the Math Club.sln
