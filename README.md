# space.less — toolkit for managing negative space

[![npm version](https://badge.fury.io/js/space.less.svg)](http://badge.fury.io/js/space.less)
[![bower version](https://badge.fury.io/bo/space.less.svg)](http://badge.fury.io/bo/space.less)

Designed to make margins, paddings, gutters consistent across the project.

From design point of view this is an argeement on what distance to use between objects in UI layout.
From frontend perspective this is a set of classnames to rule margins and paddings on different media queries breakpoints.
Together it is a part of communication language between designers and frontend developers.

## Installation

**Compiled from CDN**  
[`https://unpkg.com/space.less@0.0.2/space.css`](https://unpkg.com/space.less@0.0.2/space.css)  
[`https://unpkg.com/space.less@0.0.2/space.min.css`](https://unpkg.com/space.less@0.0.2/space.min.css)  
[`https://unpkg.com/space.less@0.0.2/space.min.css.map`](https://unpkg.com/space.less@0.0.2/space.min.css.map)

**NPM**  
`npm install space.less --save-dev`

**Bower**  
`bower install space.less --save`

## Using in HTML

Include compiled `space.css` into head of page at the bottom. Or import `space.less` into your main .less file:

```
@import (less) "node_modules/space.less/space.less";
```
Apply classes to any HTML elements to get desired margins and paddings. See [docs](http://paulradzkov.github.io/space.less/).
