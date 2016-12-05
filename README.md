ReactNative 0.39 on Ubuntu Machine  Experiement
====================

First try of ReactNative development on Ubuntu 64bit.

### Learnings

 - Make sure you have installed the 32 bit versions of the libraries
 - Here are some and mostly all

[From official documents](https://developer.android.com/studio/install.html)

`
sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386
`

[From my trial and run](https://github.com/facebook/react-native/issues/7320)
`
sudo apt-get install lib32stdc++6 lib32z1
`

Hopefully everything is fine after this point.

However if you find some more errors, try things as suggested below.

 1. The must change is `buildToolsVersion "24.0.1"` instead of the default setting in the file `android/app/build.gradle`

# Some commadline things which might help

Android Build from inside `android` folder

`
./gradlew clean
./gradlew installDebug
`

Gradle commads run from inside `android` folder

`
./gradlew tasks
./gradlew tasks --all

./gradlew projects
./gradlew model
`

Cheers