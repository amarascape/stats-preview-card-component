# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

- [Desktop View](screenshots/desktop-view-screenshot.png)
- [Mobile View](screenshots/mobile-view-screenshot.png)

### Links

- Solution URL: [https://amarascape.github.io/stats-preview-card-component/index.html](https://amarascape.github.io/stats-preview-card-component/index.html)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [justify-content | CSS-Tricks](https://css-tricks.com/almanac/properties/j/justify-content/)
- [A Complete Guide to Grid | CSS-Tricks](https://css-tricks.com/snippets/css/complete-guide-grid/) 
- [Bootstrap v5.1.0](https://www.bootstrapcdn.com/) - For styles

### What I learned

#### Centering Main on Webpage
```css
body {
  display: flex;
  align-items: center;
  padding-top: 2.5rem;
  padding-bottom: 2.5rem;
}

main {
  width: 100%;
  max-width: 85%;
  padding: 1rem;
  margin: auto;
}
```

#### Defining different images for media sizes in HTML
```html
  <picture>
    <source srcset="images/image-header-desktop.jpg" media="(min-width: 950px)">
    <source srcset="images/image-header-mobile.jpg" media="(max-width: 949px)">
    <img id="HEADER_IMAGE" class="img-fluid" alt="image: people using laptops">
  </picture>
```

#### Applying a tint to an image (where tint can be any color)
```html
 <div class="card-header-image">
   <picture>
     <source srcset="images/image-header-desktop.jpg" media="(min-width: 950px)">
     <source srcset="images/image-header-mobile.jpg" media="(max-width: 949px)">
     <img id="HEADER_IMAGE" class="img-fluid" alt="image: people using laptops">
   </picture>
 </div>
```
```css
.card-header-image {
  background-color: var(--accent-color);
}

#HEADER_IMAGE {
  object-fit: cover;
}

#HEADER_IMAGE {
  min-width: 100%;
}

#HEADER_IMAGE {
  mix-blend-mode: multiply;
  opacity: 0.8;
}
```
#### Creating a grid and defining where to place items in the grid
```html
  <div class="card">
    <div class="card"> ...
    <div class="card"> ...
  </div>
```
```css
  .card {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  .card-text-content {
    grid-column-start: 1;
    grid-row-start: 1;
  }
  ```
#### Justifying the elements in a flex box so they spread evenly 
```html
<ul class="stats-list flex-parent"> ...
```
```css
.stats-list.flex-parent {
    display: flex;
    justify-content: space-around;
}
```

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
