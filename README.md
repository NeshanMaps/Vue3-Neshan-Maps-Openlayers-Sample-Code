# Vue3 Neshanmap Openlayers Usage Code

این پروژه به این دلیل ساخته شده تا به شما نحوه استفاده‌ی پایه‌ای از نقشه 
[vue3-openlayers نشان](https://www.npmjs.com/package/@neshan-maps-platform/vue3-openlayers)
نمایش بدهد.

توجه: جهت مطالعه مستندات کامل مربوط به [استفاده از سرویسهای نقشه نشان در Vue.js اینجا کلیک کنید.](https://platform.neshan.org/sdk/%DA%A9%D8%A7%D9%85%D9%BE%D9%88%D9%86%D9%86%D8%AA-vuejs-3-openlayers/)

## ⚙️پیش از راه اندازی
برای استفاده از نقشه، شما نیاز به 
[کلید های دسترسی](https://platform.neshan.org/panel/api-key) 
دارید.
همچنین برای استفاده از سرویس های سرچ و ریورس نقشه به کلید service
نیاز دارید.

پس از گرفتن آن‌ها از [وبسایت](https://platform.neshan.org/panel/api-key)
،
کلید نقشه و در صورت نیاز،
کلید service
را در فایل src/App.vue
به جای YOUR_MAP_KEY
و
YOUR_SERVICE_KEY
قرار دهید.
## 📦 راه اندازی
ابتدا پکیج‌های مورد استفاده پروژه را نصب کنید:
```bash
npm install
```
یا
```bash
yarn
```
سپس پروژه را در حالت توسعه، شروع کنید:
```bash
npm run dev
```
یا
```bash
yarn dev
```

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Type Support For `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin) to make the TypeScript language service aware of `.vue` types.

If the standalone TypeScript plugin doesn't feel fast enough to you, Volar has also implemented a [Take Over Mode](https://github.com/johnsoncodehk/volar/discussions/471#discussioncomment-1361669) that is more performant. You can enable it by the following steps:

1. Disable the built-in TypeScript Extension
   1. Run `Extensions: Show Built-in Extensions` from VSCode's command palette
   2. Find `TypeScript and JavaScript Language Features`, right click and select `Disable (Workspace)`
2. Reload the VSCode window by running `Developer: Reload Window` from the command palette.
