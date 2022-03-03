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


## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/stats-preview-card-component-using-flexbox-GMgm_jocJ](https://www.frontendmentor.io/solutions/stats-preview-card-component-using-flexbox-GMgm_jocJ)
- Live Site URL: [https://julfinch.github.io/Stats-Preview-Card-Component/](https://julfinch.github.io/Stats-Preview-Card-Component/)

## My process
1. I first created a div container(div id="container") where inside it are two div, one is for the left div where the texts can be found (div id="left-text") and the other one is for the right div where the image-header is applied (div id="right-image").
2. Applied all the details mentioned in the style guide.
3. Applied flexbox to join the two divs and put them together at the center.
4. To make it responsive on mobile, I used media query and used column-reverse with flexbox to put the image-header first at the top of the texts.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile Responsive

### What I learned
- At first attempt, I find it hard to change the hue of the image using the provided color values. Later, I found out that I can just apply that value as background color of the right div and change the image opacity using filter.

Update: I changed it by using background-blend:multiply instead and removed the image-header-desktop in the html and applied it as background-image in the css while putting its highlight color as background color.

```css
background: hsl(277, 64%, 61%);
background-image: url("/images/image-header-desktop.jpg");
border-radius: 0 10px 10px 0;
background-blend-mode: multiply;
```

- I used flexbox for the container and to put the left div and right div at the center, I applied justify content and align-items written just like below: 

```css
#container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

But I found a problem using this method, the bottom of the left div and right div won't level equally inspite many attempts of changing their height values. So I implemented different techniques in centering elements and lastly found a perfect one, see below:

```css
#container {
    display: flex;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

Update: After learning from a feedback in my other completed challenge that using absolute positioning to center contens is already deprecated, I used Flexbox instead right after.

```css
min-height: 100vh;
display: flex;
justify-content: center;
align-items: center;
```

## Author

- Website - [Jul Danreb Lactao](https://www.your-site.com)
- Frontend Mentor - [@julfinch](https://www.frontendmentor.io/profile/julfinch)
- Twitter - [@julfinch](https://www.twitter.com/julfinch)
