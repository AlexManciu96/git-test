

# Inherit keyword

Inherits this property from its parent element. The `inherit` keyword specifies that a property should inherit its value from its parent element.

The `inherit` keyword can be used for any CSS property, and on any HTML element

Exemple: 

span {  
color: blue; 
}  
  
.extra span {  
color: inherit;
}

# @Media rule 

```
@media (feature: value) {
  selector {
    styles
  }
} 
``` 

`@media` in CSS is an **at-rule** that allows you to apply CSS rules only when certain conditions are met, such as specific screen sizes or devices. It is commonly used for making responsive designs, where the layout and styles of a web page change based on the characteristics of the user's device, such as width, height, orientation, or resolution. The basic syntax of the `@media` rule looks like this:

`@media media-type and (media-feature) {     /* CSS rules to be applied when the media query condition is met */ }`

- **`media-type`** specifies the type of media the media query applies to. Common values include `all` (applies to all media types), `print` (applies to printers), `screen` (applies to computer screens, tablets, and smartphones), and `speech` (applies to screen readers).

- **`media-feature`** defines the specific conditions for the media query. For example, you can use `max-width`, `min-width`, `orientation`, and others to specify the screen width, height, or device orientation.

Here's an example of a media query that changes the background color of the body element to yellow when the screen width is 600 pixels or less:

`@media screen and (max-width: 600px) {     body {         background-color: yellow;     } }`

In this example, the CSS rules inside the media query block will only apply if the **media type is screen** and the **screen width is 600 pixels or less**. Media queries are crucial for creating responsive web designs that adapt to different devices and screen sizes, providing a better user experience across a wide range of devices and platforms.


The `@media` at-rule, also known as a media query, is used to conditionally apply CSS. Media queries are commonly used to apply CSS based on the viewport width using the `max-width` and `min-width` properties.

In the below example the padding is applied to the `.card` class when the viewport is `960px` wide and below.

```css
@media (max-width: 960px) {
  .card {
    padding: 2rem;
  }
}
```

## Ce am inteles eu din @media rule:

@media este folosit in prinpal ca sa definesti cum o sa arate pagina intre anumite dimensiuni maxime si minime. 
# Logical Operators 

Logical operators can be used to construct more complex media queries. The `and` logical operator is used to query two media conditions.

For example, a media query that targets a display width between 500px and 1000px would be:

```css
@media (min-width: 500px) and (max-width: 1000px){

}
```


# Template pentru Media

```CSS
```.container {
     width: 100%;
     margin-left: auto;
     margin-right: auto;
     padding-left: 0.5rem;
     padding-right: 0.5rem;
}
/* xs */
 @media (min-width: 475px) {
     .container {
         max-width: 475px;
    }
}
/* sm */
 @media (min-width: 640px) {
     .container {
         max-width: 640px;
    }
}
/* md */
 @media (min-width: 768px) {
     .container {
         max-width: 768px;
    }
}
/* lg */
 @media (min-width: 1024px) {
     .container {
         max-width: 1024px;
    }
}
/* xl */
 @media (min-width: 1280px) {
     .container {
         max-width: 1280px;
    }
}
/* 2xl */
 @media (min-width: 1536px) {
     .container {
         max-width: 1536px;
    }
}
```
