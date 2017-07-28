---
layout: post
title: CSS Flexbox Layout
categories: [CSS, Frontend]
---

A Complete Guide to Flexbox

## Basics & Terminology

Flex consist of parent container and its children flex items

![flexbox-terminology]({{ site.baseurl }}/images/CSS/flexbox-terminology.png)

## Properties for the Parent (flex container)

### display
```css
.container {
  display: flex; /* or inline-flex */
}
```
### flex-direction

![flexbox-flex-direction]({{ site.baseurl }}/images/CSS/flexbox-flex-direction.png)

```css
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

### flex-wrap

![flexbox-flex-wrap]({{ site.baseurl }}/images/CSS/flexbox-flex-wrap.png)

```css
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

### flex-flow

This is a shorthand for flex-direction and flex-wrap. Default is row nowrap

```css
.container {
  flex-flow: <'flex-direction'> || <'flex-wrap'>;
}
```

### justify-content

![flexbox-justify-content]({{ site.baseurl }}/images/CSS/flexbox-justify-content.png)

```css
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
}
```

### align-items

![flexbox-align-items]({{ site.baseurl }}/images/CSS/flexbox-align-items.png)

```css
.container {
  align-items: flex-start | flex-end | center | baseline | stretch;
}
```

### align-content

![flexbox-align-content]({{ site.baseurl }}/images/CSS/flexbox-align-content.png)

```css
.container {
  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
}
```

## Properties for the Chidren (flex item)

### order

![flexitem-order]({{ site.baseurl }}/images/CSS/flexitem-order.png)

```css
.item {
  order: <integer>;
}
```

### flex-grow

![flexitem-flex-grow]({{ site.baseurl }}/images/CSS/flexitem-flex-grow.png)

```css
.item {
  flex-grow: <number>; /* default 0 */
}
```

### flex-shrink

```css
.item {
  flex-shrink: <number>; /* default 1, negative numbers are invalid */
}
```

### flex-basis

```css
.item {
  flex-basis: <length> | auto;
}
```

### flex

This is the shorthand for flex-grow, flex-shrink and flex-basis combined.

The second and third parameters are optional. (flex-shrink and flex-basis)

Default is 0 1 auto

```css
.item {
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
}
```

### flex-grow

![flexitem-align-self]({{ site.baseurl }}/images/CSS/flexitem-align-self.png)

```css
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

## Prefixing Flexbox
```scss
@mixin flexbox() {
  display: -webkit-box;
  display: -moz-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
}

@mixin flex($values) {
  -webkit-box-flex: $values;
  -moz-box-flex:  $values;
  -webkit-flex:  $values;
  -ms-flex:  $values;
  flex:  $values;
}

@mixin order($val) {
  -webkit-box-ordinal-group: $val;  
  -moz-box-ordinal-group: $val;     
  -ms-flex-order: $val;     
  -webkit-order: $val;  
  order: $val;
}

.wrapper {
  @include flexbox();
}

.item {
  @include flex(1 200px);
  @include order(2);
}
```
