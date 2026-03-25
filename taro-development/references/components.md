# Taro Components

## Usage
All components must be imported from `@tarojs/components`.

```javascript
import { View, Text, Swiper, SwiperItem, ScrollView, Image } from '@tarojs/components'
```

## Event Handling
- Events use camelCase and start with `on`. (e.g., `onClick`, `onScroll`).
- In React, click is `onClick`. In Vue, it's `@tap` or `@click`.
- Taro implements its own event system simulating DOM events. `e.stopPropagation()` works for standard bubbling.
- **Scroll Penetration**: To prevent scroll penetration on overlays, use the `catchMove` attribute on the `<View>` component: `<View catchMove></View>`.

## dataset
- You can use `data-*` attributes. They are accessed via `event.target.dataset` or `event.currentTarget.dataset` in event handlers.
