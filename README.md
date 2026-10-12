# LogicLab: Full Adder & Full Subtractor Simulator

A browser-only React + Three.js learning project. It does not connect to a microcontroller and requires no backend.

## Features
- Switch between full adder and full subtractor.
- Three interactive binary inputs.
- SVG gate-level visualization with signal highlighting.
- Interactive 3D output cubes powered by Three.js / React Three Fiber.
- Live truth table with current row highlighting.
- Boolean equations, intermediate gate values, and a short logic guide.
- Responsive dark interface.

## Requirements
- Node.js 18+ (Node.js 20+ recommended)
- npm
- Internet access for installing packages and loading the optional Google Fonts / Three.js environment preset.

## Run locally

1. Extract the ZIP.
2. Open a terminal in the extracted `digital-logic-lab` folder.
3. Install dependencies:

   ```bash
   npm install
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open the local URL Vite prints, usually `http://localhost:5173`.

## Production build

```bash
npm run build
npm run preview
```

The production-ready static site is created in `dist/`.

## Deploy
The project can be deployed to Vercel, Netlify, or GitHub Pages using the standard Vite deployment flow.

## Logic equations

### Full adder
- `Sum = A XOR B XOR Cin`
- `Cout = (A AND B) OR ((A XOR B) AND Cin)`

Equivalent carry expression: `AB + ACin + BCin`.

### Full subtractor
- `Difference = A XOR B XOR Bin`
- `Bout = ((!A) AND B) OR ((!(A XOR B)) AND Bin)`

Equivalent borrow expression: `A̅B + (A XNOR B)Bin`.

## Notes
- The circuit diagram is rendered in SVG so it stays crisp at different screen sizes.
- The 3D output cubes are genuine WebGL scenes using Three.js through React Three Fiber.
- The visual gate layout is a learning-oriented schematic. The Boolean formulas and truth table are calculated directly from the input bits.
- The website runs calculations locally in the browser; there is no database, API, or backend.
