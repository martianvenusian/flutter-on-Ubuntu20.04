# Flutter-on-Ubuntu20.04
## Install Flutter on Ubuntu 20.04 LTS

    
#### Install flutter manually
 - Download here: https://flutter.dev/docs/get-started/install/linux

    `$ sudo apt update`

    `$ cd ~`

    `$ tar xf ~/Downloads/flutter_linux_1.22.5-stable.tar.xz`

- Set path:
    
    ```export PATH="$PATH:`pwd`/flutter/bin"```

- Optionnal. If you don't want to send analytics to Google:
   
    `$ flutter config --no-analytics`

- Optionally, pre-download development binaries:
   
   `$ flutter precache`

- Run flutter doctor:
   
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
- Add path:
   
   `$ echo 'export PATH=$PATH:~/flutter/bin' >> ~/.bashrc`
   
   `$ source ~/.bashrc`
   
- Verify path:
   
   `$ echo $PATH`
   
- Verify that the flutter command is available:
   
   `$ which flutter`
    
    OR
    
   `$ which flutter dart`

#### Install Android Studio
- Download android studio: https://developer.android.com/studio

    `$ ~cd`

    `$ tar xf ~/Downloads/android-studio-ide-201.6953283-linux.tar.gz`

- Set the path:
   
    `echo 'export PATH=$PATH:~/android-studio/bin' >> ~/.bashrc`

    `source ~/.bashrc`

#### Install android licenses
 - Run flutter doctor:
    
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
 - Run android-licenses:
   
    `$ flutter doctor --android-licenses`

 - Run flutter doctor:
   
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

 - Run flutter doctor again: 

   `$ flutter doctor`
   
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
### Adding an Android Emulator
Open Android Studio > Go to [Tools] > Choose [AVD Manager]
##### Troublesoot:

In case these is troubleshoot which is `/dev/kvm is not found` then first solve the problem

![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_1.png?raw=true)

##### Solution:

 - Restart your computer and Go to the system BIOS (press Del or F2 (It is different in each system,my system is Del key))

 - In Advanced tab Choose,Cpu configuration and Enabled Intel Virtualization Technology,Finally Save the Changes and Restart Your Computer.

##### Continiue:
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_2.png?raw=true)
 - Select `Create Virtual Device`
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_3.png?raw=true)
 - Choose `Phone` and click `Next`
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_4.png?raw=true)
- Choose a device name (for ex:`PixelXL`) and click `Next`
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_5.png?raw=true)
- Download and install system image (for ex:`R`) and click `Next`
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_6.png?raw=true)
- Make AVD Name  (for ex:`Pixel XL API 30`) and click `Finish`
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_7.png?raw=true)
- Click Actions to play
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_8.png?raw=true)
- here it is
![alt text](https://github.com/martianvenusian/flutter-on-Ubuntu20.04/blob/main/images/adding_emulator_9.png?raw=true)