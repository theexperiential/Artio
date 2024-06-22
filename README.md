# :clamp: Artio
### The Ultimate Pixel Mapping Toolkit for TouchDesigner Projects
#### :floppy_disk: version 0.5.406
#### :floppy_disk: TouchDesigner 2023.11760 (Windows)
## Overview 
Artio is a powerful, industry-grade TouchDesigner component designed to streamline the creation of pixel-perfect, multi-display layouts for live events and performances. With its intuitive 3D geometry-based approach, Artio simplifies the process of generating precise pixel maps for each display, allowing you to focus on creating stunning visual experiences.

Built with flexibility in mind, Artio seamlessly integrates with your existing content mapping workflow, accepting various inputs and providing a clean, optimized pixel map output. Its highly customizable feature set empowers creative technologists to tailor every aspect of the display layout, from guidelines and tiles to masks and corners, ensuring unparalleled control and accuracy.

Whether you're working on a complex, large-scale installation or a dynamic, multi-display performance, Artio scales effortlessly to meet the demands of your project. By simplifying the technical challenges of pixel mapping, Artio enables you to push the boundaries of your creativity and deliver truly immersive, visually striking experiences to your audience.

Its name (ἄρτιος) is the Greek word for "perfectly aligned."

:point_right: Demo / Setup [YouTube Video](https://youtu.be/lP9wXwb6uHA) (out of date, to be updated...)

![Artio Single Raster](/img/Display_1.png)
![Artio Multiple Rasters](/img/render1.png)
## Key Features
- Dynamic generation of pixel maps for multiple displays
- Customizable guidelines, tiles, corners, and masks for precise alignment
- Support for various content inputs (TOPs or COMPs) and mapping methods (Orthographic or Perspective)
- Easy addition, editing, and removal of displays through custom parameters
- Storage and loading of display parameters for project persistence
- Automatic calculation of renderTOP resolution based on display sizes and positions
- Export functionality to save pixel maps as various image formats
## Usage
1. Add the Artio component to your TouchDesigner project.
2. Configure Display settings (name, resolution, position, rotation, scale, etc.) using the custom parameters on the Artio COMP.
3. Choose the desired content input source (Pixel Map, In TOP, Content TOP, or Content COMP) per Display.
4. Customize the appearance of guidelines, tiles, corners, and masks as needed.
5. Create a pixel map in your project or export them as images.
## Content Inputs
- Pixel Map - the default input: Artio's pixel map component.
- In TOP - simply wire any TOP to an Artio Display geometry component's input, and it will automatically display it.
- Content TOP - drag and drop your content TOP here and Artio will automatically display it if it detects a valid OP.
- Content COMP - drag and drop your content Container here and Artio will automatically display it if it detects a valid OP.
## Mapping Outputs
- Map COMP - Outputs the pixel map as a TOP, customizable uing the Artio COMP's Map page.
## Display Custom Parameters
- Display - Configure display name, resolution, position, rotation, scale, and color.
- Logo/Text - Customize the logo, display name text, and resolution text.
- Guidelines - Configure border, crosshair, diagonal, corner and circle guidelines.
- Tiles - Customize tile size, alignment, color, numbering, and borders.
- Masks - Add and customize masks for projection blends or complex LED tile layouts.
- Anim - Play a white gradient to confirm frame rate.
- Export - Choose file format, save folder, and filename for exporting pixel maps.
## Extension Class
The `ArtioExt` extension class provides additional functionality to the Artio component. Key features include:
- Adding, editing, and removing displays
- Storing and loading display parameters
- Updating the renderTOP resolution based on display sizes and positions
- Synchronizing the mapping sequence blocks with display changes
## Changelog
- 0.5.406 - Fix python storage re-init bug
- 0.5.405 - Add Open Display Pars button to main UI, fix saved pars
- 0.5.402 - Display reordering bug fixes and minor UI improvements
- 0.5.397 - Refactor guidelines to GLSL, VRAM optim
- 0.5.386 - Update UI to be resolution agnostic
- 0.5.384 - Cleaner save state
- 0.5.368 - More minor bug fixes with Display editing and Map sync
- 0.5.364 - Minor bug fixes and storage re-init
- 0.5.353 - Bug fixes for mapping renders, port Map to Comper (now called Mapper)
- 0.5.350 - Refactor composite for Displays to GLSL, bug fixes, blur BG for text
- 0.5.292 - Updated README and extension class documentation, Display bug fixes
- 0.5.284 - Refactor tile numbering to single textTOP, fix alignment bugs
- 0.5.270 - Add masking GLSL, cleanup and fixes
- 0.5.261 - Tiles refactor to GLSL
- 0.5.244 - Add mapping/content pipeline
- 0.5.2 - Added auto-calculation for renderTOP resolution when resizing/rotating displays, network cleanup
- 0.4.52 - Added display pivot support for rotation, bug fixes when creating displays/simplification of position/rotation/pivot parameters
- 0.4.48 - Bug fix for diagonal/border line parameter mix-ups, update to TD 2023
- 0.4.45 - Bug fixes for guidelines and tile borders/fills, added tile border width parameters, version control bug fix
- 0.4.28 - Added custom parameters for adding/editing/removing displays, fixed numerous bugs
- 0.4.1 - Added support for non-square tiles and uniform scaling (for multiple pixel pitches), simplified demo setup
- 0.4.0 - Added masking for projection blend zones and alpha support between Artio Displays
- 0.3.8 - Added built-in expression for Circle Radius parameter
- 0.3.7 - Fixed guideline border vertical line attributes
- 0.3.6 - Added exporting to various image file formats (thanks to Oleksandr Korchuk for this idea)
- 0.3.5 - Added support for lower resolutions and better text/logo scaling, minor bug fixes
## Credits
- Thanks to Aristotle Roufanis for providing the Greek translation.
- Thank you to Michel Didier / Derivative for performance suggestions along the journey.
- Many thanks to DVizion for sharing their wonderful LED Pixelmapper Template, which largely inspired Artio.
- Special thanks to Peter Sistrom for his compShader.