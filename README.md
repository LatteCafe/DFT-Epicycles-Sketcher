# Fourier Epicycles

An interactive visualization of Fourier series and discrete Fourier transforms (DFT) using rotating epicycles.

The application reconstructs 2D shapes from Fourier components and renders the resulting path in real time using HTML5 Canvas.

## Features

* Real-time epicycle animation
* Multiple built-in parametric shapes

  * Heart
  * Star
  * Infinity
  * Trefoil
  * Lissajous
  * Rose
  * Spiral
  * Butterfly
* Adjustable parameters

  * Number of circles
  * Animation speed
  * Sampling resolution
  * Trail length
* SVG import support
* Responsive canvas rendering
* Keyboard shortcuts
* Pure HTML/CSS/JavaScript (no build step)

\---

## Demo

Open the HTML file directly in a browser:

```bash
open fourier-epicycles.html
```

Or simply double-click the file.

\---

## Controls

|Action|Shortcut|
|-|-|
|Play / Pause|Space|
|Reset|R|
|Toggle Circles|C|

\---

## How It Works

1. A shape is sampled into a sequence of 2D points.
2. The points are treated as complex numbers.
3. A Discrete Fourier Transform (DFT) is computed.
4. Fourier coefficients are sorted by amplitude.
5. Rotating vectors (epicycles) reconstruct the shape over time.

The reconstruction uses:

\[
Z\_k = \\sum\_{n=0}^{N-1} z\_n e^{-2\\pi i kn/N}
]

where each coefficient corresponds to:

* frequency
* amplitude
* phase

\---

## SVG Import

You can drag and drop SVG files into the interface.

Supported SVG elements:

* `path`
* `circle`
* `ellipse`
* `rect`
* `polygon`
* `polyline`

Imported geometry is sampled and reconstructed using Fourier components.
Works best with continuous lines.
\---

## File Structure

```text
fourier-epicycles.html
```

Everything is self-contained in a single file:

* UI
* rendering
* DFT implementation
* SVG parsing
* animation loop

\---

## Browser Support

Works in modern browsers supporting:

* Canvas API
* ResizeObserver
* SVG geometry APIs
* ES6 JavaScript

Tested in:

* Chrome
* Firefox
* Edge

\---

## License

MIT License

