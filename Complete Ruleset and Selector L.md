# DAPOCSS v1.1.0 - Complete Ruleset and Selector List

## Universal and Basic Selectors

### Universal Box-sizing
- `*, *::before, *::after` - Universal box-sizing reset

### CSS Custom Properties (CSS Variables)
- `:root` - Main CSS custom properties container (appears multiple times with different property sets)

### Feature Queries
- `@supports(font-size: clamp(1rem, 1vi, 1rem))` - Modern clamp support
- `@supports not (font-size: clamp(1rem, 1vi, 1rem))` - Fallback for browsers without clamp support

### Media Queries
- `@media screen and (min-width: 1280px)` - Large screen breakpoint
- `@media(min-width: 48em)` - Medium screen breakpoint
- `@media print` - Print styles

## HTML Element Selectors

### Document Structure
- `html` - Root HTML element
- `body` - Document body
- `footer` - Footer element
- `body > footer` - Direct footer child of body

### Scrollbar Styling
- `html::-webkit-scrollbar` - Webkit scrollbar
- `html::-webkit-scrollbar-track` - Webkit scrollbar track
- `html::-webkit-scrollbar-thumb` - Webkit scrollbar thumb
- `html::-webkit-scrollbar-thumb:hover` - Webkit scrollbar thumb hover

### Selection Styling
- `::-moz-selection` - Firefox text selection
- `::selection` - Standard text selection

### Typography Elements
- `h1, h2, h3, h4, h5, h6` - All heading levels
- `h1` - Main heading
- `h2` - Secondary heading
- `h3` - Tertiary heading
- `h4` - Quaternary heading
- `h5` - Quinary heading
- `h6` - Senary heading
- `h1, h2, h3, h4, h5, h6, p` - Headings and paragraphs
- `h1, h2, h3, h4, h5, h6, b, strong, th` - Bold elements
- `p` - Paragraph
- `strong` - Strong emphasis
- `b` - Bold text
- `th` - Table header

### Quote Elements
- `q::before, q::after` - Quote pseudo-elements
- `blockquote, q` - Block quotes and inline quotes
- `blockquote > footer` - Blockquote footer
- `blockquote cite` - Blockquote citation

### Other Text Elements
- `address` - Address element
- `mark` - Marked/highlighted text
- `code, samp, time` - Code, sample, and time elements
- `code` - Code element
- `samp, time` - Sample and time elements
- `pre > code` - Code within preformatted text
- `var` - Variable element
- `kbd` - Keyboard input element

### Link Elements
- `a` - Anchor/link element
- `a:hover` - Link hover state
- `a > code, a > strong` - Code and strong within links
- `a[href^="mailto:"]::before` - Email link prefix
- `a[href^="tel:"]::before` - Telephone link prefix
- `a[href^="sms:"]::before` - SMS link prefix

## Form Elements

### Input Elements
- `input` - Generic input styling
- `input:focus` - Input focus state
- `input:disabled` - Disabled input
- `input:not([type=checkbox]):not([type=radio]), input[type=range], select, button, textarea` - Form element appearance reset
- `input, select` - Input and select display
- `[type=checkbox], [type=radio]` - Checkbox and radio display
- `input[type=checkbox], input[type=radio]` - Checkbox and radio sizing
- `input[type=radio]` - Radio button border radius
- `input[type=color]` - Color input
- `input[type=checkbox]:active, input[type=radio]:active, input[type=submit]:active, input[type=reset]:active, input[type=button]:active, input[type=range]:active, button:active` - Active state transform

### Specific Input Types
- `input[type=submit], input[type=reset], input[type=button]` - Submit, reset, and button inputs
- `input[type=submit]:hover, input[type=reset]:hover, input[type=button]:hover` - Hover states
- `input[type=submit]:focus, input[type=reset]:focus, input[type=button]:focus` - Focus states
- `input[type=submit]:active, input[type=reset]:active, input[type=button]:active` - Active states
- `input[type=submit]:disabled, input[type=reset]:disabled, input[type=button]:disabled` - Disabled states

### Range Input Styling
- `input[type=range]` - Range input base
- `input[type=range]:focus` - Range focus
- `input[type=range]::-webkit-slider-runnable-track` - Webkit track
- `input[type=range]::-webkit-slider-thumb` - Webkit thumb
- `input[type=range]:focus::-webkit-slider-runnable-track` - Webkit track focus
- `input[type=range]::-moz-range-track` - Mozilla track
- `input[type=range]::-moz-range-thumb` - Mozilla thumb
- `input[type=range]::-ms-track` - IE track
- `input[type=range]::-ms-fill-lower` - IE lower fill
- `input[type=range]::-ms-fill-upper` - IE upper fill
- `input[type=range]::-ms-thumb` - IE thumb
- `input[type=range]:focus::-ms-fill-lower` - IE lower fill focus
- `input[type=range]:focus::-ms-fill-upper` - IE upper fill focus

### Other Form Elements
- `button` - Button element
- `button:hover` - Button hover
- `button:focus` - Button focus
- `button:active` - Button active
- `button:disabled` - Button disabled
- `select` - Select element
- `select::-ms-expand` - IE select expand
- `select[multiple]` - Multiple select
- `select:focus` - Select focus
- `select:disabled` - Select disabled
- `textarea` - Textarea element
- `textarea:not([cols])` - Textarea without cols
- `textarea:not([rows])` - Textarea without rows
- `textarea:focus` - Textarea focus
- `textarea:disabled` - Textarea disabled
- `label` - Label element
- `fieldset` - Fieldset element
- `legend` - Legend element

### Form Cursors
- `button, select, input[type=submit], input[type=reset], input[type=button], input[type=checkbox], input[type=range], input[type=radio]` - Cursor pointer

### Placeholder Styling
- `::-moz-placeholder` - Mozilla placeholder
- `:-ms-input-placeholder` - Old IE placeholder
- `::-ms-input-placeholder` - IE placeholder
- `::placeholder` - Standard placeholder

## Button Classes

### Primary Button Variants
- `.btn-secondary` - Secondary button
- `.btn-secondary:hover` - Secondary button hover
- `.btn-secondary:focus` - Secondary button focus
- `.btn-secondary:active` - Secondary button active
- `.btn-secondary:disabled` - Secondary button disabled

### Secondary Outline Button
- `.btn-secondary-outline` - Secondary outline button
- `.btn-secondary-outline:hover` - Secondary outline button hover
- `.btn-secondary-outline:focus` - Secondary outline button focus
- `.btn-secondary-outline:active` - Secondary outline button active
- `.btn-secondary-outline:disabled` - Secondary outline button disabled

## Table Elements
- `table` - Table element
- `table caption` - Table caption
- `td, th` - Table cells
- `thead` - Table header
- `tfoot` - Table footer
- `tbody tr:nth-child(even)` - Even table rows
- `tbody tr:nth-child(even) button` - Buttons in even rows
- `tbody tr:nth-child(even) button:hover` - Button hover in even rows

## Media Elements
- `img, video` - Images and videos

## Line Elements
- `hr` - Horizontal rule
- `hr[secondary]` - Secondary horizontal rule
- `hr[primary]` - Primary horizontal rule

## Interactive Elements

### Details/Summary
- `details` - Details element
- `details[open]` - Open details
- `details[open] summary` - Summary in open details
- `details > :last-child` - Last child in details
- `details > :not(summary)` - Non-summary children
- `summary` - Summary element
- `summary:hover, summary:focus` - Summary hover and focus
- `summary::-webkit-details-marker` - Webkit details marker

### Dialog
- `dialog` - Dialog element
- `dialog > header:first-child` - First header in dialog
- `dialog::-webkit-backdrop` - Webkit dialog backdrop
- `dialog::backdrop` - Standard dialog backdrop

## Custom Component Selectors

### Link Buttons
- `a[button]` - Button-styled links
- `a[button]:hover` - Button link hover
- `a[button]:active` - Button link active
- `a[button]:focus` - Button link focus
- `a[small]` - Small button links
- `a[outline]` - Outline button links
- `a[outline]:hover` - Outline button hover
- `a[secondary]` - Secondary button links
- `a[secondary]:hover` - Secondary button hover
- `a[success]` - Success button links
- `a[success]:hover` - Success button hover
- `a[warning]` - Warning button links
- `a[warning]:hover` - Warning button hover
- `a[danger]` - Danger button links
- `a[danger]:hover` - Danger button hover
- `a[disabled]` - Disabled button links
- `a[disabled]:hover` - Disabled button hover
- `a[button-icon]` - Icon button links
- `a[button-icon]::before` - Icon button pseudo-element

### Button Groups and States
- `.button-group` - Button group container
- `.button-group .button` - Buttons in group
- `.button-group-v` - Vertical button group
- `.button-loading` - Loading button
- `.button-loading::after` - Loading spinner
- `.button--full` - Full width button
- `.button--auto` - Auto width button

### Grid System
- `grid` - Grid container
- `grid[one], grid[two], grid[three]` - Single column grids
- `grid[auto]` - Auto grid
- `grid[auto-two]` - Auto two column grid
- `grid[auto-three]` - Auto three column grid
- `grid[border] > card` - Cards with borders in grid
- `grid[round] > card` - Rounded cards in grid
- `grid[primary] > card` - Primary cards in grid
- `grid[primary] > card > header` - Primary card headers
- `grid[secondary] > card > header` - Secondary card headers
- `grid[two]` - Two column grid (responsive)
- `grid[three]` - Three column grid (responsive)
- `grid[hover] > card, grid[hover] > stack-grid` - Hoverable grid items
- `grid[hover] > card:hover, grid[hover] > stack-grid:hover` - Grid item hover effects
- `grid[primary] > stack-grid > stack-side` - Primary stack grid sides
- `grid[secondary] > stack-grid > stack-side` - Secondary stack grid sides

### Card System
- `card, block, card > content, card > footer` - Card components
- `card` - Card container
- `div[ratio-1] > card > img` - 1:1 aspect ratio card images
- `card > content` - Card content
- `card[border]` - Bordered cards
- `card[primary] > header` - Primary card headers
- `card[primary]` - Primary cards
- `card[secondary] > header` - Secondary card headers
- `card[secondary]` - Secondary cards
- `card > footer` - Card footers

### Stack Grid System
- `stack-grid` - Stack grid container
- `stack-side` - Stack grid side panel
- `stack-grid[primary] > stack-side` - Primary stack grid sides
- `stack-grid[secondary] > stack-side` - Secondary stack grid sides
- `stack-grid[primary] > card > header` - Primary stack grid card headers
- `stack-grid[secondary] > card > header` - Secondary stack grid card headers

## Layout and Utility Classes

### Alignment
- `[align-v=start]` - Vertical align start
- `[align-v=center]` - Vertical align center
- `[align-v=end]` - Vertical align end
- `[align=start]` - Horizontal align start
- `[align=center]` - Horizontal align center
- `[align=end]` - Horizontal align end

### Spacing
- `[space=around]` - Space around
- `[space=between]` - Space between
- `[space=evently]` - Space evenly
- `[space-v=around]` - Vertical space around
- `[space-v=between]` - Vertical space between
- `[space-v=evently]` - Vertical space evenly

### Display
- `[inline]` - Inline grid display

### Background Colors
- `[bg=light]` - Light background
- `[bg=lighter]` - Lighter background
- `[bg=dark]` - Dark background
- `[bg=darker]` - Darker background
- `[bg=primary]` - Primary background
- `[bg=primary-light]` - Primary light background
- `[bg=primary-lighter]` - Primary lighter background
- `[bg=secondary]` - Secondary background
- `[bg=secondary-light]` - Secondary light background
- `[bg=secondary-lighter]` - Secondary lighter background

### Text Colors
- `[color=primary]` - Primary text color
- `[color=secondary]` - Secondary text color
- `[color=dark]` - Dark text color
- `[color=light]` - Light text color

### Container and Section Layout
- `section` - Section element
- `container, .container` - Container classes
- `section, container, .container, card, grid` - Max width constraint
- `section:last-child` - Last section
- `block` - Block element

### Padding Utilities
- `[pad]` - Base padding
- `[pad-m]` - Medium padding
- `[pad-l]` - Large padding
- `[pad-tbr]` - Top, bottom, right padding
- `[pad-clamp], .pad-clamp` - Responsive padding

### Section Utilities
- `section[gap] > grid` - Section with gap
- `section[pad] > grid` - Section with padding
- `section > header` - Section headers

### Radius Utility
- `[radius]` - Border radius utility

## Keyframes Animation
- `@keyframes spin` - Spinning animation
  - `0%` - Start state
  - `100%` - End state

## Print Styles
All selectors within `@media print`:
- `body, pre, code, summary, details, button, input, textarea` - Print background/color reset
- `button, input, textarea` - Print borders
- `body, h1, h2, h3, h4, h5, h6, pre, code, button, input, textarea, footer, summary, strong` - Print text color
- `summary::marker` - Print marker color
- `summary::-webkit-details-marker` - Print webkit marker
- `tbody tr:nth-child(even)` - Print table row background
- `a` - Print link decoration

## Total Count Summary
**Total Approximate Selectors**: ~326 individual selectors

This framework provides a comprehensive set of styling rules for modern web applications with a focus on forms, grids, cards, and responsive design patterns.
