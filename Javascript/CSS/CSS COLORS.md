CSS COLORS:

RGB Colors:
There are two main color models: the additive RGB (red, green, blue) model used in electronic devices, and the subtractive CMYK (cyan, magenta, yellow, black) model used in print.
In this project, you'll work with the RGB model. This means that colors begin as black, and change as different levels of red, green, and blue are introduced. An easy way to see this is with the CSS `rgb` function.

A function is a piece of code that can take an input and perform a specific action. The CSS `rgb` function accepts values, or arguments, for red, green, and blue, and produces a color:

```css
rgb(red, green, blue);
```

Each red, green, and blue value is a number from `0` to `255`. `0` means that there's 0% of that color, and is black. `255` means that there's 100% of that color.


In the additive RGB color model, primary colors are colors that, when combined, create pure white. But for this to happen, each color needs to be at its highest intensity( that means at 255)


Secondary colors are the colors you get when you combine primary colors. You might have noticed some secondary colors in the last step as you changed the red, green, and blue values.
Secondary colors are the CMYK


Tertiary colors are created by combining a primary with a nearby secondary color. The combination of primary and secondary colors is known as tertiary or intermediate colors, due to their compound nature. Blue-green, blue-violet, red-orange, red-violet, yellow-orange, and yellow-green are color combinations you can make from color mixing. On a color wheel, tertiary colors are between primary and secondary colors.


A color wheel is a circle where similar colors, or hues, are near each other, and different ones are further apart. For example, pure red is between the hues rose and orange.
Two colors that are opposite from each other on the color wheel are called complementary colors. If two complementary colors are combined, they produce gray. But when they are placed side-by-side, these colors produce strong visual contrast and appear brighter.
![[colourwheel01.gif]]
It's better practice to choose one color as the dominant color, and use its complementary color as an accent to bring attention to certain content on the page.


Notice how your eyes are naturally drawn to the red color in the center? When designing a site, you can use this effect to draw attention to important headings, buttons, or links.


A very common way to apply color to an element with CSS is with hexadecimal or hex values. While hex values sound complicated, they're really just another form of RGB values.
Hex color values start with a `#` character and take six characters from 0-9 and A-F. The first pair of characters represent red, the second pair represent green, and the third pair represent blue. For example, `#4B5320`. (Deci 4B reprezinta red, 53 reprezinta green, 20 reprezinta blue)
You may already be familiar with decimal, or base 10 values, which go from 0 - 9. Hexadecimal, or base 16 values, go from 0 - 9, then A - F:

```js
0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
```

With hex colors, `00` is 0% of that color, and `FF` is 100%. So `#00FF00` translates to 0% red, 100% green, and 0% blue, and is the same as `rgb(0, 255, 0)`.


The HSL color model, or hue, saturation, and lightness, is another way to represent colors.
The CSS hsl function accepts 3 values: a number from 0 to 360 for hue, a percentage from 0 to 100 for saturation, and a percentage from 0 to 100 for lightness.
If you imagine a color wheel, the hue red is at 0 degrees, green is at 120 degrees, and blue is at 240 degrees.
Saturation is the intensity of a color from 0%, or gray, to 100% for pure color. You must add the percent sign `%` to the saturation and lightness values.
Lightness is how bright a color appears, from 0%, or complete black, to 100%, complete white, with 50% being neutral.
Exemple: background-color: hsl(240, 100%, 50%)=asa faci albastru


You've learned a few ways to set flat colors in CSS, but you can also use a color transition, or gradient, on an element.
A gradient is when one color transitions into another. The CSS `linear-gradient` function lets you control the direction of the transition along a line, and which colors are used.
One thing to remember is that the `linear-gradient` function actually creates an `image` element, and is usually paired with the `background` property which can accept an image as a value.
The `linear-gradient` function is very flexible -- here is the basic syntax you'll use in this tutorial:

```css
linear-gradient(gradientDirection, color1, color2, ...);
```

`gradientDirection` is the direction of the line used for the transition. `color1` and `color2` are color arguments, which are the colors that will be used in the transition itself. These can be any type of color, including color keywords, hex, `rgb`, or `hsl`.
gradientDirection e folosit ca sa vezi la cate grade o sa fie linia de culoare. Exemplu: 90deg o sa le puna in linie dreapta


Color-stops allow you to fine-tune where colors are placed along the gradient line. They are a length unit like `px` or percentages that follow a color in the `linear-gradient` function.
For example, in this red-black gradient, the transition from red to black takes place at the 90% point along the gradient line, so red takes up most of the available space:

```css
linear-gradient(90deg, red 90%, black);
```
The first color is at the start (0%), the second is in the middle (50%), and the last is at the end (100%) of the gradient line.
If no `gradientDirection` argument is provided to the `linear-gradient` function, it arranges colors from top to bottom, or along a 180 degree line, by default.

Gradient transitions often gradually change from one color to another. You can make the change a solid line like this:

```css
linear-gradient(
  var(--first-color) 0%,
  var(--first-color) 40%,
  var(--second-color) 40%,
  var(--second-color) 80%
);
```




Opacity describes how opaque, or non-transparent, something is. For example, a solid wall is opaque, and no light can pass through. But a drinking glass is much more transparent, and you can see through the glass to the other side.
With the CSS `opacity` property, you can control how opaque or transparent an element is. With the value `0`, or 0%, the element will be completely transparent, and at `1.0`, or 100%, the element will be completely opaque like it is by default.
Another way to set the opacity for an element is with the alpha channel. Similar to the `opacity` property, the alpha channel controls how transparent or opaque a color is.
You're already familiar with using the `rgb` function to set colors. To add an alpha channel to an `rgb` color, use the `rgba` function instead.

The `rgba` function works just like the `rgb` function, but takes one more number from `0` to `1.0` for the alpha channel:

```css
rgba(redValue, greenValue, blueValue, alphaValue);
```

You can also use an alpha channel with `hsl` and `hex` colors:
Pentru culori hex adaugi inca 2 caractere cc. Exemplu: #3B7E20CC
Pentru hsl schimbi in hsla si adaugi inca o variabila la final. Exemplu: hsla(223, 59%, 31%, 0.8)

# repeating-linear-gradient()

The **`repeating-linear-gradient()`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [function](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions) creates an image consisting of repeating linear gradients. It is similar to [`linear-gradient()`](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/linear-gradient) and takes the same arguments, but it repeats the color stops infinitely in all directions so as to cover its entire container. The function's result is an object of the [`<gradient>`](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient) data type, which is a special kind of [`<image>`](https://developer.mozilla.org/en-US/docs/Web/CSS/image).

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/repeating-linear-gradient

You can add multiple gradients to an element by separating them with a comma (`,`) like this:

```css
gradient1(
  colors
),
gradient2(
  colors
);
```


# radial-gradient()

The **`radial-gradient()`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [function](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions) creates an image consisting of a progressive transition between two or more colors that radiate from an origin. Its shape may be a circle or an ellipse. The function's result is an object of the [`<gradient>`](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient) data type, which is a special kind of [`<image>`](https://developer.mozilla.org/en-US/docs/Web/CSS/image).

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/radial-gradient