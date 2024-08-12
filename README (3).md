
# WDE05 Colorful Responsive Fun with Media Queries

### Colorful Responsive Fun
![Screenshot of the finished webpage](./assets/images/example.png)

## Description
In this assignment, you will build colorful boxes using `HTML` and `CSS` and use three different `@media` queries along with `CSS Grid` to create a responsive layout. These queries will adjust the layout and appearance of the boxes based on different screen sizes, helping you understand how to create flexible and adaptable designs.

Follow the steps below to build out the HTML and CSS for the project.

## Project Structure
```
ColorfulResponsiveBoxes/
│
├── index.html
└── styles.css
```

## Setup Steps

### Step 1: Create the Project Folder and Files
1. **Create a folder** named `ColorfulResponsiveBoxes`.
2. **Inside this folder**, create a blank file named `index.html`.
3. **In the same folder**, create another blank file named `styles.css`.

### Step 2: Build the HTML Structure
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
```

3. **Create a header** inside the `<body>` tag with an `<h1>` element. Give it a class of `title` and set the content to "Colorful Responsive Fun".

```html
<body>
  <h1 class="title">Colorful Responsive Fun</h1>
```

4. **Set up the container** for the boxes by creating a `<div>` with the class `container`. Inside this container, create nine `<div>` elements, each representing a box. Assign appropriate classes and labels to each box as shown below:

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
</body>
```

5. **Close the HTML tags** to complete the `index.html` structure.

```html
</html>
```

### Step 3: Style the Layout with CSS
1. **Open `styles.css`** and begin by resetting some basic styles for the body and the title.

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f0f0f0;
}

.title {
    text-align: center;
    color: darkblue;
    margin-top: 20px;
    margin-bottom: 20px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}
```

2. **Set up the grid container**. Define a CSS Grid layout and set the initial grid columns for larger screens.

```css
.container {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    gap: 10px;
    margin: 20px;
}
```

3. **Style the boxes** with background colors, padding, and borders. Apply different background colors for each box class.

```css
.box {
    background-color: lightgray;
    border: 2px solid #000;
    padding: 20px;
    text-align: center;
    font-size: 20px;
    color: #fff;
}

.box1 { background-color: #ff6666; }
.box2 { background-color: #cc66ff; }
.box3 { background-color: #66cc66; }
.box4 { background-color: #ff99cc; }
.box5 { background-color: #6699ff; }
.box6 { background-color: #3366ff; }
.box7 { background-color: #339933; }
.box8 { background-color: #993333; }
.box9 { background-color: #33cccc; }

.large-vertical {
    grid-row: span 2;
}

.large-horizontal {
    grid-column: span 2;
}
```

### Step 4: Add Responsive Media Queries
1. **Add media queries** to adjust the grid layout for different screen sizes. Start with the largest breakpoint at 1024px.

```css
/* Large screens */
@media (max-width: 1024px) {
    .container {
        grid-template-columns: repeat(3, 1fr);
    }

    .large-vertical, .large-horizontal {
        grid-column: span 3;
    }

    .large-vertical {
        grid-row: span 3;
    }
}
```

2. **Add a media query** for medium screens at 768px.

```css
/* Medium screens */
@media (max-width: 768px) {
    .container {
        grid-template-columns: repeat(2, 1fr);
    }

    .large-vertical, .large-horizontal {
        grid-column: span 2;
    }
}
```

3. **Add a media query** for small screens at 480px.

```css
/* Small screens */
@media (max-width: 480px) {
    .container {
        grid-template-columns: 1fr;
    }

    .box {
        grid-column: span 1;
    }

    .large-vertical {
        grid-row: auto;
    }
}
```

### Step 5: Test and Review
1. **Save your files** and open `index.html` in your browser.
2. **Resize the browser window** to test how the boxes respond to different screen sizes.
3. **Ensure the boxes** are aligned and the layout is consistent with the design requirements at all screen sizes.

## Conclusion
By following these steps, you’ve created a responsive layout using CSS Grid and media queries. The project demonstrates how to make your designs adaptable to various screen sizes, ensuring a flexible and visually appealing layout.
