# setandroidbuildenv
Script to set building environment variables ready for building library for Android

# How

It will set bunch of necessary environment variables to be used in building a library project for Android platform.

This requires you already install NDK, and set `$ANDROID_NDK_HOME` to your NDK version of choice.

There are the following configurable settings you can set

* `host_tag` - indicate host value that builds (default is `linux-x86_64`)
* `minsdkversion` - minimum sdk version to support, this is value of api level (default is 18)
* `target_abi` - a single target abi value. it can be `armeabi-v7a`, `x86`, `arm64-v8a`, or `x86_64` (default is `armeabi-v7a`)

The way to send in above parameters can be done with

```
. ./setandroidbuildenv minsdkversion=21 target_abi=arm64-v8a
```

or in case you've installed `setandroidbuildenv` to your executable path i.e. `/usr/local/bin` then you do the following instead

```
. setandroidbuildenv minsdkversion=21 target_abi=arm64-v8a
```

Note `.` which is to source exported environment variables inside the script, so we can use it outside in active shell.

# Available Commands/Parameters

* `setandroidbuildenv --help` - to print help text
* `. setandroidbuildenv --unset` - to unset all related and already set environment variables related in building operation (notice `.` source at the beginning of the command
* `setandroidbuildenv --print-active` - to print active environment variables' value
* `. setandroidbuildenv <optional configurable settings>` - to set environment variables for building

# License
[MIT](https://github.com/abzico/setandroidbuildenv/blob/master/LICENSE), Angry Baozi (https://abzi.co)
