#jQuery Exercises

####Objectives
* Checkout real world examples of jQuery on the web
* Recognize the role/use/possiblities of jQuery
* Successfuly interact with an existing codebase
* Handroll your own feature

####Exercise One
* Take a look at these examples given
* Once comfortable with the code, change something so that it works differently.
* Now that you've gained an understanding of the functionality, implement a new feature.  

####Exercise Two
Use jQuery to asynchonously load an image!

We want this...

![image](./images/async.gif)

Instead of this...

![image](./images/progressive.gif)

####Checklistt

* The jQuery

* Firstly, make sure you have jQuery included in your project. Next, use jQuery to select the image you want to eventually insert the large image into. In my example, it’s the first image on the page.

```
var $image = $("img").first();
```

* Then I need to create an image programmatically. In jQuery, you can just select the string of the tag you want to create.

```
var $downloadingImage = $("<img>");
```

* Once you set the src attribute on this image downloading will start. Before that, we want to ensure that we have a handler for the onload or load event. Once the image had been downloaded this handler will trigger.

```
$downloadingImage.load(function(){

});

```

* We want to set the destination $image source to the $downloadingImage source. The reference to $this inside the handler is the $downloadImage. We should use this since in the handler just in case we use this same handler for other images.

```
$downloadingImage.load(function(){
	$image.attr("src", $(this).attr("src"));
});
```

* Last but not least, we want to set the $downloadingImage‘s source attribute.

```
$downloadingImage.attr("src", "http://an.image/to/aynchrounously/download.jpg");
```

* This will start the image download in the background immediately. Once the download is has finished, the load callback will be triggered. The destination’s image source will be that of the newly downloaded image.


####Success Criteria
* Understand how the pieces of the puzzle are put together
* Change a major part of the existing jQuery example
* Add a new feature that improves/changes the functionality

####Examples
* [Codepen Search for jQuery](http://codepen.io/search/pens?q=jquery&limit=all&type=type-pens)
* <p data-height="268" data-theme-id="0" data-slug-hash="dteFo" data-default-tab="result" data-user="tonx" class="codepen">See the Pen <a href="http://codepen.io/tonx/pen/dteFo/">Jquery & CSS3 background</a> by enrico toniato (<a href="http://codepen.io/tonx">@tonx</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
* <p data-height="268" data-theme-id="0" data-slug-hash="rKDBx" data-default-tab="result" data-user="TimRuby" class="codepen">See the Pen <a href="http://codepen.io/TimRuby/pen/rKDBx/">CSS3/jQuery Panel</a> by Tim Ruby (<a href="http://codepen.io/TimRuby">@TimRuby</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
* <p data-height="268" data-theme-id="0" data-slug-hash="sBELl" data-default-tab="result" data-user="SaraSoueidan" class="codepen">See the Pen <a href="http://codepen.io/SaraSoueidan/pen/sBELl/">Windows-8-like Animations with CSS3 and jQuery</a> by Sara Soueidan (<a href="http://codepen.io/SaraSoueidan">@SaraSoueidan</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
* <p data-height="268" data-theme-id="0" data-slug-hash="qcyGF" data-default-tab="result" data-user="nikhil" class="codepen">See the Pen <a href="http://codepen.io/nikhil/pen/qcyGF/">Expanding search bar with jQuery</a> by nikhil (<a href="http://codepen.io/nikhil">@nikhil</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
* <p data-height="268" data-theme-id="0" data-slug-hash="ICfFE" data-default-tab="result" data-user="githiro" class="codepen">See the Pen <a href="http://codepen.io/githiro/pen/ICfFE/">SVG Doughnut chart with animation and tooltip</a> by Hiro (<a href="http://codepen.io/githiro">@githiro</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

####jQuery Plugin's

* [Plugin Registry](https://www.npmjs.com/browse/keyword/jquery-plugin)
* [Sample plugin - Slider](http://www.basic-slider.com/)
* [A list of popular plugins](http://tutorialzine.com/2013/04/50-amazing-jquery-plugins/)

####Resources

* [jQuery UI](https://jqueryui.com/accordion/)
* [jQuery Home](https://jquery.com/)
