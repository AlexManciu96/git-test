
Variable declarations begin with two dashes (`-`) and are given a name and a value like this: `--variable-name: value;`. In the rule for the `bb1` class, create a variable named `--building-color1` and give it a value of `#999`.

To use a variable, put the variable name in parentheses with `var` in front of them like this: `var(--variable-name)`. Whatever value you gave the variable will be applied to whatever property you use it on.


**Custom properties** (sometimes referred to as **CSS variables** or **cascading variables**) are entities defined by CSS authors that contain specific values to be reused throughout a document. They are set using custom property notation (e.g., **`--main-color: black;`**) and are accessed using the [`var()`](https://developer.mozilla.org/en-US/docs/Web/CSS/var) function (e.g., `color: var(--main-color);`).

Complex websites have very large amounts of CSS, often with a lot of repeated values. For example, the same color might be used in hundreds of different places, requiring global search and replace if that color needs to change. Custom properties allow a value to be stored in one place, then referenced in multiple other places. An additional benefit is semantic identifiers. For example, `--main-text-color` is easier to understand than `#00ff00`, especially if this same color is also used in other contexts.


## [Using the :root pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties#using_the_root_pseudo-class)

Notice the repetitive CSS in the example above. The background color is set to `brown` in several places. For some CSS declarations, it is possible to declare this higher in the cascade and let CSS inheritance solve this problem naturally. For non-trivial projects, this is not always possible. By declaring a custom property on the [`:root`](https://developer.mozilla.org/en-US/docs/Web/CSS/:root) pseudo-class and using it where needed throughout the document, a CSS author can reduce the need for repetition:

CSSCopy to Clipboard

```
:root {
  --main-bg-color: brown;
}

.one {
  color: white;
  background-color: var(--main-bg-color);
  margin: 10px;
  width: 50px;
  height: 50px;
  display: inline-block;
}

.two {
  color: white;
  background-color: black;
  margin: 10px;
  width: 150px;
  height: 70px;
  display: inline-block;
}
.three {
  color: white;
  background-color: var(--main-bg-color);
  margin: 10px;
  width: 75px;
}
.four {
  color: white;
  background-color: var(--main-bg-color);
  margin: 10px;
  width: 100px;
}

.five {
  background-color: var(--main-bg-color);
}
```

You should add a fallback value to a variable by putting it as the second value of where you use the variable like this: `var(--variable-name, fallback-value)`. The property will use the fallback value when there's a problem with the variable. Add a fallback value of `green` to the `background-color` of `.bb2`.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties