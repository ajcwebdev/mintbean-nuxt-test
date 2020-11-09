# Outline

* Yarn
  * Create Nuxt App
  * Setup Questions
  * Navigate into project and start dev server
* NPM
  * Create Nuxt App
  * Setup Questions
  * Navigate into project and start dev server
* Commit to Git
* Nuxt App
  * Delete boilerplate
  * Home Page
  * About Page
  * Navigation Bar in Layouts
  * `netlify.toml` for Deploying to Netlify

# Yarn

## Create Nuxt App

```bash
yarn create nuxt-app mintbean-nuxt
```

## Setup Questions

```bash
? Project name: (mintbean-nuxt)
? Programming language: JavaScript
? Package manager: Yarn
? UI framework: None
? Nuxt.js modules: None
? Linting tools: None
? Testing framework: None
? Rendering mode: Universal (SSR / SSG)
? Deployment target: Static (Static/JAMStack hosting)
? Development tools: None
? What is your GitHub username?: ajcwebdev
? Version control system: Git
```

## Navigate into project and start dev server

```bash
cd mintbean-nuxt
code .
yarn dev
```

# NPM

## Create Nuxt App

```bash
npx create-nuxt-app mintbean-nuxt
```

## Setup Questions

```bash
? Project name: (mintbean-nuxt)
? Programming language: JavaScript
? Package manager: Npm
? UI framework: None
? Nuxt.js modules: None
? Linting tools: None
? Testing framework: None
? Rendering mode: Universal (SSR / SSG)
? Deployment target: Static (Static/JAMStack hosting)
? Development tools: None
? What is your GitHub username?: ajcwebdev
? Version control system: Git
```

## Navigate into project and start dev server

```bash
cd mintbean-nuxt
code .
npm run dev
```

# Commit to Git

```bash
git add .
git commit -m "First commit"
git branch -M main
```

Create a repo on GitHub called `mintbean-nuxt` and then enter these commands:

```bash
git remote add origin https://github.com/ajcwebdev/mintbean-nuxt.git
git remote -v
git push -u origin main
```

# Nuxt App

## Delete boilerplate
* `assets`
* `middleware`
* `plugins`
* `store`
* `Logo.vue` in `components` folder

## Home Page

```html
// pages/index.vue

<template>
  <div class="container">

    <div>
      <h1 class="title">ajcwebdev</h1>

      <div class="links">
        <a
          href="https://dev.to/ajcwebdev"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Blog
        </a>
        <a
          href="https://github.com/ajcwebdev"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>

    </div>

  </div>
</template>
```

## About Page

```html
// pages/about.vue

<template>
  <div class="container">

    <div>
      <h1 class="title">About</h1>
      <p>This page tells you about stuff</p>
    </div>

  </div>
</template>
```

## Navigation Bar in Layouts

```html
// layouts/default.vue

<template>
  <div>
    <ul>
      <li>
        <NuxtLink to="/">Home</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about">About</NuxtLink>
      </li>
    </ul>

    <Nuxt />
  </div>
</template>
```

## `netlify.toml` for Deploying to Netlify

```toml
[build]
  publish = "dist/"
  command = "nuxt generate"
```

```bash
git add .
git commit -m "Wooooooo!!!"
git push origin
```
