# Expo Maestro Sandbox

An example repo demonstrating testing an Expo app using Maestro, both locally and on GitHub Actions.

## Requirements

- Node
- Xcode
- Android Studio
- Maestro

## Installation

```bash
npm install
```

## Building Dev Client

```bash
npm run ios
```

or

```bash
npm run android
```

## Running

```bash
npm start
```

Then press `a` or `i`

## Testing

Run the app in either the iOS Simulator or Android Emulator using the steps above.

```bash
maestro test .maestro/*.yaml
```

## CI

Maestro tests run on GitHub Actions on open PRs.
