# MarkAPL


## Overview

`MarkAPL` is a converter that converts [Markdown ](https://daringfireball.net/projects/markdown/ "The original Markdown specification") into valid HTML5. It is written in Dyalog.

**Note:** `MarkAPL` releases are published as [Tatin](https://tatin.dev "Link to the principal Tatin Registry") packages, see there.

Markdown aims to make the process of writing for the web much easier by improving readability and, as a consequence, maintainability.

[This is an example on the Wikipedia](https://www.wikiwand.com/en/Markdown#Example) comparing Markdown with HTML.

`MarkAPL` can convert APL variables holding Markdown as well as files holding Markdown.

Note that the original design of Markdown has proven to be an excellent idea but too limited for widespread use. Therefore extensions were implemented. Over time two approaches have proven to be particularly successful: [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/) and [PanDoc](http://pandoc.org/README.html).

For several years it seemed that the segmentation of the different implementations would be a problem, but over time the implementations got closer. There is also the [CommonMark](http://commonmark.org/) initiative which aims to standardize Markdown. `MarkAPL` tries to be compliant with CommonMark within reason.

`MarkAPL` aims to implement most concepts and also adds a couple of enhancements that might be useful, be it in general or just for APLers.

Today Markdown is used by many of the big names on the web. Examples are Git, SourceForge, Stack Overflow and Trello. Many wikis allow Markdown at least optionally for input.

The following table highlights the features supported in `MarkAPL`:

|**Name**                  | **Standard**   |**Extra**  |**Pandoc**  |**MarkAPL** |
|--------------------------|----------------|-----------|------------|------------|
|Abbreviations             |                |           |    X       |    X       |
|Automated links           |    X           |    X      |    X       |    X       |
|Blockquotes               |    X           |    X      |    X       |    X       |
|Calling APL functions     |                |           |            |    X       |
|Code blocks (indented)    |    X           |    X      |    X       |  Never!    |
|Code blocks (fenced)      |                |    X      |    X       |    X       |
|Definition lists          |    X           |    X      |    X       |    X       |
|Footnotes                 |    X           |    X      |    X       |    X       |
|Headers                   |    X           |    X      |    X       |    X       |
|HTML blocks               |    X           |    X      |    X       |    X       |
|HR (horizontal rule)      |    X           |    X      |    X       |    X       |
|Images                    |    X           |    X      |    X       |    X       |
|Inline markup             |    X           |    X      |    X       |    X       |
|Line breaks (two spaces)  |    X           |    X      |    X       |  Never!    |
|Line breaks    (`\`)      |                |           |    X       |    X       |
|Links                     |    X           |    X      |    X       |    X       |
|Link references           |    X           |    X      |    X       |    X       |
|Lists                     |    X           |    X      |    X       |    X       |
|Loose/tight lists         |    X           |    X      |    X       |            |
|Markdown inside HTML      |                |    X      |    X       |            |
|Paragraphs                |    X           |    X      |    X       |    X       |
|Tables                    |    X           |    X      |    X       |    X       |
|Table footers             |                |           |            |    X       |
|Table of contents (TOC)   |                |           |    X       |    X       |
|Sub TOC                   |                |           |            |    X       |
|Smart typography          |                |           |    X       |    X       |
|Special attributes        |                |   X       |    X       |    X       |
|Check boxes               |                |           |            |    X       |
|Collapsibles & accordions |                |           |            |    X       |
|LeanPub extensions        |                |           |            |    X       |

Note that marking up code blocks by indenting was deliberately not implemented in `MarkAPL`.


## Documentation 

A [full documentation](http://download.aplteam.com/MarkAPL.html) is available as an HTML page generated from Markdown with `MarkAPL`, as you would expect. This document is comprehensive and is therefore quite long: more than 40 pages.

There is also a [cheat sheet](http://download.aplteam.com/MarkAPL_CheatSheet.html) available for the impatient APLer.


## Markdown editor "Meddy"

Note that there is an editor available that uses `MarkAPL` as converter: [Meddy](https://github.com/aplteam/Meddy "Meddy on GitHub"). 

The editor is quite basic but it supports all `MarkAPL` features. It sports the most important features you would expect from any editor (Undo/Redo and a powerful Search/Replace) and also comes with a tree view for navigation that is auto-generated from the headers .



