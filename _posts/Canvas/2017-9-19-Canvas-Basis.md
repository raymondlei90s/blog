---
layout: post
title: Basis of Canvas
categories: [HTML, Frontend, JavaScript, Canvas]
---

Summary of Canvas basic knowledge.
* Has only two attributes, width and height
* Can be sized by CSS, be careful about the scales
* Can be styled like normal image (margin, border, background...)
* If no styles applied, it will be fully transparent
* <canvas> creates a fixed-size drawing surface that expose to 1 or * rendering contexts

```html
<canvas id="tutorial" width="150" height="150"></canvas>
```
```js
var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');
```
