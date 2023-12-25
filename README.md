# :clamp: Artio

### Dynamic pixel map generator for multi-display TouchDesigner environments

#### :floppy_disk: version 0.4.48
#### :floppy_disk: TouchDesigner 2023.11340 (Windows)

## Overview 

Artio is a highly customizable TouchDesigner component that generates a pixel map for each of your displays in a geometry COMP replicator setup. It is designed for maximum clarity and scalability for events and performances. It's name (ἄρτιος) is the Greek word for, "perfectly aligned."

:point_right: Demo / Setup [YouTube Video](https://youtu.be/lP9wXwb6uHA)

![Artio Single Raster](/img/artio.png)
![Artio Multiple Rasters](/img/render1.png)

## Content Inputs

- Pixel Map - the default input: Artio's pixel map component.
- In TOP - simply wire any TOP to an Artio Display geometry component's input, and it will automatically display it.
- Content TOP - drag and drop your content TOP here and Artio will automatically display it if it detects a valid OP.
- Content COMP - drag and drop your content Container here and Artio will automatically display it if it detects a valid OP.


## Content Outputs

- out1 - Outputs the Content Source as a TOP, per Artio Display geometry replicant.


## Parameters
### Display Page

- Display Name - The name of the display (Wall, Center, Main, Projector 4, Projector 5, etc.)
- Resolution - The resolution, in pixels, of the display; the geometryCOMP in which the display is rendered contains a rectangleSOP that is set to a size 1/1000th the scale of the resolution (a resolution of 1920 x 1080 renders at a sizex of 1.92 and sizey of 1.08)
- Position - Where the Display is rendered within the render top. 1 unit = 1,000 pixels
- Rotation - The degrees in which the Display is rotated on the z-axis (rz). Useful for portrait display orientations (90 or -90 degrees)
- Content Source - Switch between different sources of content (Pixel Map, In TOP [wire], TOP or COMP sources)
- Content TOP - The input TOP for content
- Content COMP - The input COMP for content

### Logo/Text Page

- Logo Active - Toggles visibility of the logo (Banana is default... naturally)
- Name Text Active - Toggles the visibility of the Display Name text
- Resolution Text Active - Toggles the visibility of the resolution text
- Logo/Text Offset - How far left/right and up/down the entire Logo/Text block is positioned, in pixels
- Logo/Text Rotation - How many degrees the entire Logo/Text block is rotated

- Logo File - The custom logo file to be used (expects an image or movie that a moviefileinTOP can read)
- Logo Scale - How big or small the logo is rendered
- Logo Offset - How far left/right and up/down the logo is offset from it's origin

- Text Font - The font used to render the Name, Resolution and grid number IDs
- Text Colour - The colour and alpha of the text rendered
- Text BG Colour - The colour and alpha of the plate behind text elements
- Name Text Size - The size in vertical pixels of the Name Text, in pixels
- W x H Text - Whether the Resolution Text is displayed in "XXX x XXX px" or "W XXX x H XXX" notation
- Resolution Text Size - The size in vertical pixels of the Resolution Text, in pixels
- Resolution Text Offset - How far left/right and up/down the Resolution Text is offset from it's origin, in pixels

### Guidelines Page

- Line Thickness - How thick or thin guidelines are rendered, in pixels
- Border Active - Toggles visibility of the outermost border around the entire perimeter of the display
- Border Line Dashed - Toggles whether the Border Line is rendered as a dashed line (True) or as a solid line (False)
- Border Line Colour - The colour and alpha of the Border Line
- Crosshair Lines Active - Toggles visibility of the crosshair (vertical and horizontal perpendicular) lines
- Crosshair Lines Dashed - Toggles whether the Crosshair Lines are rendered as dashed lines (True) or as solid lines (False)
- Crosshair Lines Colour - The colour and alpha of the Crosshair Lines
- Diag Lines Active - Toggles visibility of the Diagonal lines that terminate at each corner of the display
- Diag Lines Dashed - Toggles whether the Diagonal Lines are rendered as dashed lines (True) or as solid lines (False)
- Diag Lines Colour - The colour and alpha of the Diagonal Lines
- Circle Active - Toggles visibility of the perfect Circle Line (useful for verifying display ratio)
- Circle Dashed -  Toggles whether the Circle Line is rendered as a dashed line (True) or as a solid line (False)
- Circle Radius - How big or small the Circle is rendered; a radius of 10 renders the circle at the full width of a full HD display (1920 wide)
- Circle Colour - The colour and alpha of the Circle Line


### Tiles Page

- Tiles Active - Toggles visibility of the Tiles background colour fills
- Tile Size - The resolution of each tile, in pixels
- Tile Alignment - How the Tile grid is justified (top left or center center), useful for odd resolution/tile size combinations in which Tiles may be cut off
- Tile Light Colour - The colour of Tiles on the right of each gradient step
- Tile Dark Colour - The colour of Tiles on the left of each gradient step
- Tile Number Active - Toggles visibility of Tile number ID texts
- Tile Number Prefix - String to insert before each number (A1, B1, C1, etc.)
- Tile Number Colour - The colour and alpha of Tile Number texts
- Tile Number Size - The height of Tile Numbers, in pixels
- Tile Diag Lines Active - Toggles visibility of Tile Diagonal ('x') lines
- Tile Diag Lines Colour - The colour and alpha of Tile Diag Linse
- Tile Borders Active - Toggles visibility of Tile Borders
- Tile Borders Colour - The colour and alpha of Tile Borders
- BG Colour - The colour and alpha of the Background plate (behind all Tiles; Tiles Active must be set to False in order to display the BG Colour)


### Corners Page

- Corners Active - Toggles visibility of Corner triangles in each corner of the display map (useful for precisely identifying where the corner of each display is located)
- Corner Size - The size (width and height) of each corner triangle, in pixels
- Corner Colour - The Colour and alpha of each Corner triangle


### Mask Page

- Mask Active - Toggles visibility of a rectangular mask element which can be useful for projection blends
- Mask Colour - The RGBA color value of the mask
- Mask Blend - How much alpha the mask lets through to reveal other Artio Displays beneath it. Useful for projection blends
- Mask Alignment - The alignment of the mask on the display canvas (left, right, top or bottom)
- Mask Width - The total width (in pixels) of the mask 


### Export Page

- File Format - The image file format to save to
- Save Folder - The folder to save the image to. Defaults (when blank) to the project's folder
- Filename - The name of the file to save to. Remember to keep the file extension (.{me.par.Fileformat}) in this expression or it may break
- Export Image - Pulse to save out the image. Will overwrite any existing image with the same name. Will also open up a Windows File Explorer window to reveal the file


## Changelog

- 0.4.48 - Bug fix for diagonal/border line paramater mix-ups, update to TD 2023
- 0.4.45 - Bug fixes for guidelines and tile borders/fills, add tile border width parameters, version control bug fix (so version numbers are now consistent)
- 0.4.28 - Added custom parameters for adding/editing/removing displays, fixed numerous bugs
- 0.4.1 - Added support for non-square tiles and uniform scaling (for multiple pixel pitches), simplified demo setup
- 0.4.0 - Added masking for projection blend zones and alpha support between Artio Displays
- 0.3.8 - Added built-in expression for Circle Radius par
- 0.3.7 - Fixed guideline border vertical line attributes
- 0.3.6 - Added exporting to various image file formats (thank you to Oleksandr Korchuk for this idea)
- 0.3.5 - Added support for lower resolutions and better text/logo scaling, minor bug fixes


## Thanks

Shoutout to [Aristotle Roufanis](https://aristotle.photography) for providing the Greek translation.

Thank you to Michel Didier / Derivative for performance suggestions.

Many thanks to DVizion for sharing their wonderful [LED Pixelmapper Template](http://www.dvizion.net/portfolio/led-pixelmapper/), which largely inspired Artio.