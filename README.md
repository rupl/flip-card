# Polymer element for CSS 3D flip cards

Have you ever built [CSS 3D flip cards](http://css3playground.com/3d-flip-cards/)? If you found the process tedious, perhaps this is the solution. Using [Polymer](http://www.polymer-project.org/), this demo shows how creating flip cards can be as simple as:

```html
<flip-card>
  <front>Flip me</front>
  <back>You flipped me</back>
</flip-card>
```

You can put whatever markup you want inside the `<front>` and `<back>` tags.

**Advanced Example:**

```html
<flip-card axis="x" nohover flipped="{{flipped}}">
  <front>Front of card</front>
  <back>Back of card</back>
</flip-card>
<input type="checkbox" checked="{{flipped::changed}}">flip

<script>
  // Just flip
  document.querySelector('flip-card').toggle();
  // show the back
  document.querySelector('flip-card').showBack();
  // show the front
  document.querySelector('flip-card').showFront();
  
  // will reveal the back side (my-element child polymer element)
  document.querySelector('my-element').fire('show'); 
</script>
```

## Options

`axis`:

* `y` axis is what you typically see. It flips left to right. The `<flip-card>` defaults to Y if you omit the attribute.
* `x` axis means it turns upside-down while it flips.

`noHover`: 

To disable the auotomatic flipping on mouseover add the `noHover` attribute. The card can be flipped using either one of the methods below, data-binding or firing an event.


## Methods

* `showBack` shows the backside
* `showFront` shows the frontside
* `toggle` flips the card


## Properties

* `flipped`: A boolean flag that specifies if the card is flipped or not

## Events
* `show`: If this event is fired by a child element inside the `back` or `front` it will reveal the corresponding side
* `flipend`: Is fired when the flipping animation is finished.

## Ideas for future options

* ~~`stick` attribute means you click on them to interact instead of hovering. They stay put after you click.~~ (done by `noHover` attribute)
* `direction` attribute allows you to flip one way or the other. Think **clockwise** vs **counter-clockwise**.
* `origin` attribute lets you specify a CSS transform-origin, meaning the card can appear to be hinged from one side.

## Performance

It should go without saying, but a plain CSS implementation of this is much more lightweight than using Polymer. I made this in order to learn about Polymer and Web Components. So there you have it.

## Demo

[Clicky clicky](http://rupl.github.io/flip-card/)
