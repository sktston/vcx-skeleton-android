# LibVCX Skeleton Android Project
This is the Android skeleton project to use [LibVCX for Java Wrapper](https://github.com/hyperledger/indy-sdk/tree/master/vcx/wrappers/java) in your Android project.
It contains all necessary dependencies and native libraries such as libindy.so and libvcx.so under the jniLibs folder. It also contains some boilerplate code to use LibVCX for Java Wrapper.
You can just start to use LibVCX APIs in the project without any compilation issues.

## Prerequisites
#### Git Large File Storage
You need to install [Git LFS](https://help.github.com/en/github/managing-large-files/installing-git-large-file-storage) to clone this repository because it contains large native libraries.
To use [Homebrew](http://brew.sh/) on MacOS run
```
$ brew install git-lfs
$ git lfs install
```
#### Android Studio
It requires Android Studio 3.6 or newer

## Native Libraries included
- [libindy stable v1.15.0](https://repo.sovrin.org/android/libindy/stable/1.15.0/)
- [libvcx stable v0.8.0](https://repo.sovrin.org/android/libvcx/stable/0.8.0/)
- [libjnidispatch v4.5.2](https://github.com/java-native-access/jna/tree/4.5.2/lib/native)
- [libc++_shared r20](https://developer.android.com/ndk/downloads/older_releases): you can get libc++_shared.so file for each ABI in the sources/cxx-stl/llvm-libc++/libs folder. (Included shared library for C++ is for the platform Mac OS X)

## Steps to run project
#### Build  
Install the NDK (Side by side)
```
Tools -> SDK Manager -> SDK Tools -> Check 'Show Package Details' -> Install the NDK (Side by side) version 20.0.5594570
```
After installing the NDK, build the project
#### Run
If you see the empty activity application, you are done. 