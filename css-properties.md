# CSS Properties

## Flexbox

**Container properties:**

- display

  Sets the container and make it block or inline.

  - flex (block container)
  - inline-flex (inline container).

- flex-flow

  Shorthand for flex-direction and flex-wrap.

- flex-direction

  Sets how the flex items are placed in the flex container, defining the main axis and the direction.

  - row
  - row-reverse
  - column
  - column-reverse

- flex-wrap

  Sets if the flex items are forced onto one line (nowrap) or can wrap onto multiple lines (wrap).

  - nowrap
  - wrap
  - wrap-reverse

- justify-content

  Aligns flex items along the main axis.

  - flex-start
  - flex-end
  - center
  - space-between
  - space-around
  - space-evenly

- align-items

  Align items along the cross axis.

  - flex-start
  - flex-end
  - center
  - baseline
  - stretch

- align-content

  Sets ditribution of space between items along cross axis. Only applies to multi-line flex containers.

  - flex-start
  - flex-end
  - center
  - space-between
  - space-around
  - stretch
  - space-evenly

**Items properties:**

- flex

  Shorthand for flex-grow, flex-shrink and flex-basis.

- flex-grow

  Sets how much of available space the flex container the flex item will use.

  - number

- flex-shrink

  If the size of all flex items is larger than the flex container, the item shrinks based on flex-shrink property.

  - number

- flex-basis

  Sets the initial size of a flex item.

  - length
  - percentage
  - auto

- align-self

  Overrides container align-items value.

  - auto
  - flex-start
  - flex-end
  - center
  - baseline
  - stretch

- order

  The default value is 0. Anything lower than 0 come before.

  - integer

## Grid

**Parent properties:**

- display

  Sets the parent and make it block or inline.

  - grid
  - inline-grid

grid-template-columns
grid-template-rows
grid-template-areas
grid-template (shorthand)
grid-column-gap
grid-row-gap
grid-gap
justify-items
align-items
justify-content
align-content
grid-auto-columns
grid-auto-rows
grid-auto-flow
grid

**Child properties:**
