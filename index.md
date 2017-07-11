---
layout: default
title:  "Welcome to the OYMotion Community!"
---

---
## gForce Armband
gForce 100 Armband is a smart wearable [Human Interface Device][HID] for
[gesture recognition][GestureRecognition]. It recognizes gestures according
to the sEMG signals of human forearms, and as well as calculates orientation
data in quaternions or [Euler Angles][EulerAngles] from its built-in 6-axis
[IMU][IMU] and tri-axis [magnetometer][magnetometer].

### Documents
* [gForce 100 Manual](/assets/downloads/gForce100_manual_v1.1-eng.pdf) &
  [gForce 100 User Guide](doc/gForce100UserGuide)

  The User Guide provides more detailed information than the Manual.

* [gForce 100 Embedded Suite User Guide](doc/gForce100EmbeddedSuiteUserGuide)

  Provides guide of using gForce 100 in embedded devices such as robots and
  prosthetics.

* [gForce Data Protocol](doc/gForceDataProtocol)

  The specification of gForce Data Protocol defines the details of gForce
  interacting with host computers of PC, AR and VR.

* [gForce EMG Raw Data](doc/gForceEMGRawData)

  Provides more information about using EMG raw data.

### Open Source Software
* [gForce SDK for Arduino][gForceSDKArduino]

  The open source library with example code to illustrate how to connnect
  gForce to Arduino-alike devices.

* [gForce Data Protocol Sample][gForceDataProtocolSample]

  An open source simple example developed for Android to illustrate
  [gForce Data Protocol](doc/gForceDataProtocol).

* [gForce SDK][gForceSDK]

  The SDK for Windows and Android with Unity support.

* [gForceApp][gForceApp]

  The **hub** application for other applications to interact with
  gForce. It also provides utilities for users setting, firmware upgrading and
  diagnosing gForce.

### Downloads
* [gForce Armband Firmware v3.1.10-20170711](/assets/downloads/gForceAPP_R3_1_10_20170711.bin) 

    Releases of gForce Armband firmware. Please upgrade firmware using the
    latest [gForceApp for Android][gForceAppForAndroid].
    
    **Note**: gForce Armband firmware v3.x.y is only for gForce Armband hardware v3.

* [gForceApp for Android][gForceAppForAndroid]

    Pre-built releases of [gForceApp][gForceApp] for Android.

* [sEMG Raw Data Capture Utility](/assets/downloads/RawDataCapture.zip)

    Only for gForce 100 with support for raw data capturing.

* [sEMG Raw Data Capture SDK](/assets/downloads/RawDataCaptureSDK.zip)

    Only for gForce 100 with support for raw data capturing.

---
## gForce Neuron
### Documents
* [gForce Neuron User Guide](doc/gForceNeuronUserGuide)

### Open Source Software
* [sEMG Filters Library][EMGFilters]

  Provides some basic filter functions for sEMG digital signals.


[HID]: https://en.wikipedia.org/wiki/Human_interface_device
[GestureRecognition]: https://en.wikipedia.org/wiki/Gesture_recognition
[EulerAngles]: https://en.wikipedia.org/wiki/Euler_angles
[IMU]: https://en.wikipedia.org/wiki/Inertial_measurement_unit
[magnetometer]:https://en.wikipedia.org/wiki/Magnetometer
[gForceSDKArduino]: https://github.com/oymotion/gForceSDKArduino
[gForceDataProtocolSample]: https://github.com/oymotion/gForceDataProtocolSample
[EMGFilters]: https://github.com/oymotion/EMGFilters
[gForceSDK]: https://github.com/oymotion/gForceSDK
[gForceApp]: https://github.com/oymotion/gForceApp
[gForceAppForAndroid]: https://github.com/oymotion/gForceApp/releases
