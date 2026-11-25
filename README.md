# Hephaestus — Professional Drawing & Sketching Engine

Hephaestus is a professional, GPU-accelerated digital drawing, painting, and vector sketching application for Android. Built with Kotlin, Jetpack Compose, and a custom C++ Vulkan/OpenGL ES brush engine, Hephaestus delivers ultra-low-latency stylus input with pressure, tilt, speed, and orientation sensitivity.

---

## 🎨 Key Features & Subsystem Breakdown

### 🖌️ GPU Brush & Stroke Engine (`brush`)
- **Current**: Custom C++ NDK rasterization pipeline, stylus pressure & tilt dynamics, stock brushes (pencil, ink pen, marker, airbrush), stroke smoothing, and linear undo/redo.
- **Planned / Roadmap**: Custom brush dynamics node graph, multi-coat textured brushes, stamp brushes, and wet watercolor blending simulation.

### 🖼️ Multi-Layer Canvas Compositor (`canvas`)
- **Current**: Unlimited layer creation, layer opacity/visibility, blend modes (Multiply, Screen, Overlay, Add), alpha lock, and clipping masks.
- **Planned / Roadmap**: Layer grouping, non-destructive adjustment layers, 3D perspective grids, and symmetry drawing guides.

### 💾 Export & Vector Asset Engine (`export`)
- **Current**: High-resolution PNG, JPEG, and PSD layer export with ICC color profile preservation.
- **Planned / Roadmap**: SVG vector export, timelapse recording exporter, and custom brush preset sharing format.

---

## 🏗️ Architecture & Technology Stack

- **Platform**: Android 13+ (minSdk 33, targetSdk 37).
- **UI & Interface**: Kotlin, Jetpack Compose, Stylus MotionEvent API.
- **Rendering Engine**: C++20 NDK, OpenGL ES 3.2 / Vulkan 1.3 GPU shaders.
- **Licensing**: AGPL-3.0.

---

## 🛠️ Building & Running

```bash
./gradlew assembleDebug
./gradlew installDebug
```

---

## 📜 License

Hephaestus is released under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [`LICENSE`](LICENSE) for details.
