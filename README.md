# GMP for Android

This repository contains a prebuilt copy of [GMP](https://gmplib.org/) 6.2.0 compiled with the Android NDK r21 against API level 24.

Compiling against API levels greater than or equal to 21 will produce backwards incompatible binaries which reference localeconv() unless special care is taken.  It is advised to check config.h at each build and confirm that localeconv is not enabled.

The C++ bindings are included; they depend on libgmp.so, so you will need to ship *both* in your APK for each platform you support.
