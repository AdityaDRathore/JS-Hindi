# Project for DOM application 

## Project 1 Link 
[Click here](https://stackblitz.com/edit/dom-project-chaiaurcode-pd5k9b?file=1-colorChanger%2Fchaiaurcode.js,1-colorChanger%2Findex.html,1-colorChanger%2Fstyle.css)

# Project 1 solution
## Background Color Changer

```javascript
console.log("javascript");

const buttons = document.querySelectorAll('.button'); 
const body = document.querySelector("body"); 

buttons.forEach(function(button){
  console.log(button);
  button.addEventListener('click', function(e) {
    console.log(e); 
    console.log(e.target);

    if(e.target.id === 'grey') {
      body.style.backgroundColor = e.target.id; 
    }

    else if (e.target.id === 'yellow') {
      body.style.backgroundColor = e.target.id; 
    }

    else if (e.target.id === 'blue') {
      body.style.backgroundColor = e.target.id; 
    }

    else if (e.target.id ==='red') {
      body.style.backgroundColor = e.target.id; 
    }

    else {
      e.target.id = 'white'; 
      body.style.backgroundColor = e.target.id;
    }
  }) 
});
```

# Project 2 Solution
## BMI Calculator
```javascript

const form = document.querySelector('form');

form.addEventListener('submit', function (e) {
  e.preventDefault();

  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');
  const bmi = (weight / ((height * height) / 10000)).toFixed(2);
  let temp; 
  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = 'Please give a valid height';
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = 'Please give a valid weight';
  } else {
    results.innerHTML = `<span>${bmi}</span>`;
    temp = bmi; 
  }

  if(bmi < 18.6 ) {
    results.innerHTML = `<div><span>${bmi}</span> <div>You are Under Weight</div></div>`
  }
  if(bmi > 18.6 && bmi < 24.9 ) {
    results.innerHTML = `<div><span>${bmi}</span> <div>You are in Normal Range</div></div>`
  }
  else {
    results.innerHTML = `<div><span>${bmi}</span> <div>You are Overweight</div></div>`

  }
  
});

```

# Project 3 Solution
## Digital Clock

```javascript
const clock = document.getElementById('clock');

setInterval(function(){
  let date = new Date;
  clock.innerHTML = date.toLocaleTimeString(); 
}, 1000);
```