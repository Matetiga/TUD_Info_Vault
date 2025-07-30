## Bind the Class to HTML
```html
th:object="${form}"
```
- *form* is in this case a Java Class which must be **called as follows in the Controller**:
- **Note** : use **"$"** [[Variable Expressions]]
``` Java
String addEntry(@Valid @ModelAttribute("form") GuestbookForm form, Errors errors, Model model)
```
- *@ModelAttribute("form")* : this binds the variable called in html to the variable **GuestbookForm form**


---

## Accessing Class attributes 
- *after Binding the class variable and the html variable* 
- the **class variable attributes** are allowed to be **used in the html**
```html
th:field="*{name}"
```
- [[Variable Expressions]]