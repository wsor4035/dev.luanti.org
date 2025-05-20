---
title: Models
aliases:
  - /models
bookCollapseSection: true
---

# Models

Luanti supports a few different model formats.

### `.obj` Format

Useful for static models, doesn't not support animation.

Models stored in this format are expected to use a size of 1.0 for a single node centered around (0.0, 0.0, 0.0). This means a full node extends from (-0.5, -0.5, -0.5) to (0.5, 0.5, 0.5).

### `.b3d` Format

Originally from the Blitz3D Engine, this format is widespread due to its animation support. You will need [this](https://github.com/GreenXenith/io_scene_b3d) extension to export models from blender. It is recommended that you keep the source .blend file due to importing not being supported in the extension. Using gltf/glb is preferred if you don't mind not supporting older 5.x releases.

### `.x` Format

Alternative to b3d that supports animations. Unless you have a specific reason, should use gltf/glb or b3d.

### `.gltf / .glb` Format

Modern animated model support, added in release 5.10. Using this format means you can't (easily) support versions before 5.10. See [this forum topic](https://forum.luanti.org/viewtopic.php?t=31133) regarding exporting from Blender at this time.

Models stored in this format are expected to use a size of 10 units for a single node centered around (0, 0, 0). This means a full node extends from (-5, -5, -5) to (5, 5, 5).

{{< notice tip >}}
If a model does not work as expected, you can use the [glTF validator](https://github.khronos.org/glTF-Validator/) to check it for [glTF specification](https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html) compliance.
{{< /notice >}}

{{< notice tip >}}
Luanti does not support embedded images in glTF models. You can use [gltfutil](https://github.com/luanti-org/modtools/blob/main/gltfutil.py) to extract or strip textures.
{{< /notice >}}

{{< notice note >}}
In contrast to `.b3d` and `.x`, glTF animation speeds are typically in seconds rather than frames.
When exporting, make sure to use the correct frame rate setting.
When using glTF models in Luanti, you will normally want to use a speed of `1`.
{{< /notice >}}

### Node Boxes Format

{{< notice note >}}
This format is only supported for nodes.
{{< /notice >}}

See https://api.luanti.org/nodes/#node-boxes.

## Editors

- [BlockBench](/for-creators/models/blockbench)
- [Blender](/for-creators/models/using-blender)
