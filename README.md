# Animation-For-Elementor
> CSS Animations Collection with Documentation For website build with Elementor



---

## Animation 1: Glowing Text

**Description:**
Make the text emit a soft glow on hover, giving it a neon-like appearance.

**CSS:**
```css
selector:hover {
  text-shadow: 0 0 10px #00f, 0 0 20px #0ff, 0 0 30px #0f0;
}
```

**Documentation:**
- **Description:** This animation creates a neon-like glow around the text when hovered over.
- **CSS:** The `text-shadow` property applies a series of glowing shadows around the text, creating a soft and colorful glow effect.

---

## Animation 2: Inverted Colors

**Description:**
Invert the colors of the element on hover, creating a negative image effect.

**CSS:**
```css
selector:hover {
  filter: invert(100%);
}
```

**Documentation:**
- **Description:** This animation inverts the colors of the element, producing a negative image effect upon hovering.
- **CSS:** The `filter` property with the `invert` function inverts the colors, creating the negative image appearance.

---

## Animation 3: 3D Cube Rotation

**Description:**
Rotate the element in 3D space on hover, creating the illusion of a rotating cube.

**CSS:**
```css
selector {
  transition: transform 1s ease-in-out;
}

selector:hover {
  transform: rotateX(180deg) rotateY(180deg);
}
```

**Documentation:**
- **Description:** This animation simulates a 3D cube rotation effect on hover.
- **CSS:** Initially, the `transform` property is set to transition smoothly over 1 second. When hovered, the element rotates 180 degrees on both the X and Y axes, creating the illusion of a rotating cube.

---

## Animation 4: Fading Out and Back In

**Description:**
Gradually fade out the element on hover and then fade it back in when the hover state is removed.

**CSS:**
```css
selector {
  transition: opacity 0.5s ease-in-out;
}

selector:hover {
  opacity: 0;
}
```

**Documentation:**
- **Description:** This animation smoothly fades out the element on hover and fades it back in when the hover state is removed.
- **CSS:** The `opacity` property is used to control the element's visibility. It's initially set to transition over 0.5 seconds, and when hovered, the opacity is set to 0 for a fade-out effect.

---

## Animation 5: Trail Effect

**Description:**
Create a trail of semi-transparent copies of the element that follow the mouse cursor on hover.

**CSS:**
```css
selector {
  position: relative;
}

selector:hover::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url("element-image.png");
  opacity: 0.5;
  animation: trail 1s linear infinite;
}

@keyframes trail {
  0% {
    transform: translate(0, 0);
  }
  100% {
    transform: translate(100px, 100px);
  }
}
```

**Documentation:**
- **Description:** This animation creates a trail of semi-transparent copies of the element that follow the mouse cursor on hover.
- **CSS:** The `::before` pseudo-element is used to generate the trail copies. The `animation` property animates the trail's movement, and the trail follows the cursor as it hovers over the element.

---

## Animation 6: Text Typing Animation

**Description:**
Simulate a typing effect on the text, as if it's being typed out letter by letter on hover.

**CSS:**
```css
selector {
  white-space: nowrap;
  overflow: hidden;
  width: 0;
  animation: typing 3s steps(20) forwards;
}

@keyframes typing {
  0% {
    width: 0;
  }
  100% {
    width: 100%;
  }
}
```

**Documentation:**
- **Description:** This animation simulates a typing effect on the text, making it appear as if it's being typed out letter by letter on hover.
- **CSS:** The text's `white-space` is set to `nowrap` to prevent wrapping, and the `overflow` is hidden. The `width` gradually increases as the text appears, simulating typing. The `animation` property controls the typing animation.

---

## Animation 7: Split and Scatter

**Description:**
Split the element into smaller pieces and scatter them in different directions on hover.

**CSS:**
```css
selector {
  position: relative;
  overflow: hidden;
}

selector::before {
  content: "";
  position: absolute;
  background: url("element-image.png");
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transition: transform 1s ease-in-out;
  transform: scale(1, 1);
}

selector:hover::before {
  transform: scale(0.2, 0.2) translate(10%, 10%);
}
```

**Documentation:**
- **Description:** This animation splits the element into smaller pieces and scatters them in different directions on hover.
- **CSS:** The element's `overflow` is set to `hidden`, and a pseudo-element `::before` is used for the animation. The element is initially at its regular size, and on hover, it scales down and translates to create the scattering effect.

---

## Animation 8: Rain Effect

**Description:**
Add a raindrop animation to the element, with raindrops falling and splashing on hover.

**CSS:**
```css
selector {
  position: relative;
}

selector::before {
  content: "";
  position: absolute;
  top: -100px;
  left: 0;
  width: 2px;
  height: 100px;
  background: linear-gradient(to bottom, blue 50%, transparent 50%);
  animation: raindrop 2s linear infinite;
}

@keyframes raindrop {
  0% {
    transform: translate(0, 0);
  }
  100% {


    transform: translate(20px, 100px);
  }
}
```

**Documentation:**
- **Description:** This animation adds a raindrop effect to the element, with raindrops falling and splashing on hover.
- **CSS:** The `::before` pseudo-element is used to create raindrops. The `animation` property controls the raindrop's falling and splashing animation.

---

## Animation 9: Rotating Border

**Description:**
Rotate the element's border on hover, creating a spinning border effect.

**CSS:**
```css
selector {
  border: 2px solid #000;
  transition: border 0.3s ease-in-out;
}

selector:hover {
  border: 2px solid #f00;
  animation: rotateBorder 2s linear infinite;
}

@keyframes rotateBorder {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
```

**Documentation:**
- **Description:** This animation rotates the element's border on hover, creating a spinning border effect.
- **CSS:** The `border` is initially set, and the `transition` property provides a smooth transition. On hover, the border color changes and the `animation` property rotates the border 360 degrees, creating the spinning effect.

---

## Animation 10: Colorful Confetti

**Description:**
Generate a burst of colorful confetti particles around the element on hover.

**CSS:**
```css
selector {
  position: relative;
  overflow: hidden;
}

selector::before {
  content: "";
  position: absolute;
  width: 10px;
  height: 10px;
  background: linear-gradient(to bottom, red, yellow, green, blue, purple);
  animation: confetti 2s linear infinite;
}

@keyframes confetti {
  0% {
    transform: translate(0, 0);
    opacity: 1;
  }
  100% {
    transform: translate(100px, 100px);
    opacity: 0;
  }
}
```

**Documentation:**
- **Description:** This animation generates a burst of colorful confetti particles around the element on hover.
- **CSS:** The `::before` pseudo-element is used to create and animate the confetti particles. They move diagonally and fade out, creating the confetti effect.




---

## Animation 11: Magnetic Attraction

**Description:**
Simulate a magnetic effect using JavaScript to detect cursor position and calculate attractive or repulsive forces between elements. Elements move based on these forces. Cursor proximity is used to adjust element positions.

**JavaScript:**
```javascript
document.addEventListener("mousemove", function(event) {
  const elements = document.querySelectorAll(".magnetic-element");
  const attractionForce = 100; // Adjust this value to control the attraction strength
  const repulsionForce = 200; // Adjust this value to control the repulsion strength

  elements.forEach(function(element) {
    const rect = element.getBoundingClientRect();
    const elementX = rect.left + rect.width / 2;
    const elementY = rect.top + rect.height / 2;

    const cursorX = event.clientX;
    const cursorY = event.clientY;

    const deltaX = cursorX - elementX;
    const deltaY = cursorY - elementY;
    const distance = Math.sqrt(deltaX * deltaX + deltaY * deltaY);

    if (distance < 100) {
      // Apply an attractive force
      element.style.transform = `translate(${deltaX / attractionForce}px, ${deltaY / attractionForce}px)`;
    } else if (distance < 200) {
      // Apply a weaker attractive force
      element.style.transform = `translate(${deltaX / repulsionForce}px, ${deltaY / repulsionForce}px)`;
    } else {
      // No force applied
      element.style.transform = "translate(0, 0)";
    }
  });
});
```

**Documentation:**
- **Description:** This animation simulates a magnetic effect where elements react to the cursor's proximity, moving either towards or away from it.
- **JavaScript:** We detect the cursor's position and calculate the forces acting on each element. When the cursor is close, an attractive force is applied to draw the element towards it, and a weaker attractive force is applied at a moderate distance. Elements remain stationary beyond that.

---

## Animation 12: Particle Animation

**Description:**
Generate a particle system around an element on hover with particles moving in random directions.

**CSS:**
```css
selector:hover:after {
  position: absolute;
  content: '';
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -10;
  pointer-events: none;
  background-image: radial-gradient(circle, #FFF 10%, transparent 10.01%);
  background-repeat: no-repeat;
  background-position: 50%;
  transform: scale(10, 10);
  opacity: 1;
  transition: transform 0.4s, opacity 0.7s;
}

selector:hover:after {
  animation: particles 1s cubic-bezier(0.455, 0.03, 0.515, 0.955) forwards;
}

@keyframes particles {
  0% {
    transform: scale(0);
    opacity: 0.5;
  }
  50% {
    transform: scale(10);
    opacity: 0;
  }
  100% {
    transform: scale(20);
    opacity: 0;
  }
}
```

**Documentation:**
- **Description:** This animation generates a particle system around an element on hover, with particles moving in random directions.
- **CSS:** Using the `::after` pseudo-element, we create the particles. These particles grow in size and fade out during the animation. A cubic-bezier timing function is used for a smoother effect.

---

## Animation 13: Heatmap Effect

**Description:**
Create a heatmap effect by overlaying a semi-transparent gradient background over an element. Use JavaScript to track cursor position and adjust the gradient to simulate changes in color intensity, following the cursor's movement.

**CSS:**
```css
selector {
  position: relative;
}

selector:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: linear-gradient(to bottom, transparent, rgba(0, 0, 0, 0.5));
  pointer-events: none;
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}

selector:hover:before {
  opacity: 1;
}
```

**Documentation:**
- **Description:** This animation creates a heatmap effect by overlaying a semi-transparent gradient background over an element. The gradient's intensity follows the cursor's movement.
- **CSS:** We utilize the `::before` pseudo-element for the gradient. On hover, the gradient's opacity transitions from 0 to 1, creating a smooth fade-in effect.

---

## Animation 14: Fluid Typography

**Description:**
Create fluid typography by changing font-size and letter-spacing properties smoothly using CSS transitions or animations. On hover, modify these properties for a fluid and dynamic effect.

**CSS:**
```css
selector {
  font-size: 16px;
  letter-spacing: 0.05em;
  transition: font-size 0.5s ease-out, letter-spacing 0.5s ease-out;
}

selector:hover {
  font-size: 20px;
  letter-spacing: 0.07em;
  transition: font-size 0.5s ease-out, letter-spacing 0.5s ease-out;
}
```

**Documentation:**
- **Description:** This animation creates fluid typography by smoothly changing the font size and letter spacing using CSS transitions.
- **CSS:** Initial font size and letter spacing are set, and on hover, these properties are adjusted for a fluid and dynamic effect.



---

## Animation 15: Glowing Text

**Description:**
Make the text emit a soft glow on hover, giving it a neon-like appearance.

**CSS:**
```css
selector:hover {
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
}
```

**Documentation:**
- **Description:** This animation creates a soft glow effect on text when hovered over, giving it a neon-like appearance.
- **CSS:** The `text-shadow` property is used to add a white-colored, blurred glow to the text when the selector is hovered.

---

## Animation 16: Inverted Colors

**Description:**
Invert the colors of the element on hover, creating a negative image effect.

**CSS:**
```css
selector:hover {
  filter: invert(100%);
}
```

**Documentation:**
- **Description:** This animation inverts the colors of the element on hover, creating a negative image effect.
- **CSS:** The `filter` property with the `invert` function is used to invert the colors completely when the selector is hovered.

---

## Animation 17: 3D Cube Rotation

**Description:**
Rotate the element in 3D space on hover, creating the illusion of a rotating cube.

**CSS:**
```css
selector:hover {
  transform: rotateX(180deg) rotateY(180deg);
  transition: transform 1s;
}
```

**Documentation:**
- **Description:** This animation creates the illusion of a rotating 3D cube by rotating the element in 3D space when hovered over.
- **CSS:** The `transform` property is used to apply 3D rotations around the X and Y axes. The `transition` property adds a smooth animation effect.

---

## Animation 18: Fading Out and Back In

**Description:**
Gradually fade out the element on hover and then fade it back in when the hover state is removed.

**CSS:**
```css
selector {
  transition: opacity 0.3s;
}

selector:hover {
  opacity: 0;
}

selector:not(:hover) {
  opacity: 1;
}
```

**Documentation:**
- **Description:** This animation gradually fades out the element when hovered over and fades it back in when the hover state is removed.
- **CSS:** We apply transitions to the `opacity` property for smooth fading. On hover, the opacity is set to 0, and when not hovered, the opacity is set to 1.

---

## Animation 19: Trail Effect

**Description:**
Create a trail of semi-transparent copies of the element that follow the mouse cursor on hover.

**CSS:**
```css
selector {
  pointer-events: none;
}

selector:hover::after {
  content: "";
  position: absolute;
  background-color: rgba(0, 0, 0, 0.1);
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  animation: follow-cursor 2s linear infinite;
}

@keyframes follow-cursor {
  from {
    transform: translate(0, 0);
  }
  to {
    transform: translate(100%, 100%);
  }
}
```

**Documentation:**
- **Description:** This animation creates a trail effect by generating semi-transparent copies of the element that follow the mouse cursor when hovered over.
- **CSS:** The `::after` pseudo-element is used to create the trail elements. The `follow-cursor` animation moves the trail copies from their initial position to a final position, creating the trail effect.

---

## Animation 20: Text Typing Animation

**Description:**
Simulate a typing effect on the text, as if it's being typed out letter by letter on hover.

**CSS:**
```css
selector::before {
  content: "";
  display: block;
  width: 0;
  overflow: hidden;
  white-space: nowrap;
  animation: type-text 3s steps(20) forwards;
}

@keyframes type-text {
  to {
    width: 100%;
  }
}
```

**Documentation:**
- **Description:** This animation simulates a typing effect on the text, making it appear as if it's being typed out letter by letter when hovered over.
- **CSS:** A pseudo-element `::before` is used to generate the text typing animation. The `type-text` animation gradually increases the width of the element to reveal the text.

---

## Animation 21: Split and Scatter

**Description:**
Split the element into smaller pieces and scatter them in different directions on hover.

**CSS:**
```css
selector:hover {
  display: inline-block;
  position: relative;
  color: transparent;
}

selector:hover::before {
  content: "Your text here";
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  color: #000; /* Set your desired text color */
  animation: split-scatter 1s both;
}

@keyframes split-scatter {
  to {
    top: -10px;
    left: -10px;
  }
}
```

**Documentation:**
- **Description:** This animation splits the element into smaller pieces and scatters them in different directions when hovered over.
- **CSS:** The element is set to `display: inline-block`, and a pseudo-element `::before` reveals the text with a specific color. The `split-scatter` animation moves the text to create the split and scatter effect.

---

## Animation 22: Rain Effect

**Description:**
Add a raindrop animation to the element, with raindrops falling and splashing on hover.

**CSS:**
```css
selector:hover {
  overflow: hidden;
  position: relative;
}

selector:hover::before {
  content: "";
  position: absolute;
  background: transparent;
  width: 2px;
  height: 50px;
  top: -50px;
  left: 50%;
  animation: raindrop 1s infinite linear, splash 0.5s ease-in-out 1;
}

@keyframes raindrop {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(50px);
  }
}

@keyframes splash {
  0% {
    height: 50px;
  }
  100% {
    height: 0;
  }
}
```

**Documentation:**
- **Description:** This animation adds a raindrop effect to the element, with raindrops falling and splashing on hover.
- **CSS:** The `::before` pseudo-element is used to create the raindrops. The `raindrop` animation moves the raindrop from left to right, while the `splash` animation simulates the raindrop's splash.

---

## Animation 23: Rotating Border

**Description:**
Rotate the element's border on hover, creating a spinning border effect.

**CSS:**
```css
selector:hover {
  animation: rotate-border 2s linear infinite;
}

@keyframes rotate-border {
  from {
    border-width: 2px;
    transform: rotate(0deg);
  }
  to {
    border-width: 5

px;
    transform: rotate(360deg);
  }
}
```

**Documentation:**
- **Description:** This animation rotates the element's border on hover, creating a spinning border effect.
- **CSS:** The `rotate-border` animation increases the border width and applies a 360-degree rotation to achieve the spinning border effect when the selector is hovered over.

---

## Animation 24: Colorful Confetti

**Description:**
Generate a burst of colorful confetti particles around the element on hover.

**CSS:**
```css
selector {
  position: relative;
}

selector::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  pointer-events: none;
  background-image: linear-gradient(135deg, #f06, #9f6 25%, #09f 25%, #09f 50%, #f06 50%, #f06 75%, #9f6 75%, #9f6);
  background-size: 32px 32px;
  width: 100%;
  height: 100%;
  animation: confetti 2s linear forwards;
}

@keyframes confetti {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
```

**Documentation:**
- **Description:** This animation generates a burst of colorful confetti particles around the element when hovered over.
- **CSS:** A `::before` pseudo-element is used to create the confetti effect. The `confetti` animation applies a 360-degree rotation to the confetti particles, creating a colorful burst.


---

## Animation 25: Text Stacking

**Description:**
On hover, make the text characters stack on top of each other, creating a 3D effect.

**CSS:**
```css
selector:hover {
  transform: translateZ(5px);
  transition: transform 0.3s;
}
```

**Documentation:**
- **Description:** This animation stacks the text characters on top of each other to create a 3D effect when hovered over.
- **CSS:** The `transform` property is used to apply a translation along the Z-axis, creating the stacking effect with a slight hover animation.

---

## Animation 26: Neon Glow

**Description:**
Add a neon glow effect to the text or element on hover, making it appear as if it's illuminated.

**CSS:**
```css
selector:hover {
  text-shadow: 0 0 10px rgba(255, 0, 0, 0.8);
}
```

**Documentation:**
- **Description:** This animation adds a neon glow effect to the text or element, making it appear as if it's illuminated when hovered over.
- **CSS:** The `text-shadow` property is used to create a red-colored, blurred glow to achieve the neon effect.

---

## Animation 27: Rotation with Trails

**Description:**
Rotate the element on hover while leaving a trail of semi-transparent copies behind, creating a mesmerizing effect.

**CSS:**
```css
selector:hover {
  animation: rotate-with-trails 2s linear infinite;
}

@keyframes rotate-with-trails {
  from {
    transform: rotate(0);
    opacity: 1;
  }
  to {
    transform: rotate(360deg);
    opacity: 0;
  }
}
```

**Documentation:**
- **Description:** This animation rotates the element on hover while leaving a trail of semi-transparent copies behind, creating a mesmerizing effect.
- **CSS:** The `rotate-with-trails` animation applies a 360-degree rotation to the element, gradually decreasing opacity to create the trail effect.

---

## Animation 28: Text Reveal

**Description:**
Reveal the text or element gradually from left to right on hover, as if it's being written or drawn.

**CSS:**
```css
selector::before {
  content: '';
  display: block;
  width: 0;
  overflow: hidden;
  white-space: nowrap;
  animation: text-reveal 1s steps(30) forwards;
}

@keyframes text-reveal {
  to {
    width: 100%;
  }
}
```

**Documentation:**
- **Description:** This animation gradually reveals the text from left to right on hover, as if it's being written or drawn.
- **CSS:** A pseudo-element `::before` is used to create the text reveal effect. The `text-reveal` animation gradually increases the width of the element to reveal the text.

---

## Animation 29: Bouncing Element

**Description:**
Make the element bounce up and down in a continuous loop when hovered over.

**CSS:**
```css
selector:hover {
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-20px);
  }
}
```

**Documentation:**
- **Description:** This animation makes the element bounce up and down in a continuous loop when hovered over.
- **CSS:** The `bounce` animation applies vertical translation to create the bouncing effect.

---

## Animation 30: Colorful Confetti

**Description:**
Scatter colorful confetti particles around the element on hover, with particles falling and disappearing.

**CSS:**
```css
selector {
  position: relative;
}

selector::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  pointer-events: none;
  background-image: linear-gradient(135deg, #f06, #9f6 25%, #09f 25%, #09f 50%, #f06 50%, #f06 75%, #9f6 75%, #9f6);
  background-size: 32px 32px;
  width: 100%;
  height: 100%;
  animation: confetti 2s linear forwards;
}

@keyframes confetti {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
```

**Documentation:**
- **Description:** This animation scatters colorful confetti particles around the element on hover, with particles falling and disappearing.
- **CSS:** A `::before` pseudo-element is used to create the confetti effect. The `confetti` animation applies a 360-degree rotation to the confetti particles, creating a colorful burst.

---

## Animation 31: Growing Vines

**Description:**
Create animated vines or branches that grow out from the element on hover, adding an organic feel.

**CSS:**
```css
selector:hover {
  position: relative;
}

selector::before {
  content: '';
  position: absolute;
  top: 100%;
  left: 50%;
  width: 2px;
  height: 0;
  background: green; /* Set your desired vine color */
  animation: grow-vines 2s ease-in-out forwards;
}

@keyframes grow-vines {
  to {
    top: 0;
    height: 100%;
  }
}
```

**Documentation:**
- **Description:** This animation creates animated vines or branches that grow out from the element on hover, adding an organic feel.
- **CSS:** The `::before` pseudo-element is used to generate the vines. The `grow-vines` animation increases the height of the vines, making them grow from the bottom of the element.

---

## Animation 32: Blur and Unblur

**Description:**
Apply a blur effect to the element on hover, then gradually remove the blur for a focus effect.

**CSS:**
```css
selector:hover {
  filter: blur(5px);
  transition: filter 0.3s;
}

selector:not(:hover) {
  filter: blur(0);
}
```

**Documentation:**
- **Description:** This animation applies a blur effect to the element on hover and gradually removes the blur for a focus effect when the hover state is removed.
- **CSS:** The `filter` property is used to apply the blur effect. The `transition` property adds a smooth transition for the blur. When not hovered, the blur is removed.

---

## Animation 33: Text Typing Animation

**Description:**
Simulate a typing animation on the text, as if it's being typed out letter by letter, on hover.

**CSS:**
```css
selector::before {
  content: '';
  display: block;
  width: 0;
  overflow: hidden;
  white-space: nowrap;
  animation: typing-animation 2s steps(20) forwards;
}

@keyframes typing-animation {
  to {
    width: 100%;
  }
}
```

**Documentation:**
- **Description:** This animation simulates a typing effect on the text, making it appear as

 if it's being typed out letter by letter on hover.
- **CSS:** A pseudo-element `::before` is used to create the typing effect. The `typing-animation` gradually increases the width of the element to simulate typing.

---

## Animation 34: Rippling Waves

**Description:**
Add a ripple effect to the background of the element on hover, resembling waves in water.

**CSS:**
```css
selector {
  position: relative;
}

selector::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle, transparent 10%, rgba(0, 0, 255, 0.5) 10.01%);
  background-repeat: no-repeat;
  background-position: 50%;
  transform: scale(0);
  animation: ripple 0.5s ease-in-out forwards;
}

@keyframes ripple {
  to {
    transform: scale(2);
    opacity: 0;
  }
}
```

**Documentation:**
- **Description:** This animation adds a ripple effect to the background of the element on hover, resembling waves in water.
- **CSS:** A `::before` pseudo-element is used to create the ripple effect. The `ripple` animation scales the element while reducing opacity to create the ripple effect.

---

## Animation 35: Spotlight Effect

**Description:**
Add a spotlight that follows the mouse cursor and illuminates the element on hover.

**CSS:**
```css
selector::before {
  content: '';
  position: absolute;
  background: radial-gradient(circle, transparent 60%, rgba(255, 255, 255, 0.7) 61%);
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  transform: translate(-50%, -50%);
  animation: spotlight 1s infinite;
}

@keyframes spotlight {
  from {
    top: 0;
    left: 0;
  }
  to {
    top: 100%;
    left: 100%;
  }
}
```

**Documentation:**
- **Description:** This animation adds a spotlight that follows the mouse cursor and illuminates the element on hover.
- **CSS:** A `::before` pseudo-element creates the spotlight. The `spotlight` animation moves the spotlight from the top-left corner to the bottom-right corner, creating the effect of a moving spotlight.

---

## Animation 36: Rotating Text Path

**Description:**
Make the text follow a curved path and rotate along it on hover, creating an interesting motion effect.

**CSS:**
```css
selector:hover {
  animation: rotate-text-path 2s linear infinite;
}

@keyframes rotate-text-path {
  0% {
    transform: rotate(0deg) translateX(0);
  }
  100% {
    transform: rotate(360deg) translateX(100px);
  }
}
```

**Documentation:**
- **Description:** This animation makes the text follow a curved path and rotate along it on hover, creating an interesting motion effect.
- **CSS:** The `rotate-text-path` animation combines a 360-degree rotation with horizontal translation to achieve the desired effect.

---

## Animation 37: Stretch and Squash

**Description:**
Stretch the element horizontally and squash it vertically on hover, then return to its original shape.

**CSS:**
```css
selector:hover {
  transform: scaleX(1.2) scaleY(0.8);
  transition: transform 0.3s;
}

selector:not(:hover) {
  transform: scaleX(1) scaleY(1);
  transition: transform 0.3s;
}
```

**Documentation:**
- **Description:** This animation stretches the element horizontally and squashes it vertically on hover, then returns it to its original shape when the hover state is removed.
- **CSS:** The `transform` property is used to adjust the scale of the element for both horizontal (`scaleX`) and vertical (`scaleY`) stretching.

---

## Animation 38: Color Gradient Animation

**Description:**
Animate the background with a gradient that shifts colors smoothly on hover.

**CSS:**
```css
selector:hover {
  background-image: linear-gradient(45deg, #FF5733, #99CC33, #33B5E5);
  background-size: 200% 200%;
  animation: gradient-animation 3s infinite;
}

@keyframes gradient-animation {
  0% {
    background-position: 0 100%;
  }
  100% {
    background-position: 100% 0;
  }
}
```

**Documentation:**
- **Description:** This animation animates the background with a gradient that smoothly shifts colors on hover.
- **CSS:** The `background-image` property is used to set a linear gradient. The `gradient-animation` animation shifts the background position to create a color animation effect.

---

## Animation 39: Sparkling Stars

**Description:**
Generate twinkling stars around the element on hover, as if it's in the night sky.

**CSS:**
```css
selector:hover {
  position: relative;
}

selector::before {
  content: "★";
  position: absolute;
  color: #FFD700; /* Set your desired star color */
  animation: twinkling 3s infinite;
}

@keyframes twinkling {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```

**Documentation:**
- **Description:** This animation generates twinkling stars around the element on hover, creating the illusion of a night sky.
- **CSS:** The `::before` pseudo-element is used to create stars. The `twinkling` animation controls the opacity to create the twinkling effect.

---

## Animation 40: Shadow Dance

**Description:**
Create a dynamic shadow that moves and changes shape with the element on hover.

**CSS:**
```css
selector:hover {
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.7);
  transition: box-shadow 0.5s;
}

selector:not(:hover) {
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
  transition: box-shadow 0.5s;
}
```

**Documentation:**
- **Description:** This animation creates a dynamic shadow that moves and changes shape with the element on hover.
- **CSS:** The `box-shadow` property is used to create the shadow effect, and it transitions between two shadow states when hovering and not hovering.

---

## Animation 41: Mirror Reflection

**Description:**
Add a reflective surface below the element, and on hover, simulate a reflection that moves with the element.

**CSS:**
```css
selector {
  position: relative;
}

selector::before {
  content: '';
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  height: 20px;
  background: linear-gradient(transparent 5%, rgba(255, 255, 255, 0.7) 6%);
}

selector:hover::before {
  animation: move-reflection 1s linear infinite;
}

@keyframes move-reflection {
  to {
    transform: translate(0, -100%);
  }
}
```

**Documentation:**
- **Description:** This animation adds a reflective surface below the element and simulates a reflection that moves with the element on hover.
- **CSS:** The `::before` pseudo-element creates the reflective surface. The `move-reflection` animation translates the reflection vertically to create the effect of movement.

---

## Animation 42: Spiral Spin

**Description:**
Make the element spin in a spiral motion, either clockwise or counterclockwise, on hover.

**CSS:**
```css
selector:hover {
  animation: spiral-spin 3s linear infinite;
}

@keyframes spiral-spin {
  0% {
    transform: rotate(0) translate(0);
  }
  100% {
    transform: rotate(360deg) translate(50px);
  }
}
```

**Documentation:**
- **Description:** This animation makes the element spin in a spiral motion, either clockwise or counterclockwise, on hover.
- **CSS:** The `spiral-spin` animation combines a 360-degree rotation with horizontal translation to achieve the spiral effect.


---

## Animation 43: Morphing Text

**Description:**
Transform the text into a different word or shape on hover and back to its original form when the hover state is removed.

**CSS:**
```css
selector {
  transition: transform 0.5s;
}

selector:hover {
  transform: rotate(90deg) scale(0.5);
}
```

**Documentation:**
- **Description:** This animation transforms the text into a different word or shape on hover and reverts to its original form when the hover state is removed.
- **CSS:** The `transform` property is used to rotate and scale the element on hover, achieving the morphing effect.

---

## Animation 44: Elastic Deformation

**Description:**
On hover, make the element stretch and deform as if it's made of elastic material, and then return to its original shape.

**CSS:**
```css
selector {
  transition: transform 0.5s;
}

selector:hover {
  transform: scaleX(1.5) scaleY(0.7);
}
```

**Documentation:**
- **Description:** This animation makes the element stretch and deform on hover as if it's made of elastic material, returning to its original shape when the hover state is removed.
- **CSS:** The `transform` property is used to scale the element differently along the X and Y axes on hover, creating an elastic deformation effect.

---

## Animation 45: Lens Distortion

**Description:**
Apply a lens distortion effect to the element on hover, creating a magnifying glass effect.

**CSS:**
```css
selector {
  transition: transform 0.5s;
}

selector:hover {
  transform: scale(2);
}
```

**Documentation:**
- **Description:** This animation applies a lens distortion effect to the element on hover, creating a magnifying glass effect.
- **CSS:** The `transform` property is used to scale the element on hover, making it appear as if it's magnified through a lens.

---

## Animation 46: Synchronized Movement

**Description:**
Link the movement of multiple elements so that they move in sync with each other on hover.

**CSS:**
```css
parent-selector:hover > selector {
  transition: transform 0.5s;
  transform: translateX(20px);
}
```

**Documentation:**
- **Description:** This animation links the movement of multiple child elements to their parent so they move in sync with each other on hover.
- **CSS:** The `parent-selector:hover > selector` selector is used to apply the animation to the child elements when the parent is hovered. The `transform` property translates the elements horizontally.

---

## Animation 47: Retro TV Glitch

**Description:**
Simulate a glitch effect on the element, reminiscent of old TV screens malfunctioning, on hover.

**CSS:**
```css
selector:hover {
  animation: tv-glitch 0.2s infinite;
}

@keyframes tv-glitch {
  0% {
    transform: translate(-2px, -2px);
  }
  1% {
    transform: translate(2px, -2px);
  }
  2% {
    transform: translate(-2px, 2px);
  }
  3% {
    transform: translate(2px, 2px);
  }
  4% {
    transform: translate(0, 0);
  }
}
```

**Documentation:**
- **Description:** This animation simulates a glitch effect on the element, reminiscent of old TV screens malfunctioning, on hover.
- **CSS:** The `tv-glitch` animation creates a series of translations to move the element slightly in different directions, creating the glitch effect.

---

## Animation 48: Morse Code

**Description:**
Encode a message in Morse code and have the element flash it out in dots and dashes on hover.

**CSS:**
```css
selector::before {
  content: ".... --- .-.. .-.. ---";
  visibility: hidden;
  animation: morse-code 3s steps(10) infinite;
}

@keyframes morse-code {
  0%, 100% {
    visibility: hidden;
  }
  50% {
    visibility: visible;
  }
}
```

**Documentation:**
- **Description:** This animation encodes a message in Morse code and has the element flash it out in dots and dashes on hover.
- **CSS:** The `::before` pseudo-element content is set to the Morse code message. The `morse-code` animation alternates between hiding and showing the content to create the Morse code effect.

---

## Animation 49: Pixelation

**Description:**
Pixelate the element on hover, making it appear as if it's composed of pixel blocks, and then return it to its original state.

**CSS:**
```css
selector {
  transition: filter 0.3s;
}

selector:hover {
  filter: contrast(2) grayscale(1) blur(4px);
}
```

**Documentation:**
- **Description:** This animation pixelates the element on hover, making it appear as if it's composed of pixel blocks, and then returns it to its original state.
- **CSS:** The `filter` property is used to adjust the contrast, grayscale, and blur on hover, creating the pixelation effect.

---

## Animation 50: X-Ray Vision

**Description:**
Create an X-ray effect that allows users to see through the element to reveal a hidden layer or content on hover.

**CSS:**
```css
selector {
  background-color: rgba(0, 0, 0, 0);
  transition: background-color 0.3s;
}

selector:hover {
  background-color: rgba(0, 0, 0, 0.5);
}
```

**Documentation:**
- **Description:** This animation creates an X-ray effect that allows users to see through the element to reveal a hidden layer or content on hover.
- **CSS:** The `background-color` property is adjusted to control the opacity of the element, making it transparent on hover.


---

## Animation 51: Sticky Effect

**Description:**
Make the element "stick" to the cursor, following it around as the cursor moves, on hover.

**CSS:**
```css
selector {
  position: absolute;
  transition: transform 0.1s;
}

selector:hover {
  transform: translate(-50%, -50%);
}
```

**Documentation:**
- **Description:** This animation makes the element "stick" to the cursor, following it around as the cursor moves, on hover.
- **CSS:** The element is positioned absolutely, and its `transform` property is adjusted to move it according to the cursor's position.

---

## Animation 52: Liquid Ripple

**Description:**
Apply a liquid ripple effect to the element, as if it's submerged in water, on hover.

**CSS:**
```css
selector {
  transition: transform 0.3s ease-in-out, box-shadow 0.5s;
}

selector:hover {
  transform: scale(1.05);
  box-shadow: 0 0 20px rgba(0, 0, 255, 0.7);
}
```

**Documentation:**
- **Description:** This animation applies a liquid ripple effect to the element, as if it's submerged in water, on hover.
- **CSS:** The `transform` property scales the element, creating a ripple effect, and a `box-shadow` is added to simulate a water-like reflection.

---

## Animation 53: Lightning Strike

**Description:**
Simulate a lightning strike effect that illuminates the element and its surroundings on hover.

**CSS:**
```css
selector {
  background-color: #000;
  transition: background-color 0.3s;
}

selector:hover {
  background-color: #f2f2f2;
}
```

**Documentation:**
- **Description:** This animation simulates a lightning strike effect that illuminates the element and its surroundings on hover.
- **CSS:** The `background-color` is adjusted to change the element's color, creating the illusion of a lightning strike illuminating it.

---


