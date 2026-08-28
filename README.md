<div align="center">

# ReChan CRT 90s Consumer

### Analog CRT presentation for ReChan

[![Platform](https://img.shields.io/badge/platform-Windows%20x64-555555?style=flat-square)](#compatibility)
[![Renderer](https://img.shields.io/badge/renderer-OpenGL-555555?style=flat-square)](#compatibility)
[![Release](https://img.shields.io/badge/release-v1.0.4-555555?style=flat-square)](#download)
[![Status](https://img.shields.io/badge/status-community%20mod-555555?style=flat-square)](#legal)

A custom CRT post-processing mod for **ReChan**, tuned around the look and feel of a good **1990s consumer CRT television** rather than a heavy modern retro filter.

</div>

---

## Preview

### Original ReChan output

![ReChan without 90s Consumer](assets/before.png)

### ReChan CRT 90s Consumer

![ReChan with 90s Consumer](assets/after.png)

> Preview images are representative development captures. Final output can vary slightly with resolution, display scaling and ReChan build.

---

## What it does

**90s Consumer** is a native Windows x64 post-process layer loaded by a prepared ReChan executable. It keeps ReChan rendering at its normal resolution and applies the CRT presentation at the final OpenGL frame.

The visual target is a clean late-80s/90s consumer tube: visible scanlines, a subtle phosphor-style mask, controlled color response and a small amount of analog character without turning the image into a blurry nostalgia preset.

### Visual profile

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
- Border-safe geometry in the current build

---

## Download

### Current build — v1.0.4

**FINAL v2 visual tuning + Geometry Fix**

Download the complete package from the repository's **Releases** section.

For manual repository downloads, the packaged build can also be added under:

`release/ReChan_CRT_90s_Consumer_v1.0.4_COMPLETE.zip`

---

## Installation

1. Back up your current `rechan.exe`.
2. Extract the release ZIP into your ReChan folder.
3. Allow the included `rechan.exe` to replace the existing executable.
4. Confirm that this file exists:

```text
ReChan\~mods\90s Consumer\crtmod.dll
```

5. Launch `rechan.exe` normally.

### Updating from an older 90s Consumer build

If your patched `rechan.exe` already loads `~mods\90s Consumer\crtmod.dll`, you can normally update by replacing only:

```text
~mods\90s Consumer\crtmod.dll
```

---

## Removal

Restore your original `rechan.exe`, then remove:

```text
~mods\90s Consumer\
```

---

## Compatibility

- Windows x64
- ReChan Windows build compatible with the included patched executable
- ReChan OpenGL rendering path

The mod hooks the final OpenGL buffer presentation. It does **not** modify or include PlayStation game data.

---

## Technical notes

The DLL is loaded by a small modification to ReChan's Windows executable and intercepts the final OpenGL `SwapBuffers` presentation. The current effect is rendered as a post-process pass over the already-rendered frame.

The public visual profile grew out of experiments inspired in part by **newpixie CRT** shader techniques, followed by custom tuning for ReChan. The project includes the applicable third-party license notices.

Current public profile intentionally avoids temporal persistence/ghosting and avoids reducing the game's internal rendering resolution.

---

## Credits

- **ReChan** — reverse-engineering / reimplementation project by its respective author(s).
- **newpixie CRT** — original shader by Mattias Gustavsson; adapted in libretro shader collections. Relevant MIT notice is included in `licenses/`.
- **90s Consumer** — ReChan-specific loader, OpenGL post-process port and visual tuning.

---

## Legal

This is an **unofficial community modification**. It is not affiliated with or endorsed by Sony, the rights holders of Jackie Chan Stuntmaster, or the ReChan project maintainers.

No PlayStation game image, ROM, disc data, original game assets, music, voices, textures, models or other copyrighted game content are included.

You must supply any required game data yourself in accordance with ReChan's own instructions and the laws applicable to you.

---

<div align="center">

**ReChan CRT 90s Consumer**  
*Built for the look of a good tube, not a fake retro overlay.*

</div>
