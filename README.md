# Beanstalk

A flexible, responsive grid system built with attitude using Sass. Beanstalk is a simple grid solution innately created as a Sass partial for easy addition to any project. Beanstalk is powerful and customizable, but not overly complicated. It offers easy to use and edit classes for building a mobile first, 100% responsive website.

Beanstalk is based on the grid system used by Zurb's Foundation, but available for addition to any project. So if you like working with Foundation and want a similar grid system to add to other projects, Beanstalk is for you.

## Getting Started

Getting started with Beanstalk is super simple, after all the only necessity is adding the `_grid.scss` file to your Sass based project.

- Download or Clone the Beanstalk project from Github (or just the `_grid.scss` file)
- Add the `_grid.scss` partial to you Sass based project, and reference in the parent .scss file
- Compile code (I'm using Compass)
- Check the compiled CSS file, all Beanstalk grid classes should be available

Note: I suggest using the super cool global border-box method when working with Beanstalk. Doing so will allow for better, bullet proof grids with nesting capabilities. For more information about using the global border-box see what Paul Irish says about it: http://www.paulirish.com/2012/box-sizing-border-box-ftw/

```
/* apply a natural box layout model to all elements */
*, *:before, *:after {
  -moz-box-sizing: border-box; -webkit-box-sizing: border-box; box-sizing: border-box;
}
```

## How To Use

Beanstalk uses a `.row` and `.col-#` syntax to build a flexible grid.

### Variables

Beanstalk dynamically builds a grid based on customizable variables. The `_grid.scss` file includes basic variable defaults that can be modified or overwritten in a `_vars.scss` partial (or whatever method you prefer to handle variables).

The `$row-width` variable controls the max-width of a responsive site. The `$column-gutter` variable controls the gutter between grid columns. The `$total-columns` variable controls the number of columns generated in the grid. By default Beanstalk is a 12 column grid system, but changing the number of columns is easy. The `$show-grid` variable, if set to `true`, will color all grid columns a transparent red color. This is only for testing and demonstration purposes and the variable is set to `false` by default.

```
$row-width: 960px !default;
$column-gutter: 0.9375em !default;
$total-columns: 12 !default;
$show-grid: false !default;
```

### Grid Building

Beanstalk uses a `.row` and `.col-#` syntax to build a flexible grid, where all columns are contained within a parent `.row`. 

```
<div class="row">
  
  <div class="large-8 column">
    This is the main content area.
  </div>
  
  <div class="large-4 column">
    This is the sidebar area.
  </div>
  
</div>
```

#### Working Mobile First

The Beanstalk grid system works with a mobile first mentality, meaning the bare minimum of code is loaded on mobile devices (with the least amount of bandwidth) and built upon for desktop browsers (typically higher bandwidth). 

By default all `.column` grid containers are 100% full-width, defined by the `.column` class. Column widths can be specified for each available break point—small, medium, and large—defaulting to 100% width. Breakpoints are controlled via the variables `$small-screen` for the first breakpoint and `$medium-screen` for the second, but you can change the variable names to whatever you like, or a number.


```
<div class="row">

  <div class"small-6 medium-4 column">
    On mobile, will be a two column grid and on desktop will be four column
  </div>
  
  <div class"small-6 medium-4 column">
    On mobile, will be a two column grid and on desktop will be four column
  </div>
  
  <div class"small-6 medium-4 column">
    On mobile, will be a two column grid and on desktop will be four column
  </div>
  
  <div class"small-6 medium-4 column">
    On mobile, will be a two column grid and on desktop will be four column
  </div>

</div>
```

### Modifiers

Beanstalk offers several types of grid modifiers for complete control of layout.

#### Offset

#### Source Ordering

##### Push

Column ordering can be flipped using the push and pull classes. The push/pull option can be specific to breakproints by using the `.{size}-push-#` and `.{size}-pull-#` syntax.

```
<div class="row">

  <div class="medium-4 medium-push-6 column">
    A four column container.
  </div>
  <div class="medium-6 medium-pull-4 column">
    A six column container.
  </div>
  
</div>
```

##### Reset Source Order

If you need to reset the source order of elements on a breakpoint and above use the `.{size}-reset-order` class to do so. In the example below we flipped the order of the columns on a medium screen, but reset the source order on large screens.

```
<div class="row">

  <div class="medium-4 medium-push-6 large-reset-order column">
    A four column container.
  </div>
  <div class="medium-6 medium-pull-4 large-reset-order column">
    A six column container.
  </div>
  
</div>

```

#### Collapse

Adding `.collapse` along with a `.row` will zero out the gutters of all children columns.

```
<div class="row collapse">

  <div class="large-8 column">
    A main content section that no longer has gutters.
  </div>
  <div class="large-4 column">
    A secondary content section that no longer has gutters.
  </div>

</div>
```

#### Collapse-outer

Adding `.collapse-outer` along with a `.row` will zero out the left gutter of the first column and the right gutter of the last column. This allows a way to align content if needed.

```
<div class="row collapse-outer">

  <div class="large-8 column">
    A main content section that has a right gutter but the left gutter has been zeroed out.
  </div>
  <div class="large-4 column">
    A secondary content section that has a left gutter but the right gutter has been zeroed out.
  </div>

</div>
```

## Support, Questions, & Suggestions

If you have a question or issue:

1. [Log an Issue] (https://github.com/calebsylvest/beanstalk/issues "Log an Issue for Beanstalk")
2. Send me an email at [caleb.sylvest@gmail.com] (mailto:caleb.sylvest@gmail.com)
3. Find me on Twitter at [@sylvezine](https://twitter.com/calebsylvest)
