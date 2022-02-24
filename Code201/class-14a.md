# Reading Assignment 14a

## Transforms

---

- When CSS3 was introduced, there were new ways to position and alter content, one of which was the ways to size, position, and change the elemnts with the `transform` property.
- The `transform` property has two sets of properties and values, one for two-dimnsional and another for three-dimensional.
- The syntax for the property is simple, it's just the transform property followed by the value with the value specifying the type and the specific amount of change in parentheses.
- For 2D transforms, the elements may be distorted on a two dimensional plane, vertically and/or horizontally. The types of 2D transforms are;
  - `Rotate`
  - `Scale`
  - `Translate`
  - `Skew`
- It is common to combine multiple transforms together, rotating and scaling the size at the same time for example.
  - To combine multiple transforms you list the values within the `transform` in sequence without commas.
- In 3D transforms the third dimension is the z-axis or depth. The types of 3D transform are the same as 2D but also on the z-axis.

## Transitions & Animations

---

- Another advancement with CSS3 is the ability to have transitions and animations.
- Transitions alter the appearance and behavior of an element when the state changes such as hovering over it, it is focused on, it being targeted, etc.
- Animations allow elements to have the appearence and behavior be altered in multiple keyframes.

- For a transition to take place, the state of the element must have a state change and the different styles must be identified for each state.
  - The easiest way to determine the style for different states is with the `hover`, `focus`, `active` and `target` pseudo-classes.
  - For a property to be transitioned they must have an identifiable midway point between the changes. For example, the display property can't be transitioned because it doesn't have a midpoint like color or font size.
  - The duration of the transition is set with the `transition-duration` property.
  - The timing of the transition is set with the `transition-timing-function` property.
- When you need more control over the visual interaction than the single state changes of transitions, you use animations.
  - To set the miltiple points of transition, you use the `@keyframes` rule with the animation name, the breakpoints and the properties to be animated.
  - Animations also have duration, timing and delay if wanted.
  - To start, all animations need a duration and as with the transitions the duration may be set in seconds or milliseconds.
  - Animations also have the ability to further customize an elements behavior such as the ability to declare the number of times an animation runs as well as the direction the animation completes.
  - Eight common and cool transitions are;
    - Fade in
    - Change the color
    - Grow and shrink the element
    - Rotate the element
    - Make a square into a circle
    - Add a 3D shadow
    - Swing the element(Move it left and right)
    - Inset border
