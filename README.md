# Expo Maestro Sandbox

An example repo demonstrating testing an Expo app using Maestro, both locally and on GitHub Actions.

Feel free to use this configuration as a basis for your own CI tests. Although it was written with Expo, Maestro and the tooling to set up simulators will likely work similarly for other mobile platforms.

## Notes and Limitations

- This configuration currently runs the tests on each push to an open PR, but this is not a restriction or necessarily a recommendation. It would not be difficult to change the config to run on a different cadence in your own project.
- Currently succeeding on macOS and Ubuntu instances available on the free GitHub Actions tier. On the professional project this is based on, we found we needed larger instances to avoid timeouts: `macos-latest-xlarge` and `ubuntu-latest-8-cores`
- Currently rebuilds the native client on each test run, which is slow. In the professional project this is based on, we are experimenting with caching the native client and injecting updated TS/JS into it, but it's not fully reliable yet.
- This trivial app doesn't make any network API connections, so this does not address mocking network requests.

## Requirements

- Node
- Xcode
- Android Studio
- EAS CLI
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
