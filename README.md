# Simple window using the WinAPI

This is a simple window to test the mingw shell in my NixOS devbox

## Setup and Build
### if you have a NixOS install you will need to make sure you have Multiplatform support in your `configuration.nx` file.

```
  # Multi-platform Support
  boot.binfmt.emulatedSystems = [
    "x86_64-windows"
  ];
```

### Then you can go in to a nix shell, build and run the code.

```bash
nix-shell
x86_64-w64-mingw32-gcc -o win.exe winMain.c
./win.exe
```