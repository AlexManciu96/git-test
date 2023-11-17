
# Grids

Basic concepts: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Basic_concepts_of_grid_layout

Exemple: https://developer.mozilla.org/en-US/docs/Glossary/Grid


CSS Grid offers a two-dimensional grid-based layout, allowing you to center items horizontally and vertically while still retaining control to do things like overlap elements.

Begin by creating a `main` selector and giving it a `display` property set to `grid`.

CSS Grid is similar to Flexbox in that it has a special property for both the parent and child elements.
Set the content to have a three-column layout by adding a `grid-template-columns` property with a value of `1fr 94rem 1fr`. This will create three columns where the middle column is `94rem` wide, and the first and last columns are both 1 fraction of the remaining space in the grid container.

Exemple: 
```
main {

  display: grid;

  grid-template-columns: 1fr 94rem 1fr;

} 
```


Your magazine will have three primary sections. You already set the overall layout in the `main` rule, but you can adjust the placement in the child rules.

One option is the `grid-column` property, which is shorthand for `grid-column-start` and `grid-column-end`. The `grid-column` property tells the grid item which grid line to start and end at.

Create a `.heading` rule and set the `grid-column` property to `2 / 3`. This will tell the `.heading` element to start at grid line 2 and end at grid line 3.

For additional control over the layout of your content, you can have a CSS Grid within a CSS Grid.

The CSS `repeat()` function is used to repeat a value, rather than writing it out manually, and is helpful for grid layouts. For example, setting the `grid-template-columns` property to `repeat(20, 200px)` would create 20 columns each `200px` wide.

Remember that the `grid-column` property determines which columns an element starts and ends at. There may be times where you are unsure of how many columns your grid will have, but you want an element to stop at the last column. To do this, you can use `-1` for the end column.
Create a `.hero` selector and give it a `grid-column` property set to `1 / -1`. This will tell the element to span the full width of the grid

The default settings for CSS Grid will create additional rows as needed, unlike Flexbox. Give the `.social-icons` selector a `grid-template-columns` property set to `repeat(5, 1fr)` to arrange the icons in a single row.

# grid-template-columns

The **`grid-template-columns`** CSS property defines the line names and track sizing functions of the [grid columns](https://developer.mozilla.org/en-US/docs/Glossary/Grid_Column).

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns

# grid-template-rows

The **`grid-template-rows`** CSS property defines the line names and track sizing functions of the [grid rows](https://developer.mozilla.org/en-US/docs/Glossary/Grid_Row).

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-rows

# minmax()

The **`minmax()`** [CSS function](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions) defines a size range greater than or equal to _min_ and less than or equal to _max_. It is used with [CSS Grids](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout).

Use the `minmax` function to make your columns responsive on any device. The `minmax` function takes two arguments, the first being the minimum value and the second being the maximum. These values could be a length, percentage, `fr`, or even a keyword like `max-content`.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/minmax

# row-gap

The **`row-gap`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property sets the size of the gap ([gutter](https://developer.mozilla.org/en-US/docs/Glossary/Gutters)) between an element's rows.

Early versions of the specification called this property `grid-row-gap`, and to maintain compatibility with legacy websites, browsers will still accept `grid-row-gap` as an alias for `row-gap`.

To add space between rows in the grid layout, you can use the `row-gap` property

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/row-gap

# grid-column

The **`grid-column`** CSS [shorthand property](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties) specifies a grid item's size and location within a [grid column](https://developer.mozilla.org/en-US/docs/Glossary/Grid_Column) by contributing a line, a span, or nothing (automatic) to its grid placement, thereby specifying the inline-start and inline-end edge of its [grid area](https://developer.mozilla.org/en-US/docs/Glossary/Grid_Areas).

This property is a shorthand for the following CSS properties:

- [`grid-column-end`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-column-end)
-  [`grid-column-start`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-column-start)

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-column

# repeat()

The **`repeat()`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) [function](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions) represents a repeated fragment of the [track list](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Basic_concepts_of_grid_layout), allowing a large number of columns or rows that exhibit a recurring pattern to be written in a more compact form.

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/repeat

# grid-auto-flow

The **`grid-auto-flow`** CSS property controls how the auto-placement algorithm works, specifying exactly how auto-placed items get flowed into the grid.

Ca sa intelegi: Daca tu setezi grid-ul sa fie o anumita marime pe rows and columns si grid-ul este plin, daca adaugi un element nou, grid-ul automat se va extinde ca sa faca loc noului element. Cu definitia asta, poti sa pui ca exemplu ``grid-auto-flow: column`` si asa noul element introdus o sa fie pus strict pe coloana.

Apoi tot ce trebuie sa faci e sa `grid-auto-columns: value` ca sa definesti cat de mare sa fie elementul respectiv in grid


Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-flow


# grid-area

Grid-area este folosit ca sa definesti cu totul un element in CSS Grid. In loc sa pui grid-row/grid-column, poti sa folosesti grid-area ca sa definesti complet cat ocupa un element in Grid:

grid-area:  row-start / col-start / row-end / col-end;

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/grid-area


# the fr measurment unit

Fr este in principal folosit in CSS Grid ca sa determini cat din valoarea spatiului ramas ocupa acel element. Ca exemplu daca pui `grid-template-column: 1fr 1fr 1fr` iti va crea un grid cu 3 coloane care ocupa toate 3 aceiasi dimensiune, adica fiecare va ocupa o FRACTIE din spatiul ramas.


# grid-gap 

Adauga gap-uri intre coloane si row-urile din grid. Prima valoarea este pentru rows si a doua pentru coloane. In cazul de mai jos ar fii 2rem pentru rows si 4rem pentru coloane.

grid-gap: 2rem 4rem;


# grid-area-templates


Dupa ce ai definit cate row-uri si coloane are Grid-ul tau folosind functia `grid-template`, poti sa stabiliesti exact pozitia fiecarui element inca de la inceput folosind `grid-area-templates`. Uite un exemplu ca sa intelegi cum functioneaza: 

![[grid-template-areas.png]]

In exemplul asta, avem un Grid cu 3 row-uri si 2 coloane. Am creat un grid-template-area in care definim ce elemente exista in fiecare celula. Fiecare linie reprezinta row-urile si fiecare cuvant reprezinta 1 coloana. Deci in cazul lui 'header header' ar fii primul row, si din cauza ca am scris acelasi cuvant, elementul header va ocupa ambele coloane.

Apoi poti sa pui functia `grid-area` in fiecare element si definesti unde se aseaza fiecare element in parte. In exemplu de mai sus, .item-1 este definit ca fiind header, deci va ocupa pozitia header-ului.


# align-items and justify-items 

`align-items` will align child elements along the column axis, and `justify-items` will align child elements along the row axis.

# place-items

The `place-items` property can be used to set the `align-items` and `justify-items` values at the same time. The `place-items` property takes one or two values. If one value is provided, it is used for both the `align-items` and `justify-items` properties. If two values are provided, the first value is used for the `align-items` property and the second value is used for the `justify-items` property.

# gap 

The `gap` property is a shorthand way to set the value of `column-gap` and `row-gap` at the same time. If given one value, it sets the `column-gap` and `row-gap` both to that value. If given two values, it sets the `row-gap` to the first value and the `column-gap` to the second.