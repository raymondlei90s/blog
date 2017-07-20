---
layout: post
title: CSS Basics
categories: [CSS, Frontend]
---

Collection of CSS basic rules for references

## CSS Scoring

![CSS-Scoring]({{ site.baseurl }} /images/CSS/css-selector-scoring.png)


## [CSS Styles](https://cssguidelin.es/)

General Styles

```css
[selector] {
  [property]: [value];
  [<--declaration--->]
}
.foo, .foo--bar,
.baz {
  display: block;
  background-color: green;
  color: red;
}
```

Indentation CSS follow HTML DOM Structure

```css
.foo { }

  .foo__bar { }

    .foo__baz { }
```

Alignment

```css
.foo {
  -webkit-border-radius: 3px;
     -moz-border-radius: 3px;
          border-radius: 3px;
}

.bar {
  position: absolute;
  top:    0;
  right:  0;
  bottom: 0;
  left:   0;
  margin-right: -10px;
  margin-left:  -10px;
  padding-right: 10px;
  padding-left:  10px;
}
```

Meaningful white spaces
* One (1) empty line between closely related rulesets.
* Two (2) empty lines between loosely related rulesets.
* Five (5) empty lines between entirely new sections.

```css
/*------------------------------------*\
  #FOO
\*------------------------------------*/

.foo { }

  .foo__bar { }


.foo--baz { }





/*------------------------------------*\
  #BAR
\*------------------------------------*/

.bar { }

  .bar__baz { }

  .bar__foo { }
```

Object Extension Pointer

```css
/**
 * Extend `.btn {}` in _components.buttons.scss.
 */

.btn { }


/**
 * In theme file
 * These rules extend `.btn {}` in _objects.buttons.scss.
 */

.btn--positive { }

.btn--negative { }
```

Naming Conventions
* what type of thing a class does;
* where a class can be used;
* what (else) a class might be related to.

JS Hooks

```html
<input type="submit" class="btn  js-btn" value="Follow" />
```
