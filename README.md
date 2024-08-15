# WDE05 Colorful Responsive Fun with Media Queries

### Colorful Responsive Fun
![Screenshot of the finished webpage](./assets/images/example.png)

## Description
In this assignment, you will build colorful boxes using `html` and `css` and use three different `@media` queries along with `CSS Grid` to create a responsive layout. These queries will adjust the layout and appearance of the boxes based on different screen sizes, helping you understand how to create flexible and adaptable designs.

Follow the steps in the provided HTML and CSS below to complete the assignment.

## Project Structure
```
ColorfulResponsiveBoxes/
│
├── index.html
└── styles.css
```

## Setup Steps
1. Create a folder named `ColorfulResponsiveBoxes`.
2. Inside this folder, create a blank `index.html` file.
3. In the same folder, create a blank `styles.css` file.

You are now ready to begin coding your colorful responsive boxes!

## Build the HTML Structure

1. **Open `index.html`** and start by adding the basic HTML boilerplate. This includes the `DOCTYPE`, `html`, `head`, and `body` tags.
2. **Add a title** in the `<head>` section and link the `styles.css` file using the `<link>` tag.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Colorful Responsive Fun</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Add your boxes here -->
</body>
</html>
```
**Explanation:**
This code sets up the basic HTML structure needed for the project, including the `DOCTYPE` declaration, language attribute, meta tags, and linking to the external CSS file.

##

3. **Create a header** inside the `<body>` tags with an `<h1>` element. Give it a class of `title` and set the content to "Colorful Responsive Fun".

```html
<body>
  <h1 class="title">Colorful Responsive Fun</h1>

   <!-- Add your boxes here -->
    
</body>
```
**Explanation:**
This code adds a header element to the body of the HTML document with a class `title` for further styling in CSS. The content "Colorful Responsive Fun" will appear as the main heading on the webpage.

##

4. **Set up the container** for the boxes by creating a `<div>` with the class `container`. Place this code inside the `<body>` tags after the `<h1>` header tag. Inside this container, create nine more `<div>` elements, each representing a box. Assign appropriate classes and labels to each box as shown below:

```html
  <div class="container">
    <div class="box box1" aria-label="Red Box">
      <p>Red Box</p>
    </div>
    <div class="box box2" aria-label="Purple Box">
      <p>Purple Box</p>
    </div>
    <div class="box box3" aria-label="Green Box">
      <p>Green Box</p>
    </div>
    <div class="box box4" aria-label="Pink Box">
      <p>Pink Box</p>
    </div>
    <div class="box box5" aria-label="Blue Box">
      <p>Blue Box</p>
    </div>
    <div class="box box6" aria-label="Dark Blue Box">
      <p>Dark Blue Box</p>
    </div>
    <div class="box box7" aria-label="Dark Green Box">
      <p>Dark Green Box</p>
    </div>
    <div class="box large-vertical box8" aria-label="Dark Red Box">
      <p>Dark Red Box</p>
    </div>
    <div class="box large-horizontal box9" aria-label="Teal Box">
      <p>Teal Box</p>
    </div>
  </div>
```
**Explanation:**
This code block creates a container div that holds nine other divs, each representing a box. The boxes are given classes and `aria-labels` for identification and accessibility. This structure sets the stage for a grid-like layout that will be styled using CSS.

##

### Initial Testing

Now, open the `index.html` file in your browser. 
You should see a basic layout with 9 text elements representing the boxes which we will now style using `CSS`.

<img src="./assets/images/example2.png" alt="Screenshot of the finished index.html" width="300" height="300" style="border: 2px solid black;">


## Build the CSS Structure 
Place each block of code in the `styles.css` file right after the next one in order as instructed below

##

1. **Root Colors and Variables:**

```css
:root {
    --color1: #FF6F61;  /* Vibrant coral color */
    --color2: #6B5B95;  /* Muted purple tone */
    --color3: #88B04B;  /* Earthy green */
    --color4: #F7CAC9;  /* Soft pink */
    --color5: #92A8D1;  /* Light blue */
    --color6: #034F84;  /* Deep navy */
    --color7: #3d7803;  /* Dark green */
    --color8: #8b022b;  /* Dark red */
    --color9: #45B8AC;  /* Teal color */
    --text-color: #ffffff;  /* White text color */
    --border-color: #ffffff;  /* White border color */
}
```

**Explanation:**
At the top of the `styles.css` file, you'll see the `:root` selector. This is where CSS variables are defined. These variables store color values that are used throughout the styles. Each variable is prefixed with `--`, and you can use these variables later in your CSS by referring to them with `var(--variable-name)`.

##

2. **Applying Body Styles:**

```css
body {
    margin: 30px;  /* Adds space around the body content */
    font-family: Arial, sans-serif;  /* Sets a clean and readable font */
    background-color: #949191;  /* Neutral gray background */
    display: flex;  /* Enables Flexbox layout */
    flex-direction: column;  /* Aligns items vertically */
    justify-content: center;  /* Centers items vertically */
    align-items: center;  /* Centers items horizontally */
    height: 100vh;  /* Makes the body height full screen */
    padding: 30px 0;  /* Adds vertical padding for spacing */
}
```

**Explanation:**
The `body` styles set the overall layout and appearance of the page, including background color, font, and alignment and ensure that the entire page content is centered within the viewport. The Flexbox layout (`display: flex;`) is used to align and center the elements both horizontally and vertically. This styling approach creates a balanced and visually appealing layout. The neutral background color provides a subtle backdrop for the content.

##

3. **Styling the Header:**

```css
.title {
    color: var(--text-color);  /* Uses the white color defined in the variables */
    font-size: 2.5em;  /* Sets a large font size for prominence */
    margin-bottom: 40px;  /* Adds space below the title */
    text-align: center;  /* Centers the title text */
}
```

**Explanation:**
This CSS class `.title` applies specific styling to the main heading of the page. The use of `var(--text-color)` ensures that the heading color is consistent with the overall theme, utilizing the white color defined in the root variables. The large font size makes the title stand out, and the text alignment centers it within the page, creating a strong visual impact.

##

4. **Setting Up the Grid Container:**

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr) 1fr;  /* Creates 4 columns, 3 equal width and 1 column of 1fr */
    gap: 20px;  /* Adds space between grid items */
    padding: 20px;  /* Adds padding around the grid */
    width: 100%;  /* Makes the container take full width of the viewport */
    max-width: 1600px;  /* Ensures the container doesn't exceed 1600px in width */
    height: 100vh;  /* Sets the container height to full viewport height */
    grid-template-rows: repeat(3, 1fr) 200px;  /* Creates 3 equal-height rows and one row with fixed height of 200px */
}
```

**Explanation:**
The `container` class creates a grid layout to hold all the boxes. This CSS also sets up a grid container using `display: grid;`. The grid has four columns and three rows, with gaps between the grid items for spacing. The `grid-template-columns` and `grid-template-rows` properties define the structure, while `max-width` ensures the container doesn't stretch too wide on larger screens, maintaining a neat layout.

5. **Styling the Boxes:**


```css
.box {
    color: var(--text-color);  /* Text color from root variables */
    padding: 40px;  /* Adds space inside the box */
    border-radius: 10px;  /* Rounds the corners of the box */
    text-align: center;  /* Centers text inside the box */
    transition: transform 0.3s ease;  /* Adds a smooth transition effect on hover */
    display: flex;  /* Uses flexbox for centering content */
    justify-content: center;  /* Centers content horizontally */
    align-items: center;  /* Centers content vertically */
    font-size: 1.5em;  /* Sets a larger font size for the text */
    border: 2px solid var(--border-color);  /* Adds a border with color from root variables */
}
```

```css
.box1 { background-color: var(--color1); }  /* Sets background color using variable color1 */
.box2 { background-color: var(--color2); }  /* Sets background color using variable color2 */
.box3 { background-color: var(--color3); }  /* Sets background color using variable color3 */
.box4 { background-color: var(--color4); }  /* Sets background color using variable color4 */
.box5 { background-color: var(--color5); }  /* Sets background color using variable color5 */
.box6 { background-color: var(--color6); }  /* Sets background color using variable color6 */
.box7 { background-color: var(--color7); }  /* Sets background color using variable color7 */
.box8 { background-color: var(--color8); }  /* Sets background color using variable color8 */
.box9 { background-color: var(--color9); }  /* Sets background color using variable color9 */
```

**Explanation:**
The `.box` class applies various styles to each grid box, including padding, rounded corners, and a hover effect. Each box also uses a unique background color, defined by the variables in the `:root` selector, ensuring consistency in the design.

##

6. **Special Box Styles:**

```css
.large-vertical {
    grid-row: 1 / 5;  /* Spans the first box across 4 rows */
    grid-column: 4 / 5;  /* Takes up the entire last column */
    padding: 20px;  /* Adds padding inside the box */
}

.large-horizontal {
    grid-row: 4 / 5;  /* Spans the box across the last row */
    grid-column: span 3;  /* Takes up the first 3 columns */
    padding: 20px;  /* Adds padding inside the box */
}

.box7 {
    grid-column: span 3;  /* Spans the box across 3 columns */
}
```

**Explanation:**
The `large-vertical`, `large-horizontal`, and `.box7` classes are used to create boxes that span multiple rows or columns. These special classes modify the grid behavior for specific boxes, allowing them to span multiple rows or columns. This creates a dynamic and interesting layout by breaking the uniformity of the grid structure, drawing attention to certain elements.

##

7. **Hover Effect:**

```css
.box:hover {
    transform: scale(1.05);  /* Slightly scales the box when hovered */
}
```

**Explanation:**
The `box:hover` style adds a hover effect to all boxes and adds interactivity to the grid boxes, scaling them up slightly when hovered. This provides feedback to the user, enhancing the overall user experience.

##

### Media Queries

Media queries are used to make the layout responsive, adjusting the grid and box sizes based on the screen width.

1. **First Media Query (max-width: 1424px):**

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

**Explanation**
This media query adjusts the layout for screens smaller than 1424px, reducing the grid to two columns and five rows. It also ensures that boxes span appropriately within the reduced layout, and slightly decreases the font size for better readability on smaller screens.

##

2. **Second Media Query (max-width: 868px):**

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
**Explanation**
For screens smaller than 868px, this media query switches the layout to a flexbox-based vertical stack. It orders the boxes to ensure a logical flow when stacked and further reduces the font size to maintain readability.

##

3. **Third Media Query (max-width: 480px):**

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

**Explanation**
This media query is designed for mobile devices with screens smaller than 480px. It retains the flexbox layout, further reduces font size, and adds more padding inside the boxes to maintain a clean, readable appearance.

##

# Testing

* Resize the Browser Window: Gradually resize your browser window from full screen down to a smaller width, observing how the layout changes at different breakpoints (1424px, 868px, and 480px). The content should adjust accordingly, with the grid layout transforming into a vertical stack on smaller screens.

---
© All rights reserved to ThriveDX
