# Animation

## CSS properties

- transform (rotate, translate, scale)
- transition (transition property, timing-function, duration, etc.)
- animation (animation frame name, timing-function, duration, etc.)
- @keyframes (keyframes name is passed to the animation property)
  https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes

# requestAnimationFrame

This method tells the browser to request an animation (invoke callback) before the next repaint.
The number of callbacks is usually 60 times per second, but will generally match the display refresh rate in most web browsers as per W3C recommendation.

`requestAnimationFrame` callback accept only one argument, a timestamp.
The timestamp represents the beginning of the main thread frame that we’re currently in. This means that multiple different requestAnimationFrame callbacks can get back the exact same timestamp.

https://developer.mozilla.org/en-US/docs/Web/API/window/requestAnimationFrame
