# WindTurbine Simulation Plugin | EurekaSim C# SDK

This project is a custom simulation plugin built using the EurekaSim C#.NET SDK platform. It implements a fully functional 3D WindTurbine object featuring real-time continuous blade rotation logic built with OpenGL.

## Overview
The 3D model is programmatically assembled using a tapered rectangular tower column that anchors the structure, a rectangular nacelle block housing the simulated generator system at the apex, and a central rotor hub that drives three aerodynamic blades spaced uniformly at 120-degree angles.

## Project Status

- [x] Generated C++ skeleton via EurekaSim Addin Wizard.
- [x] Added `WindTurbine` object configuration parameters.
- [x] Programmed continuous, dynamic 3D blade rotation routines.
- [x] Implement identical plugin logic using C# SDK.
- [ ] Implement identical plugin logic using Python SDK.

## Key Implementation Details

* **Dynamic Animation Engine:** Uses structural rotational matrix transformations (`glPushMatrix`, `glPopMatrix`, and `glRotatef`) to update blade movement continuously on each frame render while keeping the tower stationary.
* **Managed COM Interop Architecture:** Bridges C# .NET Framework logic seamlessly with EurekaSim's native C++ rendering engine and property grids via COM-visible wrappers (`EurekaSim.Net`).
* **Procedural Geometry Generation:** Builds the 32-step circular rotor hub using managed trigonometric functions (`Math.Cos` and `Math.Sin`) and aligns the three aerodynamic blades at 120-degree intervals.

## Video Demonstration

Watch the working C# plugin with running blade rotations in the EurekaSim application:

[![WindTurbine C# Simulation Demo](https://youtube.com)](https://youtu.be)
