# DOM

The Document Object Model (DOM) is the data representation of the objects that comprise the structure and content of a document on a web page.

# DOM Node

Every object located within a document is a node of some kind. In an HTML document, an object can be an element node but also a text node or attribute node
Properties:
- `nodeName` (ex., `'H1'`)
- `nodeValue` (ex., 1 - Element, 3 - Text Node)
- `nodeType`
- `parentNode`

# DOM Element
The element type is based on Node. `Element` is represented as an html tag on the page.
Properties and Methods:
- `element.attributes`
- `element.(getAttribute | setAttribute)`
- `element.style`
- `element.classList`
- `element.classList.(add | remove | toggle)`
- `element.contains`
- `element.dataset` - set of data-attributes

# NodeList
It is array-like object. `NodeList` can dynamically change.

# DOM manipulation

- `document.createElement` (ex. `document.createElement("nav", options)`)
- `document.createTextElement`
- `document.createAttribute`

- `node.cloneNode`
- `node.appendChild`
- `node.insertBefore`
- `removeChild` (ex., `var oldChild = node.removeChild(child)`)
- `replaceChild`
  

- `element.innerHTML`
- `element.innerText`
- `element.textContent`
- `element.innerHTML`
- `insertAdjacentHtml(position, insertedHtmlString)`
  accept html string. Parse only inserted string and add it to the parent node.

- `element.classList`
- `element.style.left`
- `element.style.cssText`
- `document.createAttribute`
- `element.setAttribute`
- `element.getAttribute`
- `element.addEventListener`

# DOM access
- `document.getElementById`
- `document.getElementByClass`
- `document.getElementsByClass`






