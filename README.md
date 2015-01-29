# README #

##What is Alton?##
Alton is a scrolling plugin that utilizes custom vertical scrolling effects in order to present and navigate through web content in a unique manner. It utilizes the whole scrolljacking idea, but greatly improves upon the often-poorly-implemented scrolljacking experiences you might be used to.

## What makes Alton unique? ##
Good question. Here's why Alton rules:

1. The **Bookend** functionality. This allows you to [NATE FILL THIS SHIT OUT] which is awesome because [NATE FILL THIS SHIT OUT]. [Here's a demo of Bookend.](#)
2. The **Header Scroll** functionality. This allows you to scrolljack *only* the "Hero Section", wherein the page will scroll to the top of the next section, then re-enable native scrolling for the rest of the page. [Here's a demo of Header Scroll.](#)
3. The plugin uses **100% height** containers for full-screen presentation; it's great for impactful presentation.
4. You have options for a couple different layouts right out of the box.
5. It's lightweight, easy to implement, and not CPU intensive.


## What is scrollJacking? ##
scrollJacking is meant to provide options for those times when full page scroll doesn't make sense. We've added the option for having a header and footer area that you can scroll to, and also a featured-header single scroll.

## Compatibility ##
This plugin has been tested on IE8+. With jQuery 1.7+. Anything less and you're on your own.

## Quick start ##
### Featured Scroll ###
The Idea behind featured scroll is that you have a header and footer section with a featured area of projects or something in the middle.

Here is an example for all the options available for featuredScroll:

First ensure you have the proper HTML structure:

```
#!html

<header class="header"></header>
<section class="full">
	<div class="slide"></div>
	<div class="slide"></div>
	<div class="slide"></div>
</section>
<footer class="footer"></footer>
```
Next add the following where you want to call it. Note: **If you don't want errors to occur, only run the script on the page where scrolling occurs**
```
#!javascript

$(document).scrollJack({
	fullSlideClass: 'full',
	firstClass: 'header',
	lastClass: 'footer',
	useSlideNumbers: true,
});
```

### Header Scroll ###
The Idea behind header scroll is that you have a featured header area, that disappears on scroll, and you find yourself at the main content with native scrolling enabled.

Here is an example for all the options available for headerScroll:

First ensure you have the proper HTML structure:

```
#!html

<section class="header">
<!-- Insert Header Content Here -->
</section>
<section class="pageWrapper">
<!-- Insert Regular Content Here -->
</section>
```
Next add the following where you want to call it. Note: **If you don't want errors to occur, only run the script on the page where scrolling occurs**

```
#!javascript

$(document).scrollJack({
    firstClass : 'header', // classname of the first element in your page content
    bodyContainer: 'pageWrapper', // ID of content container
    scrollMode: 'headerScroll', // Choose scroll mode
});
```

## What's included ##

## Bugs and feature requests ##

Have a bug or a feature request? Please first read the issue guidelines and search for existing and closed issues. If your problem or idea is not addressed yet, please open a new issue.

### Currently Working On ###
* Custom Animations
* More Customization for slide number indicators (pagination)

## Keep track of our progress. ##

Follow [@paper_leaf](https://twitter.com/paper_leaf) on Twitter.

## Copyright and License ##
*Copyright 2014 Paper Leaf Design*

License: GPL v3

## Frequently Asked Questions ##
#### Does this work on touchscreens? ####
No.
#### Why not? ####
Touch events are a different beast, and considering the amount of people on cheaper, less powerful devices, or even the majority still stuck in contracts, the usability is usually non-existent. That being said, we are continuing to explore ways of implementing this for mobile devices.
#### So you are looking at adding mobile functionality? ####
Possibly!
#### What currently happens on mobile devices, then, if Alton doesn't work? ####
It falls back to regular scrolling on mobile. It's the best of both worlds, like pizza made out of candy.
#### Scrolling appears unresponsive at times. What's going on? ####
After every scroll there's a delay in effect to help get rid of Inertia Scroll on Macs. If you try to scroll within this delay it will prevent you from scrolling, until the barrage of mousewheel events has ended.
#### Why did you name this plugin Alton? ####
We're playing off the idea of height, in that this plugin uses 100% height containers. That led us to the discovery of [Robert Wadlow](http://en.wikipedia.org/wiki/Robert_Wadlow), the world's tallest man – also known as the Alton Giant. *mic drop*