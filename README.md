ReactNative 0.39 on Ubuntu Machine  Experiment
====================

First try of ReactNative development on Ubuntu 64bit.
Working fine.

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

```
./gradlew clean
./gradlew installDebug
```

Gradle commads run from inside `android` folder

```
./gradlew tasks
./gradlew tasks --all

./gradlew projects
./gradlew model
```

## NodeJS and NPM settings

[Permission settings reference](https://saumya.github.io/ray/articles/70/)

The default location of `nodejs` and `node_modules` is at `/usr/lib`

View permissions

```
ls -la /usr/lib/node_modules
```

Change permission to current user in this case it is setting as `iAmCurrent` :)

```
sudo chown -R iAmCurrent /usr/lib/node_modules
```

### Change permission of `node_modules` but not the whole `lib`. If you change the permission of `lib`, **your linux OS will be at risk and maynot allow you to work** . So be careful.

Cheers have fun
