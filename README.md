# Frontend Mentor - Order summary card solution

This is a solution to the [Order summary card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlPmajDUj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- See hover states for interactive elements

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Media queries 

if added two media queries one for the desktop view and one for the mobile view.

```css
/* global desktop view */
@media only screen and (min-width: 375px)

/* mobile view 375px */
@media only screen and (max-width: 375px) 
```

### Ccs reset

This is the css reset i used.

[Normalize](https://necolas.github.io/normalize.css/latest/normalize.css)

### background

The background was the hardest part, I didn't know how to make the curved path.

After quick research I found a video from [Brandon Stiles](https://www.youtube.com/watch?v=0QTzTOJCzLY&ab_channel=BrandonStiles%2CFrontEndDeveloper) that explains how to do it. 

I want for a SVG file witch i made with [Shapedivider](https://www.shapedivider.app/)

I simply changed the color by editing the fill attribute of the svg.

```html
<svg
  xmlns='http://www.w3.org/2000/svg'
  viewBox='0 0 64 64'
  width='64' height='64'
  fill='#D6E1FD'>
  <path d='M0 18 C32 24 32 2 64 18 L64 0 L0 0 Z' />
</svg>
```
Then i placed the svg on the background and made it cover. At first it didn't work but it turned out the Chrome was chasing even when i turned chasing off. I only had to change the background color of the body and the background was complete.

```css
body {
    background-color: hsl(225, 100%, 94%);
    background-image: url(images/background-path.svg);
    background-repeat: no-repeat;
    background-size: cover;
  }
```

### card

I couldn't find any dimensions but after adding the illustration-hero img it was easy to guess the right size because of the size the image was.

Adding the text, button and links was pretty straight forward, i didn't encounter any problems with that.

The plan selection was i bit harder because things didn't want to align up properly. thirst i added justify-content: space-between; but i needed to align two child's left and one aligned to the right. After some quick googling i found the right way to do so.

```html
<div class="plan-selection">
  <img src="images/icon-music.svg" alt="#">
    <div class="plan-text">
      <p class="clr-dark-blue" style="font-weight: 700;">Annual Plan</p>
      <p class="clr-desaturated">$59.99/year</p>
    </div>
  <a class="change" href="#">Change</a>
</div>
```
```css
.plan-selection {
  background-color: hsl(225, 100%, 98%);
  display: flex;
  align-items: center;
  justify-content: flex-start;
  border-radius: 12px;
  box-sizing:border-box;
  padding: 12px 24px;
  margin-bottom: 32px; 
}
.change {
  margin-left: auto;
  font-weight: 700;
  color: hsl(245, 75%, 52%);
  font-size: 14px;
}
```	
This is the resource i used:

https://stackoverflow.com/questions/55428040/how-can-i-align-2-first-elements-on-the-left-and-the-last-one-on-the-right

### button

For the shadow u used a [Shadow generator](https://html-css-js.com/css/generator/box-shadow/) this made it easy to compare the shadow to the design. I only had to convert the hsl to hex simply using a [converter](https://www.w3schools.com/colors/colors_converter.asp).

### Attribution 

There was not much to the attribution since it came with the document added to the challenge. i only changed the hover color of the links, The position and i wanted it to open a new tab when the link was clicked.

I had problems with the positioning of the attribution but i found a way to do it thanks to [Stackoverflow](https://stackoverflow.com/questions/2810262/how-to-stick-text-to-the-bottom-of-the-page/2810293). I also didn't know hot to make the link open a new tab so i googled it and found a article on [Stackoverflow](https://stackoverflow.com/questions/17711146/how-to-open-link-in-a-new-tab-in-html) explaining how to do that.


### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Desktop-first workflow

### Useful resources

- [Normalize](https://necolas.github.io/normalize.css/latest/normalize.css) - This helped me to even out the styling over all the different browsers.

- [Brandon Stiles](https://www.youtube.com/watch?v=0QTzTOJCzLY&ab_channel=BrandonStiles%2CFrontEndDeveloper) - This video helped me to make the background.

- [Shapedivider](https://www.shapedivider.app/) - I made the path used for the background with this tool.

- [Brandon Stiles](https://stackoverflow.com/questions/55428040/how-can-i-align-2-first-elements-on-the-left-and-the-last-one-on-the-right) - This helped me with aligning the items in the plan selection part of the card.

- [Shadow generator](https://html-css-js.com/css/generator/box-shadow/) - I made the shadow of the button with this shadow generator.

- [converter](https://www.w3schools.com/colors/colors_converter.asp) - This helped me converting hsl to hex for the shadow generator.

- [Stackoverflow](https://stackoverflow.com/questions/2810262/how-to-stick-text-to-the-bottom-of-the-page/2810293) - This helped me with aligning the attribution to the bottom of the page.

- [Stackoverflow](https://stackoverflow.com/questions/17711146/how-to-open-link-in-a-new-tab-in-html) - This helped me with opening a new tab when a link is clicked.

## Author

- Frontend Mentor - [@spacecylinder](https://www.frontendmentor.io/profile/spacecylinder)
- Twitter - [@maarten_mobron](https://twitter.com/maarten_mobron)
- Instagram - [@maarten_mobron](https://www.instagram.com/maarten_mobron/)