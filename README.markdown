Welcome to Gridosaurus
======================

A pragmatic, responsive, flexible, liquid CSS grid system using
[Compass][], [SASS][], and [Modernizr][].

Goals
-----

We needed a css grid framework to support our newer mobile-friendly
projects. After reviewing a whole bunch of excellent solutions, we ended
up creating our own.

The goal of this framework is to allow for flexible CSS grids that:

-   Support the [CSS Flexible Box Layout Module][] if available
-   Fall back to normal, static grid widths if not
-   Can choose NOT to use flexbox if desired
-   Support media queries for different grid layouts, if available
-   Support sub grids
-   Maintain consistent gutter widths, even in sub grids
-   Works with Compass and SASS, our CSS pre-processor of choice
-   Works with [CSS3 PIE][]

Approach
--------

We realized that we only needed to support flexbox on modern browsers,
but also needed a fall back for non-flexbox friendly browsers like IE.
We also needed a solution that would display something more reasonable
than the bare minimum to browers that don’t support media queries.

Some of the decisions we made were:

-   To build on the great work at [320 and up][] for media query support
    and basic mobile philosophy
-   To use a negative left margin apporach to the non-flexbox grid for
    better legacy browser and PIE support
-   To leverage Compass and SASS as much as possible
-   To compromise and usa a “row” function, so we could support better
    sub grids.

  [Compass]: http://compass-style.org/
  [SASS]: http://sass-lang.com/
  [Modernizr]: http://www.modernizr.com/
  [CSS Flexible Box Layout Module]: http://dev.w3.org/csswg/css3-flexbox/
  [CSS3 PIE]: http://css3pie.com/
  [320 and up]: http://www.stuffandnonsense.co.uk/projects/320andup/
