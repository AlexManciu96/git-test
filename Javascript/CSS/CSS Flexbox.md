

# box-sizing



By default in the [CSS box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_box_model/Introduction_to_the_CSS_box_model), the `width` and `height` you assign to an element is applied only to the element's content box. If the element has any border or padding, this is then added to the `width` and `height` to arrive at the size of the box that's rendered on the screen. This means that when you set `width` and `height`, you have to adjust the value you give to allow for any border or padding that may be added. For example, if you have four boxes with `width: 25%;`, if any has left or right padding or a left or right border, they will not by default fit on one line within the constraints of the parent container.

The `box-sizing` property can be used to adjust this behavior:

- `content-box` gives you the default CSS box-sizing behavior. If you set an element's width to 100 pixels, then the element's content box will be 100 pixels wide, and the width of any border or padding will be added to the final rendered width, making the element wider than 100px.
- `border-box` tells the browser to account for any border and padding in the values you specify for an element's width and height. If you set an element's width to 100 pixels, that 100 pixels will include any border or padding you added, and the content box will shrink to absorb that extra width. This typically makes it much easier to size elements. `box-sizing: border-box` is the default styling that browsers use for the [`<table>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table), [`<select>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select), and [`<button>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button) elements, and for [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) elements whose type is `[radio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/radio)`, `[checkbox](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox)`, `[reset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/reset)`, `[button](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/button)`, `[submit](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/submit)`, `[color](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/color)`, or `[search](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/search)`.

Din ce inteleg eu, box-sizing este folosit ca sa incadrezi elementele in alte elemente. box-sizing tine cont de elemente parinte existent si incadreaza elementul copil in el.

# text-transform

The **`text-transform`** CSS property specifies how to capitalize an element's text. It can be used to make text appear in all-uppercase or all-lowercase, or with each word capitalized. It also can help improve legibility for ruby.



## Flexbox

Flexbox is a one-dimensional CSS layout that can control the way items are spaced out and aligned within a container.

To use it, give an element a `display` property of `flex`. This will make the element a _flex container_. Any direct children of a flex container are called _flex items_.

Flexbox has a main and cross axis. The main axis is defined by the `flex-direction` property, which has four possible values:

- `row` (default): horizontal axis with flex items from left to right
- `row-reverse`: horizontal axis with flex items from right to left
- `column`: vertical axis with flex items from top to bottom
- `column-reverse`: vertical axis with flex items from bottom to top

**Note**: The axes and directions will be different depending on the text direction. The values shown are for a left-to-right text direction.

The `flex-wrap` property determines how your flex items behave when the flex container is too small. Setting it to `wrap` will allow the items to wrap to the next row or column. `nowrap` (default) will prevent your items from wrapping and shrink them if needed.
The **`flex-wrap`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property sets whether flex items are forced onto one line or can wrap onto multiple lines. If wrapping is allowed, it sets the direction that lines are stacked.
Ex: https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap


# justify-content

The `justify-content` property determines how the items inside a flex container are positioned along the main axis, affecting their position and the space around them.

The [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) **`justify-content`** property defines how the browser distributes space between and around content items along the [main-axis](https://developer.mozilla.org/en-US/docs/Glossary/Main_Axis) of a flex container, and the inline axis of a grid container.

The interactive example below demonstrates some of the values using Grid Layout.
The `justify-content` property determines how the items inside a flex container are positioned along the main axis, affecting their position and the space around them.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content

# align-items

The `align-items` property positions the flex content along the cross axis. In this case, with your `flex-direction` set to `row`, your cross axis would be vertical.

The [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) **`align-items`** property sets the [`align-self`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self) value on all direct children as a group. In Flexbox, it controls the alignment of items on the [Cross Axis](https://developer.mozilla.org/en-US/docs/Glossary/Cross_Axis). In Grid Layout, it controls the alignment of items on the Block Axis within their [grid area](https://developer.mozilla.org/en-US/docs/Glossary/Grid_Areas).

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/align-items

# Cross Axis

The cross axis in [flexbox](https://developer.mozilla.org/en-US/docs/Glossary/Flexbox) runs perpendicular to the [main axis](https://developer.mozilla.org/en-US/docs/Glossary/Main_Axis), therefore if your [`flex-direction`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction) is either `row` or `row-reverse` then the cross axis runs down the columns.

![The cross axis runs down the column](https://developer.mozilla.org/en-US/docs/Glossary/Cross_Axis/basics3.png)

If your main axis is `column` or `column-reverse` then the cross axis runs along the rows.

![The cross axis runs along the row.](https://developer.mozilla.org/en-US/docs/Glossary/Cross_Axis/basics4.png)

Alignment of items on the cross axis is achieved with the `align-items` property on the flex container or `align-self` property on individual items. In the case of a multi-line flex container, with additional space on the cross axis, you can use `align-content` to control the spacing of the rows.

# object-fit

Notice how some of your images have become distorted. This is because the images have different aspect ratios. Rather than setting each aspect ratio individually, you can use the `object-fit` property to determine how images should behave.

he **`object-fit`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property sets how the content of a [replaced element](https://developer.mozilla.org/en-US/docs/Web/CSS/Replaced_element), such as an [`<img>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) or [`<video>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video), should be resized to fit its container.

You can alter the alignment of the replaced element's content object within the element's box using the [`object-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position) property.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit

## GAP

The `gap` CSS shorthand property sets the gaps, also known as gutters, between rows and columns. The `gap` property and its `row-gap` and `column-gap` sub-properties provide this functionality for flex, grid, and multi-column layout. You apply the property to the container element.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/gap

## ::after

The `::after` pseudo-element creates an element that is the last child of the selected element. You can use it to add an empty element after the last image. If you give it the same `width` as the images it will push the last image to the left when the gallery is in a two-column layout. Right now, it is in the center because you set `justify-content: center` on the flex container.

Example:

```css
.container::after {
  content: "";
  width: 860px;
}
```

## content

The **`content`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property replaces content with a generated value. It can be used to define what is rendered inside an element or pseudo-element. For elements, the `content` property specifies whether the element renders normally (`normal` or `none`) or is replaced with an image (and associated "alt" text). For pseudo-elements and margin boxes, `content` defines the content as images, text, both, or none, which determines whether the element renders at all.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/content



# flex-direction

The **`flex-direction`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property sets how flex items are placed in the flex container defining the main axis and the direction (normal or reversed).

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction