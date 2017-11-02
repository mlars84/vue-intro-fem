# Introduction to Vue Workshop Materials

Starter Materials for Introduction to Vue.js Workshop
Author: Sarah Drasner

This repo houses the materials and resources for the Introduction to Vue.js. Most of the materials for the course are outlined below, but there are also directories housed here of very basic examples of some of the techniques we will cover so that students don't have to spend a lot of time researching in order to get started. It is recommended that students use CodePen to create work for the duration of the course, as we'll use preprocessors like SCSS as well as Babel for ES6, and resources like Vue.js, both prod and dev versions, codepen makes it easy to do so without time devoted to setup. If you like, you can also scroll to the CodePen collection section and fork one of the existing pens in those collections, they are comprehensive. There are more true-to-life build process examples, in the VueCLI, Nuxt, and Vuex Resource Sections. It's encouraged to watch the lecture to learn how to set up the builds yourself, though.

Here are the [Vue chrome devtools](https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd?hl=en)

Here is the codepen debugger [chrome extension](https://chrome.google.com/webstore/detail/codopen/agnkphdgffianchpipdbkeaclfbobaak)

Here are the snippets I'll be using [vue sublime snippets](https://github.com/sdras/vue-sublime-snippets)

For sections covering Nuxt, we will be using the directories listed in the Nuxt section below as well as their directories, prefixed with `nuxt-` here.

## Slides:
* [Intro to Vue 1: Directives & Data Rendering](http://slides.com/sdrasner/intro-to-vue-1?token=9-aFNhlX)
* [Intro to Vue 2: Methods, Computed, Watchers](http://slides.com/sdrasner/intro-to-vue-2?token=502n2b7V)
* [Intro to Vue 3: Components, Slots](http://slides.com/sdrasner/intro-to-vue-3?token=LwIVIblm)
* [Intro to Vue 4: Vue CLI & Nuxt](http://slides.com/sdrasner/intro-to-vue-4?token=Xb4oA4YR)
* [Intro to Vue 5: Vue Animations](http://slides.com/sdrasner/intro-to-vue-5?token=5zRhIuNg)
* [Intro to Vue 6: Filters, Mixins, & Custom Directives](http://slides.com/sdrasner/intro-to-vue-6?token=fcL8qgTg)
* [Intro to Vue 7: Vuex](http://slides.com/sdrasner/intro-to-vue-7?token=u9qUgRsW)

All slides have password `!vue!`

## Collections:
* [Vue Workshop Materials Collection](https://codepen.io/collection/noYZxW/)
* [Vue Animation Collection](https://codepen.io/collection/XQGkeV/)

Included in this repo are some very basic starter kits. 

## VueCLI Resources
* [Vue-CLI](https://github.com/vuejs/vue-cli)
* [Wine Label Maker Demo](https://github.com/sdras/vue-wine-label)

There's a directory you can use as a Vue-CLI starter kit:
* setup1

## Nuxt Resources
* [Nuxt Docs](https://nuxtjs.org/)
* [Nuxt Type Demo](https://github.com/sdras/nuxt-type)

There are directories you can use as Nuxt starter kits:
* setup2
* nuxt-css-animation-starter
* nuxt-js-animation-starter
* nuxt-fixed-transition-modes

## Vuex Resources
* [Vuex docs](https://vuex.vuejs.org/en/)
* [Vue Weather Notifier Demo](https://github.com/sdras/vue-weather-notifier)

There's a directory you can use as a Vuex starter kit:
* vuex-example

Here are the directories for the Vuex exercise:
* commentform-problem
* commentform-solution

## License

[![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)

## Notes
- Why Vue
  - Declarative
  - Legible
  - Easy to Maintain
  - Powerful
  - A collection of the best of the best
  - Elegant
  - Gives you want you want when you need it, and gets out of your way
  - A way to be really productive
  - Fun
- Compared to other frameworks
  - A virtual DOM
  - Reactive components that offer the View layer only
  - Props and Redux-like store similar to React
  - Conditional rendering and services, similar to Angular
  - Inspired by Polymer for simplicity and performance, Vue offers a similar development style as HTML, styles and JS are composed in tandem
  - slightly better performance than React, no use of polyfills like Polymer and an isolated, less opinionated view than 
  Angular which is an MVC.
  
  ### Directives
  - `v-text, v-html, v-show, v-if, v-else, v-else-if, v-for, v-on, v-bind, v-model, v-pre, v-cloak, v-once`
  - `v-for`
    - Loops through a set of values (aka item in items). Can also do a static number.
  - `v-model`
    - Creates a relationship between the data in the instance/component and a form input, so you can dynamically update values
