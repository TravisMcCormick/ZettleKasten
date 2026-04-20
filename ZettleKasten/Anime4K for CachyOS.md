# Anime4K for CachyOS

## Install mpv

```bash
sudo pacman -S mpv
```

---

## Create config directories

```bash
mkdir -p ~/.config/mpv/shaders
```

---

## Download shaders

```bash
curl -Lo /tmp/anime4k.zip https://github.com/bloc97/Anime4K/releases/download/v4.0.1/Anime4K_v4.0.zip
unzip /tmp/anime4k.zip -d ~/.config/mpv/shaders/
rm /tmp/anime4k.zip
```

Check the [releases page](https://github.com/bloc97/Anime4K/releases) for a newer version first.

---

## Create input.conf

```bash
vim ~/.config/mpv/input.conf
```

Paste the following (high-end GPU config). Note the `:` separators — required on Linux instead of `;`:

```
CTRL+1 no-osd change-list glsl-shaders set "~~/shaders/Anime4K_Clamp_Highlights.glsl:~~/shaders/Anime4K_Restore_CNN_VL.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_VL.glsl:~~/shaders/Anime4K_AutoDownscalePre_x2.glsl:~~/shaders/Anime4K_AutoDownscalePre_x4.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_M.glsl"; show-text "Anime4K: Mode A (HQ)"
CTRL+2 no-osd change-list glsl-shaders set "~~/shaders/Anime4K_Clamp_Highlights.glsl:~~/shaders/Anime4K_Restore_CNN_Soft_VL.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_VL.glsl:~~/shaders/Anime4K_AutoDownscalePre_x2.glsl:~~/shaders/Anime4K_AutoDownscalePre_x4.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_M.glsl"; show-text "Anime4K: Mode B (HQ)"
CTRL+3 no-osd change-list glsl-shaders set "~~/shaders/Anime4K_Clamp_Highlights.glsl:~~/shaders/Anime4K_Upscale_Denoise_CNN_x2_VL.glsl:~~/shaders/Anime4K_AutoDownscalePre_x2.glsl:~~/shaders/Anime4K_AutoDownscalePre_x4.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_M.glsl"; show-text "Anime4K: Mode C (HQ)"
CTRL+4 no-osd change-list glsl-shaders set "~~/shaders/Anime4K_Clamp_Highlights.glsl:~~/shaders/Anime4K_Restore_CNN_VL.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_VL.glsl:~~/shaders/Anime4K_Restore_CNN_M.glsl:~~/shaders/Anime4K_AutoDownscalePre_x2.glsl:~~/shaders/Anime4K_AutoDownscalePre_x4.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_M.glsl"; show-text "Anime4K: Mode A+A (HQ)"
CTRL+5 no-osd change-list glsl-shaders set "~~/shaders/Anime4K_Clamp_Highlights.glsl:~~/shaders/Anime4K_Restore_CNN_Soft_VL.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_VL.glsl:~~/shaders/Anime4K_AutoDownscalePre_x2.glsl:~~/shaders/Anime4K_AutoDownscalePre_x4.glsl:~~/shaders/Anime4K_Restore_CNN_Soft_M.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_M.glsl"; show-text "Anime4K: Mode B+B (HQ)"
CTRL+6 no-osd change-list glsl-shaders set "~~/shaders/Anime4K_Clamp_Highlights.glsl:~~/shaders/Anime4K_Upscale_Denoise_CNN_x2_VL.glsl:~~/shaders/Anime4K_AutoDownscalePre_x2.glsl:~~/shaders/Anime4K_AutoDownscalePre_x4.glsl:~~/shaders/Anime4K_Restore_CNN_M.glsl:~~/shaders/Anime4K_Upscale_CNN_x2_M.glsl"; show-text "Anime4K: Mode C+A (HQ)"
CTRL+0 no-osd change-list glsl-shaders clr ""; show-text "GLSL shaders cleared"
```

---

## Create mpv.conf

```bash
vim ~/.config/mpv/mpv.conf
```

```ini
profile=high-quality
vo=gpu-next
gpu-api=vulkan
hwdec=auto-copy-safe
```

Alternatively, copy the sample config as a starting point and edit from there:

```bash
cp -r /usr/share/doc/mpv/ ~/.config/
```

---

## Verify installation

Open any video in mpv, press `CTRL+1` to enable Mode A, then press `Shift+I` followed by `2` to open the profiler. You should see several shaders named Anime4K listed as active.

---

## Mode reference

| Key    | Mode | Optimized for                                          |
|--------|------|--------------------------------------------------------|
| CTRL+1 | A    | Most 1080p anime, heavy blur/compression artifacts     |
| CTRL+2 | B    | 720p anime, ringing/downsampling artifacts             |
| CTRL+3 | C    | 480p downscaled, near-pristine sources, wallpapers     |
| CTRL+4 | A+A  | Same as A, highest perceptual quality (requires ≥2x upscale ratio) |
| CTRL+5 | B+B  | Same as B, higher quality                              |
| CTRL+6 | C+A  | Same as C, slightly higher quality                     |
| CTRL+0 | —    | Disable all shaders                                    |

Start with Mode A. If you see ringing artifacts, switch to B. Use the profiler to confirm frame times stay under 41ms for 24fps content.
---

### **Related Notes**

- [[Linux Command Line Basics]]

