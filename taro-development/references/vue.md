# Vue in Taro

## Overview
Taro supports both Vue 2 and Vue 3.

## Entry and Pages
- **Entry Component (`app.js`)**: Exports a Vue instance configuration. It shouldn't render UI, only block or slot.
- **Page Component**: A standard Vue component. It also supports mini-program lifecycle hooks like `onShow`, `onHide`, `onReady`.

## Built-in Components
- Use kebab-case for Taro components in Vue templates: `<picker-view indicator-class="myclass" />`.
- Do not use HTML tags like `div` or `span` unless using specific H5 configurations.

## State Management
Vuex and Pinia are supported. Configure them in `app.js` and inject them into the Vue instance.
