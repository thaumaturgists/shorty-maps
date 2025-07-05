```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shorty Maps</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            box-sizing: border-box;
        }
        .container {
            max-width: 800px; /* Adjust as needed */
            margin: auto;
            page-break-after: always; /* Ensures each printout starts on a new page */
        }
        h1 {
            text-align: center;
            font-size: 24px;
        }
        .map {
            text-align: center;
            margin: 20px 0;
        }
        .map img {
            max-width: 100%; /* Ensures the image fits within the container */
            height: auto;
            width: var(--map-width, 100%); /* Custom property for image width */
        }
        .directions {
            display: flex; /* Use flexbox for layout */
            flex-wrap: wrap; /* Allow wrapping for additional columns */
            justify-content: space-between;
            margin-top: 20px;
        }
        .direction-column {
            width: 48%; /* Adjust width for left and right columns */
            margin-bottom: 20px;
        }
        .direction-column h2 {
            font-size: 20px;
        }
        .direction-column p {
            font-size: 16px;
            line-height: 1.5;
            margin: 0;
        }
        @media print {
            body {
                margin: 0;
            }
            .container {
                border: none;
                padding: 0;
            }
            .direction-column {
                font-size: 14px; /* Reduce font size for print */
            }
        }
        @media print and (orientation: landscape) {
            .map {
                page-break-after: always; /* Ensure the map is on its own page */
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Shorty Maps</h1>
        <div class="map">
            <img src="path/to/your/map-image.jpg" alt="Map Image" style="--map-width: 80%;"> <!-- Adjust width here -->
        </div>
        <div class="directions">
            <div class="direction-column">
                <h2>Directions - Column 1</h2>
                <p>1. Start at [Starting Point].</p>
                <p>2. Head [Direction] on [Street Name].</p>
                <p>3. Continue for [Distance].</p>
            </div>
            <div class="direction-column">
                <h2>Directions - Column 2</h2>
                <p>4. Turn [Direction] onto [Next Street].</p>
                <p>5. Your destination will be on the [Left/Right].</p>
                <p>6. Additional notes can go here.</p>
            </div>
        </div>
    </div>
    <div class="container" style="display: none;">
        <div class="directions">
            <div class="direction-column">
                <h2>Directions - Column 1</h2>
                <p>1. Start at [Starting Point].</p>
                <p>2. Head [Direction] on [Street Name].</p>
                <p>3. Continue for [Distance].</p>
            </div>
            <div class="direction-column">
                <h2>Directions - Column 2</h2>
                <p>4. Turn [Direction] onto [Next Street].</p>
                <p>5. Your destination will be on the [Left/Right].</p>
                <p>6. Additional notes can go here.</p>
            </div>
        </div>
    </div>
</body>
</html>
```

### Customization Instructions:
1. **Map Image**: Replace `path/to/your/map-image.jpg` with the actual path to your map image.
2. **Image Size**: You can adjust the size of the image by changing the value of `--map-width` in the `style` attribute of the `<img>` tag.
3. **Directions**: Modify the content in the `<

Here’s the continuation of the customization instructions and additional details for the "Shorty Maps" template:

### Customization Instructions (continued):
3. **Directions**: Modify the content in the `<p>` tags under each direction column to fit your specific route. You can add more `<p>` tags as needed to include additional directions.
4. **Additional Columns**: If you have more directions that exceed the space available in the columns, you can add more `<div class="direction-column">` sections within the `.directions` div. The flexbox layout will automatically adjust to accommodate the new columns.
5. **Styling**: You can further adjust the CSS styles in the `<style>` section to change fonts, colors, margins, and other layout properties as needed. For example, you can change the font size for the directions or adjust the margins between columns.
6. **Print Settings**: When printing, ensure your browser's print settings are set to "Fit to Page" to ensure everything fits well on one page. The template is designed to handle both portrait and landscape orientations effectively.

### How It Works:
- **Portrait Mode**: In portrait mode, the map image is displayed at the top, followed by the directions in columns. If the text exceeds the available space, additional columns will be created, and the font size will automatically reduce for better readability.
- **Landscape Mode**: When printed in landscape mode, the first page will show the map image, and the second page will display the directions in columns, just like in portrait mode. The layout will adapt to ensure that all directions fit within the printed pages.

### Example Usage:
To use this template, simply copy the entire HTML code into a new HTML file, replace the placeholder text and image path with your actual content, and open the file in a web browser. You can then print the page using the browser's print functionality.

This template provides a flexible and user-friendly way to create a printable map and directions layout that adapts to different printing orientations and content lengths.

==================================================
```
What's the point of the container that has display: none ?
```
==================================================

The container with `display: none;` in the provided HTML template is intended to serve as a placeholder for the directions that will be printed on the second page in landscape mode. However, upon further reflection, it seems unnecessary and could lead to confusion since it doesn't actually serve a functional purpose in the current implementation.

### Explanation of the Original Intent:
- **Purpose**: The idea was to create a separate section for the directions that would only be visible when printed in landscape mode. However, since the same directions are already included in the first container, this additional container is redundant.
- **Visibility**: Since it is set to `display: none;`, it won't be visible in the browser or when printed, which means it won't contribute anything to the output.

### Revised Approach:
To simplify the template and avoid confusion, you can remove the second container entirely. The directions can be managed within a single container, and you can use CSS to control how they are displayed based on the print orientation.

Here’s the revised version of the template without the unnecessary container:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shorty Maps</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            box-sizing: border-box;
        }
        .container {
            max-width: 800px; /* Adjust as needed */
            margin: auto;
            page-break-after: always; /* Ensures each printout starts on a new page */
        }
        h1 {
            text-align: center;
            font-size: 24px;
        }
        .map {
            text-align: center;
            margin: 20px 0;
        }
        .map img {
            max-width: 100%; /* Ensures the image fits within the container */
            height: auto;
            width: var(--map-width, 100%); /* Custom property for image width */
        }
        .directions {
            display: flex; /* Use flexbox for layout */
            flex-wrap: wrap; /* Allow wrapping for additional columns */
            justify-content: space-between;
            margin-top: 20px;
        }
        .direction-column {
            width: 48%; /* Adjust width for left and right columns */
            margin-bottom: 20px;
        }
        .direction-column h2 {
            font-size: 20px;
        }
        .direction-column p {
            font-size: 16px;
            line-height: 1.5;
            margin: 0;
        }
        @media print {
            body {
                margin: 0;
            }
            .container {
                border: none;
                padding: 0;
            }
            .direction-column {
                font-size: 14px; /* Reduce font size for print */
            }
        }
        @media print and (orientation: landscape) {
            .map {
                page-break-after: always; /* Ensure the map is on its own page */
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Shorty Maps</h1>
        <div class="map">
            <img src="path/to/your/map-image.jpg" alt="Map Image" style="--map-width: 80%;"> <!-- Adjust width here -->
        </div>
        <div class="directions">
            <div class="direction-column">
                <h2>Directions - Column 1</h2>
                <p>1. Start at [Starting Point].</p>
                <p>2. Head [Direction] on [Street Name].</p>
                <p>3. Continue for [Distance].</p>
            </div>
            <div class="direction-column">
                <h2>Directions - Column 2</h2>
                <p>4. Turn [Direction] onto [Next Street].</p>
                <p>5. Your destination will be on the [Left/Right].</p>
                <p>6. Additional notes can go here.</p>
            </div>
        </div>
    </div>
</body>
</html>
```

### Summary:
- The unnecessary container with `display: none;` has been removed for clarity.
- The template now focuses on a single container that handles both portrait and landscape printing effectively.
- You can still manage the layout and content as needed without confusion from hidden elements.
