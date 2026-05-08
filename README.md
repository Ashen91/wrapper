# wrapper

A tool to decrypt Apple Music songs. An active subscription is still needed.

Supports only x86_64 and arm64 Linux.

## Installation

This is my own installation method for MacOS under Apple M processors (arm64):

- Prebuilt binaries (from [releases](https://github.com/Ashen91/wrapper/releases))

### Login

Tested on MacOS arm64.

1. Create an .env file and enter your credentials:

```
nano .env
```

## Usage

```
docker compose up -d
```
If you get an error that repository doesn't exist, try:

```
docker build --tag wrapper .
```

## Stop

```
docker compose down
```

## Special thanks

- Anonymous, for providing the original version of this project and the legacy Frida decryption method.
- chocomint, for providing support for arm64 arch.
