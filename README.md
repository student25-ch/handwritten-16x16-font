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
- Upper: A=0, B=1 ... Z=25
- Lower: a=0, b=1 ... z=25

## How to read
Glyph address formula:
glyph_start = base_addr + char_index * 32
- `base_addr`: `font_upper` for A-Z, `font_lower` for a-z
- `char_index`: A=0, B=1 … Z=25; a=0, b=1 … z=25
- Read 32 consecutive bytes starting from `glyph_start` to get the 16×16 bitmap of this character.
