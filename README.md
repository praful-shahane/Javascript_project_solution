# Javascript_project_solution

## Project Questions link 
https://stackblitz.com/edit/dom-project-chaiaurcode

## Project Solution
=====================================================================
## Project 1  Solution

``` javascript

const buttons = document.querySelectorAll('.button');
const body = document.querySelector('body');

//on click on color, we need to change background color of entire page.
//so, click is an event.

//first iterate over Each button
buttons.forEach(function (button) {
  //on click on one button, background-color should change
  button.addEventListener('click', function (e) {
    if (e.target.id === 'grey') {
      body.style.backgroundColor = e.target.id;
    } else if (e.target.id === 'white') {
      body.style.backgroundColor = e.target.id;
    } else if (e.target.id === 'blue') {
      body.style.backgroundColor = e.target.id;
    } else if (e.target.id === 'yellow') {
      body.style.backgroundColor = e.target.id;
    }
  });
});


```

