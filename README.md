# Build Rust Projects for Windows

The official Rust Docker image is configured to build for Linux targets out-of-the-box. This Dockerfile defines a Docker image to build Rust projects targeting Windows instead.

## Build

- Download `Dockerfile`
- Navigate to where you downloaded the file
- Run `docker build . -t [image-name]`

## Use

Debug Builds: `docker run -rm -v "[path-to-Rust-project]:/app -w /app [image-name]`

Release Builds: `docker run -rm -v "[path-to-Rust-project]:/app -w /app [image-name] --release`

`.exe` files will be output in `[path-to-Rust-project]/target/x86_64-pc-windows-gnu/[debug|release]`.

## Public Image

If you want, you can use a pre-built image that I've published to Docker Hub: [jscharnitzke/rust-build-windows](https://hub.docker.com/r/jscharnitzke/rust-build-windows)
