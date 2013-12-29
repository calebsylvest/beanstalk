# Beanstalk

A flexible, responsive grid system built with attitude using Sass. Beanstalk is a simple grid solution innately created as a Sass partial for easy addition to any project. Beanstalk is powerful and customizable, but not overly complicated. It offers easy to use and edit classes for building a mobile first, 100% responsive website.

Beanstalk was loosely based off the grid system used by Zurb's Foundation, but available for addition to any project. So if you like working with Foundation and want a similar grid system to add to other project, Beanstalk is for you.

## Getting Started

Getting started with Beanstalk is super simple, after all the only necessity is adding the _grid.scss file to your Sass based project.

- Download or Clone the Beanstalk project from Github (or just the _grid.scss file)
- Add the _grid.scss partial to you Sass based project, and reference in the parent .scss file
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


### Modifiers