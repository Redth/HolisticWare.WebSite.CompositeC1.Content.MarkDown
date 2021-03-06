# Xamarin.Android.Support Libraries

xamarin-android-support-libraries.md

*   TODO
    *   old: 27.0.2
    *   new: 27.1.1

## Steps

1. get the source

   1. clone https://github.com/xamarin/androidsupportcomponents
   
   2. create branch for new versions `27.1.1`
   
2. download Android Support binaries (*.jar and *.aar)

   `sh build.sh --target=externals`
   
3. compile and fix

   `sh build.sh --target=libs`

4. diff the API of the new version and old

   `sh build.sh --target=diff`


### Build times

Just to have some information about build duration:

*   clean repo (freshly cloned) - 1 hr 20+ minutes

*   built repo - 40+ minutes

## References / Links

*   https://maven.google.com

*   https://github.com/xamarin/androidsupportcomponents

*   https://github.com/redth/mavennet


## v.27.1.1

### Steps

1.  changed Cake script so build works with newer Cake plugins (pinning the version)

2.  make new version bindings compile clean 

3.  detect/investigate new APIs

    1.  run target diff

        `sh build.sh --target=diff`

    2.  check html output: `output/AndroidSupport.api-diff.html`

    3.  inspecting `*.aar[s]` and `*.jar[s]` with decompilers (JD_GUI, Luyten, jadx)

For detailed see [./xamarin-android-support-libraries/steps.md](./xamarin-android-support-libraries/steps.md)


[./xamarin-android-support-libraries/questions.md](./xamarin-android-support-libraries/questions.md)