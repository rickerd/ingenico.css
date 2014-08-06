Ogone.css
===================

<blockquote>
	These custom CSS styles make it easier to cope with the default Ogone payment view, which is rather grotesque.
</blockquote>

<h2>Introduction</h2>
<p>
Did you ever thought, while implementing payment services from <a href="http://en.wikipedia.org/wiki/Ogone" target="_blank">Ogone</a>, that the CSS file was not being loaded on the actual payment page? Well, we did...and still do, every single time.The payment view is truly hideous and looks like a web page from the early nineties. Our guess is that "<em>level-1 PCI DSS compliant</em>" does not have anything to do with providing a user friendly interface with proper front-end code.
</p>
<p>
Luckily, for us implementors, Ogone provides an option to modify the default layout / design. As they state in their <abbr title="Frequently Asked Questions">FAQ</abbr>:
</p>
<blockquote>
<p>"There are two different ways to influence the look and feel of the payment page: by using either the static template or the dynamic template. With the dynamic template it is possible to customize the entire design of the payment page using a template and cascading style sheets (CSS)"</p>
</blockquote>
<p>
And that's where <strong>Ogone.css</strong> comes in! We provide subtle and customizable CSS styles that will make it easier to cope with the payment view.
</p>
<h2>Getting started</h2>
<p>
    All you need to do is, when implementing Ogone, make use of the <strong>templates/clean.html</strong> file. Like this:
</p>
<pre><code>&lt;input name="TP" type="hidden" value="https://e-sites.github.io/ogone.css/dist/template.html"&gt;</code></pre>
<p>
    Ogone will fetch the <strong>.html</strong> file and the string '$$$PAYMENT ZONE$$$' will be replaced with their payment form. As for the CSS styles, these will be loaded directly from GitHub.
</p>
<hr>
<h2>Roll your own styles</h2>
<p>
    The default <strong>Ogone.css</strong> styles are based on <a href="http://getbootstrap.com/" target="_blank">Bootstrap</a> but you can quite easily roll your own when you're comfortable around LESS / CSS.
</p>
<p class="alert alert-info">
    Please note that when you want to customize either the HTML or the CSS you'll need to host both files on your own server.
</p>
<hr>
<h2>Distribution build</h2>
<p>
    The original HTML and CSS is already worse as it is, so <strong>Ogone.css</strong> comes with an optimized build (created with <a href="http://gulpjs.com/" target="_blank">gulp.js</a>) for your production enviroment. All code is minified and unecessary CSS rules are stripped out with <a href="https://www.npmjs.org/package/gulp-uncss" target="_blank"><code>gulp-uncss</code></a>. After this optimization it clocks in at <strong>9KB</strong> minified and <strong>2KB</strong> when being served with gzip compression. This build is located in the <strong>dist</strong> directory.
</p>
<p>
    As for the HTML template, this is minified as well and points directly to the corresponding CSS (hosted on GitHub).
</p>
<h2>Contributing</h2>
<p>
    All help and feedback is appreciated. Perhaps we can work towards making multiple themes or build an interface to customize the payment view without even writing LESS / CSS. For now, we haven't layed out any ground rules yet, just fork this project and create a pull request when you to want get your changes merged.
</p>
<p>
    Editor preferences are available in the editor config for easy use in common text editors. Read more and download plugins at http://editorconfig.org.
</p>
<h2>Roadmap</h2>
<p>
    <strong>Ogone.css</strong> is not finished yet, we definitely got some things planned, such as:
</p>
<ul>
    <li>adding views from missing payment methods;</li>
    <li>write more documentation, both inline (in the code) as well on this very page;</li>
    <li>adding examples that work with other frameworks than Bootstrap;</li>
</ul>
<h2>About the author</h2>
<p>
    E-sites is a full service internet agency with offices in Breda (NL) and Curaçao. We create innovative, extraordinary and effective websites, (mobile) apps and web campaigns for organizations with online ambitions.
</p>
<p>
    <a href="https://twitter.com/esites" class="twitter-follow-button" data-show-count="false" data-lang="en">Follow @esites</a>
</p>
<h2>License</h2>
Copyright (C) 2014 e-sites, <a href="http://www.e-sites.nl/">http://e-sites.nl/</a> Licensed under the MIT license.
