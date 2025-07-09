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

# DapoCSS Layout Components

A comprehensive guide to using DapoCSS layout components including sections, grids, and responsive columns.

## Table of Contents
- [Container](#container)
- [Sections](#sections)
- [Grid System](#grid-system)
- [Cards](#cards)
- [Complete Examples](#complete-examples)

## Container

The container wraps your content and provides centered layout with automatic margins.

```html
<container>
    <!-- Your content goes here -->
</container>

<!-- Alternative syntax -->
<div class="container">
    <!-- Your content goes here -->
</div>
```

## Sections

Sections provide vertical spacing and can have background colors, gaps, and padding.

### Basic Section
```html
<section>
    <h1>Basic Section</h1>
    <p>Content goes here</p>
</section>
```

### Section with Gap
Adds spacing between child elements:
```html
<section gap>
    <header>
        <h3>Section Header</h3>
    </header>
    <div class="row">
        <!-- Grid content -->
    </div>
</section>
```

### Section with Padding
Adds internal padding:
```html
<section pad>
    <div class="row">
        <!-- Content with padding -->
    </div>
</section>
```

### Section with Background Colors
```html
<!-- Light background -->
<section bg="primary-light">
    <h2>Light Background Section</h2>
</section>

<!-- Primary background -->
<section bg="primary">
    <h2>Primary Background Section</h2>
</section>

<!-- Secondary background -->
<section bg="secondary-light">
    <h2>Secondary Light Background</h2>
</section>
```

## Grid System

DapoCSS uses a 12-column grid system with responsive breakpoints.

### Basic Row and Columns
```html
<div class="row">
    <div class="col-4">Column 1 (4/12)</div>
    <div class="col-4">Column 2 (4/12)</div>
    <div class="col-4">Column 3 (4/12)</div>
</div>
```

### Responsive Columns
```html
<div class="row">
    <div class="col-12 col-sm-6 col-md-4">
        <!-- Full width on mobile, half on small screens, 1/3 on medium+ -->
    </div>
    <div class="col-12 col-sm-6 col-md-8">
        <!-- Full width on mobile, half on small screens, 2/3 on medium+ -->
    </div>
</div>
```


### Grid Element (Alternative to Row)
```html
<!-- Basic grid -->
<grid>
    <card>Card 1</card>
    <card>Card 2</card>
    <card>Card 3</card>
</grid>

<!-- Two-column grid -->
<grid two>
    <card>Card 1</card>
    <card>Card 2</card>
</grid>

<!-- Grid with borders -->
<grid border>
    <card>Card 1</card>
    <card>Card 2</card>
</grid>
```

## Cards

Cards are flexible content containers with optional headers, content, and footers.

### Basic Card
```html
<card>
    <header>
        <h3>Card Title</h3>
    </header>
    <content>
        Card content goes here.
    </content>
    <footer>
        <button>Action</button>
    </footer>
</card>
```

### Card with Image
```html
<card border>
    <img src="image.jpg" alt="Card image">
    <content>
        Description of the image content.
    </content>
    <footer>
        Card Footer
    </footer>
</card>
```

### Card Variants
```html
<!-- Primary card -->
<card primary border>
    <header>Primary Card</header>
    <content>Primary themed content</content>
</card>

<!-- Secondary card -->
<card secondary border>
    <header>Secondary Card</header>
    <content>Secondary themed content</content>
</card>

<!-- Card with radius -->
<card border radius>
    <header>Rounded Card</header>
    <content>Card with rounded corners</content>
</card>
```

### Card Header with Inline Elements
```html
<card>
    <header inline padder>
        <p>Card Title</p>
        <div>
            <button>X</button>
            <button>Copy</button>
        </div>
    </header>
    <content>
        Card content
    </content>
</card>
```

## Complete Examples

### Three-Column Layout
```html
<container>
    <section>
        <h1>Three Column Layout</h1>
        <div class="row" gap>
            <card border class="col-sm-4">
                <img src="https://placehold.co/600x300/2e9578/ffffff?text=Image+1" alt="Image 1">
                <content>
                    First column content
                </content>
                <footer>
                    <button>Learn More</button>
                </footer>
            </card>
            <card border class="col-sm-4">
                <img src="https://placehold.co/600x300/2e9578/ffffff?text=Image+2" alt="Image 2">
                <content>
                    Second column content
                </content>
                <footer>
                    <button>Learn More</button>
                </footer>
            </card>
            <card border class="col-sm-4">
                <img src="https://placehold.co/600x300/2e9578/ffffff?text=Image+3" alt="Image 3">
                <content>
                    Third column content
                </content>
                <footer>
                    <button>Learn More</button>
                </footer>
            </card>
        </div>
    </section>
</container>
```

### Two-Column Responsive Layout
```html
<main class="container">
    <section bg="primary-light" gap>
        <header>
            <h3>Responsive Two Columns</h3>
        </header>
        <div class="row">
            <card secondary border radius class="col-sm-6 col-12">
                <header>
                    <p>Left Column</p>
                </header>
                <content>
                    This will stack on mobile and be side-by-side on small screens and up.
                </content>
                <footer>
                    <button>Action</button>
                </footer>
            </card>
            <card primary border radius class="col-sm-6 col-12">
                <header>
                    <p>Right Column</p>
                </header>
                <content>
                    Perfect for responsive layouts that adapt to different screen sizes.
                </content>
                <footer justify="center">
                    <button>Action</button>
                </footer>
            </card>
        </div>
    </section>
</main>
```

### Grid Layout (Alternative Syntax)
```html
<container>
    <section gap>
        <header>
            <h3>Grid Layout</h3>
        </header>
        <grid border>
            <card>
                <header>
                    <p>Auto Grid Item 1</p>
                </header>
                <content>
                    Grid automatically distributes space
                </content>
                <footer>
                    <button>Submit</button>
                </footer>
            </card>
            <card secondary>
                <header>
                    <p>Auto Grid Item 2</p>
                </header>
                <content>
                    No need to specify column sizes
                </content>
                <footer>
                    <button>Submit</button>
                </footer>
            </card>
            <card secondary>
                <header>
                    <p>Auto Grid Item 3</p>
                </header>
                <content>
                    Cards automatically wrap and size
                </content>
                <footer>
                    <button>Submit</button>
                </footer>
            </card>
        </grid>
    </section>
</container>
```

## Breakpoints

- **Default**: All screen sizes
- **sm**: 48em (768px) and up
- **md**: 64em (1024px) and up  
- **lg**: 75em (1200px) and up

## Common Utility Attributes

- `gap` - Adds spacing between elements
- `pad` - Adds internal padding
- `border` - Adds border styling
- `radius` - Adds rounded corners
- `inline` - Makes elements inline
- `bg="color"` - Sets background color
- `color="color"` - Sets text color
- `align="start|center|end"` - Aligns content
- `justify="start|center|end"` - Justifies content

## Tips

1. Use `<container>` or `.container` to wrap your main content
2. Use `<section>` for major content areas with automatic spacing
3. Use `<grid>` for simple auto-sizing layouts
4. Use `.row` and `.col-*` classes for precise control over column sizes
5. Add `gap` attribute to create spacing between grid items
6. Use responsive column classes like `col-12 col-sm-6 col-md-4` for mobile-first design
