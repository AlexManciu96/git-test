
Toate imaginile trebuie sa aiba un alt in ele care sa descrie imaginea

Elementul de <section> 
As mentioned above, <section>is a generic sectioning element, and should only be used if there isn't a more specific element to represent it. s an example, a navigation menu should be wrapped in a <nav> element, but a list of search results or a map display and its controls don't have specific elements, and could be put inside a `<section>`.

Elemetul de <fieldset>
As the example above shows, the `<fieldset>` element provides a grouping for a part of an HTML form, with a nested <legend> element providing a caption for the `<fieldset>`. It takes few attributes, the most notable of which are `form`, which can contain the `id` of a <form> on the same page, allowing you to make the `<fieldset>` part of that `<form>` even if it is not nested inside it, and `disabled`, which allows you to disable the `<fieldset>` and all its contents in one go.

Diferenta dintre in-line element si block-line element este importanta pentru CSS si stilizarea in pagina.

You can use an <hr> element to display a divider between sections of different content.

 What Is ID?

An ID allows developers to identify a single element in the HTML code and apply a particular style to it. IDs are specific and targeted, similar to a proper noun. There can be multiple elements on a page, but the ID marks a specific element. Each element can only have one ID, and each page can only have one element with that specific ID.

As an example, if we have five divs in our HTML, we can create an ID and have each of them be green and 60 pixels tall. IDs are identified with a hash character (#), followed by the ID name:

`div{   background-color: #008000;   height: 60px;   }`

What Is Class?

You should use a class if you need to use the same selector more than once within a page or a site. While an ID is specific to a single element, classes can be assigned to multiple elements on a page or throughout the website. They are not unique. And while a single element can only have one ID, it can have multiple classes.

Classes are denoted by a period, followed by the class name. In this example, all elements tagged with the class "center" will be centered and green:

`.center {   text-align: center;   color: green;   }`

IN HEAD:
<meta charset="utf-8"> ACESTA ESTE META TAG-UL PUS IN HEAD!!
<title>
<!DOCTYPE html> INAINTE DE HEAD
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<link href="styles.css" rel="stylesheet"/> RELATIE CU FISA DE styles.css
<meta name="description" content="blabla">

The <header> element represents introductory content, typically a group of introductory or navigational aids. It may contain some heading elements but also a logo, a search form, an author name, and other elements.

