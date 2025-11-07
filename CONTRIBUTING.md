# Contributing to Terminal Background Setup Tool

First off, thank you for considering contributing to Terminal Background Setup Tool! 🎉

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the issue list as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible:

* **Use a clear and descriptive title**
* **Describe the exact steps which reproduce the problem**
* **Provide specific examples to demonstrate the steps**
* **Describe the behavior you observed after following the steps**
* **Explain which behavior you expected to see instead and why**
* **Include screenshots if relevant**
* **Include your terminal emulator and OS version**

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

* **Use a clear and descriptive title**
* **Provide a step-by-step description of the suggested enhancement**
* **Provide specific examples to demonstrate the steps**
* **Describe the current behavior and explain the behavior you expected to see instead**
* **Explain why this enhancement would be useful**

### Pull Requests

1. Fork the repo and create your branch from `main`
2. If you've added code that should be tested, add tests
3. Ensure the code follows the existing style
4. Make sure your code lints
5. Issue that pull request!

## Development Setup

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/terminal-bg-setup.git

# Navigate to the project
cd terminal-bg-setup

# Install dependencies
npm install

# Start development server
npm run dev
```

## Code Style

* Use 2 spaces for indentation
* Use meaningful variable names
* Comment complex logic
* Follow React best practices
* Use functional components and hooks

## Project Structure

```
terminal-bg-setup/
├── src/
│   ├── TerminalBGSetup.jsx    # Main component
│   ├── App.jsx                # App wrapper
│   ├── main.jsx               # Entry point
│   └── index.css              # Global styles
├── public/                    # Static assets
└── README.md
```

## Adding New Terminal Support

To add support for a new terminal:

1. Add terminal info to the `terminals` array in `TerminalBGSetup.jsx`:
```javascript
{ 
  id: 'newterminal', 
  name: 'New Terminal', 
  supports: ['image', 'gif'], 
  difficulty: 'Easy', 
  popular: false 
}
```

2. Add install command to `installCommands` object:
```javascript
newterminal: 'sudo pacman -S newterminal'
```

3. Add configuration generation logic in the `generateConfig()` switch statement:
```javascript
case 'newterminal':
  config = `# Your config here`;
  break;
```

4. Update the README.md with the new terminal info

## Adding New Presets

To add a new preset theme:

```javascript
{
  id: 'preset-id',
  name: '🎨 Preset Name',
  desc: 'Description of the preset',
  gradient: 'from-color-900 to-color-700',
  opacity: 0.85,
  terminal: 'kitty',
  method: 'image'
}
```

## Commit Messages

* Use the present tense ("Add feature" not "Added feature")
* Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
* Limit the first line to 72 characters or less
* Reference issues and pull requests liberally after the first line

Examples:
* `feat: Add support for Wezterm terminal`
* `fix: Correct opacity calculation for URxvt`
* `docs: Update installation instructions`
* `style: Fix indentation in TerminalBGSetup.jsx`
* `refactor: Simplify config generation logic`

## Questions?

Feel free to open an issue with your question or reach out to [@x-cessive](https://github.com/x-cessive)

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
