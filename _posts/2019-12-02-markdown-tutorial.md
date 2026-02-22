---
layout: post
date: 2019-12-02 16:46:01 +0200
title: 
image: https://i.ytimg.com/vi/8cpwhFHE6hc/maxresdefault.jpg
categories: [Tutorial]
tags: [Code, Markdown, Kramdown]
published: true
comments_id: 3
---

Markdown is a way to write content for the web. It’s written in what people like to call “plaintext”, which is exactly the sort of text you’re used to writing and seeing. Plaintext is just the regular alphabet, with a few familiar symbols, like asterisks ( `*` ) and backticks ( `` ` `` ).

## Table of Contents
{:.no_toc}
{: #index}

----

- TOC
{:toc}

----


## Links

There are a few different ways to display links with markdown markup, but to keep some standards, let's try to use the following options only.


### Mailto links

If you're adding an email address to a page be sure to format your link with mailto to avoid creating broken links. For example, `[email](mailto:example@gitlab.com)` or `<example@github.com>`

An e-mail [email](mailto:example@gitlab.com) or <kyr@designisdesign.eu> link.

### Internet links

```
Simple inline link <http://www.google.com>, another inline link [Smaller](http://smallerapp.com), one more inline link with title [Resize](http://resizesafari.com "a safari extension")
```

Simple inline link <http://www.google.com>, another inline link [Smaller](http://smallerapp.com), one more inline link with title [Resize](http://resizesafari.com "a safari extension")

A [reference style][apple] link. Input id, then anywhere in the doc, define the link with corresponding id inside `[]` like this: 

```
[apple]: http://apple.com "To milaraki"
```

[apple]: http://apple.com "To milaraki"

Go [back](#index) to index


### Internal Links (links inside page)

If the internal content is on the same page then it is possible to link to it like this:

With this enabled each heading gets an id ref based on the [heading](#headers) text. For example to point to this heading:   


```
## My Funky Heading
```

we code like this:

```
Go to My [Funky Heading](#my-funky-heading)
```

> Note how the `My Funky Heading` becomes `#my-funky-heading`
we convert all `characters` to `lowercase` and `spaces` to `-`

If our heading contains special characters like `(, !, etc` ignore it:

example header with special characters
```
## My Funky Heading (with special characters like #$@[]} ignore all of this)
```

to link to above header we code like this:
```
[Funky](#my-funky-heading-with-special-characters-like-ignore-all-of-this)
```

How to link to a non `header` like a paragraph

Lets say we have a paragraph like this:

```
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

```
to link to this paragraph we create a link to this like:

```
{: #mylink}
```

so our paragraph becomes:

```
{: #mylink}
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

```

{: #mylink}
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

to link to this paragraph we use:

```
[Go](#mylink) to my paragraph
```

[Go](#mylink) to my paragraph

This also works for `headers` to

```
## My Funky Heading
{: #funky}
```

and our inside link will become:

```
Go to My [Funky Heading](#funky)
```

Try it click [HERE](#tables) and you jump to `### Tables` header


<!-- ##### Index -->

<!-- 1. [Buttons](#buttons) -->
<!-- 2. [Spoiler](#spoiler) -->
<!-- 3. [Strong and emphasize](#strong-and-emphasize) -->
<!-- 4. [Blockquotes](#blockquotes) -->
<!-- 5. [Headers](#headers) -->
<!-- 6. [Links and Email](#links-and-email) -->
<!-- 7. [Horizontal Rules](#horizontal-rules) -->
<!-- 8. [Banners](#banners) -->
<!-- 9. [Colors](#colors) -->



## Lists

Both ordered and unordered lists are very straight-forward to produce. There are a few ways to produce the same results, but let's stick with the following, again, to maintain some standards.

Always use **3** blank spaces to indent a nested list (to create sub items).

Tip: don't leave blank lines **between the items**, unless you have a reason to do so.

Important: always leave a blank line between the paragraph or heading and the subsequent list! If you don't, the list will not render.
{: .alert .alert-danger}

### Ordered lists

Ordered lists are pretty easy to create. Couldn't be more intuitive:
```
Paragraph:

1. Item one
   1. Sub item one
   2. Sub item two
   3. Sub item three
2. Item two
```

Paragraph:

1. Item one
   1. Sub item one
   2. Sub item two
   3. Sub item three
2. Item two

To be practical and avoid errors on the numbers, use "1" for all the items. The markdown engine will output them in the correct order.
```
Paragraph:

1. Item one
   1. Sub item one
   1. Sub item two
   1. Sub item three
1. Item two
```

### Unordered lists

Unordered lists are very easy to create too:
```
Paragraph:

- Item 1
- Item 2
- Item 3
   - Sub item 1
   - Sub item 2
- Item 4
```

Paragraph:

- Item 1
- Item 2
- Item 3
   - Sub item 1
   - Sub item 2
- Item 4

### Split lists

Let's say, for some reason, you want to split a list in different parts. To do that, use the markup ^ to indicate the end of a list and the beginning of the next:
```
- list one - item 1
- list one - item 2
   - sub item 1
   - sub item 2
- list one - item 3
^
- list two - item A
- list two - item B
^
- list three - item _i_
- list three - item _ii_
```

- list one - item 1
- list one - item 2
   - sub item 1
   - sub item 2
- list one - item 3
^
- list two - item A
- list two - item B
^
- list three - item _i_
- list three - item _ii_

Go [back](#index) to index




## Images

To insert images to your markdown file, use the markup `![ALT](/path/image.ext)`. The path can either be relative to the website, or a full URL for an external image. The supported formats are `.png`, `.jpg`, `.gif`.

Local photo (from ours blog) example:

```
![image of slovenia](/assets/images/Slovenia.jpg)
```

![description of image](/assets/images/Slovenia.jpg)

Remote image (from internet) example:
```
![image of paris](https://d2mpqlmtgl1znu.cloudfront.net/AcuCustom/Sitename/DAM/020/Paris_AdobeStock_264549883_1.jpg)
```

![description of image](https://d2mpqlmtgl1znu.cloudfront.net/AcuCustom/Sitename/DAM/020/Paris_AdobeStock_264549883_1.jpg)

You can use photos reference list for images like this: (put the list to the end of the document)
```
[slovenia]: /assets/images/Slovenia.jpg
[paris]: https://d2mpqlmtgl1znu.cloudfront.net/AcuCustom/Sitename/DAM/020/Paris_AdobeStock_264549883_1.jpg
```

[slovenia]: /assets/images/Slovenia.jpg
[paris]: https://d2mpqlmtgl1znu.cloudfront.net/AcuCustom/Sitename/DAM/020/Paris_AdobeStock_264549883_1.jpg

and call the images like this
```
![image of slovenia][slovenia]
```

![image of slovenia][slovenia]



### Clickakble images

For clickable images, simply wrap the image markup into a link markup:
```
[![description of image](https://d2mpqlmtgl1znu.cloudfront.net/AcuCustom/Sitename/DAM/020/Paris_AdobeStock_264549883_1.jpg)](google.com)
```

Click the bellow image to see it in action

[![description of image](https://d2mpqlmtgl1znu.cloudfront.net/AcuCustom/Sitename/DAM/020/Paris_AdobeStock_264549883_1.jpg)](http://images.google.com/images?um=1&hl=en&safe=active&nfpr=1&q=paris&start=30)


### Image size

To change image size append to the end of line the following for 500px wide image (change the number to your liking):
```
{: width="500px"}
```

![paris][paris]{: width="500px"}

You can also add a shadow like this `{: .shadow}`
```
![paris][paris]{: width="500px"}{: .shadow}
```

![paris][paris]{: width="500px"}{: .shadow}


### Wrap text around image

To wrap text around an `left` aligned image append the follow code like this:
```
![wrapimage](image){: .img-left}
```
![wrapimage](https://d2mpqlmtgl1znu.cloudfront.net/AcuCustom/Sitename/DAM/020/Paris_AdobeStock_264549883_1.jpg){: .img-left}
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.

To wrap text around an `right` aligned image and also justify text append the follow code like this:
```
![wrapimage](/assets/images/Slovenia.jpg){: .img-right}
Lorem Ipsum is simply dummy text of the printing and typesetting industry...
{: .text-justify}
```
![wrapimage](https://d2mpqlmtgl1znu.cloudfront.net/AcuCustom/Sitename/DAM/020/Paris_AdobeStock_264549883_1.jpg){: .img-right}
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
{: .text-justify}

The image size is set to `height:210px` in **`assets/css/kyr.css`**
{: .banner-red}

Go [back](#index) to index


## Table of Contents (ToC)

Creating a Table of Contents is the easiest thing ever! The automatic ToC will include every heading in the document, unless you don't want it to be included. You do not need to add anchors individually to every title. This is an automated process.

```
---

## On this page
{:.no_toc}

- TOC
{:toc}

---
```

The markup `{:.no_toc}` is used every time you don't want to include a heading into the ToC. Just add it right below the heading, and it won't be included into the ToC

Alternatively, you can use ordered ToC too, displaying numbers at the beginning of the list. 
```
1. TOC
{:toc}
```

The **output** ToC can be found at the very beginning of this page.

Go [back](#index) to index



## Horizontal Rules

If you type three asterisks `***` or three dashes `---` on a line, I'll display a horizontal rule:

This is an horizontal rule:

---

Go [back](#index) to index 




## Buttons 

Make any link standout more when applying the .btn class.

```
[Primary Button](#link){: .btn .btn-primary}
[Warning Button](#link){: .btn .btn-warning}
[Danger Button](#link){: .btn .btn-danger}
[Info Button](#link){: .btn .btn-info}

[Outline Danger Button](#){: .btn .btn-outline-danger}
[Outline Primary Button](#){: .btn .btn-outline-primary}
[Dark Button](http://google.com){: .btn .btn-dark}
```

[Primary Button](#link){: .btn .btn-primary}
[Warning Button](#link){: .btn .btn-warning}
[Danger Button](#link){: .btn .btn-danger}
[Info Button](#link){: .btn .btn-info}

[Outline Danger Button](#){: .btn .btn-outline-danger}
[Outline Primary Button](#){: .btn .btn-outline-primary}
[Dark Button](http://google.com){: .btn .btn-dark}


```
[<i class="fa fa-warning" aria-hidden="true"></i>My Button](#){: .button}
[My button](#){: .button}
```

[<i class="fa fa-warning" aria-hidden="true"></i>My Button](#){: .button}
[My button](#){: .button}


## Spoiler

So how do we do spoilers?

```html
<span class="spoiler">My hidden paragraph here.</span>
```

The movie ends <span class="spoiler">This is a spoiler.</span> [^emphasize] 

[^emphasize]: If **Underlines** is turned on, `_this notation_` will render as underlined instead of emphasized 

## Strong and emphasize

`**strong**` or `__strong__`  
`*emphasize*` or `_emphasize_`

**Sometimes I want a lot of text to be bold. Like, seriously, a _LOT_ of text**

Read more in [text](#text) section

{: #headers}
## Headers (like this one!)

```
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6
```


## Banners

Create colorful banners `red`, `green` and `yellow`

To put a text line inside a colorful banner put the following code bellow the text line you wish to convert to a banner

example code for a green banner:
> replace `green` with `red` or `yellow` for other colors

```
Hi, i am a green banner!
{: .banner-green }
```

Bellow is a green banner example

Hi, i am a **green** banner!
{: .banner-green }

This is a red banner

Hi, i am a **red** banner!
{: .banner-red }

This is a yellow banner

Hi, i am a **yellow** banner!
{: .banner-yellow }



## Notes

```
This is a regular paragraph.

**Note:** a note is something that needs to be mentioned but is apart from the context.
{: .alert .alert-warning}
```

This is a regular paragraph.

**Note:** a note is something that needs to be mentioned but is apart from the context.
{: .alert .alert-success}


### Colorful notes

My warning
{: .alert .alert-warning}

My danger paragraph.
{: .alert .alert-danger}

My important paragraph center.
{: .alert .alert-info .text-center}



## Text

Format text examples

```
**This line is bold**
This **word** is bold
*This line is italic*
***This line is bold italic***
~~This line is strikethrough~~
```

**This line is bold**  
This **word** is bold  
*This line is italic*  
***This line is bold italic***  
~~This line is strikethrough~~

To center a `text` to the page

```
Center-aligned
{: .text-center}
```

This line is Center-aligned
{: .text-center}

For **`headers/titles`** go to [Headers](#headers) section  
To see how to **`color`** a text line got to [Colors](#colors) section

Go [back](#index) to index




## Videos

There are two ways of displaying videos: within HTML5 `<video>` tags and within `<iframe>` tags.

### Display videos from YouTube

To display a youtube video go to <http://youtube.com> open a video you like and press the share button, then click the `Embend` button and in the next window copy the code and paste it anywhere in the page you want to display like bellow:

```
<iframe width="560" height="315" src="https://www.youtube.com/embed/o8NPllzkFhE?si=ogWir5LzSfuBm-Z1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/o8NPllzkFhE?si=ogWir5LzSfuBm-Z1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Display local videos (HTML5)

To display a local video upload first your video to `/assets/videos/` folder and an image to represent the video as a poster in the same directory, See the code and the output

```
<video width="560" height="315" controls="true" allowfullscreen="true" poster="/assets/videos/wado.jpg">
<source src="/assets/videos/Wado.m4v" type="video/mp4">
</video>
```

<video width="560" height="315" controls="true" allowfullscreen="true" poster="/assets/videos/wado.jpg">
<source src="/assets/videos/Wado.m4v" type="video/mp4">
</video>

Note that you can control the size of the video with the `width` & `height` variables
{: .alert .alert-warning}




## Colors

To change color to a text line put bellow the line this code:

```
This line becomes **red**
{: style="color:red;"}
```

This line becomes **red**
{: style="color:red;"}

```
This line becomes **blue**
{: style="color:blue;"}
```

This line becomes **blue**
{: style="color:blue;"}

More advance code:

```
This is **yellow** text with black backgroud
{: style="color:yellow;background-color:black;"}
```

This is **yellow** text with black backgroud
{: style="color:yellow;background-color:black;"}

Go [back](#index) to index



## Code blocks

There are a few options for displaying code blocks with markdown. Most of them use backticks `` ` ``.

### In-line

This is an `` `in-line` `` code block

Output:

This is an `in-line` code block


### Fenced

~~~
```
This is fenced message
```
~~~

```
This is fenced message
```

Go [back](#index) to index



## Blockquotes

Blockquotes are good resources to mentioning someone else's quotes, like we did just above. Also, can be used to emphasize a sentence or a small paragraph.

```
> Right angle brackets \> are used for block quotes.
```

> Right angle brackets \> are used for block quotes.


```
> This is a blockquote.
>     On multiple lines.
That may be lazy.
>
> This is the second paragraph.

----

> This is a paragraph.
>
> > A nested blockquote.
>
> ### Headers work
>
> * lists too
>
> and all other block-level **elements**.
>
> Even code blocks:
>
>      def hello
>        puts "Hello world!"
>      end
> {: .language-ruby}
```

> This is a blockquote.
>     On multiple lines.
That may be lazy.
>
> This is the second paragraph.

----

> This is a paragraph.
>
> > A nested blockquote.
>
> ### Headers work
>
> * lists too
>
> and all other block-level **elements**.
>
> Even code blocks:
>
>      def hello
>        puts "Hello world!"
>      end
> {: .language-ruby}


## Tables

Tables for markdown are challenging. So, we have two possible approaches: use markdown whenever possible, but if you need pretty advanced table layouts, you are free to add them in HTML markup instead.

Tables for markdown are challenging. So, we have two possible approaches: use markdown whenever possible, but if you need pretty advanced table layouts, you are free to add them in HTML markup instead.

Example table code:
```
| Option name         | Markup           | Result if enabled    |
|---------------------|:----------------:|---------------------:|
| Intra-word emphasis | So A\*maz\*ing   | So A<em>maz</em>ing  |
| Strikethrough       | \~~Much wow\~~   | <del>Much wow</del>  |
| Underline [^under]  | \_So doge\_      | <u>So doge</u>       |
| Quote [^quote]      | \"Such editor\"  | <q>Such editor</q>   |
| Highlight [^math]   | \==So good\==    | <mark>So good</mark> |
| Superscript         | hoge\^(fuga)     | hoge<sup>fuga</sup>  |
| Autolink            | http://t.co      | <http://t.co>        |
| Footnotes           | [\^4] and [\^4]: | [^4] and footnote 4  |
```

The following is a list of optional inline markups supported:

| Option name         | Markup           | Result if enabled    |
|---------------------|:----------------:|---------------------:|
| Intra-word emphasis | So A\*maz\*ing   | So A<em>maz</em>ing  |
| Strikethrough       | \~~Much wow\~~   | <del>Much wow</del>  |
| Underline [^under]  | \_So doge\_      | <u>So doge</u>       |
| Quote [^quote]      | \"Such editor\"  | <q>Such editor</q>   |
| Highlight [^math]   | \==So good\==    | <mark>So good</mark> |
| Superscript         | hoge\^(fuga)     | hoge<sup>fuga</sup>  |
| Autolink            | http://t.co      | <http://t.co>        |
| Footnotes           | [\^4] and [\^4]: | [^4] and footnote 4  |

Go [back](#index) to index or [back](#mylink) to my paragraph.

---

[^under]: If **Underline** is disabled `_this_` will be rendered as *emphasized* instead of being underlined.

[^quote]: **Quote** replaces literal `"` characters with html `<q>` tags. **Quote** and **Smartypants** are syntactically incompatible. If both are enabled, **Quote** takes precedence. Note that **Quote** is different from *blockquote*, which is part of standard Markdown.

[^math]: Internet connection required.

[^index]: This is like tables of contents.




