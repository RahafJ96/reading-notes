#  CSS Transforms, Transitions, and Animations

# CSS Transforms:
CSS transforms allow you to move, rotate, scale, and skew elements. 

In this event multiple transforms can be combined together. To combine transforms, list the transform values within the transform property one after the other without the use of commas.
The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.

Working with two-dimensional transforms we are able to alter elements on the horizontal and vertical axes `(x, y)`, however there is another axis along which we can transform elements. Using three-dimensional transforms we can change elements on the z axis, giving us control of depth `(z)` as well as length and width `(x, y)`.

# Transitions and Animations:

## Transitions:
As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the:
- `:hover`
- `:focus`
- `:active`
- `:target`

## Animations:
Animations pick up where transistions leave off. CSS has introduced countless possibilities for UX designers, and the best thing about them is that the coolest parts are really simple to implement.

### Some Simple CSS Transitions used the most:
Just a couple of lines of code will give you an awesome transition effect that will excite your users, increase engagement and ultimately, when used well, increase your conversions.

#### **1. Fade in**

Having things fade in is a fairly common request from clients. It’s a great way to emphasize functionality or draw attention to a call to action.
Fade in effects are coded in two steps: first, you set the initial state; next, you set the change, for example on hover.

```css
.fade {
  opacity:0.3;
}
.fade:hover
{
  opacity:1.8;
}
```
#### **2. Change color**
Animating a change of color used to be unbelievably complex, with all kinds of math involved in calculating separate RGB values and then recombining them. Now, we just set the div’s class to “color” and specify the color we want in our CSS.

```css
.color:hover
{
  backround:#16A474;
}
```

#### **3. Rotate elements**
CSS transforms have a number of different uses, and one of the best is transforming the rotation of an element. Give your div the class `“rotate”` and add the following to your CSS:

```css
.rotate:hover
{
  -webkit-transform: rotateZ(-90deg);
  -ms-transform: rotateZ(-90deg);
  transform: rotateZ(-90deg);
}

```
#### **4. Grow & Shrink**
To grow an element, you used to have to use its width and height, or its padding. But now we can use CSS3’s transform to enlarge.
Set your div’s class to “grow” and then add this code to your style block:

```css
.grow:hover
{
  -webkit-transform: scale(1.5);
  -ms-transform: scale(1.5);
  transform: scale(1.5);
}
```

Shrinking an element is as simple as growing it. To enlarge an element we specify a value greater than 1, to shrink it, we specify a value less than 1:
```css
.shrink:hover
{
  -webkit-transform: scale(0.6);
  -ms-transform: scale(0.6);
  transform: scale(0.6);
}
```

#### **5. Square to circle**

A really popular effect at the moment is transitioning a square element into a round one, and vice versa. With CSS, it’s a simple effect to achieve, we just transition the border-radius property.
- Give your div the class `circle` and add this CSS to your styles:
```css
.circle:hover
{
  border-radius:50%
}
```

#### **6. Swing**

Not all elements use the transition property. We can also create highly complex animations using `@keyframes`, animation and animation-iteration.
In this case, we’ll first define a CSS animation in your styles. You’ll notice that due to implementation issues, we need to use `@-webkit-keyframes` as well as @keyframes (yes, Internet Explorer really is better than Chrome, in this respect at least).

```css
@-webkit-keyframes swing
{
    15%
    {
        -webkit-transform: translateX(5px);
        transform: translateX(5px);
    }
    30%
    {
        -webkit-transform: translateX(-5px);
       transform: translateX(-5px);
    } 
    50%
    {
        -webkit-transform: translateX(3px);
        transform: translateX(3px);
    }
    65%
    {
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
    }
    80%
    {
        -webkit-transform: translateX(2px);
        transform: translateX(2px);
    }
    100%
    {
        -webkit-transform: translateX(0);
        transform: translateX(0);
    }
}
@keyframes swing
{
    15%
    {
        -webkit-transform: translateX(5px);
        transform: translateX(5px);
    }
    30%
    {
        -webkit-transform: translateX(-5px);
        transform: translateX(-5px);
    }
    50%
    {
        -webkit-transform: translateX(3px);
        transform: translateX(3px);
    }
    65%
    {
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
    }
    80%
    {
        -webkit-transform: translateX(2px);
        transform: translateX(2px);
    }
    100%
    {
        -webkit-transform: translateX(0);
        transform: translateX(0);
    }
}
```

This animation simply moves the element left and right, now all we need to do is apply it:
```css
.swing:hover
{
        -webkit-animation: swing 1s ease;
        animation: swing 1s ease;
        -webkit-animation-iteration-count: 1;
        animation-iteration-count: 1;
}
```

- Inset border, is One of the hottest button styles right now is the ghost button; a button with no background and a heavy border. We can of course add a border to an element simply, but that will change the element’s position. We could fix that problem using box sizing, but a far simpler solution is the transition in a border using an inset box shadow.

```css
.border:hover
{
  box-shadow: inset 0 0 0 25px #53a7ea;
}
```