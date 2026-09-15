# UNISEFE-WEB-CAD-3D
WEB CAD 3D
# UNISEFE CAD 3D

**UNISEFE CAD 3D · v0.0.1 Alpha**

Experimental 3D wireframe CAD running entirely in static HTML.

## Live Demo

[Open UNISEFE CAD 3D](https://riccardobasti.github.io/UNISEFE-WEB-CAD-3D/)

## Main Features

- 3D lines
- 3D circles
- 3D arcs
- Orbit
- Snap
- Selection
- Move
- Copy
- 3D Rotate
- 3D Mirror
- Trim
- Extend
- Extrude
- Revolve
- Undo
- Save / Open
- Automatic coincidence constraints through `Δ = 0`

## Philosophy

UNISEFE CAD 3D is based on a single geometric system.

The transition from 2D to 3D does not introduce a separate geometry engine: the same entities and transformations are extended into `XYZ` space.

Main principles:

- Native geometry
- No mesh required for wireframe geometry
- Arcs and circles remain native curves
- Real XYZ transformations
- Automatic geometric constraints
- `Δ = 0` as the coincidence condition
- Simple and direct interface
- No backend required

## 3D Commands

### Orbit

Allows free rotation of the view in 3D space.

### Extrude

Extrusion is treated as a geometric transformation:

`P' = P + n · d`

The selected geometry is copied along the normal of its plane.

### Revolve

Revolve uses a true 3D rotation around an axis:

`P' = ROTATE_AXIS(P, axis, θ)`

## Automatic Constraints

When two points are geometrically coincident:

`Δ = 0`

their coincidence is automatically preserved during subsequent editing operations.

No separate coincidence constraint needs to be manually created.

## Status

**Alpha**

This version is intended for testing, experimentation and development.

3D Fillet is still under refinement.

## Run Locally

No installation is required.

Simply open:

`index.html`

in a modern web browser.

## License

To be defined.

---

UNISEFE
