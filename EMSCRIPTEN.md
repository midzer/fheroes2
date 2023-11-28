# Emscripten

## Build

```
mkdir build && cd build
emcmake cmake ..
```

## Link

```
em++ -flto -O3 fheroes2.dir/*/*.o fheroes2.dir/*/*/*.o ../../engine/libengine.a ../../thirdparty/libsmacker.a -o index.html -sUSE_SDL=2 -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS='["mid"]' -sUSE_ZLIB -sASYNCIFY -sASYNCIFY_STACK_SIZE=81920 -sINITIAL_MEMORY=256MB -sENVIRONMENT=web --preload-file ../dgguspat@/etc/timidity --preload-file data/ --preload-file maps/ --preload-file files/ --closure 1
```
