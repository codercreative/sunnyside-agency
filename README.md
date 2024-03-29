# Frontend Mentor - Sunnyside agency landing page solution

This is a solution to the [Sunnyside agency landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/sunnyside-agency-landing-page-7yVs3B6ef). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Challenges along the way](#challenges-along-the-way)
  - [What I learned](#what-i-learned)
- [Resources](#resources)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### Challenges along the way

- Keeping track of all the "moving parts" in different screen sizes with grid and flexbox and determining when I should use flexbox and when to use grid
- Creating the hamburger nav
- Have text overlap images in some but not all sections
- Getting rid of default padding around images (solution: `display: block`)

### What I learned

- Remembering to use the `picture` tag to switch between mobile and desktop images based on screen size:

```html
<picture>
  <source
    media="(max-width: 375px)"
    srcset="./images/mobile/image-header.jpg"
  />
  <source
    media="(min-width: 376px)"
    srcset="./images/desktop/image-header.jpg"
  />
  <img
    src="./images/desktop/image-header.jpg"
    alt="Hero image of cut orange with blue background"
    class="hero-img"
  />
</picture>
```

- Making sure to add `display: block`to avoid any extra padding around the images:

```css
img,
picture,
svg {
  display: block;
  max-width: 100%;
}
```

Using 50vw for the article img as well as the article text to ensure that they both take up 50% of the row. I need to fix this with a container or other solution.

```css
.article-img,
.article-text {
  width: 50vw;
}
```

When I added max-width to main the log and burger menu disappeared out of view on large screens.

Learned how to keep a heading on one line:

```html
h1 { white-space: nowrap; }
```

## Resources

[Josh Comeau's custom CSS reset](https://www.joshwcomeau.com/css/custom-css-reset/)

[When to use image, figure, picture tag in html](https://www.youtube.com/watch?v=Xn5_gDQFyJg)
