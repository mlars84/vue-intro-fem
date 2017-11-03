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
- Modifiers
  - `v-model.trim` will strip any leading or trailing whitespace from the bound string
  - `v-model.number` changes strings to number inputs
  - `v-model.lazy` won’t populate the content automatically, it will wait to bind until an event happens. (It listens to change events instead of input)
- `V-IF / V-SHOW`
  - a conditional that will display information depending on meeting a requirement. This can be anything- buttons, forms, divs, components. `v-if` completes unmounts/mounts an element and `v-show` toggle visibility with `display: none;`
- `V-IF/V-ELSE`
  - Pretty straightforward- you can conditionally render one thing or another. There's also `v-else-if`
- `V-BIND or :`
  - One of the most useful directives so there's a shortcut! We can use it for so many things- class and style binding, creating dynamic props, etc...
- `V-ONCE and V-PRE`
  - Not quite as useful, `v-once` will not update once it's been rendered.
  - `v-pre` will print out the inner text exactly how it is, including code (good for documentation
- `V-ON or @`
  - Extremely useful so there's a shortcut! `v-on` is great for binding to events like click and mouseenter. You're able to pass in a parameter for the event like (e). We can also use ternaries directly
- Multiple Bindings
  ```
  <div v-on="
    click   : onClick,
    keyup   : onKeyup,
    keydown : onKeydown
  ">
  </div>
  ```
- MODIFIERS:
  - @mousemove.stop is comparable to e.stopPropogation()
  - @mousemove.prevent this is like e.preventDefault()
  - @submit.prevent this will no longer reload the page on submission
  - @click.once not to be confused with v-once, this click event will be triggered once.
  - @click.native so that you can listen to native events in the DOM
  - Keycodes, and configure your own!
- `V-HTML`
  - Great for strings that have html elements that need to be rendered, such as a tags, strong tags, etc!
- `V-TEXT`
  - Similar to using mustache templates

### METHODS
  - Are bound to the Vue instance, they are incredibly useful for functions you would like to access in directives
  