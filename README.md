# Beanstalk

A flexible, responsive grid system built with attitude using Sass. Beanstalk is a simple grid solution innately created as a Sass partial for easy addition to any project. Beanstalk is powerful and customizable, but not overly complicated. It offers easy to use and edit classes for building a mobile first, 100% responsive website.

Beanstalk was loosely based off the grid system used by Zurb's Foundation, but available for addition to any project. So if you like working with Foundation and want a similar grid system to add to other project, Beanstalk is for you.

## Getting Started

Getting started with Beanstalk is super simple, after all the only necessity is adding the `_grid.scss` file to your Sass based project.

- Download or Clone the Beanstalk project from Github (or just the `_grid.scss` file)
- Add the `_grid.scss` partial to you Sass based project, and reference in the parent .scss file
- Compile code (I'm using Compass)
- Check the compiled CSS file, all Beanstalk grid classes should be available

## How To Use

Beanstalk uses a `.row` and `.col-#` syntax to build a flexible grid.

### Variables

Beanstalk dynamically builds a grid based on customizable variables. The `_grid.scss` file includes basic variable defaults that can be modified or overwritten in a `_vars.scss` partial (or whatever method you prefer to handle variables).

The `$row-width` variable controls the max-width of a responsive site. The `$column-gutter` variable controls the gutter between grid columns. The `$total-columns` variable controls the number of columns generated in the grid. By default Beanstalk is a 12 column grid system, but changing the number of columns is easy.

```
$row-width: 960px !default;
$column-gutter: 0.9375em !default;
$total-columns: 12 !default;
```

### Grid Building

Beanstalk uses a `.row` and `.col-#` syntax to build a flexible grid, where all columns are contained within a parent `.row`. 

```
<div class="row">
  
  <div class="col-8 column">
    This is the main content area.
  </div>
  
  <div class="col-4 column">
    This is the sidebar area.
  </div>
  
</div>
```

#### Working Mobile First

The Beanstalk grid system works with a mobile first mentality, meaning the bare minimum of code is loaded on mobile devices (with the least amount of bandwidth) and built upon for desktop browsers (typically higher bandwidth). 

By default all `.column` grid containers are 100% full-width on mobile, defined by the `.column` class. The `.col-#` grid styles kick in on larger viewports through the use of a @media-query calling a `$small-screen` variable (you can change the variable to whatever your want, or just a number).

Beanstalk also offers extra mobile styles to minutely control the display of content specifically on mobile devices. Add the mobile class `.small-col-#` on top of other grid classes for specific positioning on mobile.

```
<div class="row">

  <div class"small-col-6 col-4 column">
    On mobile, will be a two column grid and on desktop will be four column
  </div>
  
  <div class"small-col-6 col-4 column">
    On mobile, will be a two column grid and on desktop will be four column
  </div>
  
  <div class"small-col-6 col-4 column">
    On mobile, will be a two column grid and on desktop will be four column
  </div>
  
  <div class"small-col-6 col-4 column">
    On mobile, will be a two column grid and on desktop will be four column
  </div>

</div>
```

### Modifiers

Beanstalk offers several types of grid modifiers allow the right amount of control of a website layout.

#### Push

Adding a `.push-#` class offers a way to bump content to the right.

```
<div class="row">

  <div class="col-4 push-2 column">
    A four column container that is pushed two column widths to the right.
  </div>
  <div class="col-6 column">
    A six column container.
  </div>
</div>

```

#### Pull

Adding a `.pull-#` class offers a way to pull content to the left.

```
<div class="row">

  <div class="col-6 column">
    A six column container.
  </div>
  <div class="col-4 pull-2 column">
    A four column container that is pulled two column widths to the left.
  </div>
</div>

```

#### Collapse

Adding `.collapse` along with a `.row` will zero out the gutters of all children columns.

```
<div class="row collapse">

  <div class="col-8 column">
    A main content section that no longer has gutters.
  </div>
  <div class="col-4 column">
    A secondary content section that no longer has gutters.
  </div>

</div>
```

#### Collapse-outer

Adding `.collapse-outer` along with a `.row` will zero out the left gutter of the first column and the right gutter of the last column. This allows a way to align content if needed.

```
<div class="row collapse-outer">

  <div class="col-8 column">
    A main content section that has a right gutter but the left gutter has been zeroed out.
  </div>
  <div class="col-4 column">
    A secondary content section that has a left gutter but the right gutter has been zeroed out.
  </div>

</div>
```

## Support, Questions, & Suggestions

If you have a question or issue:

1. [Log an Issue] (https://github.com/calebsylvest/beanstalk/issues "Log an Issue for Beanstalk")
2. Send me an email at [caleb.sylvest@gmail.com] (mailto:caleb.sylvest@gmail.com)
3. Find me on Twitter at [@sylvezine](https://twitter.com/sylvezine)
