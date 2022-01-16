# how-to notes

## install wasi-sdk into /opt

the build script assumes that wasi-sdk is installed at /opt/wasi-sdk/

```
./build-apps.sh
```

it generates both startup.wasm and blinker.wasm in the dir of wasm

## how to use wasm-micro-runtime or wasm3 with esp32?

Before running platform build, run the following command first inside the project.

```
./build-apps.sh && ls wasm/*.wasm | xargs -n 1 xxd -i > src/data.h
```

We need to build something for esp32. Perhaps the VM for esp32,
then integrate the wasm with that VM.

The question comes down as how to build this with Platform.IO.
From that platformio.ini, there are several libraries required.
Maybe that is the easy way for now.


