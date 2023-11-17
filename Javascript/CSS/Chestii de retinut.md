
For the styling of the page to look similar on mobile as it does on a desktop or laptop, you need to add a `meta` element with a special `content` attribute.

Add the following within the `head` element:

<meta name="viewport" content="width=device-width, initial-scale=1.0" />

Ca sa ai relatia facuta intre html si CSS se foloseste: 
<link href="styles.css" rel="stylesheet"/>

In CSS, inauntru selectorilor vom pune property. Exemplu de property:
width: 0px;
height: 0px;
Exemplu full:
p {
	height: 0px;
	width: 0px;
}

Property pot avea functions. Exemplu:
h1 {
	background: linear-gradient(rgb (0, 0, 0));
}
In acest exemplu, linear-gradient este un function


The `border-left` shorthand property lets you to set the left border's width, style, and color at the same time.

Here is the syntax:

```css
border-left: width style color;
```



The `box-shadow` property lets you apply one or more shadows around an element. Here is basic syntax:

```css
box-shadow: offsetX offsetY color;
```

Here's how the `offsetX` and `offsetY` values work:

- both `offsetX` and `offsetY` accept number values in `px` and other CSS units
- a positive `offsetX` value moves the shadow right and a negative value moves it left
- a positive `offsetY` value moves the shadow down and a negative value moves it up
- if you want a value of zero (`0`) for any or both `offsetX` and `offsetY`, you don't need to add a unit. Every browser understands that zero means no change.

The height and width of the shadow is determined by the height and width of the element it's applied to. You can also use an optional `spreadRadius` value to spread out the reach of the shadow. More on that later.
But what if you wanted to position your shadow on the opposite side? You can do that by using negative values for `offsetX` and `offsetY`
Notice that the edges of the shadow are sharp. This is because there is an optional `blurRadius` value for the `box-shadow` property:

```css
box-shadow: offsetX offsetY blurRadius color;
```

If a `blurRadius` value isn't included, it defaults to `0` and produces sharp edges. The higher the value of `blurRadius`, the greater the blurring effect is.
But what if you wanted to expand the shadow out further? You can do that with the optional `spreadRadius` value:

```css
box-shadow: offsetX offsetY blurRadius spreadRadius color;
```


The `vh` unit stands for viewport height, and is relative to 1% of the `height` of the viewport.
## What is The Viewport?

The viewport is the user's visible area of a web page.
The viewport varies with the device, and will be smaller on a mobile phone than on a computer screen.
Before tablets and mobile phones, web pages were designed only for computer screens, and it was common for web pages to have a static design and a fixed size.
Then, when we started surfing the internet using tablets and mobile phones, fixed size web pages were too large to fit the viewport. To fix this, browsers on those devices scaled down the entire web page to fit the screen.
This was not perfect!! But a quick fix.

Now, make the background easy on the eyes, by changing the `body` `background-color` to `#1b1b32`. Then, to see the text, change the `color` to `#f5f6f7`.

## What is the rem unit?

`rem` stands for **root em**, which is a measurement unit that refers to the `font-size` of the `root` element of a document.

It is a relative unit, which means all values that use it change when the root's `font-size` changes. The `root` element in this case refers to the `html` element.



The border of the last `fieldset` element looks a little out of place. You can select the last element of a specific type using the `last-of-type` CSS pseudo-class, like this:

```css
p:last-of-type { }
```

The rule `unset`. This will remove the earlier rule which set all the `input` elements to `width: 100%`.


To style the submit button, you can use an _attribute_ selector, which selects an element based on the given attribute value. Here is an example:

```css
input[name="password"]
```

CA SA CENTREZI IN PAGINA POTI FOLOSI: 
margin: 0 auto;

Ca sa centrezi 2 elemente sa fie pe aceiasi linie, poti sa le dai o clasa si sa foloseste vertical-aligment: center;

# Unde sa pui box-sizing-ul

Daca vrem sa punem `box-sizing`: boder-box pentru toate elementele de pe pagina, ar trebui pus in selectorul HTML, nu il selectorul universal *

# Cum sa scoti elemente din pagina cu CSS

Finally, you need to take these hidden elements out of the document flow. Give the `span[class~="sr-only"]` selector a `position` property set to `absolute`, a `padding` property set to `0`, and a `margin` property set to `-1px`. This will ensure that not only are they no longer visible, but they are not even within the page view.

# Pentru responsive web design in elementul principal, parintele tuturor

`max-width` property set to `40rem` for responsive design

# How to fix width of elements in a container

Give them a width to fill the viewport, with a minimum and maximum of `4rem`. This approach ensures that the width is fixed, whereas setting `width` specifically would allow the elements to shrink to the container.

Exemple: 
tbody td {

  width: 100vw;

  min-width: 4rem;

  max-width: 4rem;

}


# Buna practica ca sa fixez body la inceput

body {

  height: 100vh;

  margin: 0;

  overflow: hidden;

}

# Ce ar trebui sa faci la inceput de tot in CSS

```
*, ::before, ::after{

  padding: 0;

  margin: 0;

  box-sizing: border-box;

}

```
Codul asta te ajuta sa incepi toate elementele de la marginea posibila paginii.

Create an `html` selector and give it a `font-size` property set to `62.5%`. This will set the default font size for your web page to 10px (the browser default is 16px).

This will make it easier for you to work with `rem` units later, as `2rem` would be 20px.