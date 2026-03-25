---
name: taro-development
description: Use when building, debugging, or configuring a Taro application. Covers project setup, cross-platform compilation, framework selection (React/Vue), and UI component usage.
---

# Taro Development

## Overview
Taro is an open cross-platform, cross-framework solution that supports using React, Vue, Nerv, etc. to develop applications for WeChat Mini Programs, H5, React Native, and other mini-program platforms with a single codebase.

## Quick Start
- **CLI Commands**:
  - Init: `taro init myApp`
  - Dev mode (watch): `npm run dev:weapp` (or `h5`, `alipay`, `swan`, `tt`, `rn`)
  - Build mode: `npm run build:weapp`

## Core Concepts
- **App Configuration (`app.config.js`)**: Global configuration for pages, window, tabbar, etc.
- **Page Configuration (`index.config.js`)**: Configuration specific to a page (e.g., `navigationBarTitleText`).
- **Components**: Do not use `div`/`span`. Always use cross-platform components from `@tarojs/components` (e.g., `<View>`, `<Text>`, `<Image>`).
- **APIs**: Access device and platform features via the global `Taro` object (e.g., `Taro.request`, `Taro.navigateTo`).

## Framework Specifics
Choose the appropriate reference guide based on the framework being used:

- **React in Taro**: See [references/react.md](references/react.md) for React-specific lifecycle mapping, hooks, and caveats.
- **Vue in Taro**: See [references/vue.md](references/vue.md) for Vue-specific usage.

## Components & APIs Reference
- **Built-in Components**: See [references/components.md](references/components.md) for event handling, styling, and common components.
- **Taro APIs**: See [references/apis.md](references/apis.md) for networking, routing, and system APIs.

## Multi-platform Development
- Use `process.env.TARO_ENV` (e.g., `weapp`, `h5`, `rn`) to conditionally execute code for specific platforms.
- You can create platform-specific files like `api.weapp.js` and `api.h5.js`, and import them as `api.js`. Taro will automatically resolve the correct file based on the target platform.
