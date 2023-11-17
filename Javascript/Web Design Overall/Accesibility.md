
# NAV The Navigation Section element 

The **`<nav>`** [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) element represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.

Exemple: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav


A useful property of an _SVG_ (scalable vector graphics) is that it contains a `path` attribute which allows the image to be scaled without affecting the resolution of the resultant image.
Currently, the `img` is assuming its default size, which is too large. CSS has a `max` function which returns the largest of a set of comma-separated values. For example:

```css
img {
  width: max(250px, 25vw);
}
```


# What is Scalable Vector Graphics(SVG)

https://www.youtube.com/watch?v=hA7ESX7FsE4

**Scalable Vector Graphics (SVG)** is an [XML](https://developer.mozilla.org/en-US/docs/Web/XML)-based markup language for describing two-dimensional based [vector graphics](https://en.wikipedia.org/wiki/Vector_graphics).

As such, it's a text-based, open Web standard for describing images that can be rendered cleanly at any size and are designed specifically to work well with other web standards including [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS), [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model), [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript), and [SMIL](https://developer.mozilla.org/en-US/docs/Web/SVG/SVG_animation_with_SMIL). SVG is, essentially, to graphics what [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) is to text.

SVG images and their related behaviors are defined in [XML](https://developer.mozilla.org/en-US/docs/Web/XML) text files, which means they can be searched, indexed, scripted, and compressed. Additionally, this means they can be created and edited with any text editor or with drawing software.

Compared to classic bitmapped image formats such as [JPEG](https://developer.mozilla.org/en-US/docs/Glossary/JPEG) or [PNG](https://developer.mozilla.org/en-US/docs/Glossary/PNG), SVG-format vector images can be rendered at any size without loss of quality and can be easily localized by updating the text within them, without the need of a graphical editor to do so. With proper libraries, SVG files can even be localized on-the-fly.

# aspect-ratio

The **`aspect-ratio`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property allows you to define the desired width-to-height ratio of an element's box. This means that even if the parent container or viewport size changes, the browser will adjust the element's dimensions to maintain the specified width-to-height ratio. The specified aspect ratio is used in the calculation of auto sizes and some other layout functions.

At least one of the box's sizes needs to be automatic in order for `aspect-ratio` to have any effect. If neither the width nor height is an automatic size, then the provided aspect ratio has no effect on the box's preferred sizes.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/aspect-ratio


# > selector

#Child combinator

The **child combinator** (`>`) is placed between two CSS selectors. It matches only those elements matched by the second selector that are the direct children of elements matched by the first.

In the exemple below, you would target the unordered list in a nav element. 
nav > ul {

  display: flex;

  justify-content: space-evenly;

}

# Role 

The `role` attribute describes the role of an element in programs that can make use of it, such as screen readers or magnifiers.

Usage Example:

```html
<a href="#" role="button">Button Link</a>
```

Screen Readers will read this element as “button” instead of “link”.

There are four categories of roles:

- Abstract Roles
- Widget Roles
- Document Structure Roles
- Landmark Roles


# aria-labelledby

The `aria-labelledby` attribute identifies the element (or elements) that labels the element it is applied to.

## [Description](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby#description)

The `aria-labelledby` property enables authors to reference other elements on the page to define an accessible name. This is useful when using elements that don't have native support for associating elements to provide an accessible name.

Some elements get their [accessible name](https://w3c.github.io/accname/#dfn-accessible-name) from their inner content. For example, the accessible name for a [`<button>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button), [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a), or [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td) comes from the text between the opening and closing tags. Other elements, such as form [`<textarea>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea), [`<fieldset>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset), and [`<table>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table) get their accessible name from the content of associated elements; for these elements, the accessible name comes from the [`<label>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) with a `for` attribute, [`<legend>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/legend), and [`<caption>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption) respectively.

All interactive elements must have an accessible name. `aria-labelledby` can be used to reference another element to define its accessible name, when an element's accessible name needs to use content from elsewhere in the DOM.

Video explanation: https://www.youtube.com/watch?v=dnhnSoMEv6Q

# To navigate within the page

Give your anchor href the same id as the place you want the link to navigate to
Ex:

         <li><a href="#student-info">INFO</a></li>

          <li><a href="#html-questions">HTML</a></li>

          <li><a href="#css-questions">CSS</a></li>>


# sr-only class

You can add that caption to the table in the HTML and apply the sr-only class to ensure the text is available to screen readers but not visible.

A link with the `sr-only` class applied will stay hidden to sighted users at all times, evem when it receives keyboard focus. This can cause confusion when sighted users navigate a page with keyboard controls. **For this reason, `sr-only` is generally not appropriate when working with interactive elements like links, buttons, etc.** Use Visually Hidden (below) instead.

The `.sr-only` text is still visible. There is a common pattern to visually hide text for only screen readers to read.

This pattern is to set the following CSS properties:

```css
position: absolute;
width: 1px;
height: 1px;
padding: 0;
margin: -1px;
overflow: hidden;
clip: rect(0, 0, 0, 0);
white-space: nowrap;
border: 0;
```

Use the above to define the `sr-only` class.

# ::before

In CSS, **`::before`** creates a [pseudo-element](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) that is the first child of the selected element. It is often used to add cosmetic content to an element with the [`content`](https://developer.mozilla.org/en-US/docs/Web/CSS/content) property. It is inline by default.

# address: The Contact Address element

The **`<address>`** [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) element indicates that the enclosed HTML provides contact information for a person or people, or for an organization.

# br The Line Break element

The **`<br>`** [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) element produces a line break in text (carriage-return). It is useful for writing a poem or an address, where the division of lines is significant.

Exemple: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br

# text-align

The **`text-align`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property sets the horizontal alignment of the inline-level content inside a block element or table-cell box. This means it works like [`vertical-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align) but in the horizontal direction.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/text-align

# vertical-align

The **`vertical-align`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property sets vertical alignment of an inline, inline-block or table-cell box.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/vertical-align

# How to remove borders in a fieldset element

It is useful to see the default border around the `fieldset` elements, during development. However, it might not be the style you want.

Remove the border and bottom padding on the `.question` elements.

# list-style 

While `ul`/`li` elements are great at providing bullets for list items, your radio buttons don't need them. You can control what the bullets look with the `list-style` property. For example you can turn your bullets into circles with the following:

```css
ul {
  list-style: circle;
}
```

Remove the default styling for the `.answers-list` items by setting its style to `none`, and remove the unordered list padding.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/list-style


# scroll-behavior

The **`scroll-behavior`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property sets the behavior for a scrolling box when scrolling is triggered by the navigation or CSSOM scrolling APIs.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/scroll-behavior

# Media rule prefers-reduced-motion

Certain types of motion-based animations can cause discomfort for some users. In particular, people with vestibular disorders have sensitivity to certain motion triggers.

The `@media` at-rule has a media feature called `prefers-reduced-motion` to set CSS based on the user's preferences. It can take one of the following values:

- `reduce`
- `no-preference`


# accesskey

The **`accesskey`** [global attribute](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes) provides a hint for generating a keyboard shortcut for the current element. The attribute value must consist of a single printable character (which includes accented and other characters that can be generated by the keyboard).

Exemple: https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/accesskey