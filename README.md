# dapocss

dapocss is a lightweight and modern CSS styling framework designed specifically for KEBENET and KEBENET Dapo projects. It provides a clean and consistent design system to streamline the development of beautiful and responsive user interfaces.

The framework is built with **Sass** for better maintainability and scalability, focusing on essential components and utility classes that are relevant to the KEBENET ecosystem.

## ✨ Features

- **Lightweight**: A minimal footprint to ensure fast loading times
- **Sass-powered**: Built with Sass for better maintainability and scalability
- **Branded**: Styles are pre-configured with KEBENET's brand colors
- **Responsive**: Mobile-first design with fluid typography using CSS clamp()
- **Dark Mode**: Automatic dark/light theme support using `prefers-color-scheme`
- **Modern**: Uses CSS custom properties and modern CSS features
- **Modular**: Well-organized Sass architecture for easy customization

## 🚀 Quick Start

### CDN Usage

#### Full Version (Development)
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/kebenet/dapocss@main/dist/style.css">
```

#### Minified Version (Production)
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/kebenet/dapocss@main/dist/style.min.css">
```

### npm Installation
```bash
npm install dapocss
```

## 🛠️ Development

### Prerequisites
- Node.js (v14 or higher)
- npm

### Setup
```bash
# Clone the repository
git clone https://github.com/kebenet/dapocss.git
cd dapocss

# Install dependencies
npm install
```

### Build Commands
```bash
# Build expanded CSS
npm run build

# Build minified CSS
npm run build:min

# Build both versions
npm run build:all

# Watch for changes during development
npm run dev
```

## 📁 Project Structure

```
dapocss/
├── src/                    # Sass source files
│   ├── abstracts/         # Variables, mixins, functions
│   │   ├── _variables.scss # All design tokens
│   │   └── _mixins.scss   # Reusable mixins
│   ├── base/              # Base styles
│   │   ├── _reset.scss    # CSS reset and foundations
│   │   └── _typography.scss # Typography styles
│   ├── components/        # UI components
│   │   ├── _forms.scss    # Form controls
│   │   ├── _tables.scss   # Table styles
│   │   └── _content.scss  # Content elements
│   ├── layout/            # Layout components
│   │   └── _layout.scss   # Layout and print styles
│   └── main.scss          # Main entry point
├── dist/                   # Built CSS files
│   ├── style.css          # Expanded CSS
│   ├── style.min.css      # Minified CSS
│   └── *.map              # Source maps
└── package.json           # Dependencies and scripts
```

## 🎨 Customization

To customize dapocss, edit the variables in `src/abstracts/_variables.scss`:

```scss
// Brand Colors
$primary: hsla(163, 53%, 38%, 1);      // Teal green
$secondary: hsla(23, 84%, 73%, 1);     // Coral orange

// Typography Scale
$text-base: clamp(1rem, 0.45vi + 0.89rem, 1.25rem);
$text-l: clamp(1.56rem, 1.2vi + 1.26rem, 2.22rem);

// Layout
$max-width: 1100px;
$border-radius-base: 6px;
```

Then rebuild the CSS:
```bash
npm run build:all
```

