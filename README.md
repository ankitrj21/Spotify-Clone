# Spotify: UI Clone with React Native / Expo
<p align="center">
  <img src="screenshots/screenshare-4.jpg?raw=true" />
</p>

## Table of Contents

- [Install & Build](#install--build)
- [Features](#features)
- [Linting](#linting)
- [Expo Web](#expo-web)
- [Release Notes](#release-notes)

## Install & Build

First, make sure you have Expo CLI installed: `npm install -g expo-cli`

**Install:**

```bash
yarn
```

**Run Project Locally:**

```bash
yarn dev
```

## Features

- Expo SDK 48
- iOS, Android and PWA (Web App)
- React Navigation v6
- React Context
- PropTypes

## Linting

- run: `yarn lint` for a list of linting warnings/error in cli
- prettier and airbnb config
- make sure you have [prettier package](https://atom.io/packages/prettier-atom) installed on your atom/vscode editor
- then make sure to enable these options (packages → prettier):
  - eslint integration
  - stylelint integration
  - automatic format on save (toggle format on save)
- be aware of the `.prettierignore` file

**Update Linting Packages:**

```
yarn add @babel/core eslint-config-airbnb eslint-config-prettier eslint-plugin-import eslint-plugin-import-helpers eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks eslint-plugin-react-native prettier --dev
```


**Dev with Expo Web**

- Remove node_modules if they exist: `rm -rf nodes_modules`
- Install/Re-install: `yarn`
- Start development: `yarn web` or `expo start --web`
- Build PWA: `yarn web-build` or `expo build:web`

a couple manual changes within `index.html` i found needed to be made so far:

- **to make splash screen work:** "mobile-web-app-capable" => "apple-mobile-web-app-capable"
- **status bar transparent:** apple-mobile-web-app-status-bar-style="default" => "black-translucent"
- **no white background:** add background color within body{background-color: #121212; ...}
- **check output meta:** double image meta tags
- **check output js:** double/triple js packages

## Release Notes

**version 0.5.0 (current)**

- upgraded to [Expo SDK 48](https://blog.expo.dev/expo-sdk-48-ccb8302e231)
- upgraded to [Expo SDK 47](https://blog.expo.dev/expo-sdk-47-a0f6f5c038af)
- upgraded to [Expo SDK 46](https://blog.expo.dev/expo-sdk-46-c2a1655f63f7)
- upgraded to [Expo SDK 45](https://blog.expo.dev/expo-sdk-45-f4e332954a68)
- upgraded to [React Navigation v6](https://reactnavigation.org/docs/getting-started)
- upgraded to [React Navigation v5](https://reactnavigation.org/docs/5.x/getting-started)
- Removed ScreenProps for [React Context](https://reactjs.org/docs/context.html)

**version 0.4.0**

- upgraded to [Expo SDK 44](https://blog.expo.dev/expo-sdk-44-4c4b8306584a)
- upgraded to [Expo SDK 43](https://blog.expo.dev/expo-sdk-43-aa9b3c7d5541)
- upgraded to [Expo SDK 42](https://blog.expo.io/expo-sdk-42-579aee2348b6)

**version 0.3.0**

- upgraded to [Expo SDK 41](https://blog.expo.io/expo-sdk-41-12cc5232f2ef)
- upgraded to [Expo SDK 40](https://blog.expo.io/expo-sdk-40-is-now-available-d4d73e67da33)
- upgraded to [Expo SDK 39](https://blog.expo.io/expo-sdk-39-is-now-available-4c10aa825e3f)
- upgraded to [Expo SDK 38](https://blog.expo.io/expo-sdk-38-is-now-available-ab6cd30ca2ee)

**version 0.2.0**

- upgraded to [React Navigation v4](https://reactnavigation.org/docs/4.x/getting-started)
- upgraded to [Expo SDK 37](https://blog.expo.io/expo-sdk-37-is-now-available-dd5770f066a6)
- upgraded to [Expo SDK 36](https://blog.expo.io/expo-sdk-36-is-now-available-b91897b437fe)
- upgraded to [Expo SDK 35](https://blog.expo.io/expo-sdk-35-is-now-available-beee0dfafbf4)

**version 0.1.0**

- Expo Web support
- upgraded to [Expo SDK 34](https://blog.expo.io/expo-sdk-34-is-now-available-4f7825239319)
- upgraded to [Expo SDK 33](https://blog.expo.io/expo-sdk-v33-0-0-is-now-available-52d1c99dfe4c)
- started with [React Navigation v3](https://reactnavigation.org/docs/3.x/getting-started)
- iOS and Android
- Tab Navigation (stacks created)
  - Home
    - Horizontal Album component
    - Album Screen
      - animation opacity on header
      - scroll sticky of shuffle button
      - current song playing shows in album list view
      - blur view
      - SafeAreaView example
      - action list with supporting icons
    - Header animation on scroll event
      - animation opacity on iPhoneX notch
      - animation opacity on cog icon
  - Search
    - Sticky search bar (animated width)
    - Playlists sections added (with mock data)
  - Library
    - Menu items from mock data
  - Custom Bar for Music Player added to `<BottomTabBar />`
- Modals (bottom to top)
  - Music Player
