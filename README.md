#Glide.js

Glide is responsive and touch-friendly jQuery slider. Based on CSS3 transitions with fallback to older broswers. It's simple, lightweight and fast. Designed to slide, no less, no more.

##Setup

###1. Include jQuery
jQuery is the only dependency. Make sure to include it.

	<script src="http://code.jquery.com/jquery-1.9.1.min.js"></script>

###2. Include Glide.js
	<script src="jquery.glide.js"></script>

###3. Make necessary markup
Link to slider stylesheet inside document head.
	
	<link rel="stylesheet" type="text/css" href="css/style.css">
	
Make necessary markup for slider.

    <div class="slider">
    	<ul class="slides">
    		<li class="slide"></li>
    		<li class="slide"></li>
    		<li class="slide"></li>
    	</ul>
    </div>

###4. Init
Init our slider on default options ...

	<script>
		$('.slider').glide();
	</script>
	
… or init with custom options.

	<script>
		$('.slider').glide({
			autoplay: 5000,
			arrows: false
		});
	</script>

##Options
Here is all list of averaible

| Option | Default | Type | Description
|:-------|:--------|:-----
| `autoplay` | 4000 | int/bool | False for turning off autoplay 
| `animationTime` | 500 | int | !!! That option will be use only, when css3 are not suported. If css3 are supported animation time is set in css transitions declaration inside .css file !!!
| `arrows` | true | bool | Show/hide arrows       
| `arrowsWrapperClass` | slider-arrows | string | Arrows wrapper class         
| `arrowMainClass` | slider-arrow | string | Main class for both arrows      
| `arrowRightClass` | slider-arrow--right | string | Right arrow class
| `arrowLeftClass` | slider-arrow--left | string | Left arrow class
| `arrowRightText` | next | string | Right arrow text
| `arrowLeftText` | prev | string | Left arrow text
| `nav` | true | bool | Show/hide bullets navigation
| `navCenter` | true | bool | Center bullet navigation
| `navClass` | slider-nav | string | Navigation wrapper class
| `navItemClass` | slider-nav__item | string | Navigation item class
| `navCurrentItemClass` | slider-nav__item--current | string | Current navigation item class
| `touchDistance` | 60 | int/bool | Minimal touch-swipe distance to call event. False for turning off touch.

##API

Make glide api instance.

	var slider = $('.slider').glide();
	var glide = slider.data('api_glide');

Now, you can use **.play()**, **.pause()**, **.next()**, **.prev()**, **.jump()**. as bellow.

	glide.jump(3, console.log('Wooo!'));

- `.play()` - Starting autoplay
- `.pause()` - Stopping autoplay
- `.next(callback)` - Slide one forward
- `.prev(callback)` - Slide one backward
- `.jump(distance, callback)` - Jump to current slide


##Changelog

`1.0.0` / `15.08.2013` - Plugin release