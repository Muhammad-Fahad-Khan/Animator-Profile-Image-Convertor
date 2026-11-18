# 🎞️ Logo & Profile GIF Studio

[![Live Demo](https://img.shields.io/badge/Live_Demo-GitHub_Pages-4f46e5?style=for-the-badge&logo=github)](https://muhammad-fahad-khan.github.io/Animator-Profile-Image-Convertor/)
[![Client-Side](https://img.shields.io/badge/Privacy-100%25_Client--Side-10b981?style=for-the-badge)](#)
[![Output Limit](https://img.shields.io/badge/Google_Profile_Ready-%3C_1_MB-0ea5e9?style=for-the-badge)](#)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero_(Vanilla_JS)-f59e0b?style=for-the-badge)](#)

A high-precision, browser-based GIF animator engineered specifically for **Google Account profile avatars** and **business logos**. Upload one logo or pair two images (such as a portrait and a brand mark) to generate silky-smooth loops up to **60 FPS**—automatically quantized, dithered and compressed strictly under **1 MB** with zero server uploads.

👉 **[Launch Live App](https://muhammad-fahad-khan.github.io/Animator-Profile-Image-Convertor/)**

---

## ✨ Key Features

- **Dual-Image & Single-Image Modes:** Upload 1 logo for continuous looping motion or upload 2 images (`Front` & `Back`)—individually or via multi-file drop—with one-click swapping and independent framing controls.
- **Google Profile Circular Safe-Zone:** Live circular crop overlay and scale slider ensure neither portrait edges nor logo corners get clipped when uploaded to Google Workspace or Gmail accounts.
- **20 Smooth Animation Presets:** 12 dual-image transitions and 8 single-image loops with adjustable **FPS (15–60 FPS)**, loop duration and **Hold Time per Image**.
- **Anti-Pixelation Quantization Engine:**
  - Per-frame **Median-Cut 256-color** adaptive Local Color Tables.
  - Perceptual **Redmean** color distance matching.
  - **Serpentine Floyd-Steinberg Dithering** with selectable modes (*Studio Photo*, *Balanced Hybrid* and *Sharp Logo*).
  - Multi-step bicubic downsampling for crisp edges and smooth skin tones.
- **Guaranteed `< 1 MB` Auto-Optimization:** Built-in GIF89a LZW encoder pairs **Smart Static-Hold Compression** (single-frame delay encoding during stationary pauses) with an automatic size-budget optimizer (`≤ 980 KB`) so every export passes Google's 1 MB avatar limit on the first try.
- **100% Private & Zero-Backend:** All canvas rendering, color quantization and binary LZW encoding execute locally in your browser.

---

## 🎬 Built-In Animation Library

| Dual-Image Transitions (12) | Single-Image Loops (8) |
| :--- | :--- |
| • **3D Coin Flip** (Horizontal Y-Turn) | • **Gentle Pulse / Breathe** |
| • **3D Vertical Flip** (X-Axis Card Turn) | • **Smooth Float / Hover** |
| • **3D Cube Rotate** (Perspective Box Turn) | • **Glossy Light Shine** |
| • **Orbital Spin Switch** | • **3D Coin Spin** |
| • **Circle Iris Wipe** | • **Smooth Spin & Settle** |
| • **Smooth Crossfade** | • **Subtle Zoom & Glow** |
| • **Liquid Blur Morph** | • **Gentle Tilt / Sway** |
| • **Slide & Elastic Swap** | • **Heartbeat Double-Pulse** |
| • **Card Stack Peel** | |
| • **Diagonal Brand Wipe** | |
| • **Heartbeat Pulse Swap** | |
| • **Digital Slice Shift** | |

---

## 🛠️ How It Works Under the Hood

1. **Multi-Step Canvas Sampling:** High-resolution source images are stepped down iteratively on offscreen HTML5 canvases to prevent aliasing before applying per-slot zoom, X/Y pan and `Contain` / `Cover` / `Auto-Blur` backdrop rendering.
2. **Smart Static-Hold Deduplication:** Instead of writing dozens of identical frames while an image pauses between transitions, the encoder emits a single frame with an extended GIF graphic control delay—reserving file-size budget for high-FPS motion frames.
3. **Custom Binary GIF89a LZW Encoder:** Packs per-frame 256-color palettes and variable-width LZW bitstreams directly into a downloadable `Blob` in JavaScript without external libraries or WebAssembly overhead.

---

## 🚀 Local Setup

No build tools, bundlers or package installations are required:

```bash
git clone [https://github.com/muhammad-fahad-khan/Animator-Profile-Image-Convertor.git](https://github.com/muhammad-fahad-khan/Animator-Profile-Image-Convertor.git)
cd Animator-Profile-Image-Convertor
```

Open `index.html` directly in any modern browser (Chrome, Edge, Firefox, Safari) or serve it locally:

```bash
npx serve .
```

---

## 👤 Author

**Muhammad Fahad Khan**  
- Portfolio: [the-mfk.tech](https://the-mfk.tech)  
- LinkedIn: [muhammad-fahad-khan-mfk](https://www.linkedin.com/in/muhammad-fahad-khan-mfk)  
- GitHub: [@muhammad-fahad-khan](https://github.com/muhammad-fahad-khan)
