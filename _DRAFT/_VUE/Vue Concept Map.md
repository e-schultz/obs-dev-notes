---
tags: ["#vue"]
---

[[Vue]] is JavaScript framework for building web applications.

This page is a starting point to start mapping out, and documenting the Vue ecosystem, how to learn it - and some other front end development concepts.

- Vue 2 vs Vue 3 
	- Migration
- Why Vue
	- Vue vs React
	- Vue vs Angular
	- Why Vue?
	- How do you find the difference between something like view and react. 
		- How, how and why was the decision made initially to go with view over other Frameworks.
-[[ Vue Core Team]]
	- Roots of Vue
	- Inspiration
		- How it was influenced by React and Angular
    - Styling
        - How do we minimize the CSS that we ship
        - Global styles
        - scoped styles
        - tailwind 'global' styles
    - Vue Dev Tools - https://github.com/vuejs/vue-devtools
    - Template Syntax - https://vuejs.org/v2/guide/syntax.html
    - Bindings
    - Directives - https://vuejs.org/v2/guide/custom-directive.html
    - Transformation layer
        - what is a layer
        - what are the boundaries
        - why do we transform
    - [[Vuex]] - https://vuex.vuejs.org/guide/
        - State
            - What is state
            - how is state different from props
            - what is component state vs app state
        - Getters - https://vuex.vuejs.org/guide/getters.html#property-style-access
            - what logic goes into a getter and why
            - derived state - what is derived state
            - Getters help it so components don't know where in the store the data lives
                - can update the store if needed, then update the getter 
                - and not need to touch all of the components
        - Mutations
            - Mutations must be sync - https://vuex.vuejs.org/guide/mutations.html#using-constants-for-mutation-types
        - Actions
            - How do you decide what logic goes into actions vs mutations
        - Modules
            - One Module vs Many
            - how to refactor - and why
        - Initial State
            - Why is it Flat - what is the expected shape or interface for it?
                - lack of typescript
            - When updating the state - are we doing a "payload smash"
-  Front End
    - Design Systems
    - Design System vs Component Library