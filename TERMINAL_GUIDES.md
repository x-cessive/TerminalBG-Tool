# Terminal-Specific Setup Guides

Detailed setup instructions for each supported terminal emulator.

## Table of Contents
- [Kitty](#kitty)
- [Alacritty](#alacritty)
- [Konsole](#konsole)
- [Terminator](#terminator)
- [Cool Retro Term](#cool-retro-term)
- [URxvt](#urxvt)

---

## Kitty

### Installation

**Arch Linux:**
```bash
sudo pacman -S kitty
```

**Ubuntu/Debian:**
```bash
sudo apt install kitty
```

**Fedora:**
```bash
sudo dnf install kitty
```

### Configuration Location
`~/.config/kitty/kitty.conf`

### Supported Features
- ✅ Static images (PNG, JPG, WebP)
- ✅ Animated GIFs
- ✅ Video backgrounds (MP4, WebM)
- ✅ Opacity control
- ✅ Tint adjustment

### Example Configuration

```conf
# Kitty Configuration
background_image ~/Pictures/my-wallpaper.png
background_image_layout scaled
background_opacity 0.85
background_tint 0.85

# Optional settings
cursor_blink_interval 0
window_padding_width 10
font_size 12.0
```

### Tips
- Use `Ctrl+Shift+F5` to reload configuration without restarting
- The `background_image_layout` can be: `tiled`, `scaled`, `clamped`, `centered`
- `background_tint` darkens the image (0.0 = black, 1.0 = full brightness)

---

## Alacritty

### Installation

**Arch Linux:**
```bash
sudo pacman -S alacritty
```

**Ubuntu/Debian:**
```bash
sudo apt install alacritty
```

### Configuration Location
`~/.config/alacritty/alacritty.yml`

### Supported Features
- ✅ Opacity control
- ⚠️ Background images require external tools (picom + feh)

### Example Configuration

```yaml
window:
  opacity: 0.85
  padding:
    x: 10
    y: 10
  decorations: full

font:
  size: 11.0
```

### For Background Images

Since Alacritty doesn't natively support background images, use:

1. Install dependencies:
```bash
sudo pacman -S feh picom
```

2. Set background with feh:
```bash
feh --bg-scale ~/Pictures/wallpaper.png
```

3. Add to `~/.xinitrc` or startup applications

---

## Konsole

### Installation

**Arch Linux:**
```bash
sudo pacman -S konsole
```

**Ubuntu/Debian:**
```bash
sudo apt install konsole
```

### Configuration Location
- GUI: Settings → Edit Current Profile
- Manual: `~/.local/share/konsole/YourProfile.profile`

### Supported Features
- ✅ Static images
- ✅ Opacity control
- ✅ GUI-based configuration

### GUI Setup Steps

1. Open Konsole
2. Go to **Settings** → **Edit Current Profile**
3. Navigate to **Appearance** tab
4. Click **Edit** on your color scheme
5. Go to **Background** tab
6. Select **Image** and choose your file
7. Adjust opacity slider
8. Click **Apply** and **OK**

### Manual Configuration

Edit `~/.local/share/konsole/YourProfile.profile`:

```ini
[Appearance]
ColorScheme=Custom
BackgroundImage=file:///home/username/Pictures/bg.png
BackgroundImageOpacity=0.85
```

---

## Terminator

### Installation

**Arch Linux:**
```bash
sudo pacman -S terminator
```

**Ubuntu/Debian:**
```bash
sudo apt install terminator
```

### Configuration Location
`~/.config/terminator/config`

### Supported Features
- ✅ Static images
- ✅ Darkness control (similar to opacity)
- ✅ Multiple layouts

### Example Configuration

```ini
[global_config]
[keybindings]
[profiles]
  [[default]]
    background_image = /home/username/Pictures/bg.png
    background_darkness = 0.85
    background_type = image
    use_system_font = False
    font = Monospace 11
    scrollback_infinite = True
    
[layouts]
  [[default]]
    [[[window0]]]
      type = Window
      parent = ""
    [[[child1]]]
      type = Terminal
      parent = window0
```

### Tips
- Restart Terminator after changing config
- `background_darkness` ranges from 0.0 (darkest) to 1.0 (lightest)
- Set `background_type = transparent` for window transparency

---

## Cool Retro Term

### Installation

**Arch Linux (AUR):**
```bash
yay -S cool-retro-term
```

**Ubuntu/Debian:**
```bash
sudo add-apt-repository ppa:vantuz/cool-retro-term
sudo apt update
sudo apt install cool-retro-term
```

### Background Location
`~/.local/share/cool-retro-term/backgrounds/`

### Supported Features
- ✅ Static images
- ✅ Animated GIFs
- ✅ Video backgrounds
- ✅ HTML animations
- ✅ CRT effects (scanlines, curvature, jitter)
- ✅ Bloom and glow effects

### Setup Steps

1. Copy your background file to:
   ```bash
   ~/.local/share/cool-retro-term/backgrounds/
   ```

2. Launch Cool Retro Term:
   ```bash
   cool-retro-term
   ```

3. Right-click → **Settings**

4. Navigate to **Background** section

5. Select your file from the dropdown

6. Adjust:
   - Opacity
   - Bloom effect
   - Screen effects

### Creating HTML Animations

Create an HTML file with CSS animations:

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    body {
      margin: 0;
      background: linear-gradient(45deg, #667eea 0%, #764ba2 100%);
      animation: gradient 15s ease infinite;
    }
    @keyframes gradient {
      0% { filter: hue-rotate(0deg); }
      100% { filter: hue-rotate(360deg); }
    }
  </style>
</head>
<body></body>
</html>
```

Save to the backgrounds folder and select in settings!

---

## URxvt

### Installation

**Arch Linux:**
```bash
sudo pacman -S rxvt-unicode-pixbuf
```

**Ubuntu/Debian:**
```bash
sudo apt install rxvt-unicode-256color
```

### Configuration Location
`~/.Xresources`

### Supported Features
- ✅ Static images (via Pixmap)
- ✅ Transparency/shading
- ⚠️ More complex to configure

### Example Configuration

Add to `~/.Xresources`:

```xresources
URxvt.backgroundPixmap: /home/username/Pictures/bg.png;100
URxvt.transparent: false
URxvt.shading: 85
URxvt.depth: 32
URxvt.background: [85]#000000

# Font and appearance
URxvt.font: xft:Monospace:size=11
URxvt.scrollBar: false
URxvt.cursorBlink: true
```

### Reload Configuration

```bash
xrdb ~/.Xresources
```

### Tips
- The `;100` after the image path is the scaling percentage
- `shading` ranges from 0 (black) to 100 (full color)
- Requires `rxvt-unicode-pixbuf` package for image support
- True transparency requires a compositor (like picom)

---

## Troubleshooting

### Image Not Showing
- Verify the file path is correct (use absolute paths)
- Check file permissions: `chmod 644 ~/Pictures/your-image.png`
- Ensure the image file exists and is readable

### Configuration Not Loading
- Check for syntax errors in config file
- Try restarting the terminal completely
- Verify you're editing the correct config file

### Performance Issues
- Use lower resolution images
- Avoid very large or high-framerate GIFs/videos
- Reduce opacity for better text readability
- Consider using static images instead of animations

### Colors Look Wrong
- Adjust the tint/darkness settings
- Try a different color scheme
- Use images with appropriate contrast

---

## Additional Resources

- [Kitty Documentation](https://sw.kovidgoyal.net/kitty/)
- [Alacritty Documentation](https://github.com/alacritty/alacritty)
- [Arch Wiki: Konsole](https://wiki.archlinux.org/title/Konsole)
- [Terminator Documentation](https://gnome-terminator.readthedocs.io/)
- [Cool Retro Term GitHub](https://github.com/Swordfish90/cool-retro-term)
- [URxvt Documentation](http://pod.tst.eu/http://cvs.schmorp.de/rxvt-unicode/doc/rxvt.1.pod)
