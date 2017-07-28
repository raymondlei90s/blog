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
