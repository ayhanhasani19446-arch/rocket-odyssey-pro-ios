# Rocket Odyssey Pro - iOS App

A Capacitor-based iOS wrapper for the **Rocket Odyssey Pro** HTML game.

## Project Structure

```
├── www/
│   └── index.html          # The game (self-contained, all assets embedded)
├── ios/
│   └── App/
│       ├── App/
│       │   ├── AppDelegate.swift
│       │   ├── Info.plist
│       │   ├── Assets.xcassets/
│       │   │   └── AppIcon.appiconset/
│       │   └── Base.lproj/
│       │       ├── Main.storyboard
│       │       └── LaunchScreen.storyboard
│       ├── App.xcodeproj/
│       │   └── project.pbxproj
│       ├── App.xcworkspace/
│       └── Podfile
├── package.json
├── capacitor.config.json
├── codemagic.yaml
└── .gitignore
```

## Build with Codemagic

1. Push this repository to GitHub
2. Connect the repo to [Codemagic](https://codemagic.io)
3. Codemagic will auto-detect `codemagic.yaml`
4. Configure Apple Developer code signing in Codemagic
5. Start build → get IPA!

### Bundle ID
```
com.rocketodyssey.pro
```

## Local Build

```bash
npm install
npx cap sync ios
cd ios/App
pod install
# Open App.xcworkspace in Xcode
open App.xcworkspace
```

## Tech Stack

- Capacitor 6.x
- iOS Deployment Target: 14.0
- Swift 5
- Pure HTML5 game (no frameworks)
