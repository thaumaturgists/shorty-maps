# Shorty Maps

![Shorty Maps Logo](./public/sml.png) <!-- Replace with the actual path to your image -->

Shorty Maps is a simple, one-page printout template designed for map directions. It allows users to print a map along with clear, organized directions that adapt to both portrait and landscape orientations.

Currently, users can either have an agent fill in the column data or prompt the system to do so. Please keep in mind that adding columns and making adjustments may be necessary. Future enhancements aim to make this process easier and dynamically optimized.

## Badges

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE) <!-- Replace with actual badge links -->
[![Version](https://img.shields.io/badge/version-1.0.0-brightgreen.svg)](VERSION) <!-- Replace with actual badge links -->
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)](BUILD_STATUS) <!-- Replace with actual badge links -->

## Features

- **Portrait Mode**: Displays an image of the map above and directions below in columns. If the text overflows, additional columns are added, and the text size reduces for readability.
- **Landscape Mode**: The first page shows the map image, while the second page contains the directions in columns, maintaining the same adaptive layout.

## Usage

1. **Clone the Repository**: 
   ```bash
   git clone https://github.com/thaumaturgists/shorty-maps.git
   cd shorty-maps
   ```

2. **Open the HTML File**: Open the `index.html` file in your web browser.

3. **Print the Page**: Use your browser's print functionality (usually `Ctrl + P` or `Cmd + P`) to print the page. Ensure your print settings are set to "Fit to Page" for optimal results.

## Customization

You can easily customize the template to fit your needs:

- **Map Image**: Replace the placeholder image path in the `<img>` tag with the actual path to your map image:
  ```html
  <img src="path/to/your/map-image.jpg" alt="Map Image" style="--map-width: 80%;">
  ```

- **Directions**: Modify the text within the `<p>` tags under each direction column to include your specific route details. You can add more `<div class="direction-column">` sections if needed.

- **Styling**: Adjust the CSS styles in the `<style>` section to change fonts, colors, margins, and other layout properties as desired.

## Example Structure

Here’s a brief overview of the HTML structure:

```html
<div class="container">
    <h1>Shorty Maps</h1>
    <div class="map">
        <img src="path/to/your/map-image.jpg" alt="Map Image">
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
```

## License

This project is licensed under the MIT License. Feel free to use and modify it as needed.

## Acknowledgments

- Inspired by the need for clear and concise map directions for easy printing.
- Thanks to the open-source community for providing resources and inspiration.

## Contact

For any questions or feedback, please reach out to the project maintainer.
