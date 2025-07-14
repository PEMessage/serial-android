
# setup guide
```bash
a2p /opt/android-sdk/cmdline-tools/latest/bin
export ANDROID_SDK_ROOT=/opt/android-sdk
px
q-sudo sdkmanager 'ndk;21.0.6113669'
q-sudo sdkmanager 'build-tools;29.0.2'
q-sudo sdkmanager 'platforms;android-30'

export ANDROID_NDK_HOME=/opt/android-sdk/ndk/21.0.6113669
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
q-task java/toggle-gradle-mirror.sh
px -g > gradle.properties
a2p $ANDROID_NDK_HOME # for ndk-build

./build-libs.sh -d
```
