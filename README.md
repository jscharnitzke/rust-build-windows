# Build Rust Projects for Windows

This is just a simple Dockerfile that defines a Docker image to build Rust projects targeting Windows.

## Build

- Download `Dockerfile`
- Navigate to where you downloaded the file
- Run `docker build . -t [image-name]`

## Use

Debug Builds: `docker run -rm -v "[path-to-Rust-project]:/app -w /app [image-name]`

Release Builds: `docker run -rm -v "[path-to-Rust-project]:/app -w /app [image-name] --release`

`.exe` files will be output in `[path-to-Rust-project]/target/x86_64-pc-windows-gnu/[debug|release]`.
