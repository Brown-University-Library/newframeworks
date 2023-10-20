---
title: "Process"
description: ""
icon: "account_tree"
date: "2023-08-22T13:34:03-04:00"
lastmod: "2023-08-22T13:34:03-04:00"
draft: true
toc: true
weight: 20
---

If we wanted to put example code in the site for the edification of readers, we could do so:
```html
<!-- required -->
<!doctype html>

<!-- required -->
<html lang="en">

<head>
    <!-- required -->
    <meta charset="utf-8">
    <!-- required -->
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <!-- required -->
    <meta name="description" content="A short description of the page">
    <!-- required -->
    <meta name="author" content="Brown University Library">
    <!-- required -->
    <title>The page title</title>
    <!-- not required, will almost certainly appear -->
    <link type="text/css" rel="stylesheet" media="screen" href="/css/style.css'" />
</head>
```
The code highlighter Chroma [supports ~200 languages](https://gohugo.io/content-management/syntax-highlighting/#list-of-chroma-highlighting-languages).

Lotus Docs supports use of [mermaid](https://mermaid.js.org/):
```mermaid
sequenceDiagram
    Alice ->> Bob: Hello Bob, how are you?
    Bob-->>John: How about you John?
    Bob--x Alice: I am good thanks!
    Bob-x John: I am good thanks!
    Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

    Bob-->Alice: Checking with John...
    Alice->John: Yes... John, how are you?
```
