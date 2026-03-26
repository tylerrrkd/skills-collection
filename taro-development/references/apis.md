# Taro APIs

## Overview
All APIs are accessed via the `Taro` object, imported from `@tarojs/taro`.

Key concepts and conventions:
- **Specification**: Taro APIs primarily follow the WeChat Mini-Program specification.
- **Unified Namespace**: All APIs are unified under the `Taro` namespace to ensure cross-platform compatibility (e.g., mapping Ali's `my.alert` to `Taro.showModal`).
- **Promisification**: Taro automatically "promisifies" asynchronous APIs, allowing them to be used with standard `Promise` syntax or `async/await`.
- **Native APIs**: For platform-specific APIs not yet adapted by Taro, developers can use the native platform namespace directly.

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
