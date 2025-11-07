# 🚀 Quick Start Guide

Get up and running with Terminal Background Setup Tool in under 5 minutes!

## ⚡ Super Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/x-cessive/terminal-bg-setup.git
cd terminal-bg-setup

# 2. Run the setup script
./setup.sh

# 3. Start the development server
npm run dev
```

That's it! The app will open at `http://localhost:5173` 🎉

## 📋 Prerequisites

- **Node.js**: Version 16 or higher ([Download](https://nodejs.org/))
- **npm**: Comes with Node.js
- **A Linux terminal**: Kitty, Alacritty, Konsole, Terminator, Cool Retro Term, or URxvt

## 🎯 Basic Workflow

### Step 1: Select Terminal (Tab 1)
Click on your terminal emulator:
- **Kitty** - Best for videos and GIFs
- **Alacritty** - Fast and minimal
- **Cool Retro Term** - For HTML animations

### Step 2: Choose Method (Tab 2)
Select background type:
- **Image** - Static PNG/JPG
- **GIF** - Animated loops
- **Video** - MP4/WebM files
- **HTML** - Live animations

Upload your file and adjust opacity with the slider.

### Step 3: Generate Config (Tab 3)
1. Click "Generate Configuration"
2. Copy the output to your clipboard
3. Paste into your terminal's config file
4. Restart your terminal

### Quick Option: Use Presets (Tab 4)
Try pre-configured themes:
- 💀 Skeleton VHS
- 🟢 Matrix Rain
- 🌃 Cyberpunk Neon
- 🎨 Minimal Blur

Click "Apply Preset" → Generate → Copy → Done!

## 🛠️ Common Commands

```bash
# Development
npm run dev          # Start dev server
npm run build        # Build for production
npm run preview      # Preview production build
npm run lint         # Check code quality

# Git workflow
git add .
git commit -m "your message"
git push origin main
```

## 📂 Where Are Config Files?

| Terminal | Config Location |
|----------|----------------|
| Kitty | `~/.config/kitty/kitty.conf` |
| Alacritty | `~/.config/alacritty/alacritty.yml` |
| Konsole | `~/.local/share/konsole/YourProfile.profile` |
| Terminator | `~/.config/terminator/config` |
| Cool Retro Term | GUI: Right-click → Settings |
| URxvt | `~/.Xresources` |

## ❓ Troubleshooting

### App Won't Start
```bash
# Clear node_modules and reinstall
rm -rf node_modules
npm install
npm run dev
```

### Background Not Showing
- Check file path is correct
- Use absolute paths (e.g., `/home/user/Pictures/bg.png`)
- Verify file permissions: `chmod 644 yourimage.png`

### Build Errors
```bash
# Update dependencies
npm update
npm audit fix
```

## 🎓 Next Steps

1. **Read the full README**: `README.md`
2. **Check terminal guides**: `docs/TERMINAL_GUIDES.md`
3. **Learn to contribute**: `CONTRIBUTING.md`
4. **See what's new**: `CHANGELOG.md`

## 💡 Pro Tips

- Start with **presets** to learn how it works
- Use **opacity** around 85% for best readability
- **Kitty** has the best native background support
- **Cool Retro Term** is amazing for aesthetic terminals
- Keep images under **2MB** for best performance

## 🆘 Get Help

- 📖 [Full Documentation](README.md)
- 🔧 [Terminal Guides](docs/TERMINAL_GUIDES.md)
- 🐛 [Report Issues](https://github.com/x-cessive/terminal-bg-setup/issues)
- 💬 [GitHub Discussions](https://github.com/x-cessive/terminal-bg-setup/discussions)

## ⭐ Show Your Support

If you find this tool useful:
1. ⭐ Star the repository
2. 🐛 Report bugs
3. 💡 Suggest features
4. 🤝 Contribute code
5. 📢 Share with friends!

---

**Happy Terminal Customizing! 🎨✨**

Back to [Main README](README.md) | [Project Summary](PROJECT_SUMMARY.md)
