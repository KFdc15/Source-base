# Vite + Vue 3 + TypeScript + Pinia + Tailwind

Dự án frontend dùng Vite, Vue 3 (TS), Pinia và Tailwind CSS v4.

## Yêu cầu
- Node.js ≥ 18 (khuyến nghị 20 LTS)
- npm ≥ 9

## Cài đặt & chạy
```powershell
# Cài dependencies
npm install

# Chạy dev server (mặc định: http://localhost:5173)
npm run dev
```

## Build & preview
```powershell
# Build production (ra thư mục dist/)
npm run build

# Xem thử bản build
npm run preview
```

## Công nghệ
- Vite 5
- Vue 3 + TypeScript
- Pinia (state management)
- Tailwind CSS v4 (+ @tailwindcss/postcss)

## Cấu trúc thư mục (rút gọn)
```
src/
  main.ts
  style.css
  stores/
    counter.ts
  views/
    HomePage.vue
index.html
vite.config.ts
```

## Ghi chú Tailwind v4
- Dùng PostCSS plugin: `@tailwindcss/postcss`
- Trong `postcss.config.(js|cjs|mjs)`:
```js
export default {
  plugins: {
    '@tailwindcss/postcss': {},
  },
};
```
- Trong `src/style.css`:
```css
@import "tailwindcss";
```
- Không cần `tailwind.config.js` trừ khi bạn muốn mở rộng theme.

## Pinia ví dụ nhanh
Store `src/stores/counter.ts`:
```ts
import { defineStore } from 'pinia';

export const useCounterStore = defineStore('counter', {
  state: () => ({ count: 0 }),
  getters: {
    double: (s) => s.count * 2,
  },
  actions: {
    inc() { this.count++; },
    reset() { this.count = 0; },
  },
});
```
Dùng trong component:
```vue
<script setup lang="ts">
import { useCounterStore } from '@/stores/counter';
const counter = useCounterStore();
</script>

<template>
  <button @click="counter.inc">Increment</button>
  <button @click="counter.reset">Reset</button>
  <p>{{ counter.count }} (x2 = {{ counter.double }})</p>
</template>
```