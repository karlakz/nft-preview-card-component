# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U).  

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

## Overview
Build out preview card component and get it looking as close to the design as possible.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](https://i.imgur.com/ViYStdY.png)

### Links

- Solution URL: [Add solution URL here](https://github.com/karlakz/nft-preview-card-component)
- Live Site URL: [Add live site URL here](https://nft-preview-card-component-karlakz.netlify.app/)

## My process

### Built with

- Flexbox
- Mobile-first workflow

### What I learned

1. `display: flex` property will not work with `<p>` tag. It works with `<div>` tags.
2. Always apply the following piece of code at the beginning of the stylesheet.
```
:root {
    box-sizing: border-box;
}

*,
::before,
::after {
    box-sizing: inherit;
}
```
3. `<hr>` tag will look like a dot on the page without any styling. Therefore, aplly styles:
```
hr {
  border:none;
  width: 100%;
  height: .8em;
  border-bottom: 1px solid #6a6a69;
  box-shadow: 0 20px 20px -20px #333;
  margin: .1em auto; 
  color: gray;
}
```
4. To give a white border to `<img>` tag and make it look like a circle, apply the following styles:
```
img {
  border: 1px solid white;
  border-radius: 50%;
}
```
5. Flexbox creates columns of equal height automatically.
6. Use `align-items` or `align-self` to vertically center a flex item inside its flex
container.
7. Use nested flexboxes to piece together more complicated layouts and to fill the
heights of naturally sized boxes.
8. Spent overall 3 hours. 

### Continued development

Try to recreate this project with normal document flow or using another tools such as CSS Grid or floats, since the page rendering can downgrade with flexbox when the page is loaded over a slow internet connection.  

### Useful resources

- [Change img color in active state](https://stackoverflow.com/questions/19221633/can-css-be-used-to-change-an-images-color-for-active-hover) - This helped me to understand that the image color can not be changed with hover effect or active state and I need to do one of the following steps: 
1) To refer to a separate image on the hover styling rule for that element
```
img:hover {
          background:url(../images/equlibrium.png) no-repeat center left;
      }
```
2) To use [JavaScript OnClick event for the image](https://stackoverflow.com/questions/25076535/change-image-on-active-li) 
3) To use use a sprite, where all the images are loaded as one image and css just focuses on a portion of it depending on the state ie hover, active etc.

## Author

- Website - [Karlygash Yakiyayeva](https://www.your-site.com)
- Frontend Mentor - [@karlakz](https://www.frontendmentor.io/profile/karlakz)
