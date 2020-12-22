# Flutter-on-Ubuntu20.04
## Install Flutter on Ubuntu 20.04 LTS

### Install Flutter manually
`sudo apt update`

1. Download here: https://flutter.dev/docs/get-started/install/linux

`$ cd ~`
`$ tar xf ~/Downloads/flutter_linux_1.22.5-stable.tar.xz`

2. Set path:
```export PATH="$PATH:`pwd`/flutter/bin"```

3. Optionnal. If you don't want to send analytics to Google:
`$ flutter config --no-analytics`

4. Optionally, pre-download development binaries:
`$ flutter precache`

5. Run flutter doctor:
`$ flutter precache`

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
1. Add path
`$ echo 'export PATH=$PATH:~/flutter/bin' >> ~/.bashrc`
`$ source ~/.bashrc`
2. Verify path
`$ echo $PATH`
3. Verify that the flutter command is available
`$ which flutter`
OR
`$ which flutter dart`

### Install Android 
1. Download android studio
https://developer.android.com/studio

`$ ~cd`

`$ tar xf ~/Downloads/android-studio-ide-201.6953283-linux.tar.gz`

`echo 'export PATH=$PATH:~/android-studio/bin' >> ~/.bashrc`

`source ~/.bashrc`

2. Run Android Studio 
`studio.sh`
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/android_install_1.png?raw=true)