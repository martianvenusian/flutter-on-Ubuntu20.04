# Flutter-on-Ubuntu20.04
## Install Flutter on Ubuntu 20.04 LTS

    
#### Install flutter manually
1. Download here: https://flutter.dev/docs/get-started/install/linux

    `$ sudo apt update`

    `$ cd ~`

    `$ tar xf ~/Downloads/flutter_linux_1.22.5-stable.tar.xz`

2. Set path:
    
    ```export PATH="$PATH:`pwd`/flutter/bin"```

3. Optionnal. If you don't want to send analytics to Google:
   
    `$ flutter config --no-analytics`

1. Optionally, pre-download development binaries:
   
   `$ flutter precache`

1. Run flutter doctor:
   
   `$ flutter doctor`

```
Downloading Material fonts...                                       0.3s
Downloading Gradle Wrapper...                                       0.0s
Downloading package sky_engine...                                   0.1s
Downloading flutter_patched_sdk tools...                            1.1s
Downloading flutter_patched_sdk_product tools...                    1.4s
Downloading linux-x64 tools...                                      2.4s
Downloading linux-x64/font-subset tools...                          0.2s
Downloading android-arm-profile/linux-x64 tools...                  0.2s
Downloading android-arm-release/linux-x64 tools...                  0.2s
Downloading android-arm64-profile/linux-x64 tools...                0.2s
Downloading android-arm64-release/linux-x64 tools...                0.2s
Downloading android-x64-profile/linux-x64 tools...                  0.2s
Downloading android-x64-release/linux-x64 tools...                  0.2s
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 1.22.5, on Linux, locale en_US.UTF-8)
[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.dev/docs/get-started/install/linux#android-setup for detailed instructions).
      If the Android SDK has been installed to a custom location, set ANDROID_SDK_ROOT to that location.
      You may also want to add it to your PATH environment variable.

[!] Android Studio (not installed)
[!] Connected device
    ! No devices available

! Doctor found issues in 3 categories.

```

#### Update your path
1. Add path:
   
   `$ echo 'export PATH=$PATH:~/flutter/bin' >> ~/.bashrc`
   
   `$ source ~/.bashrc`
   
2. Verify path:
   
   `$ echo $PATH`
   
3. Verify that the flutter command is available:
   
   `$ which flutter`
    
    OR
    
   `$ which flutter dart`

#### Install Android Studio
1. Download android studio: https://developer.android.com/studio

    `$ ~cd`

    `$ tar xf ~/Downloads/android-studio-ide-201.6953283-linux.tar.gz`

2. Set the path:
   
    `echo 'export PATH=$PATH:~/android-studio/bin' >> ~/.bashrc`

    `source ~/.bashrc`

#### Install android licenses
1. Run flutter doctor:
    
    `$ flutter doctor`

    ```
    Doctor summary (to see all details, run flutter doctor -v):
    [✓] Flutter (Channel stable, 1.22.5, on Linux, locale en_US.UTF-8)
    [!] Android toolchain - develop for Android devices (Android SDK version 30.0.3)
        ✗ Android licenses not accepted.  To resolve this, run: flutter doctor --android-licenses
    [!] Android Studio
        ✗ Flutter plugin not installed; this adds Flutter specific functionality.
        ✗ Dart plugin not installed; this adds Dart specific functionality.
    [!] Connected device
        ! No devices available

    ! Doctor found issues in 3 categories.
    ```
2. Run android-licenses:
   
    `$ flutter doctor --android-licenses`

3. Run flutter doctor:
   
    `$ flutter doctor`

    ```
    Doctor summary (to see all details, run flutter doctor -v):
    [✓] Flutter (Channel stable, 1.22.5, on Linux, locale en_US.UTF-8)
    [✓] Android toolchain - develop for Android devices (Android SDK version 30.0.3)
    [!] f Studio
        ✗ Flutter plugin not installed; this adds Flutter specific functionality.
        ✗ Dart plugin not installed; this adds Dart specific functionality.
    [!] Connected device
        ! No devices available

    ! Doctor found issues in 2 categories.
    ```


#### Set Flutter and Dart plugin

- Start the Android Studio application.
- File>Settings>Plugins.
- Select Browse repositories…, select the Flutter plug-in and click install .
- Click Yes when prompted to install the Dart plugin.
- Click Restart when prompted.

![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/flutter_plug-in_1.png?raw=true)
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/flutter_plug-in_2.png?raw=true)

 - if you still get `flutter and dart plugin not installed` error, do following: 

    `$ flutter channel dev`

    `$ flutter upgrade`

    `$ flutter doctor`

    ```
    Downloading package sky_engine...                                  238ms
    Downloading flutter_patched_sdk tools...                         1,606ms
    Downloading flutter_patched_sdk_product tools...                 1,168ms
    Downloading linux-x64 tools...                                   2,917ms
    Downloading linux-x64/font-subset tools...                         426ms
    Doctor summary (to see all details, run flutter doctor -v):
    [✓] Flutter (Channel dev, 1.26.0-1.0.pre, on Linux, locale en_US.UTF-8)
    [✓] Android toolchain - develop for Android devices (Android SDK version 30.0.3)
    [✓] Android Studio
    [!] Connected device
        ! No devices available
    ```
