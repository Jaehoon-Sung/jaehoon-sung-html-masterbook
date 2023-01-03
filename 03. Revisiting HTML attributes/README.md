# Revisiting HTML attributes

## HTML attributes

We learned what HTML attributes are. We already saw that there are actually two types of HTML `attribute`. One is a `global` attribute, and the other is a `local` attribute. `Global` attribute is an attribute which can be used in any HTML element. `Local` attribute is that used in some certain HTML elements.

## Global attributes

If you want to see the whole list of HTML global attributes, please see this MDN link.  
https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes

### draggable

```
<h1 draggable="true">You can drag this paragraph.</h1>
```  

`draggable` is the attribute which allows you to "drag" the selected element. This can be useful when you want to implement some drag events.

### lang

```
<p lang="ko">이 문장은 한국어로 쓰였습니다.</p>
``` 

`lang="ko"` means that the element is written in Korean. "이 문장은 한국어로 쓰였습니다" is a real sentence which means "This sentence is written in Korean"! :) This `lang` attribute is useful to help define the language of the element and assist search engines to analyze the webpage contents.

### hidden

```
<p hidden>You cannot see this contents!</p>
<p hidden="true">You cannot see this contents, too!</p>
```

If you add `hidden` attribute, the element is not visible on the browser. You can just add `hidden` in a start tag, or gives `true` as a value of `hidden` attribute.

### id

```
<p id="must be unique">This paragraph has an id!</p>
```

`id` is an attribute to specify HTML element you want to visit. Here, `id` must be unique, because you will call this attribute when you want to visit the specfic and unique HTML element having this `id`. Let's see another example where `id` attribute is used below.

```
<label for="userId">user ID</label>
<input type="text" id="userId" />
```

`<label>` is used to define what input the user should enter in its corresponding input. Here, `id` plays a role as corresponding `<label>` to `<input>`. Sometimes, many people implement the `input` element shown as below.

```
user ID <input type="text" id="userId" />
```

On the browser, we cannot see any difference between these two code blocks, seeing the result on the browser. However, there is a huge difference in performance for a screen reader or a search engine optimization. Let's imagine we use a screen reader only without seeing the browser.

When a screen reader encounters `user ID <input type="text" id="userId" />`, it just says like "user ID" and "text input". But, when it encounters the input element linked with a label element (see above), it reads as "user ID" and "text input for user ID". What is the difference? The former does not specify what the text input exists for, while the latter specifies that the text input is for user ID input.

### spellcheck / contenteditable

```
<p spellcheck="true" contenteditable="true">This is another paraggraph. I know that there is a spelling error.</p>
```

`contenteditable` allows the user to edit the contents in the element, and `spellcheck` allows the user to see the red squiggly line for misspelled words.

### style

```
<p style="color: red; background-color: yellow">Can you see me?</p>
```

`style` allows the programmar to design the HTML element. It gives an inline CSS style for an element. Practically, we control the design and styles for HTML elements using `CSS`. This inline CSS styling should be avoided.

### tabindex

```
<a href="" tabindex="1">Google</a>
<a href="" tabindex="3">Youtube</a>
<a href="" tabindex="2">Facebook</a>
```

`tabindex` specifies what element will be focused when the user presses the `tab` key. If you press the `tab`, the tab will visit Google, Facebook, and Youtube. If there is no `tabindex`, it just focuses the inputs from top to bottom. This `tabindex` is also an important attribute for a screen reader.

```
<button title="This button processes the order submission.">Order</button>
```

If you hover the button, you can see the contents in the `title` attribute. This helps the user understand the expected functions of buttons.

## Local attributes

Below are some HTML elements which contain their local attributes.

```
<a href="www.google.com" target="_blank">Go to google!</a>
<img src="../02. Basic HTML tags/GitHub_Logo.png" alt="Github logo" width="50%" height="auto" />
<img src="../02. Basic HTML tags/GitHub_Logo.png" alt="Github logo" width="100px" height="auto" />
```

## Style attributes

`style` attribute is used to style HTML elements. As mentioned above, we are strongly encouraged to control the design and styles of HTML elements using `CSS` external file, not inline CSS styling using `style` attribute.

Please see `04-style-attributes.html` to see some inline CSS style. If you want to learn about inline CSS, internal CSS, and external CSS styles, please see my css-masterbook.

## Do we memorize all of these global and local attributes?

**NO!** We cannot memorize them. This is just to let you know that there are two types of attributes, `global` and `local`, and show some examples for each.
