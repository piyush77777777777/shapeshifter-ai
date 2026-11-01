# ShapeShifter AI – From a 2D Sketch to a 3D Asset

<div align="center">

![ShapeShifter AI](https://img.shields.io/badge/ShapeShifter-AI%20v2.0-8b5cf6?style=for-the-badge&logo=three.js&logoColor=white)
![In-Browser](https://img.shields.io/badge/WebGL-100%25%20Client--Side-f0abfc?style=for-the-badge)
![Formats](https://img.shields.io/badge/Export-OBJ%20%7C%20STL%20%7C%20PNG-4ade80?style=for-the-badge)
![Deployment](https://img.shields.io/badge/Deploy-GitHub%20Pages%20Ready-blue?style=for-the-badge&logo=github)

<br/>

**Transform 2D hand-drawn sketches into solid, watertight 3D models with natural language prompt guidance, real-time WebGL rendering, and instant CAD/3D-printing export.**

🌐 **Live Demo**: [https://piyush77777777777.github.io/shapeshifter-ai/](https://piyush77777777777.github.io/shapeshifter-ai/)

</div>

---

## 🌟 Overview

**ShapeShifter AI** bridges the gap between rough ideation and physical 3D reality. With an ultra-responsive client-side geometry synthesis engine, users can draw freehand sketches or upload concept art, describe materials through natural language prompts, and preview full watertight 3D meshes in real-time.

- **High-Impact Landing Page**: Showcases core capabilities, 5-stage synthesis pipeline, interactive preset gallery, and industry use cases.
- **Exclusive Free Trial Studio Flow**: Clicking **Free Trial** enters the full-featured 3D synthesis studio.
- **100% Client-Side Privacy**: Runs locally in your browser via WebGL and Three.js — no cloud queue, no GPU latency, zero data uploaded.
- **Production-Ready CAD Exports**: One-click download of `.OBJ` (with vertex colors) and `.STL` (verified for 3D printing slicers).

---

## 🎨 Interactive Preset Gallery

| Preset | Domain | Material & Prompt | Key Highlights |
| :--- | :--- | :--- | :--- |
| **Cottage House** | Architecture | *"A small cottage with a red roof and a wooden door"* | Dual-material separation with pitch gable roof and recessed timber doorway. |
| **Ergonomic Chair** | Furniture | *"A wooden chair with a red cushion"* | Open-line strokes converted into structural support ribs and solid cushion depth. |
| **Cyber Sports Car** | Automotive | *"A red car"* | Aerodynamic silhouette, circular wheel geometries, and cockpit glass canopy. |
| **Organic Pine Tree** | Environment | *"A green tree with a brown trunk"* | Puffy organic crown volume with a rigid, textured timber trunk. |
| **Retro Mech Robot** | Characters | *"A blue robot"* | Multi-box modular humanoid composition with antenna line detail and joint bevels. |
| **Art Deco Lamp** | Industrial | *"A yellow lamp with a black base"* | Warm luminescent lampshade, columnar stem, and weighted stability pedestal. |

---

## 🚀 Key Features

| Feature | Description |
| :--- | :--- |
| **Dual-Pass Distance Field Synthesis** | Converts freehand outlines into high-precision distance-from-edge topological height fields. |
| **Semantic Natural Language Colors** | NLP parser scans prompts for colors (`red`, `blue`, `gold`, `wood`) and accents target regions. |
| **Parametric Sculpting Controls** | Adjust **Thickness** (0.8x - 4.0x), **Smoothness** (0 - 8 iterations), and **Style** (*Puffy*, *Flat*, *Sharp*) in real-time. |
| **Watertight Solid Geometry** | Closed contours are automatically turned into 3D volumes; open lines become structural surface ribs. |
| **360° Real-Time WebGL Viewport** | Orbit with mouse/touch, scroll/pinch to zoom, auto-rotate turntable, and wireframe overlay. |
| **Instant Production Export** | Direct download of `.OBJ` (with vertex colors), `.STL` (for 3D printing), and `.PNG` high-res snapshots. |

---

## 🛠️ The 5-Stage Synthesis Pipeline

```
┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐
│  1. Draw / Drop  │ ──> │  2. Text Prompt  │ ──> │ 3. AI Analysis   │ ──> │ 4. Image-to-3D   │ ──> │ 5. 3D Inspection │
│  480x480 raster  │     │  NLP color scan  │     │ Flood fill mask  │     │ Height field mesh│     │ Orbit, STL, OBJ  │
└──────────────────┘     └──────────────────┘     └──────────────────┘     └──────────────────┘     └──────────────────┘
```

1. **Draw / Upload**: Sketch directly on the paper canvas using your mouse or finger, or upload an image.
2. **Text Prompt**: Type an optional description (e.g. *"A small cottage with a red roof and a wooden door"*).
3. **AI Shape Analysis**: Morphological dilation closes boundary micro-gaps, while exterior flood fill isolates solid bodies.
4. **Image-to-3D Synthesis**: Distance transform generates front and back surfaces connected by continuous quad side walls.
5. **Preview & Export**: Inspect with real-time directional and rim lighting, then export OBJ or STL.

---

## 💻 Local Quickstart

Because ShapeShifter AI is 100% client-side with zero dependencies, you can run it immediately:

```bash
# Option 1: Using Node
node server.js
# Or
npx serve .

# Option 2: Direct file
# Double click index.html
```

Visit [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🌐 Deploy to GitHub Pages

This project is pre-configured with a complete GitHub Actions CI/CD workflow at `.github/workflows/deploy.yml`.

To deploy:
1. Push to your GitHub repository:
   ```bash
   git add .
   git commit -m "Deploy ShapeShifter AI"
   git push origin main
   ```
2. In GitHub, go to **Settings** > **Pages** > **Build and deployment** > Source: **GitHub Actions**.
3. Your site will automatically go live at:
   `https://piyush77777777777.github.io/shapeshifter-ai/`

---

## 📄 License

MIT License &copy; 2026 Piyush Kumar Dey / ShapeShifter AI Team.
