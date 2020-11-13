# Build OpenCV

### Build `opencv.js` and `opencv.wasm`

remove flag `SINGLE_FILE` from `module/js/CMakelist.txt`
line 105: 

`set(EMSCRIPTEN_LINK_FLAGS "${EMSCRIPTEN_LINK_FLAGS} -s MODULARIZE=1")`

