# Quick_Slides is a repo for quick HTML/ Markdown based slides

## Slidev

Links:
  * [Slidev - website](https://sli.dev/)
  * [Slidev - Github](https://github.com/slidevjs/slidev)
  * [@slidev/cli - npm](https://www.npmjs.com/package/@slidev/cli)

### Commands to open, edit, build, and deploy the slidev onto Github Pages

When opening the terminal:  

```bash
npm install
npm install --save @slidev/cli
npm install --save gh-pages
```

When starting a new slide deck:  

```bash
npm init slidev
```

When opening a slide deck:  

```bash
slidev --open

npx slidev --open

npm run dev
```

  * Visit <http://localhost:3030>
  * Edit the [slides.md](./slides.md) to see the changes.


```bash
slidev build --base /Quick_Slides/lewagon_cybozu/
 && cp -R ./img ./dist/img && node ./modIndex.js && gh-pages -d dist
```

### Customizations & Themes

[lightvue/slidev-theme-light-icons: A light and Elegant theme for Slidev](https://github.com/lightvue/slidev-theme-light-icons)
