## perspective-origin

It's the css property that changes the [[vanishing point]] of the [[css-property -- perspective]]. Syntax is:

## [Syntax](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective-origin#syntax "Permalink to Syntax")

```css
perspective-origin: x-position;
perspective-origin: x-position y-position;
perspective-origin: y-position x-position;
perspective-origin: inherit;
perspective-origin: initial;
perspective-origin: revert;
perspective-origin: unset;
```

### [Values](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective-origin#values "Permalink to Values")

_x-position_

Indicates the position of the abscissa of the _vanishing point_. It can have one of the following values:

-   [`<length-percentage>`](https://developer.mozilla.org/en-US/docs/Web/CSS/length-percentage) indicating the position as an absolute length value or relative to the width of the element. The value may be negative.
-   `left`, a keyword being a shortcut for the `0` length value.
-   `center`, a keyword being a shortcut for the `50%` percentage value.
-   `right`, a keyword being a shortcut for the `100%` percentage value.

_y-position_

Indicates the position of the ordinate of the _vanishing point_. It can have one of the following values:

-   [`<length-percentage>`](https://developer.mozilla.org/en-US/docs/Web/CSS/length-percentage) indicating the position as an absolute length value or relative to the height of the element. The value may be negative.
-   `top`, a keyword being a shortcut for the `0` length value.
-   `center`, a keyword being a shortcut for the `50%` percentage value.
-   `bottom`, a keyword being a shortcut for the `100%` percentage value.