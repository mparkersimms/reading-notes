# Class 12 
## [Home Page](../README.md)

#### References:


Read this article on the Chart.js API.

Chart.js docs: You’ll be needing these!

Read the following articles on the Canvas API.

Basic usage
Drawing shapes with canvas
Applying styles and colors
Drawing text

Using Chart.js

- download the plugin 

- drawing a line chart
- then ad the dimensions of the chart
- declare the variable
- set lables and data sets, color options

- drawing a pie chart is very similar

the <`canvas`> element

- looks alot like and img element at first

- but it doesnt have a src and alt attributes

- you can set using DOM properties

- styled like normal.. 

- initially be fully transparent

- if specifying a fallback you need a closing tag

- use getContext(); to obtain rendering context and its drawing functions

- `var canvas = document.getElementById('tutorial');
var ctx = canvas.getContext('2d');`

Drawing shapes with canvas 

- Normally 1 unit in the grid corresponds to 1 pixel on the canvas. The origin of this grid is positioned in the top left corner at coordinate (0,0).

- All elements are placed relative to this origin

- fillRect(x, y, width, height)
Draws a filled rectangle.

- strokeRect(x, y, width, height)
Draws a rectangular outline.

- clearRect(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.

Drawing Paths

- beginPath()
Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.

- Path methods
Methods to set different paths for objects.  

- closePath()
Adds a straight line to the path, going to the start of the current sub-path.

- stroke()
Draws the shape by stroking its outline.

- fill()
Draws a solid shape by filling the path's content area.

- moveTo(x, y)
Moves the pen to the coordinates specified by x and y.

- lineTo(x, y)
Draws a line from the current drawing position to the position specified by x and y.

-  arc(x, y, radius, startAngle, endAngle, anticlockwise)
Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).
- arcTo(x1, y1, x2, y2, radius)
Draws an arc with the given control points and radius, connected to the previous point by a straight line.

- quadraticCurveTo(cp1x, cp1y, x, y)
Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.

- bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)
Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).

- rect(x, y, width, height)
Draws a rectangle whose top-left corner is specified by (x, y) with the specified width and height.

- Path2D()
The Path2D() constructor returns a newly instantiated Path2D object, optionally with another path as an argument (creates a copy), or optionally with a string consisting of SVG path data.


applying styles and colors

- fillStyle = color
Sets the style used when filling shapes.
- strokeStyle = color
Sets the style for shapes' outlines.

- globalAlpha = transparencyValue
Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.

- lineWidth = value
Sets the width of lines drawn in the future.

- lineCap = type
Sets the appearance of the ends of lines.

- lineJoin = type
Sets the appearance of the "corners" where lines meet.

- miterLimit = value
Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.

- getLineDash()
Returns the current line dash pattern array containing an even number of non-negative numbers.

- setLineDash(segments)
Sets the current line dash pattern.

- lineDashOffset = value
Specifies where to start a dash array on a line.

- createLinearGradient(x1, y1, x2, y2)
Creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2).

- createRadialGradient(x1, y1, r1, x2, y2, r2)
Creates a radial gradient. The parameters represent two circles, one with its center at (x1, y1) and a radius of r1, and the other with its center at (x2, y2) with a radius of r2.

- gradient.addColorStop(position, color)
Creates a new color stop on the gradient object. The position is a number between 0.0 and 1.0 and defines the relative position of the color in the gradient, and the color argument must be a string representing a CSS <color>, indicating the color the gradient should reach at that offset into the transition.

- createPattern(image, type)
Creates and returns a new canvas pattern object. image is a CanvasImageSource (that is, an HTMLImageElement, another canvas, a <video> element, or the like. type is a string indicating how to use the image.
- repeat
Tiles the image in both vertical and horizontal directions.

- repeat-x
Tiles the image horizontally but not vertically.

- repeat-y
Tiles the image vertically but not horizontally.

- no-repeat
Doesn't tile the image. It's used only once.

- shadowOffsetX = float
Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

- shadowOffsetY = float
Indicates the vertical distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

- shadowBlur = float
Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.

- shadowColor = color
A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.

- fillText(text, x, y [, maxWidth])
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.

- strokeText(text, x, y [, maxWidth])
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.