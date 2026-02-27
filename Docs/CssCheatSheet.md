# CSS Cheat Sheet

## 🎨 Colors & Backgrounds
| Property                | Purpose                          |
| ----------------------- | -------------------------------- |
| `color`                 | Text color                       |
| `background-color`      | Background color                 |
| `background-image`      | Background image                 |
| `background-repeat`     | Repeat style (repeat, no-repeat) |
| `background-position`   | Position of background image     |
| `background-size`       | Size of background image         |
| `background-clip`       | Painting area for background     |
| `background-attachment` | Scroll or fixed background       |

---

## 🖋️ Fonts & Text
| Property          | Purpose                                  |
| ----------------- | ---------------------------------------- |
| `font-family`     | Font type                                |
| `font-size`       | Font size                                |
| `font-weight`     | Boldness                                 |
| `font-style`      | Italic/normal                            |
| `font-variant`    | Small-caps                               |
| `line-height`     | Line spacing                             |
| `letter-spacing`  | Space between letters                    |
| `word-spacing`    | Space between words                      |
| `text-align`      | Alignment (left, right, center, justify) |
| `text-decoration` | Underline, overline, line-through        |
| `text-transform`  | Uppercase, lowercase, capitalize         |
| `text-shadow`     | Shadow effect                            |

---

## 📐 Box Model
| Property                    | Purpose                                         |
| --------------------------- | ----------------------------------------------- |
| `width`                     | Element width                                   |
| `height`                    | Element height                                  |
| `max-width` / `min-width`   | Width limits                                    |
| `max-height` / `min-height` | Height limits                                   |
| `margin`                    | Outer spacing                                   |
| `padding`                   | Inner spacing                                   |
| `border`                    | Border style                                    |
| `border-radius`             | Rounded corners                                 |
| `box-shadow`                | Shadow around box                               |
| `box-sizing`                | Box model calculation (content-box, border-box) |

---

## 📦 Layout & Positioning
| Property                         | Purpose                                                 |
| -------------------------------- | ------------------------------------------------------- |
| `display`                        | Display type (block, inline, flex, grid, none)          |
| `position`                       | Positioning (static, relative, absolute, fixed, sticky) |
| `top`, `right`, `bottom`, `left` | Offset positions                                        |
| `z-index`                        | Stack order                                             |
| `float`                          | Float element (left, right)                             |
| `clear`                          | Control float wrapping                                  |
| `overflow`                       | Content overflow (hidden, scroll, auto)                 |
| `visibility`                     | Show/hide element                                       |

---

## 🧩 Flexbox
| Property          | Purpose                              |
| ----------------- | ------------------------------------ |
| `display: flex`   | Enable flex container                |
| `flex-direction`  | Row or column layout                 |
| `flex-wrap`       | Wrap items                           |
| `flex`            | Flex shorthand (grow, shrink, basis) |
| `justify-content` | Align items horizontally             |
| `align-items`     | Align items vertically               |
| `align-content`   | Align multiple lines                 |
| `order`           | Item order                           |

---

## 🗂️ Grid
| Property                | Purpose               |
| ----------------------- | --------------------- |
| `display: grid`         | Enable grid container |
| `grid-template-columns` | Define columns        |
| `grid-template-rows`    | Define rows           |
| `grid-gap` / `gap`      | Space between items   |
| `grid-column`           | Column span           |
| `grid-row`              | Row span              |
| `justify-items`         | Horizontal alignment  |
| `align-items`           | Vertical alignment    |

---

## 🎬 Animation & Transition
| Property                     | Purpose                            |
| ---------------------------- | ---------------------------------- |
| `transition`                 | Shorthand for transitions          |
| `transition-property`        | Property to animate                |
| `transition-duration`        | Duration                           |
| `transition-delay`           | Delay                              |
| `transition-timing-function` | Easing (ease, linear, ease-in-out) |
| `animation`                  | Shorthand for animations           |
| `animation-name`             | Keyframe name                      |
| `animation-duration`         | Duration                           |
| `animation-delay`            | Delay                              |
| `animation-iteration-count`  | Repeat count                       |
| `animation-direction`        | Normal, reverse, alternate         |
| `@keyframes`                 | Define animation steps             |

---

## 🔗 Miscellaneous
| Property    | Purpose                               |
| ----------- | ------------------------------------- |
| `cursor`    | Mouse cursor style                    |
| `opacity`   | Transparency                          |
| `clip-path` | Shape clipping                        |
| `filter`    | Effects (blur, brightness, grayscale) |
| `content`   | Insert content (pseudo-elements)      |

---

## 🚫 Deprecated/Obsolete CSS
Avoid these older properties; use modern alternatives:
| Property                | Purpose (Obsolete)   | Modern Alternative   |
| ----------------------- | -------------------- | -------------------- |
| `clip`                  | Rectangular clipping | `clip-path`          |
| `zoom`                  | Scale element        | `transform: scale()` |
| `-webkit-border-radius` | Vendor prefix        | `border-radius`      |
| `-moz-box-shadow`       | Vendor prefix        | `box-shadow`         |

---

## 📌 Notes
- CSS has **hundreds of properties**; this cheat sheet covers the most commonly used ones.  
- Always prefer **modern layout systems** (Flexbox, Grid) over floats and tables.  
- Use **CSS variables (`--var`)** and **custom properties** for maintainability.  
