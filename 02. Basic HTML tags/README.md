# Basic HTML tags

## HTML Structure

Below is the basic but necessary structure of `HTML` file!

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

`<!DOCTYPE html>` makes the browser know that the file is `HTML`! Technically, it gives the browser the information that the document type is `HTML 5`.

FYI : If you want to declare that the document type is older versions of `HTML`, you must use `DTD`, Document Type Definition.  
For example, if you want to declare that the document type is `HTML 4.01`, you should write the `<!DOCTYPE>` shown as below.

Example 1 : `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">`  
Example 2 : `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">`

Virtually, we use `HTML 5` only. We don't have to worry about older versions of `HTML`!

## HTML element

HTML `element` refers to the whole information which HTML `tag` contains. Let's look at `<h1> Hi! This is HTML!</h1>`. Here, we can say this is a HTML `h1` element. `<h1>` is a start tag, while `</h1>` is an end tag. In other words, HTML `element` is an information composed of a start tag, an end tag, and some contents between two tags.

Most HTML tags have a start tag and an end tag like `<h1>Hi! This is heading 1!</h1>` and `<p>This is paragraph!</p>`. However, not every HTML tag has an end tag. For example, `<br>` tag which enables a line break does not have an end tag and some contents, but `<br>` tag is still a HTML element. Let's look at the HTML file shown as below.

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1> Hi This is a heading </h1>
    <p> This is a paragraph. <br/> There was a line break. </p>
  </body>
</html>
```

We can say there is a `<html>` element which contains the whole information of the document. We can also say that there are some `<meta>` elements in `<head>` element! Even though `<head>` element has an end tag, each `<meta>` element in `<head>` element does not have an end tag. There is also a `<body>` tag, and `<h1>` and `<p>` elements in it. Looking at the `<p>` element, we can see a `<br/>` element which does not have an end tag!

So, can we just understand that HTML `element` is same as HTML `tag`? Roughly, maybe YES. But, technically NO!  
In this masterbook, I might use `element` with `tag` explaining my notes. :)

## Basic HTML tags \: \<h1\> to \<h6\> / \<p\> / \<a\> / \<img\>

`<h1>` to `<h6>`tags describes any contents for headings, and `<p>` is the tag to declare the paragraph. See that there is a line-break and margin between the first paragraph and the second paragraph, even though there is no `<br>` between `<p>` tags. This is because `<p>` element is actually a block element. The difference between `block` and `inline` elements is covered in my css masterbook.

Below are the screenshot of the `01-basic-html-tags.html` file and how it looks on the chrome browser.

Let's see how the `<a>` tag looks.

```
<a href="wwww.google.com">Go to Google</a>
```

In the start tag, there is some additional information called `href`. Any keywords like `href` are called HTML `attribute`. HTML `attribute` exists to provide additional information for HTML element. HTML `attribute` must be in the start tag, and the structure of HTML `attribute` is declared as `attribute-name = attribute-value`. For the example above, `<a>` element has an attribute called `href`, and the value of `attribute` is `www.google.com`.

There are actually two types of HTML `attribute`. One is a `global` attribute, and the other is a `local` attribute. `global` attribute is an attribute which can be used in any HTML element. `local` attribute is that used in some certain HTML elements.

Now, we might be able to analyze `<img>` tag more easily.

```
<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub-Cat-Logo" />
<img src="./GitHub_Logo.png" alt="GitHub-Alphabet-Logo" />
```

`src` is an attribute which takes the address of the image to be displayed, and `alt` is an attribute to provide short (but `alt`ernative) description of the image. This description will be displayed on the browser when the brower fails to load the corresponding image. In addtion, `alt` is a very important attribute for web accessibility. A screen reader for blind people reads the image information contained in this `alt` attribute.
