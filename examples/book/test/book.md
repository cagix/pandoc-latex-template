---
title: "Example PDF"
author: "Vorname Name"
#lang: de-DE
lang: en-US

bibliography: wuppi.bib
link-citations: true
csl: "chicago-author-date.csl"
#csl: "chicago-author-date-de.csl"
#csl: "din-1505-2-alphanumeric.csl"
#csl: "din-1505-2-numeric-alphabetical.csl"
#csl: "din-1505-2.csl"
#csl: "springer-lecture-notes-in-computer-science.csl"
#csl: "springer-lecture-notes-in-computer-science-alphabetical.csl"

references:
- type: article-journal
  id: WatsonCrick1953
  author:
  - family: Watson
    given: J. D.
  - family: Crick
    given: F. H. C.
  issued:
    date-parts:
    - - 1953
      - 4
      - 25
  title: 'Molecular structure of nucleic acids: a structure for deoxyribose
    nucleic acid'
  title-short: Molecular structure of nucleic acids
  container-title: Nature
  volume: 171
  issue: 4356
  page: 737-738
  DOI: 10.1038/171737a0
  URL: http://www.nature.com/nature/journal/v171/n4356/abs/171737a0.html
  language: en-GB
- id: doe99
  type: book
  author:
  - family: Urma
    given: R.-G.
  - family: Fusco
    given: M.
  - family: Mycroft
    given: A.
  issued:
  - year: 2014
  title: 'Java 8 in Action: Lambdas, Streams, and Functional-Style Programming'
  publisher: Manning Publications
  ISBN: 978-1-6172-9199-9
- id: smith04
  type: book
  author:
  - family: Osherove
    given: R.
  issued:
  - year: 2014
  title: The Art of Unit Testing
  publisher: Manning
  ISBN: 978-1-6172-9089-3
---

<!--
pandoc book.md -o book.pdf --filter=pandoc-citeproc 
-->

<!-- XXX
https://groups.google.com/forum/#!topic/pandoc-discuss/phRIa9TeQbs

https://editor.citationstyles.org/visualEditor/
https://www.zotero.org/styles
-->


# Vinaque sanguine metuenti cuiquam Alcyone fixus

de-DE: [@WatsonCrick1953] ... [@WatsonCrick1953, Seite 111] und [@WatsonCrick1953, Kapitel 111] ...

en-US: [@WatsonCrick1953] ... [@WatsonCrick1953, page 111] und [@WatsonCrick1953, section 111] und [@WatsonCrick1953, chapter 111] ...


# Excerpt from https://pandoc.org/demo/example19/Extension-citations.html

Citations go inside square brackets and are separated by semicolons. Each citation must have a key, composed of `@' + the citation identifier from the database, and may optionally have a prefix, a locator, and a suffix. The citation key must begin with a letter, digit, or _, and may contain alphanumerics, _, and internal punctuation characters (:.#$%&-+?<>~/). Here are some examples:

Blah blah [see @doe99, pp. 33-35; also @smith04, chap. 1].

Blah blah [@doe99, pp. 33-35, 38-39 and *passim*].

Blah blah [@smith04; @doe99].

pandoc-citeproc detects locator terms in the CSL locale files. Either abbreviated or unabbreviated forms are accepted. In the en-US locale, locator terms can be written in either singular or plural forms, as book, bk./bks.; chapter, chap./chaps.; column, col./cols.; figure, fig./figs.; folio, fol./fols.; number, no./nos.; line, l./ll.; note, n./nn.; opus, op./opp.; page, p./pp.; paragraph, para./paras.; part, pt./pts.; section, sec./secs.; sub verbo, s.v./s.vv.; verse, v./vv.; volume, vol./vols.; ¶/¶¶; §/§§. If no locator term is used, “page” is assumed.

pandoc-citeproc will use heuristics to distinguish the locator from the suffix. In complex cases, the locator can be enclosed in curly braces (using pandoc-citeproc 0.15 and higher only):
[@smith04{ii, A, D-Z}, with a suffix]
[@smith04, {pp. iv, vi-xi, (xv)-(xvii)} with suffix here]

A minus sign (-) before the @ will suppress mention of the author in the citation. This can be useful when the author is already mentioned in the text:
smith04 says blah [-@smith04].

You can also write an in-text citation, as follows:

@smith04 says blah.

@smith04 [p. 33] says blah.


# Literatur 

