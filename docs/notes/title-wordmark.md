# Title wordmark

`WAD.WAD` entry 95 (offset 0x50C3800, length 0x9D000) holds at +0x40800 the 512 x 256-halfword block that lands as
VRAM (512, 256)..(1024, 512) (`docs/re-frontier.md`, title text). The SPYRO RIPTO'S RAGE! wordmark plate is image 0
of the boot overlay's table at `0x80063F44` (bytes 0, 0, 0, 0xFF, 0xFF, 0x60): 8-bit page (512, 256), u 0, v 0,
255 x 96 texels, CLUT (512, 511), i.e. row 255 of the block. Colour 0 is transparent.
