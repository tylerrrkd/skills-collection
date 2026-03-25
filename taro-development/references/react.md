# React in Taro

## Imports
React APIs must be imported from the `react` package, not from Taro.
```javascript
import React, { useState, useEffect, Component } from 'react'
```

## Lifecycle Mapping
- `componentWillMount()`: Triggered after `onLoad`, before the page component renders to Taro's virtual DOM.
- `componentDidMount()`: Triggered after rendering to Taro's virtual DOM. Note: `createSelectorQuery` cannot be used here to get mini-program layer DOM nodes. Use it in `onReady`.
- Mini-program page events (e.g., `onPullDownRefresh`, `onReachBottom`, `onShareAppMessage`) can be used as methods in Class components, or via Hooks in Functional components (e.g., `usePullDownRefresh`).

## Hooks
Taro provides custom hooks for mini-program lifecycles (imported from `@tarojs/taro`):
- `useLoad(options)`: Equivalent to `onLoad`.
- `useReady()`: Equivalent to `onReady`. Use this to safely query DOM nodes.
- `useDidShow()` / `useDidHide()`: Equivalent to `onShow` / `onHide`.
- `useShareAppMessage(res)`: Equivalent to `onShareAppMessage`.

## Caveats
- `dangerouslySetInnerHTML`: Has specific configurations in mini-programs. It uses `RichText` under the hood.
- Error "Minified React error #152": Taro uses production React by default. Enable `mini.debugReact` in compilation config to see development stack traces.
