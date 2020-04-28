# LibVCX Skeleton Android Project
This is the Android skeleton project to use [LibVCX for Java Wrapper](https://github.com/hyperledger/indy-sdk/tree/master/vcx/wrappers/java) in your Android project.
It contains all necessary dependencies and native libraries such as `libindy.so` and `libvcx.so` under the jniLibs folder if you run the script included. It also contains some boilerplate code to use LibVCX for Java Wrapper.
You can just start to use LibVCX APIs in the project without any compilation issues.

## Prerequisites
#### Android Studio
It requires Android Studio 3.6 or newer

#### Create Native Libraries
Run the script. This will download all native libraries needed for this project, and create the jniLib folder with required ABIs
```
$ ./populate_libraries.sh
``` 

**Note**: You can change the version numbers for `libindy` and `libvcx` in the script `populate_libraries.sh`

## Native Libraries included
All libraries will be available after running the script, but if you want to get those libraries by yourself, please refer to the below.

- [libindy stable v1.15.0](https://repo.sovrin.org/android/libindy/stable/1.15.0/)
- [libvcx stable v0.8.0](https://repo.sovrin.org/android/libvcx/stable/0.8.0/)
- [libjnidispatch v4.5.2](https://github.com/java-native-access/jna/tree/4.5.2/lib/native): You can extract `libjnidispatch.so` from `jar` file using, for example `unzip android-x86.jar libjnidispatch.so` command. Alternatively, you may get a file in the local gradle folder (You can get a location of file in the Android Studio > Project tab > expand External Libraries > expand `net.java.dev.jna:jna:4.5.2@aar` > right click on classes.jar > Reveal in Finder > they are under `jni` folder)
- [libc++_shared r21b](https://developer.android.com/ndk/downloads): If your platform is macOS, and downloaded the latest NDK, you can get libc++_shared.so file for each ABI in the `~/Library/Android/sdk/ndk/21.1.6352462/sources/cxx-stl/llvm-libc++/libs` folder

## Steps to run project
#### Build  
After populating all necessary native libraries in the prerequisites section, build the project

#### Run
If you see the empty activity application, you are done. 