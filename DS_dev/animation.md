# https://github.com/daneden/animate.css

> A cross-browser library of CSS animations. As easy to use as an easy thing.


***
***
> Basic Usage

Include the stylesheet on your document's <head>

<head>
  <link rel="stylesheet" href="animate.min.css">
</head>
Add the class animated to the element you want to animate. You may also want to include the class infinite for an infinite loop.

Finally you need to add one of the following classes:

bounce
flash
pulse
rubberBand
shake
headShake
swing
tada
wobble
jello
bounceIn
bounceInDown
bounceInLeft
bounceInRight
bounceInUp
bounceOut
bounceOutDown
bounceOutLeft
bounceOutRight
bounceOutUp
fadeIn
fadeInDown
fadeInDownBig
fadeInLeft
fadeInLeftBig
fadeInRight
fadeInRightBig
fadeInUp
fadeInUpBig
fadeOut
fadeOutDown
fadeOutDownBig
fadeOutLeft
fadeOutLeftBig
fadeOutRight
fadeOutRightBig
fadeOutUp
fadeOutUpBig
flipInX
flipInY
flipOutX
flipOutY
lightSpeedIn
lightSpeedOut
rotateIn
rotateInDownLeft
rotateInDownRight
rotateInUpLeft
rotateInUpRight
rotateOut
rotateOutDownLeft
rotateOutDownRight
rotateOutUpLeft
rotateOutUpRight
hinge
rollIn
rollOut
zoomIn
zoomInDown
zoomInLeft
zoomInRight
zoomInUp
zoomOut
zoomOutDown
zoomOutLeft
zoomOutRight
zoomOutUp
slideInDown
slideInLeft
slideInRight
slideInUp
slideOutDown
slideOutLeft
slideOutRight
slideOutUp
Full example:

<h1 class="animated infinite bounce">Example</h1>

***
***
> Usage

To use animate.css in your website, simply drop the stylesheet into your document's <head>, and add the class animated to an element, along with any of the animation names. That's it! You've got a CSS animated element. Super!

<head>
  <link rel="stylesheet" href="animate.min.css">
</head>
You can do a whole bunch of other stuff with animate.css when you combine it with jQuery or add your own CSS rules. Dynamically add animations using jQuery with ease:

$('#yourElement').addClass('animated bounceOutLeft');
You can also detect when an animation ends:

$('#yourElement').one('webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend', doSomething);
View a video tutorial on how to use Animate.css with jQuery here.

Note: jQuery.one() is used when you want to execute the event handler at most once. More information here.

You can also extend jQuery to add a function that does it all for you:

$.fn.extend({
    animateCss: function (animationName) {
        var animationEnd = 'webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend';
        $(this).addClass('animated ' + animationName).one(animationEnd, function() {
            $(this).removeClass('animated ' + animationName);
        });
    }
});
And use it like this:

$('#yourElement').animateCss('bounce');
You can change the duration of your animations, add a delay or change the number of times that it plays:

#yourElement {
  -vendor-animation-duration: 3s;
  -vendor-animation-delay: 2s;
  -vendor-animation-iteration-count: infinite;
}
Note: be sure to replace "vendor" in the CSS with the applicable vendor prefixes (webkit, moz, etc)

***
***
> Custom Builds

Animate.css is powered by gulp.js, and you can create custom builds pretty easily. First of all, you’ll need Gulp and all other dependencies:

$ cd path/to/animate.css/
$ sudo npm install
Next, run gulp to compile your custom builds. For example, if you want only some of the the “attention seekers”, simply edit the animate-config.json file to select only the animations you want to use.

"attention_seekers": {
  "bounce": true,
  "flash": false,
  "pulse": false,
  "shake": true,
  "headShake": true,
  "swing": true,
  "tada": true,
  "wobble": true,
  "jello":true
}
License

Animate.css is licensed under the MIT license. (http://opensource.org/licenses/MIT)