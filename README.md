# Welcome to svelte-kit-demo 👋

![Version](https://img.shields.io/badge/version-0.0.1-blue.svg?cacheSeconds=2592000)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](#)
[![Twitter: jellydn](https://img.shields.io/twitter/follow/jellydn.svg?style=social)](https://twitter.com/jellydn)

> Simple setup with Svelte-kit with tailwind,graphql and deployment to Vercel/Firebase

[![Svelte Kit - NextJs for Svelte](https://img.youtube.com/vi/p5RJdCk09SM/0.jpg)](https://www.youtube.com/watch?v=p5RJdCk09SM)

## 🏠 [Homepage](https://svelte-kit-test.web.app/)

### ✨ [Demo](https://svelte-kit-test.vercel.app/)

## Build with

- [svelte-kit](https://svelte.dev/blog/whats-the-deal-with-sveltekit)
- [tailwindcss](https://tailwindcss.com/)
- [svelte-adders](https://github.com/svelte-add/svelte-adders)

## Install

```sh
yarn install
```

## Usage

```sh
yarn dev
```

## Deploy to Firebase

Change adapter to `static` on `svelte.config.js` file.

```ts
import adapter from '@sveltejs/adapter-static';
```

```sh
yarn build
yarn deploy
```

## Deploy to Vercel

Change adapter to `vercel` on `svelte.config.js` file.

```ts
import adapter from '@sveltejs/adapter-vercel';
```

```sh
# you need to have `vercel` install globally
# need to change output folder on vercel deployment to `/build`
yarn build
vercel
```

## Author

👤 **Dung Huynh (Kaka)**

- Website: https://productsway.com/
- Twitter: [@jellydn](https://twitter.com/jellydn)
- Github: [@jellydn](https://github.com/jellydn)

## Stargazers

[![Stargazers repo roster for @jellydn/svelte-kit-demo](https://reporoster.com/stars/jellydn/svelte-kit-demo)](https://github.com/jellydn/svelte-kit-demo/stargazers)

## Show your support

Give a ⭐️ if this project helped you!

---

_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_
