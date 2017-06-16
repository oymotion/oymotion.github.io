---
layout: default
---

# gForce 100 Armband User Guide

June 15th, 2017

* This will become a table of contents (this text will be scraped).
{:toc}

## Overview
gForce 100 Armband is a smart wearable device designed to recognize gestures
according to the sEMG signals when the user wears it on one of his/her forearms.
It also calculates orientation data in quaternions from its built-in 9-axis
MEMS at a refresh rate of 50Hz (100Hz will be supported).

![gForce100Armband](/assets/images/gForce100Armband.jpg)

## Predefined Gestures
The six predefined gestures are:
* _Fist_
* _Spread Fingers_
* _Wave In_
* _Wave Out_
* _Pinch_
* _Shoot_

Note:
> When both your arm and hand are at a rest state, it will be recognized as a
> '_Relax_' gesture.

## Instructions to Wearing and Performing Gestures
To make sure gForce armband can recognize your gestures, please refer to 
[Guide to Performing Gestures][GuideToPerformingGestures] and spend several minutes 
learning and training yourself. The recognition rate can reach 95% and even higher 
after you get familiar with performing the gestures properly.


## Turning on/off
- Turn on

    When the gForce 100 Armband is off, its green light LED will be off. To turn
    it on, simply press the button in the middle of its main block.

    When the gForce 100 Armband is powering on, it will vibrate for about 0.5 second.
    After successfully powering on, the green light LED will flash every 2
    seconds.

    Make sure the Armband has sufficient power, otherwise re-charge it with
    a micro USB line.

- Turn off

    When the gForce 100 Armband is on, pressing and holding the button for about 5
    seconds and then releasing will turn it off. The green LED being off
    indicates the device has been turned off successfully.

**Note**:
> If gForce 100 Armband is not in use, please turn it off. Right now the
> auto-low-power mode is not implemented yet.

## Re-charging
gForce 100 Armband is equipped with Li-ion battery (200mAh). The USB port on
the main block is used for battery re-charging.

During re-charging, the red light LED on the main block is on. Re-charging will
maximally take 2 hours, and after re-charging completes, the red light LED is
turned off.

**Note**:
>gForce 100 Armband is NOT designed to work during re-charging, as this brings in
>electrical noise which contaminates the weak EMG biometric signals.

## Other Status Indication

- When BLE connection is not established, the green light LED flashes with an
  interval of 2 seconds (2 seconds on and 2 seconds off).

- When connection with a BLE central (e.g. gForceJoint, gForceDongle or any
  other BLE central device), the green light LED flashed in a much higher
  frequency.

- The device will vibrate for about 100ms when a gesture is recognized.

[GuideToPerformingGestures]: https://www.youtube.com/watch?v=wBsYJf0wrkk
