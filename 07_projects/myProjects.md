# Project for DOM application 

## Project 1 Link 
[Click here](https://stackblitz.com/edit/dom-project-chaiaurcode-pd5k9b?file=1-colorChanger%2Fchaiaurcode.js,1-colorChanger%2Findex.html,1-colorChanger%2Fstyle.css)

# Project 1 solution

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