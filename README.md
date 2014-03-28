# Pai Pai

Pai Pai is a no intrusive, gutterless grid system build with stylus, it is very simple and not requires
any additional html markup. 

It works really nice for some kind of designs where other more advanced grid systems adds unnecessary complexity to the layout layer.

## Configuration

Pai Pai comes with a few configuration variables, inside and outside media manages when the Pai Pai classes will be inside a media querie context or not. You can choose what type of selector you want you like clases or placeholders.

Pai Pai use two strategies for dealing with the inline block gap problem, the default one uses a font with zero spaces, so if you use this one you should set the base-font-family configuration variable to your own font, if you prefer the font size 0 solution don't forget to set the base-font-size configuration variable to your base one, default is 16px. If you like more any of the solutions based on html set inline-block-gap to null.

Pai Pai allows you to create whatever size classes and breakpoints you need, just add them to the custom-sizes and custom-bps hashes, then you can call them in the same way of any other Pai Pai class.

## Usage

Pai Pai is really simple to use, all classes are prefixed with p or pp, where p indicates that the styles will affect only the element with a prefixed p class, pp classes will affect the children of the prefixed pp class.

### Core classes

.p

'''
<div class=".p"></div>
'''

use .p to make your html element a grid.


### Vertical align

.p--top

'''
<div class=".p .p--top"></div>
'''

aligns the element to the top in the y axis.

.p--middle

'''
<div class=".p .p--middle"></div>
'''

aligns the element to the middle in the y axis.

.p--bottom

'''
<div class=".p .p--bottom"></div>
'''

aligns the element to the bottom in the y axis.

.pp--top

'''
<div class=".p .pp--top">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

aligns item-1 and item-2 to the top in the y axis, this is the default behaviour.

.pp--middle

'''
<div class=".p .pp--middle">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

aligns item-1 and item-2 to the middle in the y axis.

.pp--bottom

'''
<div class=".p .pp--bottom">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

aligns item-1 and item-2 to the bottom in the y axis.

.pp--strecth

'''
<div class=".p .pp--strecth">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

item-1 and item-2 will have the same height. (one true layout method)


### Horizontal align

.pp--left

'''
<div class=".p .pp--left">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

aligns item-1 and item-2 to the left in the x axis

.pp--right

'''
<div class=".p .pp--right">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

aligns item-1 and item-2 to the right in the x axis

.pp--center

'''
<div class=".p .pp--center">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

aligns item-1 and item-2 to the center in the x axis

.pp--justify

'''
<div class=".p .pp--justify">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

justify item-1 and item-2 in the x axis


### Order

.pp--reverse

'''
<div class=".p .pp--reverse">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

changes the order from item-1 and item-2 to item-2 and item-1

### Sizes

Pai Pai comes with default sizes as portions in the form of 1of2 indicating 50%, 2of3 for 66.666% and so on.

.p--1of2

'''
<div class=".p .p--1of2"></div>
'''

div will have a width of 50%.

.pp--1of2

'''
<div class=".p .pp--1of2">
  <div class=".p item-1"></div>
  <div class=".p item-2"></div>
</div>
'''

item-1 and item-2 will both have a width of 50%.

### Push and pull

You can use push and pull classes to align items in other way than the align classes do it or to set any order for grid items.

.p-push-1of-2

'''
<div class=".p .p-push-1of2"></div>
'''

moves the div 50% to the left.

.p-pull-1of-2

'''
<div class=".p .p-pull-1of2"></div>
'''

moves the div 50% to the right.

### Media queries

Pai Pai comes with a default collection of breakpoints for the most common devises used today, but you can set your own in the custom-bps hash. In order to use all the classes listed above but inside a media queries you can call them with a prefix indicating the breakpoint as follows.

.p-at-mb-p--2of3

'''
<div class=".p .p-at-mb-p--2of-3"></div>
'''

where at-mb-p (mobile portrait) is your breakpoint, the div element will change its size to 66.666% when the breakpoint triggers.

