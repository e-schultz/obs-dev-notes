---
tags: ["#DRAFT"]
---

# Started with a Mockup

The other night I was walking through a process of how I might start approaching taking static markup from a designer, and breaking it down into components in Vue.
The starting point was a quick layout done by a designer using the TailwindCSS Playground - [[Initial Static Layout using TailwindCSS|initial layout]] [^initlayout] ^2d3216


# Initial Markup Components
![[Initial Static Layout using TailwindCSS#Layout using Tailwind CSS]]

I then did a quick refactoring of breaking things out into components, creating ones like

- Container
- List
- ListItem
- etc

# Initial Vue Version

![[Initial Vue Version]]
  
  
  When I first did this, it was a quick after work thing on Friday - and one of the components I had done was bothering me.
  
  
  Displaying the list of mentions - `@tushar, @katia` etc - was initially done like this
  
  # Room for Improvement
  
 Initially I had build a `Mention` component like:
 
 ```html
<code class="text-sm font-bold text-gray-900">
	<slot></slot>
</code>
```
 
 which allowed me to use it in the layout like:
 
 ```html
 <List>
 	<ListItem> Hand off code to <Mention>@tusash</Mention></ListItem>
 </List>
 ```
  
I thought - "what if the common use case is to pass in a list of names, repeating that might get tedious" - and wanted to be able to pass in an array of names to display, and be able to use the component more like.

```html
 <List>
 	<ListItem> Hand off code to 
		<MentionList :names="names" :use-and="true"/>
	</ListItem>
 </List>

```
  
 I had added the `useAnd` property - because I thought maybe sometimes we might want to list them as
 
 `@x, @y, @z` or `@x, @y, and @z`
  
```html
 <div class="inline-block">
  <span :key="item" v-for="(item, index) in names">
      <span v-if="index === names.length - 1 && useAnd"> and </span>
      <span v-else> {{ index > 0 ? "," : "" }} </span>
      <Mention>{{ item }}</Mention>
    </span>
</div>
```
  
 
 ## What's not to like?
 
 With [[Vue Single File Components]] - Vue needs you to have a [single root element](https://vuejs.org/v2/guide/components.html#A-Single-Root-Element) in the component, so I had to add an extra `<div>` to wrap the list of `<span>` tags.
 
While there are ways to [create multi-root components](https://zendev.com/2018/05/07/multi-root-vue-components.html)  in [[Multi-Root Components|Vue]] - that's a topic for another day, and not the appropiate use case here as semantic HTML is the better option.
 
 I had also introduced a bunch of logic into the template to figure out 
 
 - do I need to display a comma or not
 - Do I need to display an "and" or not

I didn't want to have `@x, @y, and , @z` for example.

And when I said

> to wrap the list of `<span>` tags

That's probably a sign that I should be using a list - not a bunch of span tags.

### Making it a List and using CSS

_warning_: my css skills are not great

I replaced the `div` and list of `span` tags, with a more semantically correct list using `ul` and `li` - and then using CSS selectors to control the "," and the "and"

```html
  <ul :class="{ useAnd }">
    <li v-for="item in names" :key="item">
      <Mention>{{ item }}</Mention>
    </li>
  </ul>

```

and the css

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

li {
  float: left;
  padding: 2px;
}
li:not(last-child):after {
  content: ", ";
}

.useAnd > li:last-child:before {
  content: " and ";
}

.useAnd > li:last-child:after {
  content: ".";
}

```

With this change, I was able to accomplish the goals of

- Having a single root element
- Removing logic from the template
- Use semantic HTML for handling a list



[^initlayout]:  [initial layout](https://play.tailwindcss.com/qB1gyRcncp)