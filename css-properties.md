# CSS Properties

## Flexbox container properties

### display

Sets the container and make it block or inline. Values: flex (block container), inline-flex (inline container).

### flex-flow

Shorthand for flex-direction and flex-wrap.

### flex-direction

Sets how the flex items are placed in the flex container, defining the main axis and the direction. Values: row, row-reverse, column, column-reverse.

### flex-wrap

Sets if the flex items are forced onto one line (nowrap) or can wrap onto multiple lines (wrap). Values: nowrap, wrap, wrap-reverse.

## justify-content

Aligns flex items along the main axis. Values: flex-start, flex-end, center, space-between, space-around, space-evenly.

## align-items

Align items along the cross axis. Values: flex-start, flex-end, center, baseline, stretch.

## align-content

Sets ditribution of space between items along cross axis. Only applies to multi-line flex containers. Values: flex-start, flex-end, center, space-between, space-around, stretch, space-evenly.

---

## Flexbox items properties

## flex

Shorthand for flex-grow, flex-shrink and flex-basis.

## flex-grow

Sets how much of available space the flex container the flex item will use. Values: number.

## flex-shrink

If the size of all flex items is larger than the flex container, the item shrinks based on flex-shrink property. Values: number.

## flex-basis

Sets the initial size of a flex item. Values: length, percentage, auto.

## align-self

Overrides container align-items value. Values: auto, flex-start, flex-end, center, baseline, stretch.

## order

The default value is 0. Anything lower 0 come before.
