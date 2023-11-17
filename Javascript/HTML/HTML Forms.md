
The `method` attribute specifies how to send form-data to the URL specified in the `action` attribute. The form-data can be sent via a `GET` request as URL parameters (with `method="get"`) or via a `POST` request as data in the request body (with `method="post"`).

The GET Method[](https://www.baeldung.com/cs/http-get-vs-post#the-get-method)

GET is used to request data from a specified resource. It can retrieve any visible data to a client, such as HTML documents, images, and videos:

![Image for Get Method](https://www.baeldung.com/wp-content/uploads/sites/4/2023/01/Get-Method.jpg)  
To send a GET request, a client needs to specify the [URL of the resource](https://www.baeldung.com/java-url-vs-uri) it wants to retrieve. The request is then sent to the server, which processes the request and sends the requested data back to the client.

##  The POST Method[](https://www.baeldung.com/cs/http-get-vs-post#the-post-method)

The POST sends data to a server to create or update a resource. For example, it is often used to submit an HTML form to a server:

![Image for POST Method](https://www.baeldung.com/wp-content/uploads/sites/4/2023/01/POST-Method.jpg)  
To send a POST request, a client needs to specify the URL of the resource to which it wants to send data and the data itself. The request is then sent to the server, which processes the request and sends a response back to the client.  
  
The POST method is often used to submit forms or upload files to a server.


The `<label>` element is one of a handful of elements that only exists and makes sense in relationship to another element. In the case of `<label>`, the label has to be associated with a form field (usually in [`<input>`](https://html.com/tags/input/) element of [one sort or another](https://html.com/attributes/input-type/).

For a `<label>` to work properly, it must include a `for` attribute, which identifies the `<input>` to which it is associated. The `for` attribute’s value should match the `id` (not the `name`) of the `<input>` element.. Label is inline
## Code Example

```
<form>
 <label for="favorite-animal">Favorite Animal</label><br>
 <input name="favorite-animal" id="favorite-animal">
</form>
```


The first `input` element with a `type` of `submit` is automatically set to submit its nearest parent `form` element.
To handle the form submission, after the last `fieldset` element add an `input` element with the `type` attribute set to `submit` and the `value` attribute set to `Submit`.


With `type="password"` you can use the `pattern` attribute to define a regular expression that the password must match to be considered valid.
Add a `pattern` attribute to the password `input` element to require the input match: `[a-z0-5]{8,}`


Certain `type` attribute values come with built-in form validation. For example, `type="email"` requires that the value be a valid email address.
Add custom validation to the password `input` element, by adding a `minlength` attribute with a value of `8`. Doing so prevents inputs of less than 8 characters being submitted.


You only want one radio input to be selectable at a time. However, the form does not know the radio inputs are related.
To relate the radio inputs, give them the same `name` attribute with a value of `account-type`. Now, it is not possible to select both radio inputs at the same time.


Adding a dropdown to the form is easy with the `select` element. The `select` element is a container for a group of `option` elements, and the `option` element acts as a label for each dropdown option. Both elements require closing tags.
Start by adding a `select` element below the two `label` elements. Then nest 5 `option` elements within the `select` element.


The `textarea` element acts like an `input` element of type `text`, but comes with the added benefit of being able to receive multi-line text, and an initial number of text rows and columns.
The `textarea` appears too small. To give it an initial size, you can add the `rows` and `cols` attributes.
To give Campers an idea of what to put in their bio, the `placeholder` attribute is used. The `placeholder` accepts a text value, which is displayed until the user starts typing.


During development, it is useful to see the `fieldset` default borders. However, they make the content appear too separated.

