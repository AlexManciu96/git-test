# aria-hidden

The `aria-hidden` state indicates whether the element is exposed to an accessibility API.

## [Description](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-hidden#description)

The `aria-hidden` attribute can be used to hide non-interactive content from the accessibility API.

Adding `aria-hidden="true"` to an element removes that element and all of its children from the accessibility tree. This can improve the experience for assistive technology users by hiding:

# ~= pseudoselector

The CSS you are about to write is a common set of properties used to ensure elements are completely hidden visually.

The `span[class~="sr-only"]` selector will select any `span` element whose `class` _includes_ `sr-only`.

# clip

The **`clip`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property defines a visible portion of an element. The `clip` property applies only to absolutely positioned elements — that is, elements with [`position:absolute`](https://developer.mozilla.org/en-US/docs/Web/CSS/position) or [`position:fixed`](https://developer.mozilla.org/en-US/docs/Web/CSS/position).

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/clip

# clip-path

The **`clip-path`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property creates a clipping region that sets what part of an element should be shown. Parts that are inside the region are shown, while those outside are hidden.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path

# white-space

The **`white-space`** CSS property sets how [white space](https://developer.mozilla.org/en-US/docs/Glossary/Whitespace) inside an element is handled.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/white-space

# :first-of-type

The **`:first-of-type`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) represents the first element of its type among a group of sibling elements.

In writing it would look like this : h1 .flex span:first-of-type

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/:first-of-type

# :last-of-type

The **`:last-of-type`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) represents the last element of its type among a group of sibling elements.

In writing it would look like this : h1 .flex span:last-of-type

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/:last-of-type

# calc()

The `calc()` function is a CSS function that allows you to calculate a value based on other values. For example, you can use it to calculate the width of the viewport minus the margin of an element:

```css
.example {
  margin: 10px;
  width: calc(100% - 20px);
}
```

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/calc
 
# How to target all classes within an element

The `span[class]` syntax will target any `span` element that has a `class` attribute set, regardless of the attribute's value.

Exemple: 

.years span[class] {

  bold: 4.5em;

}


# :not()

The **`:not()`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) represents elements that do not match a list of selectors. Since it prevents specific items from being selected, it is known as the _negation pseudo-class_.

The `:not()` pseudo-selector is used to target all elements that do not match the selector, in this case, any of your `span` elements that do not have the `sr-only` 

span:not(.sr-only) {

  font-weight: normal;

}

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/:not


# !important

A `!` delimiter followed by the `important` keyword marks the declaration as important. The `!important` flag alters the rules selecting declarations inside the [cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade). A declaration that is not _important_ is called _normal_.

To mark a declaration important, add the _important flag_ (`!important`) after the value in the declaration. While white space is allowed between the delimiter and the keyword, the flag is generally written as `!important` without any white space.

```
selector {
  property: value; /* normal declaration */
  property: value !important; /* important declaration (preferred) */
  property: value ! important; /* important declaration (not preferred) */
}
```

The `!important` comes after the value of the property value pair declaration, preceded by at least one space. The important flag must be the last token in the declaration. In other words, there can be white space and comments between the flag and the declaration's ending semicolon, but nothing else.

Rather than having to constantly double-check you are not overwriting your earlier properties, you can use the `!important` keyword to ensure these properties are always applied, regardless of order or specificity.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/important

# [attribute="value"] pseudoselector

The `[attribute="value"]` selector targets any element that has an attribute with a specific value

Exemple:
tr[class="total"] {

  border-bottom: 4px double;

  font-weight: bold;

}

The key difference between `tr[class="total"]` and `tr.total` is that the first will select `tr` elements where the _only_ class is `total`. The second will select `tr` elements where the class _includes_ `total`.

# :nth-of-type()

The **`:nth-of-type()`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) matches elements based on their position among siblings of the same type (tag name).

The `:nth-of-type()` pseudo-selector is used to target specific elements based on their order among siblings of the same type

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-of-type

# ::before

In CSS, **`::before`** creates a [pseudo-element](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) that is the first child of the selected element. It is often used to add cosmetic content to an element with the [`content`](https://developer.mozilla.org/en-US/docs/Web/CSS/content) property. It is inline by default.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/::before

# ::after

In CSS, **`::after`** creates a [pseudo-element](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) that is the last child of the selected element. It is often used to add cosmetic content to an element with the [`content`](https://developer.mozilla.org/en-US/docs/Web/CSS/content) property. It is inline by default.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/::after


# ::first-letter

The `::first-letter` pseudo-selector allows you to target the first letter in the text content of an element.
