# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Frontend Mentor - Testimonials grid section solution](#frontend-mentor---testimonials-grid-section-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![Screenshot](./screenshot.jpg)

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/testimonial-grid-section-KG8m1DBlv](https://www.frontendmentor.io/solutions/testimonial-grid-section-KG8m1DBlv)
- Live Site URL: [https://fem-testimonials-grid-section-snowy.vercel.app/](https://fem-testimonials-grid-section-snowy.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- Learnt how to effectively exploit the power of css custom properties. As a parent class holds the general styles of other elements, modifier classes can be used to alter/override the styles from the parent class using CSS variables, as shown below:

```css
.daniel,
.jonathan,
.patrick {
  --opacity: 1;
  --clr-prim-whte: hsla(0, 0%, 100%, var(--opacity));
  color: var(--clr-prim-whte);
}

.daniel.span,
.jonathan.span,
.patrick.span {
  --opacity: 0.5;
}

.daniel.card__desc,
.jonathan.card__desc,
.patrick.card__desc {
  --opacity: 0.7;
}
```

- Also learnt how to layout elements in a little complex grid-like structure(`display:grid` was already called on `.main` in the mobile-first workflow):

```css
.main {
  margin: 6rem auto;
  width: 70%;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: auto;
}

.daniel {
  grid-column: 1/3;
}
.jeanette {
  grid-column: 1;
}

.patrick {
  grid-column: 2/4;
}
.kira {
  grid-column: 4;
  grid-row: 1/3;
}
```

### Useful resources

- [Traversy Media - Grid Layout Crash Course](https://www.youtube.com/watch?v=jV8B24rSN5o&t=1017s) - This helped understand how the `display:grid` works.
- [Web Dev Simplified - CSS Custom Properties](https://blog.webdevsimplified.com/2020-02/css-custom-properties/) Helped understand how overriding of custom properties can used.

## Author

- Frontend Mentor - [@Pap-Ski](https://www.frontendmentor.io/profile/Pap-Ski)
