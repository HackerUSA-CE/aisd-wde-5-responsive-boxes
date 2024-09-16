# Colorful Responsive Fun with Media Queries

![Screenshot of the finished webpage](./assets/images/example.png)

## Description 📄
In this assignment, you will work to build colorful boxes using `html` and `css` and use three different `@media` queries along with `CSS Grid` to create a responsive layout. These queries will adjust the layout and appearance of the boxes based on different screen sizes, helping you understand how to create flexible and adaptable designs.

Follow the steps in the provided HTML and CSS below to complete the assignment.

## Expected Project Structure 🏗️
```
ColorfulResponsiveBoxes/
│
├── index.html
└── styles.css
```

# Instructions ✅

## 1. **Create the Project Folder and Files**
   - [ ] Create a folder named `ColorfulResponsiveBoxes` to store all your project files.
   
   - [ ] Inside the `ColorfulResponsiveBoxes` folder, create a file named `index.html`. This will be your main HTML file.
   
   - [ ] Also, in the `ColorfulResponsiveBoxes` folder, create another file named `styles.css`. This file will contain the CSS used to style your HTML content.

### You are now ready to begin coding your colorful responsive boxes!

## 2. **Build the HTML Structure**
Set up the basic HTML structure as needed for the project, 

- [ ] Open `index.html` and start by adding the basic HTML boilerplate code below. This includes the `DOCTYPE`, `html`, `head`, and `body` tags.
- [ ] Add a **title** in the `<head>` section as seen below.
- [ ] Finally link the `styles.css` file using the `<link>` tag.

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

## 3. **Create the Header** 

- [ ] Open the `index.html` file and add this code inside the `<body>` tags.  Give it a class of `title` and set the content to "Colorful Responsive Fun".

```html

  <h1 class="title">Colorful Responsive Fun</h1>

```
**Explanation:**
This code adds a header element to the body of the HTML document with a class `title` for further styling in CSS. The content "Colorful Responsive Fun" will appear as the main heading on the webpage.


## 4. **Set up the container** 
Now add the code for our main web page content.

- [ ] Create a `<div>` with the class `container` inside the `<body>` tags after the `<h1>` header tag. 
- [ ] Inside this container, create nine more `<div>` elements, each representing a box. Assign appropriate classes and labels to each box as shown below:

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



## 5.  **Initial Testing**
In this step, you'll open the index.html file in your browser to verify that the basic layout, consisting of 9 text elements representing the boxes, is displayed correctly.

- [ ] Open the `index.html` file in your browser. 

**Explanation:**
You should see a basic layout with 9 text elements representing the boxes as seen below: 
 ##
 ![Screenshot of the finished webpage](./assets/images/example2.png)
 ##

### Now style the page using `CSS`.

## 6. **Root Colors and Variables:**
In this step, you'll define a set of root-level CSS variables for colors that will be used throughout your stylesheet, making it easier to maintain and update your color scheme.

- [ ] Open your `styles.css` file and add the following code.

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

## 7. **Applying Body Styles:**
In this step, you'll apply styles to the body element to set up the overall layout and appearance of the webpage.

- [ ] Open your `styles.css` file and add the following code next.

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
The body styles use Flexbox to center the content both horizontally and vertically, set a neutral gray background, and apply a clean, readable font. This approach ensures the page content is balanced and visually appealing within the viewport.

## 8. **Styling the Header:**
In this step, you'll style the main heading of the page using the .title class to make it prominent and visually aligned with the overall design.

- [ ] Open your `styles.css` file and add the following code next.

```css
.title {
    color: var(--text-color);  /* Uses the white color defined in the variables */
    font-size: 2.5em;  /* Sets a large font size for prominence */
    margin-bottom: 40px;  /* Adds space below the title */
    text-align: center;  /* Centers the title text */
}
```

**Explanation:**
The .title class styles the main heading with a large font size, centered alignment, and white color from the root variables. This ensures the title stands out and is consistent with the page's color scheme, enhancing the visual impact of the heading.

## 9. **Setting Up the Grid Container**
In this step, you'll set up the grid container using the .container class to organize the layout of your webpage into a structured grid.

- [ ] Open your `styles.css` file and add the following code next.

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
The .container class creates a grid layout with four columns and three rows, ensuring even spacing and alignment of grid items. The grid-template-columns and grid-template-rows properties define the grid structure, while max-width prevents the container from becoming too wide on large screens, maintaining a balanced and organized layout.

## 10. **Styling the Boxes:**
In this step, you'll apply styles to the grid boxes, including padding, rounded corners, centered text, and unique background colors for each box.

- [ ] Open your `styles.css` file and add the following lines of CSS code.

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
The .box class styles each grid box with padding, rounded corners, and centered content using Flexbox. It also includes a smooth hover effect. Each box is assigned a unique background color from the defined CSS variables, ensuring a cohesive and visually appealing design.

## 11. **Special Box Styles:**
In this step, you'll apply special styles to specific boxes, allowing them to span multiple rows or columns within the grid layout.

- [ ] Open your `styles.css` file and add the following lines of CSS code.

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
The large-vertical, large-horizontal, and .box7 classes adjust the grid positioning of certain boxes, enabling them to span across multiple rows or columns. This breaks the grid's uniformity, creating a more dynamic and visually engaging layout that highlights specific elements.

## 12. **Hover Effect:**
In this step, you'll add a hover effect to the grid boxes, making them slightly scale up when hovered over.

- [ ] Open your `styles.css` file and add the following code next.

```css
.box:hover {
    transform: scale(1.05);  /* Slightly scales the box when hovered */
}
```

**Explanation:**
The `box:hover` style introduces a hover effect that slightly scales up the boxes when the user hovers over them. This adds interactivity and visual feedback, enhancing the overall user experience on the webpage.



## 13. **First Media Query (max-width: 1424px)**
Media queries are used to make the layout responsive, adjusting the grid and box sizes based on the screen width.

- [ ] Open your `styles.css` file and add the following code next.


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

## 14. **Second Media Query (max-width: 868px)**

- [ ] Open your `styles.css` file and add the following code next.

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

## 15. **Third Media Query (max-width: 480px)**

- [ ] Open your `styles.css` file and add the following code next.

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

## 16. **Testing Your Layout**

- [ ] Open your `index.html` file in the browser.
- [ ] Resize the Browser Window: Gradually resize your browser window from full screen down to a smaller width, observing how the layout changes at different breakpoints (1424px, 868px, and 480px). The content should adjust accordingly, with the grid layout transforming into a vertical stack on smaller screens.

## 17. **Commit and Push to Github**
 - [ ] Commit and push your work to Github.

 # Conclusion 📄
In this project, you built a responsive webpage featuring colorful boxes arranged in a grid layout using HTML, CSS, and media queries. You started by setting up the basic HTML structure, defined root-level color variables, and applied styles to the body, header, and boxes. You then used CSS Grid and Flexbox to create a dynamic and adaptable layout that adjusts to different screen sizes with the help of three media queries.

##

### Solution codebase 👀
🛑 **Only use this as a reference** 🛑

💾 **Not something to copy and paste** 💾

**Note:**  This lab references a solution file located [here](https://github.com/HackerUSA-CE/aisd-wde-5-responsive-boxes/tree/solution) (link not shown).



---
© All rights reserved to ThriveDX
