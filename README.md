# Folio

A minimal, beautiful Android reading tracker. Manage your personal library, track reading progress, and discover what to read next.

---

## Overview

Folio is an offline first reading app for people who want a clean and private way to manage their books. No accounts, no cloud, no distractions. Everything stays on your device.

Built with React Native and Expo, it uses SQLite as the main database so everything works smoothly even without internet.

---

## Features

- Add books with covers, ratings, notes, and tags
- Track reading status like not started, reading, and finished
- Search and filter your library
- Pick a random next book with animation
- Set yearly reading goals
- View reading statistics and genre breakdown
- Export your library as JSON or CSV
- Fully offline usage, no data leaves your device

---

## Tech Stack

- React Native with Expo SDK 56
- Expo Router for navigation
- SQLite with expo-sqlite
- Drizzle ORM for database management
- React Query for async data handling
- Zustand for UI state
- React Native Reanimated for animations
- FlashList for fast list rendering

---

## Getting Started

### Clone the project

```bash
git clone https://github.com/darshan-regmi/folio.git
cd folio
```

### Install dependencies

```bash
pnpm install
```

### Start the app

```bash
pnpm start
```

### Run on Android

```bash
pnpm android
```

---

## Requirements

- Node.js 20 or higher
- pnpm 9 or higher
- Android Studio with SDK 34
- Expo CLI

```bash
pnpm add -g expo-cli
```

- EAS CLI for builds

```bash
pnpm add -g @expo/eas-cli
```

---

## Database Setup

Generate migrations

```bash
pnpm drizzle-kit generate
```

If something breaks with migrations

```bash
rm -rf src/db/migrations
pnpm drizzle-kit generate
```

---

## Building the App

### Development build

```bash
eas build --platform android --profile development
```

### Production build

```bash
eas build --platform android --profile production
```

### Local Android build

```bash
npx expo prebuild --platform android --clean
cd android
./gradlew assembleRelease
```

---

## Environment Variables

Create a .env file in the root

```
EXPO_PUBLIC_APP_VERSION=1.0.0
```

No API keys are required. The app runs completely offline.

---

## Screenshots

Add screenshots after first build

| Home  | Library | Book Detail | Picker |
| ----- | ------- | ----------- | ------ |
| ![]() | ![]()   | ![]()       | ![]()  |

---

## Troubleshooting

Metro not starting

```bash
pnpm start --clear
```

Drizzle migration issues

- Delete src/db/migrations
- Run generate again

FlashList blank screen

- Make sure estimatedItemSize is set

Image picker not working

- Check READ_MEDIA_IMAGES permission in app.config.ts

---

## Contributing

Fork the repo
Create a branch

```bash
git checkout -b feat/your-feature
```

Commit changes

```bash
git commit -m "feat: add new feature"
```

Push branch

```bash
git push origin feat/your-feature
```

Open a pull request

---

## Branch Structure

- **main** for production releases
- **develop** for ongoing work
- **feat** for new features
- **fix** for bug fixes
- **chore** for maintenance tasks

---

## Commit Style

Use conventional commits

```markdown
feat: add reading streak tracker
fix: cover image crash issue
chore: update dependencies
docs: improve readme
```

---

## License

MIT License. See LICENSE file for details.
