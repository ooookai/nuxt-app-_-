# nuxt-app-_-

## This repository is for a [nuxt](https://github.com/nuxt/nuxt.js) issue report.

#### The reproduction steps:
1. run `yarn install`.
2. add an `app.vue` file in the `/pages/`.
3. run `yarn dev`, it works.
4. run `yarn generate`, everything looks good in the terminal.
5. run `yarn start`, the page is always in loading status.
6. and then you open the `/dist/index.html`, you can't see any .js file there.
7. if you remove the file `app.vue`. it works again.

#### IMO
- **So I guess there's a silent name conflict when you name an `app.vue` file as a page. Only in production mode.**

---

### The initial environment is created by `create nuxt-app`. 

#### Here're the options:
```
$ yarn create nuxt-app nuxt-app-_-

create-nuxt-app v3.2.0
✨  Generating Nuxt.js project in nuxt-app-_-
? Project name: nuxt-app-_-
? Programming language: JavaScript
? Package manager: Yarn
? UI framework: Tailwind CSS
? Nuxt.js modules: Axios, Progressive Web App (PWA)
? Linting tools: ESLint, Prettier
? Testing framework: None
? Rendering mode: Single Page App
? Deployment target: Static (Static/JAMStack hosting)
? Development tools: jsconfig.json

```