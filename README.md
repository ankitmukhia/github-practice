# github-practice

### Add you utility function, that are usefull for daily coding practices.

- Utility function for delaying.
```js
const delay = (ms) new Promise((resolve) => setTimeout(() => resolve()), ms)
```
- Utility function for Debouncing a function call.
```js
const debounce = (func, delay) => {
  let timeoutId;
  return function (...args) {
    if (timeoutId) clearTimeout(timeoutId);
    timeoutId = setTimeout(() => {
      func.apply(this, args);
    }, delay);
  };
};
```
- Utility function for sorting any array of object by specific key.
```js
export function sortByKey(array, key) {
    return array.sort((a, b) => (a[key] > b[key] ? 1 : -1));
}
```
- Utility function for generating random id.
```js
function generateId(prefix = 'id') {
    return `${prefix}_${Math.random().toString(36).substr(2, 9)}`;
}
```
- Utility function deep copy of object 
```js
export function deepClone(obj) {
    return JSON.parse(JSON.stringify(obj));
}
```
