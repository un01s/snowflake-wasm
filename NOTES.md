# how-to notes

The original repo is [here](https://github.com/kabbi/m5-atom-wasms) by [Dmitry Kabak](https://github.com/kabbi).

Have no M5-Atom but have a snowflake with 25 RGB LEDs. Modify the blinker C coder to make it show random color instead of Red only.

## install wasi-sdk into /opt

the build script assumes that wasi-sdk is installed at /opt/wasi-sdk/

```
./build-apps.sh
```

it generates both startup.wasm and blinker.wasm in the dir of wasm

## how to use wasm-micro-runtime or wasm3 with esp32?

Before running platformio build, run the following command first inside the project.

```
./build-apps.sh && ls wasm/*.wasm | xargs -n 1 xxd -i > src/data.h
```

## where is the button?

The snowflake has no buttons. M5-Atom has its button. However, accidently the touch around the USB bus pins generates the same function. The ESP32 dev board is ESP32-PICO-Mini-02 based.

