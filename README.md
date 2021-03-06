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
  - Runs whenever an update occurs
  - Not cached
  - Typically invoked from v-on/@, but flexible
  - Getter/setter (By default a getter)

### Computed
  - Computed properties are calculations that will be cached and will only update when needed.
  - Highly performant but use with understanding.
  - a different view of the same data. Kinda like `.map()`. 
  - Runs only when a dependency has changed
  - Cached
  - Should be used as a property, in place of data
  - By default getter only, but you can define a setter

### Reactive Programming
  - Watchers & Vue's Reactivity System
  - is programming with asynchronous data streams
  - A stream is a sequence of ongoing events ordered in time that offer some hooks with which to observe it. 
  - When we use reactive premises for building apps, this means it's very easy to update state in reaction to events.
  - [Andre Stalz post](https://gist.github.com/staltz/868e7e9bc2a7b8c1f754) on the intro to Reactive Programming you've been missing.

### What is Reactive
  - Angular 1.x has dirty checking
  - Cycle.js and Angular 2 use reactive streams like XStream and Rx.js
  - Vue.js, MobX or Ractive.js all use a variation of getters/setters.
  - Despite the name, React is not Reactive - it uses a "pull" approach (rather than a "push")
  - [Vue Reactivity Docs](https://vuejs.org/v2/guide/reactivity.html)
  - [How to build a reactive engine in JS](https://www.monterail.com/blog/2016/how-to-build-a-reactive-engine-in-javascript-part-1-observable-objects)
  
### In Vue
  - Vue takes the object, walks through it's properties and converts them to getters/setters
  ```new Vue({
    data: {
      text: 'msg'
    }
  })
  ```
  - Vue cannot detect property addition or deletion, so we create this object to track

### Watchers
- Each component has a watcher instance
- The properties touched by the watcher during the render are registered as dependencies
- When the setter is triggered, it lets the watcher know and causes the component to re-render

- The Vue instance is the middle man between the DOM and the business logic
- Watch updates the DOM only if it's required- performing calculations in JS is really performant but accessing the DOM is not. So we have a Virtual DOM which is like a copy, but parsed in JavaScript
- It will only update the DOM for things that need to be changed, which is faster.
- Good for asynchronous updates and updates/transitions with data changes 
- 