# kit
![](https://user-images.githubusercontent.com/3920290/224488465-97efadf4-718d-4a9f-99c3-805821bdc376.gif)

A tiny library for making small games with big pixels

Based on rxi/kit but this version uses SDL and could be compiled on Linux. 

Use with caution, I don't know C or SDL, basically I have no idea what I did here.

## Example
```c
#define KIT_IMPL
#include "kit.h"

int main(void) {
    kit_Context *ctx = kit_create("hi", 320, 200, KIT_SCALE2X);
    while (kit_step(ctx, NULL)) {
        kit_draw_text(ctx, KIT_WHITE, "Hello world!", 10, 10);
    }
    kit_destroy(ctx);
    return 0;
}
```

## Overview
- Small single header library: ~1.3k lines of C
- Software rendered images and bitmap fonts
- Keyboard and mouse input
- PNG Loading (borrowed from [tigr](https://github.com/erkkah/tigr))

## Usage
Build using `tcc`, `gcc` (`-lSDL2`) or `msvc`. See the [demo](demo).

## License
Public domain ⁠— no warranty implied; use at your own risk.
