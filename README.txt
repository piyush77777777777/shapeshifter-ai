ShapeShifter AI - From a 2D Sketch to a 3D Asset
=================================================
HOW TO RUN: double-click index.html (needs internet once, to load Three.js).

FEATURES
- Draw or upload a sketch, add an optional text prompt (colours/materials)
- Generates a smooth solid 3D model, orbit with mouse / pinch to zoom
- Thickness, Smoothness and Style (puffy/flat/sharp) controls
- 6 examples: house, chair, car, tree, robot, lamp
- Wireframe toggle, Save image (PNG), Export OBJ and STL

HOW IT WORKS (honest summary)
Geometry engine, not a trained AI model: sketch -> pixel grid -> fill closed
shapes -> distance-from-edge -> smoothed height field -> front/back/side mesh.
Prompt words are matched to colours. Roadmap: replace the 3D step with an
image-to-3D model such as TripoSR for realistic hidden sides.
Built with Three.js (r128).
