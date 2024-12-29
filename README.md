# Expo Linking.getInitialURL() Inconsistent null return

This repository demonstrates a bug in Expo's `Linking.getInitialURL()` API where it inconsistently returns `null` even when the app is launched via a deep link. This makes handling deep links unreliable.

## Steps to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install` or `yarn install`.
3. Run the app on a physical device or emulator.
4. Launch the app using a deep link. Observe the behavior; sometimes the app logs the deep link URL, other times it logs 'null'.

## Expected Behavior
`Linking.getInitialURL()` should consistently return the deep link URL when the app is launched from it.

## Actual Behavior
`Linking.getInitialURL()` intermittently returns `null`, making it impossible to reliably process the deep link.

## Workaround
See `bugSolution.js` for a potential workaround.