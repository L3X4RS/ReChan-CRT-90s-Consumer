<div align="center">

# ReChan CRT 90s Consumer

### Analog CRT presentation for ReChan

[![Platform](https://img.shields.io/badge/platform-Windows%20x64-555555?style=flat-square)](#compatibility)
[![Renderer](https://img.shields.io/badge/renderer-OpenGL-555555?style=flat-square)](#compatibility)
[![Current build](https://img.shields.io/badge/current_build-v1.0.4-555555?style=flat-square)](RELEASE_NOTES_v1.0.4.md)
[![License](https://img.shields.io/badge/license-MIT-555555?style=flat-square)](LICENSE)

A custom CRT post-processing mod for **ReChan**, tuned around the look and feel of a good **1990s consumer CRT television** instead of a heavy modern retro filter.

</div>

---

## About

**ReChan CRT 90s Consumer** is a Windows x64 OpenGL post-process mod for ReChan.

It preserves ReChan's normal rendering resolution and applies the CRT treatment to the final frame, with a visual profile designed around the character of a good consumer television from the 1990s.

The goal is not to make the game look artificially low-resolution. The goal is to make the final image feel like it is being displayed through a convincing CRT presentation.

---

## Visual profile

- Refined CRT scanlines
- Subtle vertical phosphor / aperture-style mask
- Mild RGB separation
- Slightly lifted midtones while retaining dark blacks
- Vivid but controlled color response
- Very light analog noise and flicker
- No temporal ghosting
- No heavy vignette
- No fake 240p downsample
- No TV bezel or physical frame overlay
- Geometry Fix in the current build to remove frame-edge distortion

---

## Current build

### v1.0.4 — FINAL v2 + Geometry Fix

This is the current recommended public build.

The v1.0.4 update preserves the selected **FINAL v2** color, scanline, mask and brightness profile while removing the warp/ripple geometry that caused visible distortion near the borders.

See: [Release notes](RELEASE_NOTES_v1.0.4.md) · [Changelog](CHANGELOG.md)

---

## Download

Binary packages are distributed through **GitHub Releases**:

**[Open Releases](https://github.com/L3X4RS/ReChan-CRT-90s-Consumer/releases)**

Recommended package name:

```text
ReChan_CRT_90s_Consumer_v1.0.4_COMPLETE.zip
```

---

## Installation

1. Back up your current `rechan.exe`.
2. Extract the complete release ZIP into your ReChan folder.
3. Replace files when prompted.
4. Confirm that the mod DLL exists at:

```text
ReChan\~mods\90s Consumer\crtmod.dll
```

5. Launch `rechan.exe` normally.

For more detail, see [INSTALLATION.md](INSTALLATION.md).

---

## Updating

If your current patched `rechan.exe` already loads:

```text
~mods\90s Consumer\crtmod.dll
```

you can normally update by replacing only the DLL.

---

## Removal

Restore your original `rechan.exe`, then remove:

```text
~mods\90s Consumer\
```

---

## Compatibility

- Windows x64
- ReChan Windows build compatible with the prepared executable
- ReChan OpenGL rendering path

The mod hooks the final OpenGL `SwapBuffers` presentation and applies the CRT effect to the already-rendered frame.

It does **not** modify or include PlayStation game data.

---

## Technical notes

The CRT layer is loaded by a small modification to ReChan's Windows executable and intercepts the final OpenGL presentation.

The public visual profile grew out of experiments inspired in part by **newpixie CRT** shader techniques, followed by custom ReChan-specific tuning.

The current public build intentionally avoids temporal persistence/ghosting and avoids reducing the game's internal rendering resolution.

---

## Credits

- **ReChan** — reverse-engineering / reimplementation project by its respective author(s)
- **newpixie CRT** — original shader by Mattias Gustavsson; relevant MIT notice included in `licenses/`
- **ReChan CRT 90s Consumer** — ReChan-specific loader, OpenGL post-process port and visual tuning

See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

---

## Legal

This is an **unofficial community modification**.

It is not affiliated with or endorsed by Sony, the rights holders of *Jackie Chan Stuntmaster*, or the ReChan project maintainers.

No PlayStation game image, ROM, disc data, original game assets, music, voices, textures, models or other copyrighted game content are included.

You must supply any required game data yourself in accordance with ReChan's own instructions and the laws applicable to you.

---

<div align="center">

**ReChan CRT 90s Consumer**  
*Built for the look of a good tube, not a fake retro overlay.*

</div>
