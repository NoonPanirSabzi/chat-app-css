# Chat app CSS illustration

## Table of contents

- [Overview](#overview)
  - [Screenshot and live site URL](#screenshot-and-live-site-url)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)
- [Inspired by](#inspired-by)

## Overview

### Screenshot and live site URL

| Desktop                                    | Mobile                                   |
| ------------------------------------------ | ---------------------------------------- |
| ![desktop](/images/desktop-screenshot.png) | ![Mobile](/images/mobile-screenshot.png) |

[Live Site URL](Link)

## My process

### Built with

- HyperText Markup Language
- pure Cascading Style Sheets for visuals

### What I Learned

1. **CSS clamp for responsive sizing**  
   how to create a range of values that decreases as the viewport gets larger:

   ```css
   clamp(75px, 625px - 22.6vw, 300px);
   ```

   As the viewport width increases, the subtracted value (`22.6vw`) grows, which makes the overall result smaller.

2. **Creating negative values in CSS**  
   In CSS, you can create negative numbers by using the `calc()` function. For example:

   ```css
   calc(0px - 10px)  /* results in -10px */
   ```

3. **Handling decorative boxes with overflow**  
   At first, I placed decorative boxes inside the `<body>` and used `position: absolute`. However, when I set `body { overflow: hidden; }`, it also clipped the `<main>` content.
   The solution was to place the decorative boxes inside `<main>` instead. Since the boxes are absolutely positioned, they are taken out of normal flow, while `<main>` still sizes itself based on the content. This way, applying `overflow: hidden` to `<main>` achieves the desired effect without clipping the actual content.

4. **Controlling flex container width**  
   In a row flex container with lots of horizontal space, the container will try to stretch and occupy all available width—even if child elements have fixed widths.
   One way to control this is:

   * Give children a fixed width.
   * Set the desired gap between them.
   * Then set the container’s `inline-size` (or `width`) to `fit-content`.

## Author

- Github - [@AminForouzan](https://github.com/AminForouzan)
- Frontend Mentor - [@AminForouzan](https://www.frontendmentor.io/profile/AminForouzan)

## Inspired by

- [Chat app CSS illustration challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/chat-app-css-illustration-O5auMkFqY).
