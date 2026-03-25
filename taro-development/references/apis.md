# Taro APIs

## Overview
All APIs are accessed via the `Taro` object, imported from `@tarojs/taro`.

```javascript
import Taro from '@tarojs/taro'
```

## Common APIs
- **Network Request**: `Taro.request({ url, data, method, ... })` returns a Promise.
- **Routing**:
  - `Taro.navigateTo({ url })`: Pushes a new page.
  - `Taro.redirectTo({ url })`: Replaces the current page.
  - `Taro.switchTab({ url })`: Switches to a tabbar page.
  - `Taro.navigateBack({ delta })`: Goes back.
- **UI Interaction**:
  - `Taro.showToast({ title, icon, duration })`
  - `Taro.showLoading({ title })` and `Taro.hideLoading()`
  - `Taro.showModal({ title, content })`
- **Storage**:
  - `Taro.setStorageSync(key, data)`
  - `Taro.getStorageSync(key)`
