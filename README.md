function addNumber(num) {
  return function(n) {
    return n + num;
  }
}

// Example usage:
const addFive = addNumber(5);
console.log(addFive(10)); // Output: 15
console.log(addFive(20)); // Output: 25

function searchArray(arr, val) {
  if (arr.length === 0) {
    return false;
  }
  
  if (arr[0] === val) {
    return true;
  }
  
  return searchArray(arr.slice(1), val);
}

// Example usage:
const arr = [1, 2, 3, 4, 5];
console.log(searchArray(arr, 3)); // Output: true
console.log(searchArray(arr, 6)); // Output: false
function addParagraph(text) {
  const paragraph = document.createElement("p");
  const node = document.createTextNode(text);
  paragraph.appendChild(node);
  document.body.appendChild(paragraph);
}

// Example usage:
addParagraph("Hello, world!");

function addListItem(text) {
  const listItem = document.createElement("li");
  const node = document.createTextNode(text);
  listItem.appendChild(node);
  const list = document.querySelector("ul");
  list.appendChild(listItem);
}

// Example usage:
addListItem("Item 1");

function changeBackgroundColor(element, color) {
  element.style.backgroundColor = color;
}

// Example usage:
const myElement = document.getElementById("my-element");
changeBackgroundColor(myElement, "red");

function saveToLocalStorage(key, obj) {
  localStorage.setItem(key, JSON.stringify(obj));
}

// Example usage:
const myObj = { name: "John", age: 30 };
saveToLocalStorage("my-object", myObj);
function getFromLocalStorage(key) {
  const objStr = localStorage.getItem(key);
  return JSON.parse(objStr);
}

// Example usage:
const retrievedObj = getFromLocalStorage("my-object");
console.log(retrievedObj); // Output: { name: "John", age: 30 }



function saveObjectToLocalStorage(obj) {
  for (const prop in obj) {
    if (obj.hasOwnProperty(prop)) {
      localStorage.setItem(prop, JSON.stringify(obj[prop]));
    }
  }
  return getFromLocalStorage();
}

// Example usage:
const myObj = { name: "John", age: 30 };
const savedObj = saveObjectToLocalStorage(myObj);
console.log(savedObj); // Output: { name: "John", age: 30 }
