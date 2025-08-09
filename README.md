# Animate — Animated Website Demo (HTML • CSS • JS)

A visually engaging, accessible, and performant demo showcasing modern UI animations using pure HTML, CSS, and vanilla JavaScript. Includes animated gradient backgrounds, reveal-on-scroll effects, 3D hover tilts, interactive controls, and responsive accessibility.

##  Features

- **Animated gradient background**  
  Smooth, continuous color transitions via CSS `@keyframes`.

- **Floating blurred blobs**  
  Adds visual depth and dynamic background layers.

- **Responsive, accessible navigation**  
  Clean desktop navigation with a keyboard-accessible mobile menu toggle.

- **Hero section**  
  Includes animated headings, lift-on-focus search input, and a demo button with parallax-style animation.

- **Reveal-on-scroll animations**  
  Elements fade and slide into view using `IntersectionObserver`.

- **3D interactive cards**  
  Hover-induced tilt effect with perspective and smooth scaling, plus fallback for keyboard focus.

- **Subtle UI transitions**  
  Buttons and inputs gently elevate on hover/focus for tactile feedback.

### CSS Highlights
- CSS Variables : Define theme colors (--accent-1, --accent-2, etc.) and timing (--ease) for easy customization.

- Animated Gradient Background : CSS animation (@keyframes gradientShift) creates a flowing, dynamic backdrop.

- Floating Blobs : Blurred, semi-transparent circles for depth and visual interest.

- Reveal Animations : Elements marked with .reveal start hidden and animate into place once scrolled into view by toggling .in-view.

- Card Hover Effects : Cards use CSS transitions for elevation and scaling on hover and focus.

## JavaScript Functionality
- IntersectionObserver for reveal-on-scroll : Observes .reveal elements and applies .in-view when they enter the viewport.

- 3D Card Tilt Effect : On mousemove, compute relative cursor position and apply rotateX/rotateY transforms with perspective. On mouseleave, resets transform. On keyboard focus (:focus), applies simplified elevation.

- Debounce Utility : Simple utility to throttle frequent event handlers (e.g., mousemove) for performance.

- Mobile Menu Toggle : Accessible toggle button to show/hide navigation on small screens.

- “Demo” Button Animation : Plays a subtle lift-and-shadow animation on a poster element when clicked.

## Accessibility & Performance
- Keyboard navigable: Cards are focusable (via tabindex="0"), and all interactive elements include visible focus styles.

- Reduced motion friendly: Animations are smooth and subtle. Can be extended with prefers-reduced-motion media query for motion-sensitive users.

- Efficient scroll handling: Uses IntersectionObserver, which is far more performant than scroll event listeners.
