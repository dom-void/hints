# `XMLHttpRequest` example

```js
let response;

function loadDoc(url) {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      response = this.responseText;
    }
  };
  xhttp.open("GET", url, true);
  xhttp.send();
  return response;
}
```

[AJAX - The XMLHttpRequest Object (@w3schools)](https://www.w3schools.com/xml/ajax_xmlhttprequest_create.asp)
