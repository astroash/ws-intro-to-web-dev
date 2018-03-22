# Codealong Notes
## Intro
This workshop is designed to be a codealong for beginners in html & css animations.  

## Setup & Animations
1. Setup HTML doc and create a `<div class='box'>`
  - show how to link up css file
  ```html
  <link rel="stylesheet" href="./main.css">
  ```
  - style to box class with `width`, `height`, `background`
  - add transition shorthand property `transition:all 1s ease`. It takes 4 values: 
  ```css
  transition-property /*name of the target CSS property */
  transition-duration /*length of transition */
  transition-timing-function /* speed curve */
  transition-delay 
  ```

2.  Add a `<div>` with class `box` and `fade-in`
  - in css set standard opacity to 0.6
  - in css set hover pseudo-class opacity to 1 --pseudo classes are used to define a special state of an element 
  ```css
  .fade-in {
    opacity:0.6;
  }

  .fade-in:hover {
    opacity:1;
  }
  ```
3.  Add a `<div>` with class `box` and `chameleon`
  - in css set hover bg colour to pink 
  ```css
  .chameleon:hover {
    background: pink;
  }
  ```
4.  Add a `<div>` with class `box` and `grow`
  - in css set transform property on hover. Transform 2D/3D changes to an element such as rotate, scale, move and skew.
  - prefixes need to be added for browser support
  ```css
  .grow:hover {
    -ms-transform: scale(1.3,1.3); /* ie 9 */
    -webkit-transform: scale(1.3,1.3); /* safari */
    transform: scale(1.3,1.3)
  }
  ```
5.  Add a `<div>` with class `box` and `shrink`
  - in css set transform property on hover. 
  ```css
  .shrink:hover {
    -ms-transform: scale(0.7, 0.7);
    -webkit-transform: scale(0.7,0.7);
    transform: scale(0.7, 0.7)
  }
6.  Add a `<div>` with class `box` and `shape`
  - in css set border radius on hover. 
  ```css
  .shape:hover {
    border-radius: 50%
  }
  ```
7.  Add a `<div>` with class `box` and `swing`
  - add animation shorthand property `animation: swinging 1s ease;`.
  - It can take the following values:
  ```css
  animation-name /*pick a name to define later*/
  animation-duration
  animation-iteration-count
  animation-direction: alternate; /* or: normal */
  animation-timing-function: ease-out; /* or: ease, ease-in, ease-in-out, linear, cubic-bezier(x1, y1, x2, y2) */
  animation-fill-mode: forwards; /* or: backwards, both, none */
  animation-delay:

  ```
  - Now you need to define what your animation does. Using your animation name add keyframes to describe what you want to happen at each interval.
  - In production you should use prefixes for different browers, but will skip for now
  ```css
  @keyframes swinging {
    20% { transform: translateX(2px) }
    40% { transform: translateX(-4px) }
    60% { transform: translateX(4px) }
    80% { transform: translateX(-3px) }
    100% { transform: translateX(1px) }
  }
  ```
8.  Add a `<div>` with class `box` and `rainbow`
  - add animation property on hover. 
  ```css
  .rainbow:hover {
    animation: rainbow 7s linear
  }
  ```
  - Now let's define our keyframes
  ```css
    @keyframes rainbow {
  15% { background: red }
  30% { background: orange } 
  45% { background: yellow }
  60% { background: green }
  75% { background: blue }
  90% { background: purple}
}
  ```
## Let's make it pretty

9. Add some layout to div box css
  - Put them in a row with `display: inline-block;`
  - Space them out with `margin: 1rem;`
  - Hack the text height with `line-height: 3;`
  - And make it white `color: white;`
10. Enclose animation divs's in two row divs
  ```html
  <div class="row">
    <div class="box"....
  ```
  - and center align them with `text-align: center;`