# Pixels (Device & CSS Pixels)

- **Device Pixel:** a pixel on a physical screen. For desktops, device and CSS pixels are most often the same but ..
  - on a Retna display, 1 CSS pixel = 2 Device pixels

**Zoom**
- The the user zooms in the CSS pixels get larger (smaller when zoom out). The actuall number of pixels does not chagne but the number of pixels that can be viewed on the screen does. Which brings us to ...

- **The layout viewport:** is similar to device pixels in that its measurements are always the same, regardless of orientation or zoom level. 
- **The visual viewport:** however, varies. This is the part of the page that’s actually shown on the screen at any given point. 

**Mobile phones are crazy**
- the iPhone has a layout viewport width of 980px but, Opera Mobile returns 850px and Android WebKit returns 800px. This means that if you create a 320px element on the iPhone, it will fill up only about a third of the screen real estate.

The fix for this is the viewport tag. It has the following properties
- Width: best to set to device-width which is the actual device width
  <meta name=”viewport” content=”width=device-width” />

- Height
  <meta name=”viewport” content=”height=device-height” />