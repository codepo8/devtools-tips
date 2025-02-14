---
title: Automatically logging name and value in console.log()
tags: ["Console", "JavaScript", "Debugging", "browser:edge", "browser:chrome", "browser:firefox","browser:safari"]
---
Using the [Console](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/) of DevTools you can to log some information to debug your JavaScript.

The common way to do that is to add a `console.log()` statement where you want to learn the value of a certain variable. In the following example the mouse position and how far the document has scrolled.

```javascript
document.body.addEventListener('click', e => {
  let x = e.pageX;
  let y = e.pageY;
  let top = document.documentElement.scrollTop;
  console.log(x);  
  console.log(y);  
  console.log(top);  
})
```

The problem is that this results in lots of numbers in the Console without explanations what they are. If you wrap the values you want to read out in curly brackets `{}`, the Console automatically displays both the name and the value of the variable.

```javascript
document.body.addEventListener('click', e => {
  let x = e.pageX;
  let y = e.pageY;
  let top = document.documentElement.scrollTop;
  console.log({x});  
  console.log({y});  
  console.log({top});  
})
```

You can see the difference in the following screencast or in [this quick demo on YouTube](https://www.youtube.com/watch?v=xTnqsA5vZX4).

![Screencast showing the different ways the variables are logged with and without curly braces](/assets/img/automatically-log-name-and-value.gif)