---
tags: ["#draft", "#vue"]
---
#draft/updated [[2020-12-02]]

```html
<template>
	<p>this is</p>
	<p>ok not</p>
</template>

```

^fa5108

Initially, in my example from [[_Building Vue Components]] - I was not wanting to add this extra div to the component.

![[_Building Vue Components#^10268e]]

However, maybe turning it into a list containing mentions is not the best option.

We could turn this into a [[Vue Functional Components]].

To do this, we'd need to set the `functional` property to true on the component, and implement a `render` function.

```js
Vue.component('my-component', {
  functional: true,
  // Props are optional
  props: {
    // ...
  },
  // To compensate for the lack of an instance,
  // we are now provided a 2nd context argument.
  render: function (createElement, context) {
    // ...
  }
})
```
_component definition_[^1]


To turn our `MentionList` into a functional component:

## MentionList as Functional Component

```js
import Mention from "./Mention";
export default {
  functional: true,
  components: { Mention },
  name: "MentionList",
  props: ["names"],
  render(createElement, context) {
    const names = context.props.names;
    return names
      .map((name, i) => (i === 0 ? `${name}` : `, ${name}`))
      .map((name, i) => createElement("Mention", name));
  },
};
```
see on [codesandbox](https://codesandbox.io/s/vue-ps-tailwind-test-3-udg1q?file=/src/components/MentionList.vue:56-412)

[^1]: [Vue - Render Functions and Functional Components](https://vuejs.org/v2/guide/render-function.html#Functional-Components)