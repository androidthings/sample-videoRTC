# Android Things video call sample app using WebRTC

This Android Things sample app demonstrates how to establish WebRTC video call. It's based on the
original [WebRTC Android sample](https://webrtc.org/native-code/android/), slightly modified
to easily run on Android Things devices. For simplicity it creates a WebRTC room with a random ID,
which is shown on display and in logcat, and then auto-joins the room on boot. Now this room
can be joined to establish a video call connection from either a web client at https://appr.tc or
an Android client running the original WebRTC sample by entering the same room ID.

Two WebRTC clients need to exchange session description when establishing video call connection
via a signal server. This sample uses a hosted version of the [WebRTC signaling server](https://appr.tc).
Please refer to https://www.html5rocks.com/en/tutorials/webrtc/infrastructure/ for more information
on WebRTC signaling.

> **Note:** The Android Things Console will be turned down for non-commercial
> use on January 5, 2022. For more details, see the
> [FAQ page](https://developer.android.com/things/faq).

## Pre-requisites

1. Android Things compatible boards e.g. Raspberry Pi 3 or NXP boards
1. Android Things compatible camera (for example, the Raspberry Pi 3 camera module)
1. Android Studio 3+

## WebRTC-specific dependencies

This sample has the following dependencies but they are either already included or directly linked
so that no additional steps are necessary.

* [WebRTC signaling server](https://appr.tc): The sample is set up to use the one hosted in https://appr.tc,
[source code](https://github.com/webrtc/apprtc#apprtc-demo-code).
* [The Autobahn libraries for WebSocket and WAMP](https://crossbar.io/autobahn/) with the autobanh.jar
included at app/libs/autobanh.jar inside this project.
* [WebRTC library at bintray/JCenter] (https://bintray.com/google/webrtc/google-webrtc)

## Build and Run

Build this app in Android Studio and run it on an Android Things board:

* Deploy and run the `app` module, which creates and joins a room with random ID
* The room ID will be shown on the display and on logcat. Take note of it, so that you can join the room with another device

Join the room from another WebRTC client:

* From a web browser, go to https://appr.tc and enter the same room ID shown on the Android Things display, or
* Use one of the native webRTC samples, like [Android](https://webrtc.org/native-code/android/) or [iOS](https://webrtc.org/native-code/ios/) app and enter the room ID to join

## Categories

- Android Things

## Solutions

- IoT

## Languages

- Java


## License

See LICENSE
