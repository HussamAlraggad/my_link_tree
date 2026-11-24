---
name: Contact Sheet
description: A printed index of channels on warm paper, led by the colored character mark.
colors:
  paper: "#F4F0E8"
  card: "#FBF8F1"
  desk: "#E4DDCF"
  ink: "#1A1714"
  muted: "#6E655B"
  line: "rgba(26, 23, 20, 0.18)"
  line-strong: "rgba(26, 23, 20, 0.42)"
  highlight: "rgba(255, 255, 255, 0.55)"
  mark: "#D4552F"
  mark-deep: "#A23A22"
  brown: "#623B24"
typography:
  display:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(2.7rem, 5.6vw, 5rem)"
    fontWeight: 500
    lineHeight: 0.88
    letterSpacing: "-0.052em"
  title:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "21px"
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: "-0.02em"
  body:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "11px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0.16em"
  meta:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "10px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: "0.18em"
  display-compact:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(2.5rem, 7.4vw, 4.2rem)"
    fontWeight: 500
    lineHeight: 0.88
    letterSpacing: "-0.052em"
  display-mobile:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "clamp(2.25rem, 8.6vw, 3.1rem)"
    fontWeight: 500
    lineHeight: 0.88
    letterSpacing: "-0.052em"
  display-small:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "2rem"
    fontWeight: 500
    lineHeight: 0.88
    letterSpacing: "-0.052em"
  title-mobile:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "19px"
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: "-0.02em"
  body-compact:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.55
  body-mobile:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "13.5px"
    fontWeight: 400
    lineHeight: 1.5
  body-small:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 400
    lineHeight: 1.5
  icon:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1
  micro:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "8px"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0.18em"
  micro-small:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "7px"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0.18em"
rounded:
  none: "0px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "14px"
  lg: "18px"
  xl: "26px"
  "2xl": "38px"
  "3xl": "58px"
components:
  sheet:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "0"
  frame:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "14px 18px 16px"
  frame-primary:
    backgroundColor: "{colors.card}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
  label:
    textColor: "{colors.muted}"
    typography: "{typography.label}"
---

# Design System: Contact Sheet

## Overview

**Creative North Star: “The Contact Sheet”**

The page is a single sheet of warm paper resting on a darker desk. It behaves like a printed index of six channels: a masthead, a cover frame holding the colored character mark, a numbered 2×3 grid of frames, and a colophon footer. The character mark is the only illustration; the black version of the same mark is printed faintly into the paper like a watermark.

The page refuses the default link-in-bio stack of centered pills over a gradient. It also refuses the portfolio's dark instrument world: this surface is light, physical, and human. The connection to the portfolio is the mark, the direct voice, and the refusal of decoration that does not carry meaning.

**Key Characteristics:**

- Warm paper and ink, with the mark's own orange and brown as the only warmth inside the artwork.
- One 1px rule language, square corners, no cards floating on shadows.
- One grotesque for meaning and one mono voice for measurement.
- Six numbered frames, not six buttons.
- A colored mark as the hero; a black mark as a 3.5% watermark.
- No executable JavaScript. The hover states are CSS; the only script element is JSON-LD metadata.

## Colors

A printed sheet, an ink pen, and a grease-pencil accent.

- **Paper (#F4F0E8):** the sheet. **Card (#FBF8F1):** the primary frame only, one step lighter. **Desk (#E4DDCF):** the surface around the sheet.
- **Ink (#1A1714):** names, labels, rules, body copy.
- **Muted (#6E655B):** handles, secondary copy, metadata. This replaces the earlier `#8C8275` faint tone for all text because it failed contrast on the card.
- **Line (rgba(26,23,20,.18)):** every internal border. **Line strong (rgba(26,23,20,.42)):** the outer sheet and section rules.
- **Mark (#D4552F):** the live status dot and the hover arrow only.
- **Mark deep (#A23A22):** the “PRIMARY” text inside the email frame. The lighter mark red is 3.9:1 on the card and is not used for text.
- **Brown (#623B24):** the kicker, status text, hovered frame label, and the mark’s mustache in the artwork.
- The colored mark also contains **orange #F6AB66** and **black #000000**. Those are image colors, not CSS tokens.

**Named Rules**

**The No-Circle Rule.** There is no hand-drawn circle, ellipse, or pencil mark around a link, on hover or at rest. The primary email frame is identified by its lighter paper and its “PRIMARY” tag, not by a ring. The hover response is paper, label color, and arrow.

**The Watermark Rule.** The black mark appears six times on desktop and four on mobile, at 3.5% opacity, behind the content, clipped by the sheet. It is a texture on the paper, not a sticker on top of it. The transparent frames let it show through; the primary frame hides it.

## Typography

**Display / Body:** Archivo (latin variable subset, 30 KB).
**Labels / Metadata:** the system monospace stack.

One grotesque carries the name, the role, and the frame titles. The mono voice carries numbers, metadata, and the colophon. Mono never sets prose.

### Hierarchy

- **Display** (500, clamp(2.7rem, 5.6vw, 5rem), 0.88, −0.052em): the name only.
- **Title** (500, 21px, 1.15, −0.02em): frame labels.
- **Body** (400, 16px, 1.55): the role line.
- **Label** (400, 11px, 1.4, .16em, uppercase, mono): frame numbers, frame kinds, masthead, kicker, status, handles.
- **Meta** (400, 10px, 1.4, .18em, uppercase, mono): the footer only.

**Named Rules**

**The 11px Rule.** Functional text never drops below 11px. The footer is the single 10px exception because it is non-interactive metadata. The “00” and “MARK” portrait captions are decorative and may be 8px, but they are `aria-hidden`.

## Layout

The sheet is 1040px wide maximum, with a 6px ink top bar and a 1px outer border. A 30px masthead opens it; the identity is a 250px portrait plus a copy column; the frames are a 2×3 grid with 1px internal rules; the footer closes it. On a 1440×900 screen the sheet fits with room above and below.

Below 820px the identity narrows; below 620px the frames stack to one column and the sheet scrolls; below 380px the identity stacks the portrait above the copy. Nothing scrolls horizontally at 320px.

**Named Rules**

**The Sheet Rule.** The only shadow belongs to the sheet on the desk. Frames have no shadow, no radius, and no fill unless they are the primary frame or being hovered.

## Components

### The Frame

A six-item index. Each frame is a link with a number, a kind, a label, a handle, and an arrow. The grid is drawn with 1px borders; the frame background is transparent so the paper and the watermark show through. Hover and focus change the paper to `card`, the label to brown, the top line to brown, the handle to ink, and the arrow to `mark`. The focus outline is 2px brown, inset 2px.

### The Primary Frame

The email frame is the only opaque frame (`card`). It carries the “PRIMARY” tag in `mark-deep` and the longest handle. It is not hover-only information; the tag is always visible.

### The Watermarks

Six black-mark images, positioned and rotated, 3.5% opacity, `aria-hidden`, clipped by the sheet. They sit behind the masthead, identity, frames, and footer. The colored mark is never used as a watermark.

### The Portrait

A square frame with the colored mark, one black border, a “00” code, and a “MARK” caption. The mark is decorative here; the name is text beside it.

### The Status

A small mark-red dot and the words “Open to internships” in brown mono.

## Motion

One staggered entrance for the sheet, identity, frames, and footer, 0.58s with a short stagger. Reduced motion disables all animation and transitions. There is no scroll animation, no cursor effect, and no JavaScript.

## Do's and Don'ts

### Do

- Keep the sheet as the only elevated object.
- Keep every functional label at 11px or larger and the footer at 10px.
- Keep the watermark at 3.5% and behind the content.
- Keep the colored mark as the hero and the black mark as the texture.
- Keep the hover response to paper, label color, and arrow.
- Keep the page two files with no executable JavaScript.

### Don't

- Don't draw a circle or pencil mark around a link.
- Don't use the faint #8C8275 for functional text; it fails on the card.
- Don't use the light mark red for text; use `mark-deep` for the primary tag.
- Don't add gradients, rounded corners, or shadows to the frames.
- Don't set prose in monospace.
- Don't add a second display face or a photo.
- Don't let the mobile layout depend on hover.
