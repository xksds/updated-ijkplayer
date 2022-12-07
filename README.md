# updated ijkplayer
 ### For Android arm64 only
 ### Based on ffmpeg release 5.1 and openssl 3.0
 - ijkplayer : https://github.com/bilibili/ijkplayer.git, commit id : 30eb9441945da795079492041a791c121d2b8206
 - FFmpeg    : https://git.ffmpeg.org/ffmpeg.git, release/5.1
 - Openssl   : https://github.com/openssl/openssl.git, origin/openssl-3.0

 ### Build env
 - Host : MacOS Catalina, Version 10.15.7
 - NDK  : android-ndk-r20, GNU Make 3.81

 ### Build
```
git clone git@github.com:xksds/updated-ijkplayer.git
# Current branch is main

cd ijkplayer-with-ffmpeg_release5.1/android/contrib

./compile-openssl.sh clean && ./compile-openssl.sh arm64
# Optional, only when you need openssl compiled.

./compile-ffmpeg.sh clean && ./compile-ffmpeg.sh arm64
# Compile ffmpeg

cd ..

./compile-ijk.sh clean && ./compile-ijk.sh arm64
# Compile ijk wrapper.

# After jobs above finished, three shared libraries will be generated at $(SOURCE_ROOT_PATH)/android/ijkplayer/ijkplayer-arm64/src/main/libs/arm64-v8a

```

### Notice
 - libavformat related which modify by ijk NOT merged !!!


### License

```
Copyright (c) 2017 Bilibili
Licensed under LGPLv2.1 or later
```

ijkplayer required features are based on or derives from projects below:
- LGPL
  - [FFmpeg](http://git.videolan.org/?p=ffmpeg.git)
  - [libVLC](http://git.videolan.org/?p=vlc.git)
  - [kxmovie](https://github.com/kolyvan/kxmovie)
  - [soundtouch](http://www.surina.net/soundtouch/sourcecode.html)
- zlib license
  - [SDL](http://www.libsdl.org)
- BSD-style license
  - [libyuv](https://code.google.com/p/libyuv/)
- ISC license
  - [libyuv/source/x86inc.asm](https://code.google.com/p/libyuv/source/browse/trunk/source/x86inc.asm)

android/ijkplayer-exo is based on or derives from projects below:
- Apache License 2.0
  - [ExoPlayer](https://github.com/google/ExoPlayer)

android/example is based on or derives from projects below:
- GPL
  - [android-ndk-profiler](https://github.com/richq/android-ndk-profiler) (not included by default)

ios/IJKMediaDemo is based on or derives from projects below:
- Unknown license
  - [iOS7-BarcodeScanner](https://github.com/jpwiddy/iOS7-BarcodeScanner)

ijkplayer's build scripts are based on or derives from projects below:
- [gas-preprocessor](http://git.libav.org/?p=gas-preprocessor.git)
- [VideoLAN](http://git.videolan.org)
- [yixia/FFmpeg-Android](https://github.com/yixia/FFmpeg-Android)
- [kewlbear/FFmpeg-iOS-build-script](https://github.com/kewlbear/FFmpeg-iOS-build-script)

### Commercial Use
ijkplayer is licensed under LGPLv2.1 or later, so itself is free for commercial use under LGPLv2.1 or later

But ijkplayer is also based on other different projects under various licenses, which I have no idea whether they are compatible to each other or to your product.

[IANAL](https://en.wikipedia.org/wiki/IANAL), you should always ask your lawyer for these stuffs before use it in your product.
