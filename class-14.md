# CSS Transitions & Animations &  Transforms

## Transform 2D & 3D

**The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.**
```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```


> 2D Rotate : The rotate value provides the ability to rotate an element from 0 to 360 degrees. ex (rotate(20deg)).

> 2D Scale :  property allows you to change the appeared size of an element. ex (scale(.75)).

> 2D Translate : The translate value works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow of the document. ex( ```.box-1 {
  transform: translateX(-10px);
}
.box-2 {
  transform: translateY(25%);
}
.box-3 {
  transform: translate(-10px, 25%);
}```
).

>2D Skew :  is used to distort elements on the horizontal axis, vertical axis, or both. ex(```.box-1 {
  transform: skewX(5deg);
}
.box-2 {
  transform: skewY(-20deg);
}
.box-3 {
  transform: skew(5deg, -20deg);
}```).

>3D smae as 2d but you ned to add z axies.


## Transitions

transitions As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

```
 transition: background .2s linear, border-radius 1s ease-in 1s;
```


## Animations

Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.

```
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;

  @keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}
```


## 8 simple CSS3 transitions that will wow your users

1. Fade in
1. Change color
1. Grow & Shrink
1. Rotate elements
1. Square to circle
1. 3D shadow
1. Swing
1. Inset border

[More Info About Movment](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)