[parm]:title             = 'MarkAPL Quick Intro'
[parm]:enforceEdge       = 1
[parm]:leanpubExtensions = 1
[parm]:printCSS          = 'BlackOnWhite_print.css'
[parm]:screenCSS         = 'BlackOnWhite_screen.css'
[parm]:linkToCSS         = 0
[parm]:saveHTML          = 1
[parm]:toc               = 2 3 4 5 6
[parm]:numberHeaders     = 2 3 4 5 6




Quick introduction to `MarkAPL`
=============================

By now you are likely aware that `MarkAPL` converts Markdown to HTML5.

All you need is the [Tatin package](https://tatin.dev "Link to the principal Tatin registry") `MarkAPL`.


Quick start
----------

### Making `MarkAPL` available


Assuming that you have some Markdown in the workspace:

~~~
      MyMarkdown←'# MarkAPL' 'All about **_MarkAPL_**'
~~~

There are two possible scenarios:


### Converting Markdown into HTML

To convert Markdown into HTML, call the `Markdown2HTML` method:

~~~
      (html ns)←MarkAPL.Markdown2HTML MyMarkdown
      50↑∊html
<a id="markapl" class="autoheaderlink"><h1>MarkAPLstrong></p>
~~~

Note that not only the HTML but also a namespace `ns` is returned which, among other stuff, has a variable `report` that might carry warnings and error reports. Ideally `report` is empty.

This way of calling `Markdown2HTML` relies entirely on defaults. If you are not happy with those you must specify parameters in one of two ways:

* Create a parameter space (usually by calling `MarkAPL.CreateParms`), modify the parameters, and pass the namespace as the left argument to `Markdown2HTML`. The next topic explains this process.
* Embed the specific parameters you need into your Markdown. The subsequent topic elaborates on this approach.


### Creating a fully fledged HTML page with a parameter space

To instruct `MarkAPL` to generate a complete HTML page, you can either specify `outputFilename` or set the `createFullHtmlPage` flag to 1:

~~~
      parms←MarkAPL.CreateParms
      parms.createFullHtmlPage←1
      (html ns)←parms MarkAPL.Markdown2HTML MyMarkdown
      ⍪4↑html
 <!DOCTYPE html>        
 <html>                 
 <head>                 
 <meta charset="utf-8"> 
~~~

Setting `outputFilename` has the additional benefit of writing the HTML to that file. 

Note that `parms` is a namespace that stores default values. You can list them by calling `parms.∆List`.


### Create a fully fledged HTML page with embedded parameters

To make `MarkAPL` generate a complete HTML page, you can _embed_ `outputFilename` or `createFullHtmlPage` into the Markdown:

~~~
      (html ns)←MarkAPL.Markdown2HTML (⊂'[parm]:createFullHtmlPage=1'),MyMarkdown
      ⍪4↑html
 <!DOCTYPE html>        
 <html>                 
 <head>                 
 <meta charset="utf-8"> 
~~~


Documentation
------------

* For the cheat sheet call `MarkAPL.Help 0`
* For comprehensive documentation, call `MarkAPL.Reference 0`


Misc
----

Please send comments, suggestions and bug reports to kai@aplteam.com.   

Kai Jaeger ⋄ 2016-02-17

Last update: 2023-11-16

