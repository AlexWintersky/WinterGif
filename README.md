# WinterGif

<div align="center">

**Lightweight screen capture, frame editing, and GIF export for Windows**

*Fast, intuitive, dark-mode, local-first, and built for creators who want clean GIF workflows without cloud tools.*

![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-1f6feb?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![UI](https://img.shields.io/badge/UI-CustomTkinter-111827?style=for-the-badge)
![Mode](https://img.shields.io/badge/Mode-Offline-0f766e?style=for-the-badge)
![Output](https://img.shields.io/badge/Export-GIF-f59e0b?style=for-the-badge)

</div>

---

## Preview

![WinterGif interface screenshot](assets/wintergif-ui.png)

## What is WinterGif?

**WinterGif** is a lightweight desktop tool for capturing a region of the screen, reviewing frames, trimming unwanted sections, cropping content, and exporting clean animated GIFs.

It was designed to be:

- **Fast to open**
- **Simple to use**
- **Fully local and offline**
- **Friendly for creators and developers**
- **Easy to distribute as a portable Windows app**

No cloud rendering. No account. No browser workflow. Just capture, edit, and export.

---

## Why it stands out

- **Modern dark interface** with a clean visual hierarchy
- **Region-based capture** for focused recordings
- **Frame-aware editing** for quick cleanup before export
- **Selection markers** that make trim operations easier to understand
- **Local-only workflow** for privacy and speed
- **Portable EXE distribution** for non-technical users
- **Bilingual interface** with **English** and **Brazilian Portuguese** support

---

## Core features

| Feature | Description |
|---|---|
| Capture region | Record a custom screen area instead of the full desktop |
| Stop with F8 | Quickly end a capture with a global hotkey |
| Playback preview | Review the animation before exporting |
| Timeline editing | Work with selected ranges and individual frames |
| Keep / Delete selection | Preserve only the important part or remove unwanted ranges |
| Crop tool | Remove unnecessary margins and focus the output |
| Undo support | Revert edits safely |
| GIF export | Save optimized animated GIFs locally |
| Offline operation | No cloud dependency for capture and editing |
| Bilingual UI | Switch between English and Portuguese |

---

## Editing workflow

WinterGif is built around a straightforward workflow:

1. **Capture a region** of the screen
2. **Stop recording** with the interface or **F8**
3. **Preview playback** in the app
4. Use the **range markers** to define the portion you want to keep or remove
5. **Delete a frame** if necessary
6. **Crop** the visible area if needed
7. **Export** the final GIF

This makes it ideal for:

- software demos
- UI showcases
- gameplay snippets
- animation previews
- tutorial clips
- portfolio material for GitHub and documentation

---

## Download and use

### For end users

Download **`WinterGif-Windows-x64.zip`** from [GitHub Releases](../../releases), extract the folder, and open:

```text
WinterGif.exe
```

### End-user highlights

- No Python installation required
- No terminal window required
- No internet required after download
- Everything runs locally on Windows

> Keep the `_internal` folder next to `WinterGif.exe` when using the packaged build.

---

## Build the Windows EXE

This repository includes a simple build launcher:

```text
BUILD_EXE.bat
```

Double-click it on a **Windows 10/11 64-bit** machine with **Python 3.10+** installed.

The script will:

1. Detect a compatible local Python installation
2. Create a temporary build environment
3. Install dependencies and PyInstaller
4. Run basic tests
5. Generate a portable release folder
6. Create a final ZIP ready for distribution

### Generated output

```text
WinterGif-Release/
  WinterGif.exe
  _internal/
  LEIA-ME.txt
  SHA256.txt

WinterGif-Windows-x64.zip
```

This output is ready to upload to **GitHub Releases**.

---

## Build automatically with GitHub Actions

If you do not want to build locally:

1. Push the source repository, including `.github/workflows/build-windows.yml`
2. Open the **Actions** tab
3. Run **Build portable Windows app**
4. Download the generated artifact
5. Upload it to **Releases**

---

## Project structure

```text
WinterGif.py             # Main application code
WinterGif.pyw            # GUI entry point without console
BUILD_EXE.bat            # Double-click Windows build launcher
build_release.ps1        # Build and packaging logic
RELEASE-README.txt       # Included in the release folder
requirements.txt         # Runtime dependencies
tests/                   # Basic automated tests
assets/                  # README images and visual assets
.github/workflows/       # Optional CI build pipeline
```

---

## Tech stack

- **Python**
- **CustomTkinter** for the dark desktop UI
- **MSS** for fast screen capture
- **Pillow** for image processing and GIF export
- **PyInstaller** for Windows packaging

---

## Notes

- GIF files do **not** contain audio
- Large captures or long recordings will use more memory
- Windows may show a SmartScreen warning because the app is unsigned
- Compiled binaries should always be tested on Windows before public release

---

## License

No open-source license has been selected yet.

If you want others to reuse, modify, or redistribute the code, add a license such as **MIT**.

---

## Portuguese summary / Resumo em português

**WinterGif** é uma ferramenta leve para **capturar uma região da tela, editar frames e exportar GIFs** com uma interface moderna em modo escuro.

Principais pontos:

- roda localmente
- não depende de nuvem
- permite capturar, visualizar, cortar e exportar GIFs
- possui interface em **inglês** e **português do Brasil**
- pode ser distribuído como **aplicativo portátil para Windows**

---

## Status

**Current version:** `v1.2.0`

The app is already usable and the project is being refined for better portability, UX polish, and public showcase quality.
