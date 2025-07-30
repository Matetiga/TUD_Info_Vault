## "#" : Message Expressions 
- **Purpose**: Used for accessing entries from message/properties files, primarily for localization.
- **Syntax**: `th:text="#{register.password}"`
- **Example Use**: Referencing language-specific properties.
- **Usage**: If `register.password` is defined in `messages.properties`, `#{register.password}` will be replaced by its localized value.

```
<label th:text="#{register.password}" for="password">Passwort</label>
```
- this will get the "pre written message" for example in *message.properties* file
- **Note** : this uses **th:text**

---

## $*$ : Selection Variables 
- **Purpose**: Works within a form or collection context and accesses fields of the selected object, often used with `th:object`. 
	- **used to assign values to a variable** 

- **Syntax**: 
``` html
th:text="*{password}"

th:field="*{password}" 
```
- <span style="color:#ffff00">th:field:</span> used for [[Binding variables between html and java]]

- **Example Use**: Accessing fields in a form-bound object.
- **Usage**: If a form has `th:object="${user}"`, then `th:text="*{password}"` will retrieve the `password` field from the `user` object.


---

## "$": Variable Expressions

- **Purpose**: Used to access variables in the model (e.g., values passed from the controller).
- **Syntax**: 
```html 
th:text="${passwordError}"
```
- **Example Use**: Display error messages or any dynamic data that’s stored in the model.
- **Usage**: If you have an attribute called `passwordError` in your model, `${passwordError}` will retrieve its value.
### Difference with th:text="`*{...}`"
- when using *"$"*  there is no need of using *th:object...* prior (*not bound to an specific object and can be any variable passed to the model from the controller*)