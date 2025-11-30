---
title: High-performance debug rendering library for .NET and OpenGL
description: This is an example project.
image: /assets/img/project_debugDraw_1.png
timespan: Oct. 2025 – Present
link: https://github.com/Felix-CodingClimber/DebugDraw
linkText: GitHub
---

Developed a high-performance debug rendering library for .NET, providing an immediate-mode API for drawing debug primitives in OpenGL-based 3D applications.

The library makes heavy use of modern C# and .NET features like Span<T>, CollectionsMarshal, or ref structs to prevent runtime allocations and provide the best performance possible.

### Features:
- Immediate-mode debug drawing API
- Modern OpenGL GPU-driven instanced rendering with minimal CPU overhead
- No runtime allocations during rendering
- Support for common 3D debug primitives: boxes, spheres, lines, cylinders, cones, capsules, arrows, and grids (wireframe and solid)
- Custom mesh registration support
- Backend implementations for OpenTK and Silk.NET (easy to extend to other OpenGL bindings)
