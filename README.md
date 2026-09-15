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

## Technical Comparison

The table below compares the current **UNISEFE CAD 3D v0.0.2 Alpha**
with established CAD systems.

This is not intended as a claim of overall superiority.
It compares architectural characteristics and currently available capabilities.

| Area | UNISEFE CAD 3D | Onshape | Autodesk Fusion | Tinkercad | OpenSCAD |
|---|---|---|---|---|---|
| Runs directly in browser | Yes | Yes | Yes* | Yes | No |
| Single static HTML possible | **Yes** | No | No | No | No |
| Backend required for core CAD | **No** | Yes | Cloud-connected | Yes | No |
| Native 3D wireframe editing | **Yes** | Yes | Yes | Limited | Script-based |
| Native lines / arcs / circles | **Yes** | Yes | Yes | Limited | Primarily constructive |
| XYZ Move / Copy / Rotate / Mirror | **Yes** | Yes | Yes | Partial | Script transformations |
| Orbit | **Yes** | Yes | Yes | Yes | Yes |
| Extrude | **Yes** | Yes | Yes | Yes | Yes |
| Revolve | **Yes** | Yes | Yes | Limited | Yes |
| 3D dimensions | **Yes** | Yes | Yes | No | No |
| Screen-space readable dimension text | **Yes** | Yes | Yes | No | No |
| Automatic coincidence from Δ = 0 | **Yes** | Constraint system | Constraint system | No | Code-defined |
| Parametric relationships | Early Alpha | Advanced | Advanced | Limited | Advanced / code-based |
| Surface modelling | Not yet | Advanced | Advanced | Limited | Limited |
| Solid modelling | Not yet | Advanced | Advanced | Yes | CSG |
| Boolean solids | Not yet | Advanced | Advanced | Yes | Yes |
| NURBS / advanced surfaces | No | Yes | Yes | No | No |
| Assemblies | No | Yes | Yes | No | No |
| CAM | No | Available | Advanced | No | No |
| Simulation | No | Available | Advanced | No | No |
| CAD state directly inspectable as web markup | **Yes** | No | No | No | Source script |
| Custom geometry logic without external engine | **Yes** | FeatureScript | API / extensions | Limited | **Yes** |
| Offline standalone file | **Yes** | No | Limited | No | Yes |
| Current maturity | **Alpha** | Production | Production | Production | Production |

\* Autodesk Fusion now provides browser access for eligible users, while its main platform also remains strongly cloud-connected.

### Architectural Focus

UNISEFE CAD 3D currently does not attempt to match mature commercial CAD
systems feature-for-feature.

Its experimental focus is different:

- a single geometric space;
- native XYZ geometry;
- a self-contained HTML application;
- no mandatory backend for the CAD core;
- geometry and state directly represented in the document;
- minimal separation between 2D and 3D operations;
- automatic geometric relationships such as coincidence through `Δ = 0`;
- reuse of fundamental transformations rather than separate modelling engines.

For example:

- **Extrude** is derived from a translation along a plane normal.
- **Revolve** is derived from rotation around a 3D axis.
- **3D constraints** can emerge from geometric coincidence.
- The same Move / Copy / Rotate logic is reused across the 3D environment.

### Current Limitations

UNISEFE CAD 3D is still an Alpha project.

The most important missing areas are currently:

- continuous surface representation;
- solid representation;
- robust 3D Boolean operations;
- general 3D fillet / chamfer;
- advanced constraint solving;
- assemblies;
- manufacturing and simulation workflows.

These limitations are intentional areas of ongoing research rather than hidden capabilities.
---

UNISEFE
