---
layout: post
title: How I Designed & Built This Minimalistic Blog
category: Design
tags: jekyll design css
year: 2012
month: 4
day: 11
published: true
---

<p>
I'm a native Android & iOS developer, and not exactly doing web development every day - I'm surely ignorant of some fancy twists (tricking IE6 into doing things). However, I have spent upwards of 1000 hours with HTML 4 and CSS 1/2 in my teens, building a PHP CMS for a local shop and other stuff. To refresh my web development abilities, I decided to <b>design my blog from scratch</b> - CSS and HTML-wise.
<br>
This post is about how I did it.
</p>

<h2>Requirements</h2>

What I want for my blog:
<ul>
	<li>Minimalistic but beautiful design</li>
	<li>Low loading times (few requests, lean resources)</li>
	<li>Inexpensive hosting</li>
</ul>

<h2>Technical Setup</h2>

<p>
	After considering my requirements, I came up with this setup:
</p>

<ul>
	<li>Jekyll</li>
	<li>HTML 5, CSS 3</li>
	<li>No self-written JS (for the time being)</li>
	<li>Widgets for added functionality</li>
</ul>

<p>
	I chose <a href="https://github.com/mojombo/jekyll" target="_blank"><b>Jekyll</b></a>, a semi-static site framework for Rails, for reasons of <b>performance and flexibility</b>. Pages reportedly load very fast, and you can host them at your own Github subdomain - neat! While your pages are mostly served statically, you can add "dynamic" functionality by using external services, like in-site Google search, all the web's widgets, and even comments (e.g., via Disqus). Eric Jones went to the absolute max with widget integration in his <a href="http://erjjones.github.com/blog/How-I-built-my-blog-in-one-day/" target="_blank">blog</a> - a great resource for reference!
</p>
<p>
As I thought it would not be necessary, I did not employ SASS. If CSS code becomes any more complicated, I will probably make the <a href="http://mikeferrier.com/2011/04/29/blogging-with-jekyll-haml-sass-and-jammit/" target="_blank">switch</a>.
</p>

<h2>Choosing Layout and Colors</h2>
<p>
I then surfed the web for blog layouts I wanted to borrow from - and found <a href="http://www.philterdesign.com/?p=541" target="_blank">this one</a> by Phil Chung. Then kicked up Photoshop, loaded a screenshot of Phil's blog, and created a <b>color palette</b> by overlaying all relevant elements. It's advisable to use an actual layout to find a palette, because a color's effect depends on the amount of screen space it is given.
</p>
<p>
Over time I have grown addicted to this shade of purplish red: <span style="color: #ff002a;"><b>#ff002a</b></span> - call it my favourite color - and now I can finally put it to use in my own blog.
Also, I like <b>high contrasts and warm colors</b> (that means, red or orange tint), as they are easy on the eye and comforting.
</p>

<figure>
<img src="/img/2012-04-11/layout_and_palette.png" style="margin: 20px auto; display: block;" title="Talent borrows...">
</figure>

<h2>Selecting Typefaces</h2>
<p>
The <a href="http://www.myfonts.com/fonts/exljbris/museo/" target="_blank">Museo family</a> is really great, I'm definitely a Museo fan (gotta watch out that I don't use it too often). Also, some of them are free, and can be downloaded at MyFonts as drop-in web fonts, readily shipped with <a href="http://www.fontspring.com/blog/the-new-bulletproof-font-face-syntax" target="_blank">bulletproof</a> CSS code. Therefore, I'm using <b>Museo 300</b> and <b>Museo 500</b> for headings and the navigation menu.
</p>
<p>
For the sake of readability of the body copy, I opted for <b>Helvetica Neue</b>, and as a fallback for Windows users, <b><span style="font-family: Arial">Arial</span></b> (yeah, I know :/).
</p>
<p>
<b>Font size</b> is not so easy to get right, but is VERY important for readability. There are people claiming that going below 16 points would be stupid. I am going with 1.1em which amounts to 19px on my 15" Macbook Pro at standard browser settings. It amounts to <b>11-15 words per line</b>, which will (hopefully) average in the oft-praised <a href="http://www.maxdesign.com.au/articles/em/" target="_blank">12 words per line</a>.
</p>

<h2>Adding Eye Candy</h2>
<p>
As a Photoshop addict, I HAD to take the chance to play around with <b>subtle effects and textures</b>. After all, the little details make all the difference.
</p>
<p>
After layout, colors, and typefaces had been set, I headed over to <a href="http://subtlepatterns.com" target="_blank">Subtle Patterns</a> to find nice textures. With some brightness modifications to <a href="http://subtlepatterns.com/?p=203" target="_blank">one of those</a>, a <b>pattern for the header area</b> was born, looking somewhat like denim cloth:
</p>

<figure>
<img src="/img/2012-04-11/stripes_pattern.png" title="Dark Stripes" style="margin: 20px auto; display: block;">
</figure>

<p>
The <b>main area</b> (on which you are currently reading) also needed some <b>texture</b>, so I went the good ol' noise route: Added <a href="/img/2012-04-11/transparent_noise.png" target="_blank">this pattern</a> as pattern overlay, with blend mode Luminosity and Opacity set to 10% - voilá.
</p>

<p>To add a fancy touch to the banner, I decided to go with a <b>pattern of cut circles</b> at its bottom, softening the transition from dark to bright. Adding a white inner shadow (angle: 90°, distance: 1px, size: 0px, blend mode: Normal) gives it a slight 3D effect:
</p>

<figure>
<img src="/img/2012-04-11/round_thing_enlarged.png" style="margin: 20px auto; display: block;" title="Pseudo 3D effect pattern">
</figure>

<p>The <b>photo of me</b> at the top left of every page makes the blog more personal (at least I hope so :^) ), and I wanted it to look like a physical print of a photograph, stuck into a fold of the "blog paper" (curious people, look into the <a href="/img/2012-04-11/photo.psd" target="_blank">PSD file</a>):
</p>

<figure>
<img src="/img/2012-04-11/photo.png" title="Dark Stripes" style="margin: 20px auto; display: block;">
</figure>

<h2>Slicing It Up</h2>
<p>
Having finished the Photoshop mockup, I proceeded to extract images from it and created a layout in CSS. 
The first thing I did was load a <a href="http://meyerweb.com/eric/tools/css/reset/">CSS Reset</a> to minimize strange cross-browser surprises. After that, the layout elements were placed in their own HTML containers and assigned CSS layout properties. Curious people, look at the details in the site's <a href="/css/style.css" target="_blank">main CSS file</a>, or better, use your browser's element inspector. The box layout looks like this (click to enlarge):
</p>

<figure>
<a href="/img/2012-04-11/layout_detailed.png" target="_blank"><img src="/img/2012-04-11/layout_detailed_small.png" title="Dark Stripes" style="margin: 20px auto; display: block;"></a>
</figure>

<p>
As every resource (JS, CSS, Image,...) is served in its own request, a page's loading time can be lowered by putting as many images as possible in <b>sprites</b>. I used <a href="TODO" target="_blank">SpriteRight</a> to wrap all reoccurring, non-repeated images into one single file, which currently looks like this:
</p>
<figure>
<img src="/img/2012-04-11/sprite.png" style="margin: 20px auto; display: block;" title="Sprite">
</figure>

<h2>More CSS Eye Candy</h2>

<p>
Holding the finished HTML & essential CSS code in my hands, I went on to add some more details to make the page look more refined.
</p>

<p><b>Shadowed text</b> looks very nice on most backgrounds, as subtle as the effect may be (under some lighting conditions, it's not visible on this blog). A white shadow added to a dark font increases the contrast, making it look crisper by seemingly sharpening the edges.
</p>
{% highlight css %}
article {
	text-shadow: 0px 1px 1px #ffffff; 
	filter: dropshadow(color=#ffffff, offx=0, offy=1);
	//...
}
{% endhighlight %}

<p>
Fancy <b>link color hover transitions</b> can be had by adding some CSS: 
</p>
{% highlight css %}
a { -webkit-transition: color 0.2s linear; 
    -moz-transition: color 0.2s linear; 
     transition: color 0.2s linear; }
{% endhighlight %}

<p>One more subtlety is the manipulation of <b>text selection</b> background and color. In my case, I also had to disable text shadows:</p>
{% highlight css %}
::selection { background:#ff002a; 
			  color:#fff; 
		      text-shadow:0px 0px 0px #000000; 
			  filter:dropshadow(color=#000,offx=0,offy=0);}
::-moz-selection { background:#ff002a; 
				   color:#fff; 
				   text-shadow:0px 0px 0px #000000; }
::-webkit-selection { background:#ff002a; 
				      color:#fff; 
					  text-shadow:0px 0px 0px #000000;}
{% endhighlight %}

<h2>Code Highlighting</h2>

<p>
Jekyll comes with support for <b>Pygments</b>, a python syntax highlighter which also generates CSS code based on predefined styles. Installing and configuring Pygments is straightforward on OSX (Python is preinstalled on OSX >= 10.4):
</p>

{% highlight ruby %}
sudo easy_install Pygments
# Generate a highlight stylesheet with style "monokai",
# then paste result into CSS file:
pygmentize -S monokai -f html
{% endhighlight %}

<p>
You may have noticed that the generated highlighting is not perfect, and I might therefore switch to another technology - e.g. <a href="http://daniel-salazar.com/jekyll/code-highlighting-with-coderay-in-jekyll.html" target="_blank">CodeRay</a>.	
</p>

<h2>JS or No</h2>
<p>
Fully blown JS frameworks like jQuery have found their way into most blog templates, be it sensible or not. Since low loading time is one of my main priorities for this blog, I meditated if I needed any client-side code - turns out: <b>No</b>.
I have been able to achieve everything I wanted for this blog, without JS.</p>
<p>
I might add Disqus and Google Analytics support later on, but for the time being, I'm fine with plain HTML & CSS plus the following HTML5 JS hack for older browsers.
</p>

<h2>HTML5 for Older Browsers</h2>
<p>
<b><a href="http://code.google.com/p/html5shiv/" target="_blank">html5shiv</a></b> provides a drop-in JS snippet to force browsers like IE6 to eat your HTML5, and you need not host it yourself: 
</p>
{% highlight html %}
<!--[if lt IE 9]>
<script src="//html5shiv.googlecode.com/svn/trunk/html5.js">
</script>
<![endif]-->
{% endhighlight %}
	

<h2>Cross-Browser Testing</h2>
<p>
To make sure my blog looks the same for most of the users (I developed it with Safari), I started some other browsers (FF, Chrome, Opera) and only minor problems showed: FF sets font-weight to bold for headings (which I disabled then), and Opera made Pygment's syntax highlighting appear super-huge (which I don't care about).
</p>
<p>Anxiously, I then booted into Windows and started IE6.
	
<h2>Atom Feed</h2>
<p>
To provide an Atom feed for my blog, I copied one of the many templates floating around the interwebs and made some modifications like filling in my name (TODO link to Gist), and saved it as <b>atom.xml</b>. Currently, the posts are sent in whole on every Atom request (making for a lot of traffic) - I might shorten the posts later on, but for the time being I have not found a way to do this in Liquid.
</p>
	
<h2>Deploying to Github</h2>
<p>
Pushing a Jekyll site to Github was straightforward - after setting up a public repo called <b>manmal.github.com</b>, I just pushed it up there, and, after a few minutes, received the first build notification per email. That was easy!
</p>
	
<h2>Remaining Issues</h2>
<p>
When validating my blog's markup via <a href="http://html5.validator.nu/" target="_blank">html5.validator.nu</a>, I got errors because all figure tags were wrapped in paragraph (p) tags - it seems Jekyll generates those without asking. I will look into this soon.
</p>