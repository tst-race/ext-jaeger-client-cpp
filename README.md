# Jaeger Client C++ API for RACE

This repo provides scripts to custom-build the
[Jaeger Client C++ API library](https://github.com/jaegertracing/jaeger-client-cpp)
for RACE.

## License

The Jaeger Client C++ API library is licensed under Apache 2.0.

Additionally the build scripts in this repo are licensed under Apache 2.0.

## Dependencies

Jaeger Client C++ API has dependencies on the following custom-built libraries:

* Boost
* nlohmann-json
* OpenTracing C++ API
* Apache Thrift
* yaml-cpp

## How To Build

The [ext-builder](https://github.com/tst-race/ext-builder) image is used to
build Jaeger Client C++ API.

```
git clone https://github.com/tst-race/ext-builder.git
git clone https://github.com/tst-race/ext-jaeger-client-cpp.git
./ext-builder/build.py \
    --target linux-x86_64 \
    ./ext-jaeger-client-cpp
```

## Platforms

Jaeger Client C++ API is built for the following platforms:

* `linux-x86_64`
* `linux-arm64-v8a`
* `android-x86_64`
* `android-arm64-v8a`

## How It Is Used

Jaeger Client C++ API is used directly by the RACE core.
