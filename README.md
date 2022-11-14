修改MsQuic以支持更低版本的移动平台
IOS: 9+
android: 5+


### CHECK OUT:

* git clone --depth 1 --branch fix_mobile_2_1_3 https://github.com/fofewyoung/msquic
* git submodule update --init --recursive



### BUILD:

pwsh

// linux
scl enable devtoolset-8 bash
./scripts/build.ps1 -Config Release -Static -Clean -Tls openssl -Arch x64 -Platform linux

// ios
./scripts/build.ps1 -Config Release -Static -Clean -Tls openssl -Arch arm64 -Platform ios

// android
./scripts/build.ps1 -Config Release -Static -Clean -Tls openssl -Arch arm64 -Platform android
./scripts/build.ps1 -Config Release -Static -Clean -Tls openssl -Arch arm -Platform android
