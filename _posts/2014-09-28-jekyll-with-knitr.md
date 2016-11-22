---
layout: post
title:  "Serve Jekyll Websites with servr and knitr"
comments:  false
published:  true
categories: [jekyll, rstats]
tags: [knitr, servr, httpuv, websocket]
---
## On the Markdown renderers

Jekyll supports a number of Markdown renderers, such as kramdown, redcarpet, rdiscount, and so on. At the moment, it is a little annoying that kramdown supports LaTeX math expressions via `$$ math $$`[^4], but does not support syntax highlighting of code blocks using the three backticks syntax (you must write the awkward Liquid tags); on the other hand, redcarpet does not support LaTeX math but does support three backticks. In my opinion, all the different flavors and implementations of Markdown is the biggest problem of Markdown, since there is not an unambiguous spec for Markdown. [CommonMark](http://commonmark.org) looks like a promising project to set up a common spec for Markdown, and [Pandoc](http://johnmacfarlane.net/pandoc/) is a great implementation that has brought almost all the features that you may ever need in Markdown. You may find some Pandoc plugins for Jekyll by searching online. However, GitHub Pages does not support arbitrary Jekyll plugins, so you cannot just use a Pandoc plugin there, but that does not mean you cannot use Pandoc locally, nor does it mean you cannot push locally compiled HTML pages to Git
