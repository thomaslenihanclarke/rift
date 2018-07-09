# Rift
Rift is a highly customisable Sass grid generator, built to be lightweight, legacy browser compatible and flexible to even the most demanding of column layouts.

## How it works
Rift uses padding to seperate grids and columns, using padding as opposed to margin allows you to maximise the power of relative units and make it easy to maintain matching vertical and horizontal padding. 

Like most grids the columns are nested in a container and if you want to place columns inside an existing column you can easily reset the padding using the nest class. All column content, except for nested columns, should be placed within a module div in order to correctly display the gutters.

## Variables
These variables allow you to define your build specific grid requirements:

| Variable                   | Usage                                                                         |
|:---------------------------|:------------------------------------------------------------------------------|
| $container-class           | Name your grid container class here.                                          |
| $column-class              | Name your column class here.                                                  |
| $offset-class              | Name your offset class here.                                                  |
| $transitional-column-class | Name your transitional column class here.                                     |
| $transitional-offset-class | Name your transitional offset class here.                                     |
| $nest-class                | Name your nest class here.                                                    |
| $max-container-width       | Define the maximum width of the grid container.                               |
| $grid-list                 | Define the number of columns you need, multiple values create multiple grids. |
| $container-padding         | Define the amount of vertical padding required for your container.            |
| $vertical-gutter           | Define the amount of vertical padding required for your columns.              |
| $horizontal-gutter         | Define the amount of horizontal padding required for your columns.            |
| $transitional-start        | Define the media query min-width attribute of your transitional class.        |
| $transitional-end          | Define the media query max-width attribute of your transitional class.        |
| $breakpoint-list           | This is declared for use in the grid generator, do not amend.                 |
| $total-columns             | This is declared for use in the grid generator, do not amend.                 |

Once your settings have been updated compile the rift.scss file, call it in the head of your html and your grid is ready to use.

## Additional Options
The below classes are supplied to add a little extra flexibilty to the rift grid.

##### .no-max
This class can be applied to your container div to remove the max-width css attribute, useful if you need a full width grid container.

##### .no-gutters
This class can be applied to your container div to remove all padding associated with your grid container and nested columns.

## Basic Usage
Here is an example using a variety of the available column settings to show how diverse and changing your layout could be. The classes used are the defaults provided in the grid generator:

```html
<div class="rift-12">
	<div class="column-3 offset-1 tablet-column-6 tablet-offset-0 nest">
		<div class="column-6 tablet-column-12">
			<div class="module">
				<p>1</p>
			</div>
		</div>
		<div class="column-6 tablet-column-12">
			<div class="module">
				<p>2</p>
			</div>
		</div>
	</div>
	<div class="column-6 offset-1 tablet-offset-0">
		<div class="module">
			<p>3</p>
		</div>
	</div>
</div>
```

## Ackowledgements
This Sass grid generator was inspired in part by [Skeleton](http://getskeleton.com) and the CSS Tricks article ['Dont Overthink It Grids'](https://css-tricks.com/dont-overthink-it-grids/). 