# Installation Guide

Complete installation instructions for Terminal Background Setup Tool.

## Table of Contents
- [System Requirements](#system-requirements)
- [Quick Start](#quick-start)
- [Detailed Installation](#detailed-installation)
- [Terminal Emulator Setup](#terminal-emulator-setup)
- [Troubleshooting](#troubleshooting)

---

## System Requirements

### Software Requirements
- **Node.js**: v16.0.0 or higher
- **npm**: v8.0.0 or higher (or yarn/pnpm)
- **Git**: For cloning the repository
- Modern web browser (Chrome, Firefox, Safari, Edge)

### Operating System
- Linux (primary target)
- macOS (limited support)
- Windows WSL2 (experimental)

### Recommended
- 4GB RAM minimum
- 1GB free disk space
- Internet connection for dependencies

---

## Quick Start

The fastest way to get up and running:

```bash
# Clone the repository
git clone https://github.com/x-cessive/terminal-bg-setup.git

# Navigate to directory
cd terminal-bg-setup

# Install dependencies
npm install

# Start development server
npm run dev
```

Open your browser to `http://localhost:3000` and you're ready!

---

## Detailed Installation

### Step 1: Clone the Repository

```bash
# HTTPS
git clone https://github.com/x-cessive/terminal-bg-setup.git

# OR SSH
git clone git@github.com:x-cessive/terminal-bg-setup.git

# Navigate to project
cd terminal-bg-setup
```

### Step 2: Install Dependencies

Using npm:
```bash
npm install
```

Using yarn:
```bash
yarn install
```

Using pnpm:
```bash
pnpm install
```

### Step 3: Verify Installation

Check that all dependencies are installed:
```bash
npm list --depth=0
```

Expected core dependencies:
- react@^18.2.0
- react-dom@^18.2.0
- lucide-react@^0.294.0

### Step 4: Run Development Server

```bash
npm run dev
```

The application should open automatically at `http://localhost:3000`.

### Step 5: Build for Production (Optional)

```bash
npm run build
```

This creates an optimized build in the `dist` folder.

---

## Terminal Emulator Setup

To use the generated configurations, you'll need the terminal emulators installed.

### Arch Linux / Manjaro

```bash
# Kitty
sudo pacman -S kitty

# Alacritty
sudo pacman -S alacritty

# Konsole
sudo pacman -S konsole

# Terminator
sudo pacman -S terminator

# URxvt (with pixbuf support)
sudo pacman -S rxvt-unicode-pixbuf

# Cool Retro Term (AUR)
yay -S cool-retro-term
```

### Ubuntu / Debian

```bash
# Kitty
sudo apt install kitty

# Alacritty
sudo apt install alacritty

# Konsole
sudo apt install konsole

# Terminator
sudo apt install terminator

# URxvt
sudo apt install rxvt-unicode
```

### Fedora

```bash
# Kitty
sudo dnf install kitty

# Alacritty
sudo dnf install alacritty

# Konsole
sudo dnf install konsole

# Terminator
sudo dnf install terminator
```

### macOS

```bash
# Using Homebrew
brew install --cask kitty
brew install --cask alacritty
```

---

## Configuration File Locations

After generating configurations, place them in these locations:

### Kitty
```
~/.config/kitty/kitty.conf
```

### Alacritty
```
~/.config/alacritty/alacritty.yml
# OR
~/.config/alacritty/alacritty.toml  (newer versions)
```

### Konsole
```
~/.local/share/konsole/YourProfile.profile
```

### Terminator
```
~/.config/terminator/config
```

### Cool Retro Term
```
~/.local/share/cool-retro-term/backgrounds/
```

### URxvt
```
~/.Xresources
```

---

## Troubleshooting

### Port Already in Use

If port 3000 is already in use:

```bash
# Edit vite.config.js and change port
export default defineConfig({
  server: {
    port: 3001, // Change to different port
  }
})
```

### Dependencies Installation Failed

Try clearing npm cache:
```bash
npm cache clean --force
rm -rf node_modules package-lock.json
npm install
```

### Module Not Found Errors

Ensure all required packages are installed:
```bash
npm install react react-dom lucide-react
npm install -D tailwindcss postcss autoprefixer vite @vitejs/plugin-react
```

### Build Fails

Check Node.js version:
```bash
node --version  # Should be v16+
```

Update Node.js if needed:
```bash
# Using nvm
nvm install 18
nvm use 18
```

### Terminal Background Not Showing

1. **Check file path**: Ensure the image path in config is correct
2. **Verify permissions**: File should be readable
3. **Restart terminal**: Some terminals need restart to apply changes
4. **Check terminal version**: Older versions may not support backgrounds

#### Alacritty Specific
Alacritty doesn't support backgrounds natively. Use `feh` or `picom`:

```bash
# Install feh
sudo pacman -S feh

# Set background
feh --bg-scale ~/Pictures/wallpaper.png
```

#### URxvt Specific
Make sure you have the pixbuf version:
```bash
sudo pacman -S rxvt-unicode-pixbuf
```

Reload Xresources:
```bash
xrdb ~/.Xresources
```

---

## Environment Variables

You can customize the application with environment variables:

Create a `.env` file in the project root:
```env
VITE_PORT=3000
VITE_HOST=localhost
```

---

## Docker Installation (Optional)

For containerized deployment:

```bash
# Build image
docker build -t terminal-bg-setup .

# Run container
docker run -p 3000:3000 terminal-bg-setup
```

*(Dockerfile not included in v1.0.0, planned for future release)*

---

## Updating

To update to the latest version:

```bash
cd terminal-bg-setup
git pull origin main
npm install
npm run dev
```

---

## Uninstalling

To completely remove the application:

```bash
cd ..
rm -rf terminal-bg-setup
```

To remove terminal backgrounds:
1. Remove or comment out background lines from terminal config files
2. Restart your terminal

---

## Getting Help

If you encounter issues not covered here:

1. Check [GitHub Issues](https://github.com/x-cessive/terminal-bg-setup/issues)
2. Search [Discussions](https://github.com/x-cessive/terminal-bg-setup/discussions)
3. Create a new issue with:
   - Operating system and version
   - Node.js version
   - Error messages
   - Steps to reproduce

---

## Next Steps

After installation:
1. Read the [README.md](README.md) for usage instructions
2. Check out [CONTRIBUTING.md](CONTRIBUTING.md) to contribute
3. Explore the preset themes in the application
4. Customize your terminal!

---

**Happy terminal customizing!** 🎨
