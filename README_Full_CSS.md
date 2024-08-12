
## Build the CSS Structure

1. **Root Colors and Variables:**

* At the top of the `styles.css` file, you'll see the `:root` selector. This is where CSS variables are defined. These variables store color values that are used throughout the styles.

```css
:root {
    --color1: #FF6F61;
    --color2: #6B5B95;
    --color3: #88B04B;
    --color4: #F7CAC9;
    --color5: #92A8D1;
    --color6: #034F84;
    --color7: #3d7803;
    --color8: #8b022b;
    --color9: #45B8AC;
    --text-color: #ffffff;
    --border-color: #ffffff;
}
```
* Each variable is prefixed with `--`, and you can use these variables later in your CSS by referring to them with `var(--variable-name)`.

2. **Body Styles:**

* The body styles set the overall layout and appearance of the page, including background color, font, and alignment.

```css
body {
    margin: 30px;
    font-family: Arial, sans-serif;
    background-color: #949191;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    padding: 30px 0; /* Increased margin at the top and bottom */
}
```
* This code centers the content vertically and horizontally and applies a neutral background color.

3. **Styling the Header:**

* The `title` class is used to style the main heading of the page.

```css
.title {
    color: var(--text-color);
    font-size: 2.5em;
    margin-bottom: 40px;
    text-align: center;
}
```
* Here, the title is centered, with a large font size, and the text color is set to white.

4. **Setting Up the Grid Container:**

* The `container` class creates a grid layout to hold all the boxes.

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr) 1fr;
    gap: 20px;
    padding: 20px;
    width: 100%;
    max-width: 1600px; /* Larger starting container width */
    height: 100vh;
    grid-template-rows: repeat(3, 1fr) 200px;
}
```
* This grid has four columns and three rows, with gaps between the grid items. The container also has a maximum width, ensuring it doesn't stretch too wide on large screens.

5. **Styling the Boxes:**

* Each box is styled with a background color, padding, and rounded corners.

```css
.box {
    color: var(--text-color);
    padding: 40px;
    border-radius: 10px;
    text-align: center;
    transition: transform 0.3s ease;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.5em;
    border: 2px solid var(--border-color);
}
```
* The `transition` property adds a smooth hover effect, making the boxes scale up slightly when hovered.

```css
.box1 { background-color: var(--color1); }
.box2 { background-color: var(--color2); }
.box3 { background-color: var(--color3); }
.box4 { background-color: var(--color4); }
.box5 { background-color: var(--color5); }
.box6 { background-color: var(--color6); }
.box7 { background-color: var(--color7); }
.box8 { background-color: var(--color8); }
.box9 { background-color: var(--color9); }
```
* Each box has a unique background color, using the variables defined in the `:root`.

6. **Special Box Styles:**

* The `large-vertical` and `large-horizontal` classes are used to create boxes that span multiple rows or columns.

```css
.large-vertical {
    grid-row: 1 / 5;
    grid-column: 4 / 5;
    padding: 20px;
}

.large-horizontal {
    grid-row: 4 / 5;
    grid-column: span 3;
    padding: 20px;
}
```

* These styles ensure that certain boxes take up more space in the grid, adding variety to the layout.

7. **Hover Effect:**

* The `box:hover` style adds a hover effect to all boxes.

```css
.box:hover {
    transform: scale(1.05);
}
```
* This effect makes the boxes slightly larger when the mouse hovers over them, providing a simple but effective interaction.

### Step 3: Media Queries

* Media queries are used to make the layout responsive, adjusting the grid and box sizes based on the screen width.

1. **First Media Query (max-width: 1424px):**

* This media query adjusts the grid layout for screens smaller than 1424px.

```css
@media (max-width: 1424px) {
    .container {
        grid-template-columns: repeat(2, 1fr); /* Reduces the grid to 2 columns */
        grid-template-rows: repeat(5, 1fr); /* Creates 5 equal-height rows */
    }

    .large-vertical {
        grid-column: span 2; /* Spans both columns */
        grid-row: auto; /* Adjusts the row span automatically */
    }

    .large-horizontal,
    .box7 {
        grid-column: span 2; /* Spans across both columns */
    }

    .box {
        font-size: 1.4em; /* Reduces font size slightly */
    }

    .box, .large-vertical, .large-horizontal {
        height: auto;
        min-height: 150px; /* Ensure all boxes have at least a minimum height */
    }
}
```

2. **Second Media Query (max-width: 868px):**

* This media query adjusts the layout for tablets and smaller screens.

```css
@media (max-width: 868px) {
    .container {
        display: flex; /* Switches to a flexbox layout */
        flex-direction: column; /* Stacks the boxes vertically */
    }

    .box1 { order: 1; }
    .box2 { order: 2; }
    .box3 { order: 3; }
    .box4 { order: 4; }
    .box5 { order: 5; }
    .box6 { order: 6; }
    .box7 { order: 7; }
    .large-vertical { order: 8; }
    .large-horizontal { order: 9; }

    .box, .large-vertical, .large-horizontal {
        font-size: 1.3em;
        height: auto;
        min-height: 150px; /* Ensure uniform height across all boxes */
    }
}
```

3. **Third Media Query (max-width: 480px):**

* This media query further adjusts the layout for mobile devices.

```css
@media (max-width: 480px) {
    .container {
        display: flex; /* Retains the flexbox layout */
        flex-direction: column; /* Continues stacking boxes vertically */
    }

    .box1 { order: 1; }
    .box2 { order: 2; }
    .box3 { order: 3; }
    .box4 { order: 4; }
    .box5 { order: 5; }
    .box6 { order: 6; }
    .box7 { order: 7; }
    .large-vertical { order: 8; }
    .large-horizontal { order: 9; }

    .box {
        font-size: 1.2em; /* Further reduces the font size */
        padding: 30px; /* Adds more padding inside the boxes */
        height: auto;
        min-height: 150px; /* Uniform height for all boxes */
    }

    .large-vertical,
    .large-horizontal {
        height: auto;
        min-height: 150px; /* Ensure consistent height across these boxes */
    }
}
```

* By following these steps, you'll create a responsive and visually appealing layout that adjusts based on the device's screen size. This exercise demonstrates the power of CSS Grid and media queries in crafting adaptive web designs.
