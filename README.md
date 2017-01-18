# GoogleMapsApiStackOverflowError
This repository is for verify that GoogleMaps API for Android occurred StackOverflowError.

I had [the issue](https://code.google.com/p/gmaps-api-issues/issues/detail?id=10604) too.

So I created a new google maps project by Android Studio 2.2.3 and I run the app then I got StackOverflowError and ANR.


## Movies and logs
### StackOverflowError

![gmapi_stackoverflowerror](https://cloud.githubusercontent.com/assets/1450486/22019759/25471e6c-dcf8-11e6-938b-e4a920a14dc6.gif)

```
DynamiteModule: Local module descriptor class for com.google.android.gms.googlecertificates not found.
DynamiteModule: Considering local module com.google.android.gms.googlecertificates:0 and remote module com.google.android.gms.googlecertificates:2
DynamiteModule: Selected remote version of com.google.android.gms.googlecertificates, version >= 2
System  : ClassLoader referenced unknown path: /data/user/0/com.google.android.gms/app_chimera/m/00000014/n/armeabi
art     : Background sticky concurrent mark sweep GC freed 260251(12MB) AllocSpace objects, 18(1236KB) LOS objects, 21% free, 30MB/39MB, paused 11.742ms total 96.870ms
AndroidRuntime: FATAL EXCEPTION: GLThread 2541
AndroidRuntime: Process: com.tech_vein.googlemapsapistackoverflowerror, PID: 8420
AndroidRuntime: java.lang.StackOverflowError: stack size 1038KB
AndroidRuntime: 	at java.util.HashMap.get(HashMap.java:300)
AndroidRuntime: 	at maps.U.d.c(Unknown Source)
AndroidRuntime: 	at maps.K.h.a(Unknown Source)
AndroidRuntime: 	at maps.K.h.a(Unknown Source)
AndroidRuntime: 	at maps.K.h.c(Unknown Source)
```

### ANR
![gmapi_anr](https://cloud.githubusercontent.com/assets/1450486/22019894/c7f0f732-dcf8-11e6-8be4-09c7b02ed3d4.gif)

```
W/DynamiteModule: Local module descriptor class for com.google.android.gms.googlecertificates not found.
I/DynamiteModule: Considering local module com.google.android.gms.googlecertificates:0 and remote module com.google.android.gms.googlecertificates:2
I/DynamiteModule: Selected remote version of com.google.android.gms.googlecertificates, version >= 2
W/System: ClassLoader referenced unknown path: /data/user/0/com.google.android.gms/app_chimera/m/00000014/n/armeabi
I/art: Thread[2,tid=13732,WaitingInMainSignalCatcherLoop,Thread*=0xaee72000,peer=0x12d0c0a0,"Signal Catcher"]: reacting to signal 3
I/art: Wrote stack traces to '/data/anr/traces.txt'
```

## About phone

* Model number: Nexus 5
* Android version: 6.0.1


