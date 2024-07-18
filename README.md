# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![Screenshot](./screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [https://ryan-ohanlon.github.io/testimonials-grid-section-main/](https://ryan-ohanlon.github.io/testimonials-grid-section-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

From this challenge, I learned how when creating a website using your own CSS rules that using CSS Flexbox and CSS Grid will be used together in order to align HTML elements and be able to place containers such as section and div on specific places on a webpage.

I also learned how to nest CSS rules into classes which has helped reduce the amount of CSS classes but also keep CSS rules organized and specific for each container. 

While this does have a downside of repeating CSS rules, being able to contain the rules being nested makes reading the CSS document a lot easier. The other potential downside with this challenge is that since there were two white containers that I put all the CSS formatting rules into, when it came time to designing the grid for a desktop view, I had to create a new set of CSS classes to use the grid-area-template to assign each container to a specific section.

```css
body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    font-size: 13px;
    background-color: hsl(210, 46%, 95%);
    min-height: 100vh;
}
main {
    display: grid;
    grid-template-columns: 1fr;
    min-width: 325px;
    gap: 2em;
    margin: 1em;
}
```

```css
@media screen and (min-width:1024px) {
    body {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
    }
    main{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        grid-template-areas: 
        "daniel daniel jonathan kira"
        "jeanette patrick patrick kira";
        gap: 20px;
        max-width: 1024px;
        margin: 1em;
    }
    .box1{
        grid-area: daniel;
    }
    .box2{
        grid-area: jonathan;
    }
    .box3{
        grid-area: jeanette;
    }
    .box4{
        grid-area: patrick;
    }
    .box5{
        grid-area: kira;
    }
}
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

I'm going to continue to develop how to contain HTML elements in section and div elements, using a better categorization system to name HTML elements and use that system to organize CSS rules, and use CSS grid more and figure out how to place elements where I need them to be set.


### Useful resources

- [W3Schools](https://www.w3schools.com/html/html_images_background.asp) - This helped me understand how to implement images behind text and into container elements like div. Being able to place image elements behind text is very useful.
- [GridbyExample](https://gridbyexample.com/examples/) - This is an amazing site that is focused on how to practically use CSS Grid to be able to build objects.

## Author

- Website - [Ryan O'Hanlon](https://ryan-ohanlon.github.io/)
- Frontend Mentor - [@Ryan-OHanlon](https://www.frontendmentor.io/profile/Ryan-OHanlon)
- Twitter - [@RyanROHanlon](https://x.com/RyanROHanlon)

