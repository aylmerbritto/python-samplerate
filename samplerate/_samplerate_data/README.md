# libsamplerate binaries

These are statically compiled dynamic libraries of
[libsamplerate](http://www.mega-nerd.com/libsamplerate/).

## DLLs for Windows (32-bit and 64-bit)

The instructions follow the README of [libsndfile-binaries]. The DLLs were
created on macOS using [MXE](http://mxe.cc) with the `build_samplerate_mxe.sh`
script:

    git clone https://github.com/mxe/mxe.git
    patch -p1 -d mxe < mxe_libsamplerate-0.1.9.patch
    ./build-samplerate.sh

## Dylib for macOS (64-bit)

Build using [Homebrew](http://brew.sh/):

    brew install libsamplerate
    cp /usr/local/lib/libsamplerate.dylib .
    # There should be no further dependencies:
    otool -L libsamplerate.dylib