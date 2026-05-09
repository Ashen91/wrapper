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

2. Create an external docker volume

```
docker volume create rootfs
```

## Usage

Build:

```
docker build --tag wrapper .
```

Launch:

```
docker compose up -d
```

(First time only) If your Apple ID has Two-Factor Authentication (2FA) enabled, you need to provide the verification code:

```
docker exec -it wrapper sh -c 'echo -n XXXXXX > /app/rootfs/data/data/com.apple.android.music/files/2fa.txt'
```

Replace XXXXXX with the 6-digit verification code sent to your device.

## Stop

```
docker compose down
```

## Special thanks

- Anonymous, for providing the original version of this project and the legacy Frida decryption method.
- chocomint, for providing support for arm64 arch.
