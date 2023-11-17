
# Center vertically and horizontally with position(middle of the page)

  position: absolute;

  top: 0;

  left: 0;

  right: 0;

  bottom: 0;

  margin: auto;

# position

The **`position`** [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) property sets how an element is positioned in a document. The [`top`](https://developer.mozilla.org/en-US/docs/Web/CSS/top), [`right`](https://developer.mozilla.org/en-US/docs/Web/CSS/right), [`bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/bottom), and [`left`](https://developer.mozilla.org/en-US/docs/Web/CSS/left) properties determine the final location of positioned elements.

CSS positioning lets you set how you want an element to be positioned in the browser. It has a `position` property you can set to `static`, `absolute`, `relative`, `sticky` or `fixed`.

Once you set the `position` property of the element, you can move the element around by setting a pixel or a percentage value for one or more of the `top`, `right`, `left`, or `bottom` properties.

`static` is the default positioning for all elements. If you assign it to an element, you won't be able to move it around with `top`, `right`, `left`, or `bottom`.

When you use the `relative` value, the element is still positioned according to the normal flow of the document, but the `top`, `left`, `bottom`, and `right` values become active.

The next position property is `absolute`. When you use the `absolute` value for your `position` property, the element is taken out of the normal flow of the document, and then its position is determined by the `top`, `right`, `bottom`, and `left` properties.

`fixed` is a `position` property value that lets you make an element fixed to the page no matter where the user scrolls to on the page.

The last position property value is `sticky`. `sticky` positioning is a hybrid of `relative` and `fixed` positioning. It allows an element to **stick** to a specific position within its containing element or viewport, based on the scroll position.

DE RETINUT: Daca copilului unui element are un position, si parintele ar trebui sa aiba un position ca sa aiba child element-ul un punct de referinta!

Exemple: https://developer.mozilla.org/en-US/docs/Web/CSS/position

# The loading attribute of img


The `loading` attribute on an `img` element can be set to `lazy` to tell the browser not to fetch the image resource until it is needed (as in, when the user scrolls the image into view). As an additional benefit, lazy loaded elements will not load until the non-lazy elements are loaded - this means users with slow internet connections can view the content of your page without having to wait for the images to load.

Exemple: https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading

# Referer

The `Referer` HTTP header contains information about the address or URL of a page that a user might be visiting from. This information can be used in analytics to track how many users from your page visit freecodecamp.org, for example. Setting the `rel` attribute to `noreferrer` omits this information from the HTTP request. 

Exemple: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referer


# Cum sa faci icons pentru pagina

1. Creeaza un div care sa le contina cu clasa social-icons

2. Pui cate un anchor cu link catre paginile dorite pentru fiecare icon

3. Trebuie sa incarci un font care are icons in el. Alternativ, ai putea tu sa cauti pe net imagini cu icons pentru ce iti trebuie(cum ar fii logo-uri de la retele sociale)

4. Inauntru la anchor, adaugi elementul de <i></i> `<i>` si ii dai o clasa specifica. De obicei, clasa specifica se mentioneaza in site-ul unde gasesti font-ul. Asta automat iti transforma ancora intr-un icon. Alternativ, ai putea in loc de elementul `<i>`, sa pui un img cu logo-ul.


# The Block Quotation element

The **`<blockquote>`** [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) element indicates that the enclosed text is an extended quotation. Usually, this is rendered visually by indentation (see [Notes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote#usage_notes) for how to change it). A URL for the source of the quotation may be given using the `cite` attribute, while a text representation of the source can be given using the [`<cite>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/cite) element.

Exemple: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote

# The Article Contents element

The **`<article>`** [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) element represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). Examples include: a forum post, a magazine or newspaper article, or a blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.

Exemple: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article

# The Aside element

The **`<aside>`** [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML) element represents a portion of a document whose content is only indirectly related to the document's main content. Asides are frequently presented as sidebars or call-out boxes.

Exemple: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside


