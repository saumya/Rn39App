React Native 0.39 App
====================

Well seems that

`
react-native run-android
`

does not compile. The must change is `buildToolsVersion "24.0.1"` instead of the default setting in the file `android/app/build.gradle`