# HTML5 Tag Cheat Sheet

## 📑 Document & Metadata
| Tag          | Purpose                            |
| ------------ | ---------------------------------- |
| `<!DOCTYPE>` | Defines document type (HTML5)      |
| `<html>`     | Root element                       |
| `<head>`     | Metadata container                 |
| `<title>`    | Document title                     |
| `<base>`     | Base URL for relative links        |
| `<meta>`     | Metadata (charset, viewport, etc.) |
| `<link>`     | External resources (CSS, icons)    |
| `<style>`    | Internal CSS                       |
| `<script>`   | JavaScript                         |
| `<noscript>` | Fallback for disabled scripts      |

---

## 📝 Sections & Structure
| Tag         | Purpose              |
| ----------- | -------------------- |
| `<body>`    | Main content         |
| `<header>`  | Introductory content |
| `<footer>`  | Footer content       |
| `<main>`    | Main content area    |
| `<section>` | Thematic grouping    |
| `<article>` | Independent content  |
| `<aside>`   | Side content         |
| `<nav>`     | Navigation links     |

---

## 🔤 Text Content
| Tag            | Purpose           |
| -------------- | ----------------- |
| `<h1>`–`<h6>`  | Headings          |
| `<p>`          | Paragraph         |
| `<br>`         | Line break        |
| `<hr>`         | Horizontal rule   |
| `<span>`       | Inline span       |
| `<pre>`        | Preformatted text |
| `<blockquote>` | Quoted block      |

---

## ✨ Inline Text Semantics
| Tag        | Purpose           |
| ---------- | ----------------- |
| `<a>`      | Hyperlink         |
| `<em>`     | Emphasis          |
| `<strong>` | Strong importance |
| `<small>`  | Side comments     |
| `<mark>`   | Highlighted text  |
| `<abbr>`   | Abbreviation      |
| `<cite>`   | Citation          |
| `<code>`   | Code snippet      |
| `<kbd>`    | Keyboard input    |
| `<samp>`   | Sample output     |
| `<var>`    | Variable          |
| `<time>`   | Date/time         |
| `<b>`      | Stylistic bold    |
| `<i>`      | Stylistic italic  |
| `<u>`      | Underline         |
| `<s>`      | Strikethrough     |
| `<sub>`    | Subscript         |
| `<sup>`    | Superscript       |

---

## 📷 Media
| Tag            | Purpose                 |
| -------------- | ----------------------- |
| `<img>`        | Image                   |
| `<audio>`      | Audio content           |
| `<video>`      | Video content           |
| `<source>`     | Media source            |
| `<track>`      | Text tracks (subtitles) |
| `<figure>`     | Self-contained media    |
| `<figcaption>` | Caption for figure      |

---

## 📊 Tables
| Tag          | Purpose            |
| ------------ | ------------------ |
| `<table>`    | Table              |
| `<caption>`  | Table caption      |
| `<thead>`    | Table header group |
| `<tbody>`    | Table body group   |
| `<tfoot>`    | Table footer group |
| `<tr>`       | Table row          |
| `<td>`       | Table cell         |
| `<th>`       | Header cell        |
| `<col>`      | Column definition  |
| `<colgroup>` | Group of columns   |

---

## 🖊️ Forms
| Tag          | Purpose               |
| ------------ | --------------------- |
| `<form>`     | Form container        |
| `<input>`    | Input field           |
| `<textarea>` | Multi-line input      |
| `<button>`   | Button                |
| `<select>`   | Dropdown              |
| `<option>`   | Option in dropdown    |
| `<optgroup>` | Grouped options       |
| `<label>`    | Label for input       |
| `<fieldset>` | Group of inputs       |
| `<legend>`   | Caption for fieldset  |
| `<datalist>` | Predefined options    |
| `<output>`   | Calculation result    |
| `<progress>` | Progress indicator    |
| `<meter>`    | Measurement indicator |

---

## 🎛️ Interactive Elements
| Tag         | Purpose             |
| ----------- | ------------------- |
| `<details>` | Expandable details  |
| `<summary>` | Summary for details |
| `<dialog>`  | Dialog box          |
| `<menu>`    | Menu list           |

---

## ⚙️ Embedded Content
| Tag        | Purpose               |
| ---------- | --------------------- |
| `<iframe>` | Inline frame          |
| `<embed>`  | External content      |
| `<object>` | External resource     |
| `<param>`  | Parameters for object |

---

## 🧩 Other Useful Tags
| Tag        | Purpose                  |
| ---------- | ------------------------ |
| `<canvas>` | Drawing surface          |
| `<svg>`    | Scalable vector graphics |
| `<map>`    | Image map                |
| `<area>`   | Hotspot in image map     |

---

## 🚫 Deprecated/Obsolete Tags
These tags are **not recommended** in modern HTML5. Avoid using them; use CSS or semantic alternatives instead.

| Tag          | Purpose (Obsolete)   | Modern Alternative     |
| ------------ | -------------------- | ---------------------- |
| `<acronym>`  | Acronym text         | `<abbr>`               |
| `<applet>`   | Java applet          | `<object>`             |
| `<basefont>` | Base font size/color | CSS                    |
| `<big>`      | Large text           | CSS (`font-size`)      |
| `<blink>`    | Blinking text        | CSS animations         |
| `<center>`   | Centered text        | CSS (`text-align`)     |
| `<font>`     | Font styling         | CSS                    |
| `<frame>`    | Frameset             | `<iframe>`             |
| `<frameset>` | Frames container     | `<iframe>`             |
| `<noframes>` | Fallback for frames  | `<iframe>`             |
| `<isindex>`  | Single-line input    | `<input>`              |
| `<marquee>`  | Scrolling text       | CSS animations         |
| `<tt>`       | Teletype text        | `<code>` / CSS         |
| `<dir>`      | Directory list       | `<ul>`                 |
| `<menuitem>` | Menu item            | `<li>` inside `<menu>` |

---

## 📌 Notes
- HTML5 defines **~110 tags** (including obsolete ones).  
- Always prefer **semantic tags** (`<section>`, `<article>`, `<nav>`, `<main>`) for accessibility and SEO.  
- Deprecated tags may still render in browsers but are **bad practice** for modern web development.
