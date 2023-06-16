---
title: 'Style Guide'
---

A collection of guidelines to follow when writing
source (R) Markdown files for use with {sandpaper}.
The Carpentries also provides a [general Style Guide](https://docs.carpentries.org/topic_folders/communications/resources/style-guide.html)
for written content e.g. blog posts, website and lesson content, etc.

- [Fenced Divs](#fenced-divs)
  - [Fence Length](#fence-length)
  - [Whitespace](#whitespace)
- [Figures](#figures)
- [Line Length](#line-length)

## Fenced Divs

### Fence Length

For increased legibility, we recommend an opening fence length of at least 50 colons
(half to two-thirds of the screen), 
with a single space between the last colon and the class keyword.
The length of closing fences should match the length of the opening fence plus keyword,
for example:

```markdown
:::::::::::::::::::::::::::::::::::::::::::::::::: callout

### An example callout

This callout was opened with a fence of 50 colons.
The end of the closing fence aligns with
the last character in the 'callout' keyword.

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
```

Where fenced divs are nested,
e.g. attaching a solution block to a challenge,
we recommend making the inner fences noticably shorter
than the outer fences, e.g. 25 colons (one quarter to one third of the screen).
E.g.

```markdown
:::::::::::::::::::::::::::::::::::::::::::::::::: challenge

### An example challenge

This challenge was opened with a fence of 50 colons.

:::::::::::::::::::::::: solution

The nested solution block was opened with 25 colons,
to make it stand out from the challenge.

:::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
```

### Whitespace

For legibility and to avoid potential formatting issues,
empty lines should flank the fences of a fenced div, e.g.

```markdown
:::::::::::::::::::: callout

### Good: whitespace either side of the fences

This will ensure Markdown content renders as intended.

::::::::::::::::::::::::::::

:::::::::::::::::::: callout
### Not recommended
Without empty lines flanking the opening and closing fences,
this callout is more difficult to read
and some Markdown 
[content such as lists may not render as intended](https://github.com/carpentries/sandpaper/issues/355).
::::::::::::::::::::::::::::
```

## Figures

We recommend splitting Markdown image elements across multiple lines,
to enhance readability:

```markdown
![
The text in these square brackets provides a caption to images in 
[the Markdown syntax of The Carpentries Workbench](https://carpentries.github.io/sandpaper-docs/example.html#figures).
](path/to/figure.svg){
alt='Alternative text descriptions are defined here'
width='33%'
}
```

![
The text in these square brackets provides a caption to images in 
[the Markdown syntax of The Carpentries Workbench](https://carpentries.github.io/sandpaper-docs/example.html#figures).
](https://placekitten.com/300/300){
alt='A random picture of a cute kitten'
width='33%'
}

Source Markdown for figures can be difficult to read when confined to a single line,
especially if the image caption contains its own Markdown elements such as links. 

For comparison, here is the one-line equivalent to the example above:

```markdown
![The text in these square brackets provides a caption to images in [the Markdown syntax of The Carpentries Workbench](https://carpentries.github.io/sandpaper-docs/example.html#figures).](path/to/figure.svg){alt='Alternative text descriptions are defined here' width='33%'}
```

## Line Length

We recommend the use of [_Semantic Line Breaks_][sembr]
with a maximum line length of 100 characters.
As detailed in the Semantic Line Breaks specification,

> A line MAY exceed the maximum line length if necessary, 
> such as to accommodate hyperlinks, code elements, or other markup.

[sembr]: https://sembr.org/