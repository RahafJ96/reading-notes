# Local Storage
_HTML Storage_: is a specification named Web Storage, which was at one time part of the HTML5 specification proper, but was split out into its own specification for uninteresting political reasons. Certain browser vendors also refer to it as `Local Storage` or “ DOM Storage.” The naming situation is made even more complicated by some related, similarly-named, emerging standards.

_localStorage_ is a property that allows JavaScript sites and apps to save key-value pairs in a web browser with no expiration date. This means the data stored in the browser will persist even after the browser window is closed.
For a visual refresher on how to use localStorage in JavaScript. localStorage data is specific to the protocol of the document. In particular, for a site loaded over HTTP `(e.g., http://example.com)`, localStorage returns a different object than localStorage for the corresponding site loaded over HTTPS `(e.g., https://example.com)`.

## How does localStorage work?
To use localStorage in your web applications, there are five methods to choose from:

- `setItem():` Add key and value to localStorage
- `getItem():` This is how you get items from localStorage
- `removeItem():` Remove an item by key from localStorage
- `clear():` Clear all localStorage
- `key():` Passed a number to retrieve the key of a localStorage

_Examples:_
1. Storage.setItem()
The setItem() method of the Storage interface, when passed a key name and value, will add that key to the given Storage object, or update that key's value if it already exists.

```javascript
// snippet accesses the current domain's local Storage object and adds a data item to it using Storage.setItem()
localStorage.setItem('myCat', 'Cookie');

```


```javascript
//Just as the name implies, this method allows you to store values in the localStorage object. It takes two parameters: a key and a value. The key can be referenced later to fetch the value attached to it.
window.localStorage.setItem('name', 'Rahaf Al-Jazzazi');
```
Where name is the key and Rahaf Al-Jazzazi is the value. Also note that localStorage can only store strings.
To store arrays or objects, you would have to convert them to strings.

To do this, we use the `JSON.stringify()` method before passing to `setItem()`.
```javascript
let person = {
     name: "Rahaf Al-Jazzazi", 
     location: "Jordan", 
     
     } 

window.localStorage.setItem('user', JSON.stringify(person));
```

2. Reading localStorage
The syntax for reading the localStorage item is as follows:
```javascript
const cat = localStorage.getItem('myCat');
```

### How to get items from localStorage
To get items from localStorage, use the `getItem()` method. `getItem()` allows you to access the data stored in the browser’s localStorage object.
`getItem()` accepts only one parameter, which is the key, and returns the value as a string.
To retrieve a user key:
```javascript
window.localStorage.getItem('user');
```
This returns a string with value as:
```javascript
{ name:"Rahaf Al-Jazzazi",location :"Jordan"}
```
To use this value, you would have to convert it back to an object.
To do this, we make use of the JSON.parse() method, which converts a JSON string into a JavaScript object.
```javascript

JSON.parse(window.localStorage.getItem('user'));
```

3. Removing localStorage
The syntax for removing the localStorage item is as follows:

```javascript
localStorage.removeItem('myCat');
```

To delete local storage sessions, use the `removeItem()` method.

When passed a key name, the `removeItem()` method removes that key from the storage if it exists. If there is no item associated with the given key, this method will do nothing.

```javascript
window.localStorage.removeItem('name');
```

4. Clear localStorage
The syntax for removing all the localStorage items is as follows:
```javascript
localStorage.clear();
```
Use the `clear()` method to delete all items in localStorage.
This method, when invoked, clears the entire storage of all records for that domain. It does not receive any parameters.

```javascipt
window.localStorage.clear();

```