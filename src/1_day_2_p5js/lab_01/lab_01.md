# Lab — MS Paint 🎨 (150 points)

## What You'll Make

In this lab, we'll be using some of our knowledge from the lecture and yesterday's lab 3 to make a simple MS Paint clone!

---

## Learning Goals

By the end of this lab you will be able to:

- Use `pmouseX` and `pmouseY` to draw lines
- Manipulate these values to make symmetry
- Respond to keyboard input with `keyPressed()`
- Work with p5.js colour values using `color()`, `red()`, `green()`, and `blue()`

---

## Background

### Key Functions

| Function | When it runs |
|---|---|
| `keyPressed()` | Once, every time a key on the keyboard is pressed |
| `line(startX, startY, endX, endY)` | When called |
| `strokeWeight(weight)` | When called |

### Working with Colour

| Function | What it does | Example |
|---|---|---|
| `color(r, g, b)` | Creates a colour value you can store in a variable | `let c = color(255, 0, 0)` |
| `fill(c)` | Applies a stored colour as the fill | `fill(c)` |
| `red(c)` | Extracts the red channel from a colour | `red(c)` → `255` |
| `green(c)` | Extracts the green channel | `green(c)` |
| `blue(c)` | Extracts the blue channel | `blue(c)` |
| `random(min, max)` | Returns a random number between min and max | `random(0, 255)` |

---

## Part 1 — Polka Dots

### Step 1 — Set up our canvas (20 points)

Start with this base. Notice we don't set the background every frame, because we want our lines to persist.

```js
function setup() {
  createCanvas(500, 500);
  background(255);
  noLoop();
}

function draw() {
    // your logic here...
}
```

---

### Step 2 — Draw simple lines (30 points)

Using `mouseX`, `mouseY`, `pmouseX` and `pmouseY`, in `draw()`, draw a line between where the mouse was last frame and where it is this frame. 

---

### Step 3 — Change the thickness (50 Points)

Using `keyPressed()` and the `key` variable, create a function that sets the stroke weight to a random value when a key (e.g. `w`) is pressed. Fiddle wit the range of this value until it seems reasonable!

```js
function keyPressed() {
    // your logic here, using `key`...
}
```

---

### Step 4 — Vary the Colour (50 Points)

Like in yesterday's lab 3, use `keyPressed()` to make a key that changes the color of the line we draw! You can again fiddle with the values to get something nice.

---

## Part 2 — Extension

### Step 1 — Change stroke weight (nicer) (50 points)

Instead of randomly setting the stroke weight, choose a good value for it at the start, and then make two keys that can increase and decrease it! You could also add a help message that prints to the console if the key isn't suitable.

```js
let weight;

function setup() {
  createCanvas(500, 500);
  background(255);
  weight = 5;
  noLoop();
}

function keyPressed() {
    // your logic here...
}
```

---

### Step 2 - Mirroring (150 points)

Some paint programs have a mode where they mirror your lines vertically or horizontally. Replicate this feature! At first, just make every line mirrored. 

To do the mirroring, recall that if you have a canvas of size e.g. 400 x 400, then the coordinates (x, y) will be mirrored:
- Vertically: (x, 400 - y)
- Horizontally: (400 - x, y)
- Both: (400 - x, 400 - y)

Then, add extra `line` calls to draw these in.

---

### Step 3 — Toggleable mirroring (100 points)

Like how we made our stroke weight variable with a global variable, make the mirroring toggleable! If you want to get really fancy, make both the horizontal and vertical mirroing toggleable independantly.


Try painting some abstract art with these features!
---

## Challenge Activity

Add extra features as you want! Anything cool gets points as allocated by mentors.

---