# 🖥️ Terminal Background Setup Tool

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![React](https://img.shields.io/badge/React-18+-61DAFB?logo=react)
![Tailwind](https://img.shields.io/badge/Tailwind-3.0+-38B2AC?logo=tailwind-css)

**A beautiful, interactive web tool for generating terminal background configurations**

[Features](#-features) • [Demo](#-demo) • [Installation](#-installation) • [Usage](#-usage) • [Supported Terminals](#-supported-terminals) • [Contributing](#-contributing)

</div>

---

## 📖 Overview

Terminal Background Setup Tool is a modern React-based web application that simplifies the process of configuring custom backgrounds for Linux terminal emulators. No more digging through documentation or manually editing config files—just select your terminal, choose your background method, and generate ready-to-use configurations!

## ✨ Features

- 🎯 **6 Terminal Emulators Supported**: Kitty, Alacritty, Konsole, Terminator, Cool Retro Term, and URxvt
- 🖼️ **Multiple Background Types**: Static images, animated GIFs, videos, and live HTML
- 🎨 **Pre-built Presets**: Quick-start templates for popular aesthetics
- 📋 **One-Click Copy**: Copy generated configs directly to clipboard
- 🎚️ **Opacity Control**: Fine-tune transparency with an interactive slider
- 📱 **Responsive Design**: Works perfectly on desktop, tablet, and mobile
- ⚡ **Zero Configuration**: No complex setup—just open and use
- 🎭 **Beautiful UI**: Modern gradient design with smooth animations

## 🎬 Demo

![Terminal BG Setup Demo](assets/demo.gif)

*Note: Add a GIF/screenshot of your app in action*

## 🚀 Quick Start

### Prerequisites

- Node.js 16+ and npm/yarn
- A supported terminal emulator installed on your Linux system

### Installation

```bash
# Clone the repository
git clone https://github.com/x-cessive/terminal-bg-setup.git

# Navigate to project directory
cd terminal-bg-setup

# Install dependencies
npm install

# Start development server
npm run dev
```

The app will be available at `http://localhost:5173`

## 📝 Usage

### Step 1: Select Your Terminal

Choose from 6 popular Linux terminal emulators:

| Terminal | Difficulty | Supports |
|----------|-----------|----------|
| **Kitty** | Easy | Images, GIFs, Videos |
| **Alacritty** | Medium | Images (via compositor) |
| **Konsole** | Easy | Images |
| **Terminator** | Easy | Images |
| **Cool Retro Term** | Easy | Images, GIFs, Videos, HTML |
| **URxvt** | Hard | Images |

### Step 2: Choose Background Method

- 🖼️ **Static Image**: PNG, JPG, or WebP files
- 🎬 **Animated GIF**: Looping animations
- 🎥 **Video Background**: MP4 or WebM videos
- 💻 **Live HTML**: Interactive animations and effects

### Step 3: Upload & Configure

1. Upload your background file
2. Adjust opacity with the slider (0-100%)
3. Click "Generate Configuration"
4. Copy the generated config to your clipboard

### Step 4: Apply Configuration

Paste the configuration into your terminal's config file and restart. Detailed instructions are provided for each terminal!

## 🎨 Quick Presets

Choose from pre-configured themes:

- 💀 **Skeleton VHS**: Retro glitch aesthetic
- 🟢 **Matrix Rain**: Classic falling code effect
- 🌃 **Cyberpunk Neon**: Vibrant neon city vibes
- 🎨 **Minimal Blur**: Clean, focused workspace

## 🔧 Supported Terminals

### Kitty

```bash
# Install
sudo pacman -S kitty

# Config location
~/.config/kitty/kitty.conf
```

**Supports**: Images, GIFs, Videos, Opacity control  
**Reload**: `Ctrl+Shift+F5`

### Alacritty

```bash
# Install
sudo pacman -S alacritty

# Config location
~/.config/alacritty/alacritty.yml
```

**Supports**: Opacity control (images via compositor)  
**Note**: Requires `picom` + `feh` for background images

### Konsole

```bash
# Install
sudo pacman -S konsole

# Config location
~/.local/share/konsole/YourProfile.profile
```

**Supports**: Images, GUI-based configuration  
**Setup**: Settings → Edit Current Profile → Appearance

### Terminator

```bash
# Install
sudo pacman -S terminator

# Config location
~/.config/terminator/config
```

**Supports**: Images with darkness control  
**Reload**: Restart Terminator

### Cool Retro Term

```bash
# Install
yay -S cool-retro-term

# Background location
~/.local/share/cool-retro-term/backgrounds/
```

**Supports**: Images, GIFs, Videos, HTML animations  
**Features**: CRT effects, scanlines, screen curvature

### URxvt

```bash
# Install
sudo pacman -S rxvt-unicode-pixbuf

# Config location
~/.Xresources
```

**Supports**: Images via Pixmap  
**Reload**: `xrdb ~/.Xresources`

## 🛠️ Development

### Project Structure

```
terminal-bg-setup/
├── src/
│   ├── TerminalBGSetup.jsx    # Main component
│   ├── App.jsx                # App wrapper
│   └── main.jsx               # Entry point
├── public/
│   └── assets/                # Static assets
├── package.json
├── vite.config.js
└── README.md
```

### Built With

- **React 18**: UI framework
- **Tailwind CSS**: Styling
- **Lucide React**: Icon library
- **Vite**: Build tool and dev server

### Scripts

```bash
# Development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Lint code
npm run lint
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. 🍴 Fork the repository
2. 🌿 Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. 💾 Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. 📤 Push to the branch (`git push origin feature/AmazingFeature`)
5. 🔀 Open a Pull Request

### Ideas for Contributions

- Add support for more terminal emulators
- Create additional preset themes
- Improve mobile responsiveness
- Add dark/light mode toggle
- Create video tutorials
- Translate documentation

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Inspired by the Linux terminal customization community
- Icons by [Lucide Icons](https://lucide.dev)
- Styled with [Tailwind CSS](https://tailwindcss.com)

## 📧 Contact

**x-cessive** - [@x-cessive](https://github.com/x-cessive)

Project Link: [https://github.com/x-cessive/terminal-bg-setup](https://github.com/x-cessive/terminal-bg-setup)

---

<div align="center">

**⭐ Star this repo if you find it helpful!**

Made with ❤️ for the Linux community

</div>
