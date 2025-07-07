# DapoCSS - The KEBENET Design System

DapoCSS is the core CSS framework and design system for all **KEBENET** and **KEBENET Dapo** projects. It is built with a "design-first" philosophy, starting with a robust, standalone CSS/Sass foundation that will evolve into a complete Lit component library.

This repository currently represents **Phase 1** of our component strategy: a lightweight, modern, and maintainable styling framework. It provides a consistent design language, a responsive grid, and a rich set of pre-configured KEBENET brand styles to streamline the development of beautiful user interfaces.

## ✨ Features

-   **Design-First Architecture**: Establishes a solid foundation of styles, naming conventions, and design tokens before component logic.
-   **Sass-powered**: Built with Sass for modularity, maintainability, and scalability.
-   **KEBENET Branded**: All styles are pre-configured with KEBENET's primary and secondary brand colors.
-   **Responsive First**: Mobile-first design with a flexible grid and fluid typography using CSS `clamp()`.
-   **Automatic Dark Mode**: Seamlessly supports light and dark themes using the `prefers-color-scheme` media query.
-   **Modern CSS**: Leverages CSS custom properties for dynamic and themeable components.
-   **Future-Proof**: Designed as the source of truth for an upcoming Lit component library.

## 🗺️ Component Strategy Roadmap

Our goal is to create a robust and scalable component ecosystem. We are approaching this in three distinct phases:

### **Phase 1: The Design Foundation (Current)**
-   **Focus**: Define and perfect the visual language of KEBENET components using custom tags and CSS/Sass.
-   **Outcome**: A stable, standalone CSS framework (`dapocss`) that establishes our brand's look, feel, and style architecture. This includes design tokens, class names, and responsive behaviors.

### **Phase 2: The Transformation Engine (Future)**
-   **Focus**: Develop an automated toolchain.
-   **Outcome**: A build process that can parse the styles and structure defined in Phase 1 to programmatically generate the boilerplate for Lit components. This will ensure perfect consistency between our CSS framework and our future web components.

### **Phase 3: The Lit Component Library (Future)**
-   **Focus**: Release a full suite of interactive components.
-   **Outcome**: A library of highly optimized, reusable, and encapsulated Lit components (e.g., `<kebenet-card>`, `<kebenet-button>`). These components will be ready for use in any modern web application, providing both the KEBENET style and functionality out of the box.

## 🚀 Quick Start

### CDN Usage

#### Full Version (Development)
```html
<link rel="stylesheet" href="[https://cdn.jsdelivr.net/gh/kebenet/dapocss@main/dist/style.css](https://cdn.jsdelivr.net/gh/kebenet/dapocss@main/dist/style.css)">

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

