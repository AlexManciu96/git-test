
# transform-origin

The `transform-origin` property is used to set the point around which a CSS transformation is applied. For example, when performing a `rotate` (which you will do later in this project), the `transform-origin` determines around which point the element is rotated.

Give the `.line` selector a `transform-origin` property of `0% 0%`. This will offset the origin point by `0%` from the left and `0%` from the top, setting it to the top left corner of the element.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/transform-origin



# @keyframe

The `@keyframes` at-rule is used to define the flow of a CSS animation. Within the `@keyframes` rule, you can create selectors for specific points in the animation sequence, such as `0%` or `25%`, or use `from` and `to` to define the start and end of the sequence.

`@keyframes` rules require a name to be assigned to them, which you use in other rules to reference. For example, the `@keyframes freeCodeCamp { }` rule would be named `freeCodeCamp`.

You now need to define how your animation should start. To do this, create a `0%` rule within your `@keyframes wheel` rule. The properties you set in this nested selector will apply at the beginning of your animation.

As an example, this would be a `12%` rule:

```css
@keyframes freecodecamp {
  12% {
    color: green;
  }
}```

# animation-name and animation-duration

The `animation-name` property is used to link a `@keyframes` rule to a CSS selector. The value of this property should match the name of the `@keyframes` rule. Give your `.wheel` selector an `animation-name` property set to `wheel`.

The `animation-duration` property is used to set how long the animation should sequence to complete. The time should be specified in either seconds (`s`) or milliseconds (`ms`).

# animation-iteration-count

The `animation-iteration-count` property sets how many times your animation should repeat. This can be set to a number, or to `infinite` to indefinitely repeat the animation.



# animation-timing-function

The `animation-timing-function` property sets how the animation should progress over time. There are a few different values for this property, but you want the Ferris wheel animation to run at the same rate from start to finish.

# animation

With your `.wheel` selector, you created four different properties to control the animation. For your `.cabin` selector, you can use the `animation` property to set these all at once.

Set the `animation` property of the `.cabin` rule to `cabins 10s linear infinite`. This will set the `animation-name`, `animation-duration`, `animation-timing-function`, and `animation-iteration-count` properties in that order.