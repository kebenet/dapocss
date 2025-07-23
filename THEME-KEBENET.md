

@use "sass:color";
$theme-colors: (
  "primary": hsla(163, 53%, 38%, 1),
  "secondary": hsla(23, 85%, 73%, 1),
  "info": hsla(190, 60%, 65%, 1),
  "danger": hsla(0, 70%, 55%, 1),
  "success": hsla(120, 60%, 45%, 1),
  "warning": hsla(45, 90%, 50%, 1)
);


$tints: (100: 0.08, 200: 0.2, 300: 0.44 );


// Theme Mixins (Using Generic Variables)
// =============================================================================
@mixin default-theme-colors {

  @each $name, $color in $theme-colors {
    --#{$name}: #{$color};
    @each $level, $alpha in $tints {
      --#{$name}-#{$level}: #{color.change($color, $alpha: $alpha)};
    }
  }



$theme-colors: (
  "primary": #2e9578,
  "secondary": #f4ae81,
  "info": #00b0f4,
  "danger": red,
  "success": #11b76b,
  "warning": #ffa100
);

#2e9578
#f4ae81

$theme-colors: (
  "primary": #2e9578,
  "secondary": #f4ae81,
  "info": #00b0f4,
  "danger": red,
  "success": #11b76b,
  "warning": #ffa100
);


## Html Tags
------------
a, abbr, address, bdi, bdo, big, blockquote, body, br, button, caption, cite, code, col, colgroup,
dd, del, details, dfn, dialog, dir, dl, dt, em, fieldset, figcaption, figure, footer, form,
h1, header, hgroup, hr, input, ins, kbd, label, legend, li, link, mark, marquee, menu, meta, 
nav, ol, optgroup, option, output, p, picture, pre, progress, q, s, samp, search, select, slot,
small, source, span, strike, strong, sub, summary, sup, table, tbody, td, template, textarea,
tfoot, th, thead, time, title, tr, track, tt, u, ul,