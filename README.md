# Tibia Android Game

A 2D top-down RPG inspired by Tibia, built with **libGDX** (Java) for Android.

## Features

- Tile-based map with grass, dirt, water, trees, walls, and buildings
- Player movement (WASD / arrow keys / on-screen controls planned)
- Monsters that chase and attack the player
- Combat system (click to attack nearby monsters)
- Leveling system with HP, mana, and experience
- HUD showing health, mana, and stats

## Build

### Debug APK

```bash
./gradlew android:assembleDebug
```

APK output: `android/build/outputs/apk/debug/`

### Release APK

```bash
./gradlew android:assembleRelease
```

## GitHub Actions

Every push to `master` triggers a CI build that produces a debug APK as a downloadable artifact.

## Controls

| Key | Action |
|-----|--------|
| W / Up | Move up |
| S / Down | Move down |
| A / Left | Move left |
| D / Right | Move right |
| Left Click | Attack nearby monsters |
| ESC | Exit game |

## Project Structure

```
tibia-android-game/
├── core/                   # Game logic (cross-platform)
│   └── src/main/java/com/tibiagame/
│       ├── TibiaGame.java  # Main game class
│       ├── GameScreen.java # Main game screen & rendering
│       ├── GameMap.java    # Tile map generation & rendering
│       ├── Player.java     # Player entity
│       ├── Monster.java    # Monster AI & combat
│       └── Tiles.java      # Tile type constants
├── android/                # Android-specific code
│   └── src/main/java/com/tibiagame/android/
│       └── AndroidLauncher.java
├── .github/workflows/      # CI/CD pipeline
└── build.gradle            # Root build config
```

## Tech Stack

- **libGDX 1.12.1** — cross-platform game framework
- **Java 8** — language
- **Gradle 8.5** — build system
- **Android SDK 34** — target platform
