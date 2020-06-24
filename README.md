## SCSS Auto Contrast Checker (experimental)

The goal for this project is to generate an automatic set of color contrast test swatches given a set of color values defined in a scss map.

A live demo is provided here: [SCSS Auto-contrast Checker Live Demo](https://wondermart.github.io/scss-auto-contrast-checker/). It doesn't actually work yet!

### Background and Purpose

I make a lot of pattern libraries. Part of the process of building a pattern library is setting up a system for color scheming, and then providing documentation for how that system works. In recent libraries, I've been including a color contrast reference ([here's an example](https://newcity.gitlab.io/gmu-cos/components/preview/color-contrast.html)). This reference page shows all the colors available in this library, tested for passing contrast ratios against each other. The test checks for a contrast of 4.5:1 (WCAG 2.0 AA).

This reference is helpful, but annoying to update as the system grows and changes (especially during the library's initial development). It requires the developer to define the colors in two places - both in the scss configuration, and in the data file that drives the static site generator (Fractal, in the example's case). That also means that it depends on these colors having the same names in both places, and is a whole don't-repeat-yourself failure.

So my objective with this experiment was to find a good way to declare the colors **once** in the scss and let the system handle the rest. There are probably a lot of really gross ways to achieve this (probably including whatever is currently happening on the live demo right now) — hopefully I can isolate at least one good one.
