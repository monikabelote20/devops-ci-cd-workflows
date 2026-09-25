# Telemetry Core Engine (C++20)

High-performance, lock-free telemetry ingestion and ring-buffer aggregation engine.

## Architecture
- **Lock-Free Ring Buffer**: Cache-line aligned (`alignas(64)`) circular buffer to eliminate false sharing.
- **SIMD String Scanner**: Fast tokenization of metric key-value tags.
- **Zero-Copy Serialization**: Memory mapped ring-buffer dumps for downstream microservices.

## Build Requirements
- CMake >= 3.20
- GCC >= 11 or Clang >= 14 (C++20 support)
- GoogleTest for unit testing

## Quickstart
```bash
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
ctest --test-dir build --output-on-failure
```
