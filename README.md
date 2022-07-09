# :clamp: Artio

### Dynamic pixel map generator for multi-display TouchDesigner environments

#### :floppy_disk: Current Version: 0.3.2
#### :floppy_disk: TouchDesigner Build: 2022.25370 (Windows)

## Overview 

Artio is a highly customizable TouchDesigner component that generates a pixel map for each of your displays in a geometry COMP replicator setup. It is designed for maximum clarity and scalability for events and performances. It's name (ἄρτιος) is the Greek word for, "perfectly aligned."

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
- Content Source - Switch between different sources of content
- Content TOP - The input TOP for content
- Content COMP - The input COMP for content

### Text/Logo Page

- Name Text Active - Toggles the visibility of the Display Name text
- Resolution Text Active - Toggles the visibility of the resolution text
- Text Font - The font used to render the Name, Resolution and grid number IDs
- Text Colour - The colour and alpha of the text rendered
- Text BG Colour - The colour and alpha of the plate behind text elements
- Text Size - The size in vertical pixels of the Name Text (scales Resolution Text proportionally)
- Logo Active - Toggles visibility of the logo (Banana is default... naturally)
- Logo File - The custom logo file to be used (expects an image or movie that a moviefileinTOP can read)
- Logo Scale - How big or small the logo is rendered
- Logo Offset - How far left/right and up/down the logo is offset from its origin


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

## Thanks

Shoutout to [Aristotle Roufanis](https://aristotle.photography) for providing the Greek translation.

Many thanks to DVizion for sharing their wonderful [LED Pixelmapper Template](http://www.dvizion.net/portfolio/ffgl-masterfx/), which largely inspired Artio.