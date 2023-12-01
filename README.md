# Frontend Mentor - Newsletter sign-up form with success message solution

This is a solution to the [Newsletter sign-up form with success message challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/newsletter-signup-form-with-success-message-3FC1AZbNrv). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- Add their email and submit the form
- See a success message with their email after successfully submitting the form
- See form validation messages if:
  - The field is left empty
  - The email address is not formatted correctly
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

![](design/Captura-de-tela.png)


### Links

- Solution URL: [Add solution URL here](https://github.com/felipe1000/newsletter)
- Live Site URL: [Add live site URL here](https://felipe1000.github.io/newsletter/index.html)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- JavaScript (DOM)
- Mobile-first workflow

### What I learned

I had to remove the native form validation in HTML5 using novalidate to create my own validation in JS

See below:

```html
<form action="thanks.html" method="get" autocomplete="off" novalidate>
<input type="submit" value="Subscribe to monthly newsletter" onclick="checkEmail()" id="submitButton">
```
```js
    emailInput.addEventListener('input', checkEmail);

    function checkEmail() {
    const emailValue = emailInput.value;

    if (emailValue.indexOf('@') === -1) {
        msg.innerHTML = 'Valid email required';
        event.preventDefault(); // Isso impede o envio do formulário
    } else {
        msg.innerHTML = '';
    }
```

## Author

- Website - [Felipe Maciel](https://felipeguedesmaciel.000webhostapp.com/)
- Frontend Mentor - [@felipe1000](https://www.frontendmentor.io/profile/felipe1000)