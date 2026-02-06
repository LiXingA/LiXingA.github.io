<!--{"pinCode":false,"dname":"d3b3ab07-184e-446a-b339-40d833614d89","codeMode":"markdown"}-->
````md
Headers
---------------------------

# Header 1

## Header 2

### Header 3



Styling
---------------------------

*Emphasize* _emphasize_

**Strong** __strong__

==Marked text.==

~~Mistaken text.~~

> Quoted text.

H~2~O is a liquid.

2^10^ is 1024.



Lists
---------------------------

- Item
  * Item
    + Item

1. Item 1
2. Item 2
3. Item 3

- [ ] Incomplete item
- [x] Complete item



Links
---------------------------

A [link](http://example.com).

An image: ![Alt](img.jpg)

A sized image: ![Alt](img.jpg =60x50)



Code
---------------------------

Some `inline code`.

```
// A code block
var foo = 'bar';
```

```javascript
// An highlighted block
var foo = 'bar';
```



Tables
---------------------------

Item     | Value
-------- | -----
Computer | $1600
Phone    | $12
Pipe     | $1


| Column 1 | Column 2      |
|:--------:| -------------:|
| centered | right-aligned |



Definition lists
---------------------------

Markdown
:  Text-to-HTML conversion tool

Authors
:  John
:  Luke



Footnotes
---------------------------

Some text with a footnote.[^1]

[^1]: The footnote.



Abbreviations
---------------------------

Markdown converts text to HTML.

*[HTML]: HyperText Markup Language
````

<!--{"pinCode":false,"dname":"1de7a950-e351-4dac-9853-cd78351ebb8e","codeMode":"markdown"}-->
```md
LaTeX math
---------------------------

The Gamma function satisfying $\Gamma(n) = (n-1)!\quad\forall
n\in\mathbb N$ is via the Euler integral

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$
```

<!--{"pinCode":false,"dname":"693ddff7-a5ba-41ed-ae3d-344a01121f1a","codeMode":"markdown"}-->
```md
## Grove extension config
```

<!--{"pinCode":false,"dname":"feb3c0ec-cd66-4dec-a5d4-67b23a13ef5c","codeMode":"markdown"}-->
```md
\*\* admin >> Extensions >> Grove >> Config(JSON) \*\*
```

```
  {"noOnlineRequire":false,"isStaticConfig":false, "isGroveHub":false, "liteDashboard":false, "noRecordTabs": true}
```

<!--{"pinCode":false,"dname":"68ac40db-97b6-4983-bbf1-79a7cc37e05e","codeMode":"markdown"}-->
```md
1. noOnlineRequire:  offline or online to fetch librarys

2. isStaticConfig: **fetch github site** to get datas to decide whether need display the static grove pages

3. isGroveHub: **graphxr admin** to decide whether need display the static grove pages, which in "Grove Hub" project json configuration.

4. liteDashboard: simple no code grove UI

5. noRecordTabs: don't not record tabs?
```
