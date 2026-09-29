# Floating Balloon Popups

An interactive JavaScript animation where colorful balloons float upward and burst when clicked, tapped, or when they automatically reach their destination. Each balloon reveals an animated information card after popping.

Built with **HTML, CSS, SVG, Vanilla JavaScript, and GSAP**.

## Demo

**Live Demo:**
https://aminulsarkar.com/floating-balloon-popups/

**Repository:**
https://github.com/aminulsarkar/floating-balloon-popups

---

## Preview

The application creates floating balloons dynamically using SVG.

Users can:

* Click a balloon to pop it
* Tap a balloon on mobile devices
* Allow balloons to automatically float and burst
* View a contextual information card after a balloon bursts
* Close the information card manually
* See animated burst particles
* Experience responsive positioning near the edges of the screen

---

## Features

### Interactive Floating Balloons

Balloons are generated dynamically with JavaScript and positioned randomly across the screen.

### SVG-Based Balloon Graphics

Each balloon is constructed programmatically using SVG elements, including:

* Ellipse balloon body
* Radial gradient
* Highlight effect
* Knot
* Balloon string

This avoids the need for separate balloon image assets.

### Randomized Appearance

Each balloon receives:

* A random hue
* A randomized scale
* A randomized horizontal starting position
* Random horizontal drifting

This creates a more natural floating effect.

### Click and Touch Interaction

Balloons can be popped using:

* Mouse click
* Mobile touch

The interaction is designed to work across desktop and mobile devices.

### Automatic Balloon Bursting

Balloons automatically float upward and burst after completing their animation.

Users can also manually trigger the same burst interaction by clicking or tapping a balloon.

### Animated Burst Particles

When a balloon bursts, SVG particles are generated around the balloon's position and animated outward using GSAP.

### Animated Information Cards

After a balloon pops, a contextual information card appears at the burst location.

The card includes:

* Title
* List of information
* Optional CTA
* Close button
* Entrance animation
* Automatic dismissal

### Responsive Positioning

Information cards are automatically repositioned when a balloon bursts near the edge of the viewport to reduce the possibility of the card being cut off.

### GSAP Animations

GSAP handles the major animations, including:

* Balloon movement
* Balloon bursting
* Particle animation
* Card entrance
* Card content animation
* Card dismissal

---

## Technologies

* HTML5
* CSS3
* JavaScript
* SVG
* GSAP
* Google Fonts

### Main Animation Library

[GSAP](https://gsap.com/)

---

## How It Works

The application follows a simple interaction flow:

```text
Create balloon
      ↓
Randomize color, size and position
      ↓
Animate balloon upward
      ↓
User clicks/taps balloon
      OR
Balloon reaches destination
      ↓
Balloon bursts
      ↓
Burst particles animate outward
      ↓
Information card appears
      ↓
Card automatically disappears
      OR
User closes the card
```

---

## Project Structure

```text
floating-balloon-popups/
│
├── index.html
│
├── css/
│   ├── style.css
│
├── js/
│   └── balloon-popups.js
│
│
├── README.md
├── LICENSE
└── PROJECT.txt
```

> The balloon interaction itself can be separated into its own JavaScript file for a cleaner standalone implementation.

---

## Customizing the Content

The balloon content is controlled through the `data` array in the JavaScript.

Example:

```javascript
const data = [
  {
    title: "There is so much to love!",
    items: [
      "Music and more music throughout the day",
      "Food trucks + Craft beer + Wine",
      "A laser light show",
      "A spectacular hologram display"
    ]
  },
  {
    title: "Bring the whole family!",
    items: [
      "Superhero meet and greets",
      "Bounce zone",
      "Family lawn"
    ]
  }
];
```

You can replace the titles and content with your own information without changing the animation logic.

---

## Customizing Balloon Colors

Balloon colors are generated dynamically using HSL colors.

```javascript
const hue = Math.floor(Math.random() * 360);
```

This allows each balloon to have a different color.

You can replace the random hue with a fixed value if you want to use a specific brand color.

---

## Customizing Animation Speed

The balloon's floating duration can be adjusted here:

```javascript
duration: gsap.utils.random(8.5, 10.5)
```

For faster balloons:

```javascript
duration: gsap.utils.random(5, 7)
```

For slower balloons:

```javascript
duration: gsap.utils.random(12, 15)
```

---

## Customizing Balloon Spacing

The vertical spacing between balloons can be changed using:

```javascript
const verticalGap = 220;
```

Increase the value for more space between balloons.

---

## Customizing Information Card Duration

The information card currently disappears automatically after approximately 6 seconds.

```javascript
delay: 6.0
```

You can increase or decrease this value depending on your content.

---

## Running Locally

No build process is required.

Clone the repository:

```bash
git clone https://github.com/aminulsarkar/floating-balloon-popups.git
```

Open the project folder and launch `index.html` in a browser.

For the best development experience, use a local development server such as VS Code Live Server.

---

## Browser Support

The application uses modern web technologies including:

* SVG
* ES6 JavaScript
* CSS3
* GSAP

Modern versions of Chrome, Edge, Firefox, and Safari are recommended.

---

## Performance Notes

The animation is designed to use lightweight SVG elements rather than image-based balloon assets.

GSAP handles the animation lifecycle and removes completed particle elements from the DOM after their animations finish.

For production use, unused libraries should be removed from the project to reduce unnecessary requests and dependencies.

---

## Possible Use Cases

This interaction can be adapted for:

* Event websites
* Festival websites
* Product launches
* Marketing campaigns
* Interactive landing pages
* Benefits/features sections
* Promotional websites
* Celebration pages
* Portfolio experiments
* Interactive UI demonstrations

---

## Author

**Aminul Sarkar**

Website:
https://aminulsarkar.com

GitHub:
https://github.com/aminulsarkar

Senior Full Stack Developer specializing in WordPress, Shopify, WooCommerce, PHP, JavaScript, and custom web experiences.

---

## License

This project is available under the MIT License.

See the `LICENSE` file for details.
