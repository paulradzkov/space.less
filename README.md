# space.less — toolkit for managing negative space

[![npm version](https://badge.fury.io/js/space.less.svg)](http://badge.fury.io/js/space.less)
[![bower version](https://badge.fury.io/bo/space.less.svg)](http://badge.fury.io/bo/space.less)

Designed to make margins, paddings, gutters consistent across the project.

From design point of view this is an argeement on what distance to use between objects in UI layout.
From frontend perspective this is a set of classnames to rule margins and paddings on different media queries breakpoints.
Together it is a part of communication language between designers and frontend developers.

## Installation

**Compiled from CDN**  
[`https://unpkg.com/space.less@0.0.3/space.css`](https://unpkg.com/space.less@0.0.3/space.css)  
[`https://unpkg.com/space.less@0.0.3/space.min.css`](https://unpkg.com/space.less@0.0.3/space.min.css)  
[`https://unpkg.com/space.less@0.0.3/space.min.css.map`](https://unpkg.com/space.less@0.0.3/space.min.css.map)

**NPM**  
`npm install space.less --save-dev`

**Bower**  
`bower install space.less --save`

## Usage in HTML

Link compiled `space.css` in the head of your page.
Apply classes to any HTML element to get desired margins and paddings.
See [docs](http://paulradzkov.github.io/space.less/) for classnames.

## Usage in LESS

Install library with `npm install space.less --save-dev` and include its main file inside your project less file:

```less
@import (less) "./node_modules/space.less/space.less";
```

That is enough to run library with default parameters.

### Default parameters

Parameters stored in mixin:

```less
.space-settings() {

    @spaces: 0, 8px, 16px, 24px, 40px, 64px, 104px, 168px;
    @spacealias: -zero, -nano, -micro, -mili, -base, -kilo, -mega, -giga;

    // media breakpoints
    @breakpoints:
        ~"(min-width: 576px)",
        ~"(min-width: 768px)",
        ~"(min-width: 992px)",
        ~"(min-width: 1200px)";

    // names for breakpoint suffixes
    @suffixes: ~"\:xs", ~"\:sm", ~"\:md", ~"\:lg", ~"\:xl";

    // IMPORTANT: suffixes count should be bigger than breakpoints count by 1
    // suffixes-count = breakpoints-count + 1
}
```

### Redefining parameters

To change any (or every) parameter add setting mixin after import inside your .less file:

```less
@import (less) "./node_modules/space.less/space.less";

.space-settings() {

    @spaces: 0, 5px, 10px, 25px, 50px;
    @spacealias: _zero, _small, _normal, _large, _huge;

}
```

Only sizes and names for spacing was redefined in example above. Breakpoint parameters remains default.
