

# Md-Viewer


React component to render markdown with side panel.


## Contents

*   [What is this?](#what-is-this)
*   [Install](#install)
*   [Use](#use)
*   [props](#props)
*   [Syntax](#syntax)

## What is this?

This package is a [React][] component that can be given a string of markdown
that it’ll safely render to React elements, with also a side panel with a list of the headers. which can be used to scroll to a heading. 

*   to learn markdown, see this [cheatsheet and tutorial][cheat]


## Install

This package is not on npm now, I am working on dat. 
For now, u will have to fork from github anfd pull into ur project as a COmponent in ur react project.


## Use

A basic MdViewer use:

```jsx
import React from 'react'
import ReactMarkdown from 'react-markdown'
import ReactDom from 'react-dom'

md = "# Hello, *world*!"
ReactDom.render(
  <MdViewer markdown={md}/>,
  document.body
)

```


<details>
<summary>Show equivalent JSX</summary>

```jsx
<h1>
  Hello, <em>world</em>!
</h1>
```


## `props`

*   `markdown` (`string`, default: `''`)\
    markdown to parse
*   `isMobile` (`boolean`, default: `false`)\
    if true, no side panel, just react page
    (`data-sourcepos="3:1-3:13"`)
*   `right` (`boolean`, default: `false`)\
    if true, side panel is at right, else left
    (`sourcePosition: {start: {line: 3, column: 1}, end:…}`)
*   `width` (`boolean`, default: `50`)\
    width for images in markdown

    
## Syntax

`react-markdown` follows CommonMark, which standardizes the differences between
markdown implementations, by default.
Some syntax extensions are supported through plugins.

We use [`micromark`][micromark] under the hood for our parsing.
See its documentation for more information on markdown, CommonMark, and
extensions.
