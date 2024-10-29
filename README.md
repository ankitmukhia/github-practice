# github-practice
This is just github exampl/practice.

## Add you utility function, that are usefull for daily coding practices.

## Utility function for delaying.
```js
  const delay = (ms) new Promise((resolve) => setTimeout(() => resolve()), ms)
```

- Utility function for Debouncing 
```js
const debounce = (func, delay) => {
  let timeoutId;
  return function(...args) {
    if(timeoutId) clearTimeout(timeoutId);
    timeoutId = setTimeout(() => {
      func.apply(this, args);
    }, delay)
  }
}
```
