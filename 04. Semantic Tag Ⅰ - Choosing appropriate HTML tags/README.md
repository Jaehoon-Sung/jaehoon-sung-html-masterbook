# Choosing appropriate HTML tags

## Why should we learn how to choose appropriate HTML tags to make webpage "meaningful"?

Let's see the example below.

```
<p style="font-weight: bold">This paragraph is bold.</p>
<p><b>This paragraph is also bold. Can you find any difference?</b></p>
<p><strong>This last paragraph is also bold. Can you find any difference?</strong></p>
```

If you see three elements above on the browser, you cannot find any visual difference. Then, why does HTML give us many ways to boldify the text? Even though these three elements show us visually identical contents, `<strong>` tag **semantically** emphasizes on the contents in a `<strong>` element. Using **semantic** tags allows a search engine and a screen-reader to detect what texts are emphasized. A screen-reader reads the contents in `<strong>` element "strongly". We should know that implementing visually perfect HTML files would not guarantee a full web accessibility for an assistive device or a full search engine optimization.

Let's see another example.

```
<p style="font-style: italic">Now the text is italicized.</p>
<p><i>Now the text is italicized.</i></p>
<p><em>This text is also italicized.</em></p>
```

The elements shown above show italicized texts. Here, a screen-reader can detect that the text is italicized (technically, emphasized), only when the text is included in `<em>` tags. `<em>` is an abbreviation for "emphasis".

Many examples for semantic tags are shown in `05-semantic-tags-1.html`. We will revisit semantic tags again!

## Block Element VS Inline Element

`06-div-span.html` demonstrates basic examples of a block element and an inline element!
