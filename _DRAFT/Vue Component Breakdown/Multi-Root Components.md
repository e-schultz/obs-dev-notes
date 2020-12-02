When using [[Vue Single File Components]], it is expected that you have a single root element in the template

# What is a Single Root Element?

```html
<template>
	<section>
<!--- a DOM element that contains all the children -->	
	</section>
</template>
```

# What is a Multi Root Component?

A multi-root component, is when you have a component that does not have a single parent - but return a bunch of siblings. 

Using Single File Components, this would not be possible

```html
<template>
	<span>Hello</span>, 
	<span>how are you today?</span>
</template>
```

This is because there is no root container to wrap the two `span` tags.

# Why?

#TODO  #tk 

# How

#TODO #tk 

- Use Vue Functional Components
- Implement your own `render` method
- Can use JSX if you want

See this blog post on [Creating Multi-root Vue.js Components](https://zendev.com/2018/05/07/multi-root-vue-components.html)