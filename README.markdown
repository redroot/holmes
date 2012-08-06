holmes.css - CSS Markup Detective
=================================

Holmes is stand-alone diagnostic CSS stylesheet that can highlight
potentially invalid, inaccassible or erroneous HTML(5) markup by adding one class.

### What does it cover?

The holmes.css file will display either an error (red outline), a warning (yellow outline), or a deprecated style (dark grey outline)
for flags such as:

+	__Missing required attributes on tags__, such as alt tags on images (lots of these)
+	__Deprecated and Non-W3C Elements__ - see [http://www.w3.org/TR/html5/obsolete.html#obsolete] (W3C.org's article on obselete tags)
+	__Non-W3C Attributes__ - as above, just the most important ones since there are MANY

Hovering over most elements will cause a description to be displayed in the top left, or top right corner of the screen.
	
### Why should I use it?

holmes.css is useful for checking the quality of your code (up to W3C HTML5 standards), nitpicking over ensuring markup is valid and semantic, and when you are tasked to fix up
and debug an old, OLD website. It has a simple implementation and a mostly unobtrusive effect on your page. Not recommended for live enviroments.

Remember too that these are just guidelines: if something is flagged but you can't change it for a good reason, don't worry about it :) Also use a validator if you want to be 100% sure.
	
### How do I use it?

Simply download a version of the CSS, minified or normal (with docs), and include a stylesheet link to it on your 
page. Or copy the contents into one of your own stylesheets. Then add the class "__holmes-debug__" to either your BODY or HTML tag, and you're set to go.

In terms of configuration, such as changing the flag colours: go nuts!

### Browser Support

Works 100% in

-	Google Chrome 10+
-	Safari 5+
-	Opera 10+
-	Firefox 3.5+

Due to extensive use of the __:not__ CSS3 selector, holmes.css does not function well in IE 8 and below,
but it should (NB: not tested yet) work in Internet Explorer 9. Oh well.

### License

Licenced under GPL license
http://www.gnu.org/licenses/gpl.html

### Acknowledgments

Inspired by [http://csswizardry.com/inuitcss/](InuitCSS),[http://meyerweb.com/eric/tools/css/diagnostics/](Eric Meyer), [http://www.nealgrosskopf.com/tech/thread.php?pid=17](Neal Grosskopf) and procrastination from coursework! 

Thanks for [http://www.twitter.com/MrNibbles](@MrNibbles) for the debug message on hover code!

Changelog 
---------

+ 06.08.12 - Removed error for missing title attributes, and downgraded empty alt to warning
+ 14.08.11 - Removed check for u tag since this is now valid in HTML5
+ 03.06.11 - Changes references of 'darkgrey' to a hex code to attempt to ensure the stylesheet is valid css3 (still 4 errors)
+ 27.04.11 - thanks to [http://www.twitter.com/MrNibbles](@MrNibbles), there is now a message on hover on any flagged elements. No support for ::after on images though :/
+ 27.04.11 - Changed the no title/empty title on anchor links to a warning level instead of a error level
+ 25.04.11 - Removed test for plaintext, even though it's still in the CSS file, since it BUTCHERED the rest of the testsuite page.
