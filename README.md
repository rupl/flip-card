# Polymer element for CSS 3D flip cards

Have you ever built [CSS 3D flip cards](http://css3playground.com/3d-flip-cards/)? If you found the process tedious, perhaps this is the solution. Using [Polymer](http://www.polymer-project.org/), this demo shows how creating flip cards can be as simple as:

```html
<flip-card>
  <front>Flip me</front>
  <back>You flipped me</back>
</flip-card>
```

You can put whatever markup you want inside the `<front>` and `<back>` tags.

## Options

Currently, the only attribute it takes is `axis`.

* `y` axis is what you typically see. It flips left to right. The `<flip-card>` defaults to Y if you omit the attribute.
* `x` axis means it turns upside-down while it flips.

## Ideas for future options

* `stick` attribute means you click on them to interact instead of hovering. They stay put after you click.
* `direction` attribute allows you to flip one way or the other. Think **clockwise** vs **counter-clockwise**.
* `origin` attribute lets you specify a CSS transform-origin, meaning the card can appear to be hinged from one side.

## Performance

It should go without saying, but a plain CSS implementation of this is much more lightweight than using Polymer. I made this in order to learn about Polymer and Web Components. So there you have it.

## Demo

[Clicky clicky](http://rupl.github.io/flip-card/)
