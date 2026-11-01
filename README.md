# Handwritten 16×16 Font
A simple hand-style 16x16 bitmap font, row-major.
**License: GPLv3**

## Spec
- Size: 16 × 16 pixels per glyph
- Storage: row-major (each row = 2 bytes, big-endian)
- Each character: 32 bytes total
- Suitable for: OS dev, embedded MCU, OLED/LCD, NASM, C, Rust, etc.
- No platform lock, everyone can use it.

## File split
- `font_upper.asm` → A ~ Z (26 glyphs)
- `font_lower.asm` → a ~ z (26 glyphs)

## Index
- Upper: A=0, B=1 … Z=25
- Lower: a=0, b=1 … z=25

## How to read
