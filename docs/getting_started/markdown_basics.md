---
layout: default
title: Markdown basics
parent: Getting started
nav_order: 4
---

# Markdown basics

Source: https://github.github.com/gfm/


[//]: # "This text will not render in the preview"

### Line breaks
Pressing the `enter` key will not generate empty lines. For that you can use a line break `<br/>`

### Headers

Represented by adding 1 to 6 leading # signs

### Emphasis

**bold text**

__bold text__

*italic text*

_italic text_


### Highlighting
`This text is highlighted using backward ticks`

### Monospace font
    You have to indent to have a monospace font. Typically used for writing code
    

### Blockquotes
> "Every great developer you know got there by solving problems they were unqualified to solve until they actually did it." *- Patrick McKenzie*

### Bullet lists
- item 1
- item 2
- item 3


### Numbered Lists
1. item 1
2. item 2
3. item 3


### Mixed lists
1. item 1
    - item 1a
    - item 1b
 


### In-line links
[Link to github-flavored markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


### Referenced links
[Try a live Markdown editor in your browser][1]

[1]: https://stackedit.io


### In-line images
Here is some text followed by an image: 
![alt_text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Instead of this image from an URL you can also link images in your own computer using the fullpath of the image.

### Referenced images
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

### Horizontal lines
[//]: # "Dashes"
--- 

[//]: # "Asterics"
***

[//]: # "Underscores"
___


### Code
`s = "Python inline code syntax highlighting"`

```python
s = "Python code block syntax highlighting"
print(s)
```

### Tables
You can use some online Markdown table generators

| item     | quantity | price |
|----------|----------|-------|
| oranges  | 5        | 0.45  |
| carrots  | 14       | 1.65  |
| goldfish | 1        | 5.00  |
