# Javascript_project_solution

## Project Questions link 
https://stackblitz.com/edit/dom-project-chaiaurcode

## Project Solution
=====================================================================
## Project 1  Solution (Color Changer)

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

## Project 2  Solution (BMI Calculator)

``` javascript

// here we have form, after we click on submit button,GET/POST method will hit
// and data will move to service side through URL.
//we should get a data on UI side only not move to service side.
//to prevent this from happening, we use preventDefault() method.

const form = document.querySelector('form');

//we could not write this weight and height variable to capture a data outside of a form bcz
// we get value of height and weight on submit only
//otherwise we get empty value.

// const weight = parseInt(document.querySelector('#weight').value);
//   const height = parseInt(document.querySelector('#height').value);

//form has submit event
form.addEventListener('submit', function (e) {
  //to capture a value of height in cm  and weight in kg.
  //by default we get string value, we need to convert into integer.
  const weight = parseInt(document.querySelector('#weight').value);
  const height = parseInt(document.querySelector('#height').value);
  const results = document.querySelector('#results');

  //isNan() method will check a height is number or not.
  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = `Please give a valid height ${height}`;
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = `Please give a valid weight ${weight}`;
  } else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);
    if (bmi < 18.6) {
      results.innerHTML = `<span> UnderWeight ${bmi}</span>`;
    } else if (bmi > 18.6 && bmi < 24.9) {
      results.innerHTML = `<span> NormalWeight ${bmi}</span>`;
    } else {
      results.innerHTML = `<span> OverweightWeight ${bmi}</span>`;
    }
  }
});


```

