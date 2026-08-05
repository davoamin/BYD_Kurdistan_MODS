# BYD KR Vision

<p align="center">
  <strong>Camera projection, digital mirror views, blind-spot monitoring, crop calibration, and steering-wheel button customization for compatible BYD DiLink vehicles.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Version-3.0.11-blue" alt="Version">
  <img src="https://img.shields.io/badge/Android-9%2B-green" alt="Android">
  <img src="https://img.shields.io/badge/Platform-BYD%20DiLink-orange" alt="Platform">
  <img src="https://img.shields.io/badge/Source-Proprietary-red" alt="Source">
</p>

> [!IMPORTANT]
> BYD KR Vision is an independent third-party project.

---

## Overview

**BYD KR Vision** provides advanced camera and instrument-cluster functions for compatible BYD DiLink 5 vehicles.

The app supports:

- Instrument-cluster camera projection
- Dashcam live view
- Digital rear-view mirror
- Front camera view
- Dual side-mirror view
- Automatic left and right blind-spot cameras
- Custom steering-wheel button actions
- Vehicle sleep and wake recovery
- Device-bound licensing
- GitHub OTA update checking


---

## Release Information

| Item | Value |
|---|---|
| Version | `3.0.11` |
| Version code | `674` |
| Package name | `com.byd.kurdistan.dashcam` |
| GitHub release tag | `v3.0.11` |
| APK name | `BYD-KR-Vision-v3.0.11-release.apk` |

---

## Camera Views

### Dashcam

Displays the vehicle dashcam feed on the selected screen.

### Rear Camera

Uses the panoramic AVM camera as a digital rear-view mirror.

### Front Camera

Displays the dedicated front AVM camera as a single forward-facing view.

### Dual Mirror

Displays the left and right side cameras together on the instrument cluster.

Dual Mirror supports:

- Separate left and right camera surfaces
- Correct rear-facing mirror direction
- Independent crop calibration
- Normal and Rear Focus tuning modes
- Shared panoramic AVM camera session


---

## Instrument-Cluster Projection

Supported camera views can be projected to the secondary instrument-cluster display on compatible BYD DiLink systems.

Projection functions include:

- Start projection
- Stop projection
- Restore the original BYD dashboard
- Reuse an existing projection task
- Recover projection after screen sleep
- Recover projection after vehicle wake
- Keep projection active while returning to the main launcher
- Automatic secondary-display detection
- Modern and legacy display-control paths
- Compatibility handling for DiLink UI5, UI6, and UI7

Compatibility depends on the vehicle model, firmware, Android configuration, display layout, and available system permissions.

---

## Automatic Blind-Spot Camera

BYD KR Vision can display the corresponding side camera when the left or right turn indicator is activated.

Features include:

- Independent left and right indicator detection
- Separate destination selection for each side
- Instrument-cluster display option
- Main-screen display option
- Automatic activation
- Automatic restoration when the indicator is cancelled
- Shared AVM session for faster camera switching
- Manual Test Left and Test Right controls

---

## Camera Crop Calibration

Each camera view stores its own crop and position values.

Available controls:

- Horizontal crop
- Vertical crop
- Move Y
- `−5` fine adjustment
- `+5` fine adjustment

Each `−5` or `+5` press:

- Changes the selected value by exactly five units
- Applies the result immediately
- Saves the new value
- Uses the supported range from `-600` to `600`
- Updates only the currently selected camera profile

Separate crop profiles are maintained for:

- Dashcam
- Rear Camera
- Front Camera
- Dual Mirror

---

## Dual Custom Steering-Wheel Buttons

Version 3.0.11 provides two independent custom-button profiles:

```text
Custom Button 1
Custom Button 2
```

Existing configurations from older versions remain available as **Custom Button 1**.

Each profile supports:

- Independent physical-button detection
- Separate key-code and scan-code storage
- Single-press action
- Double-press action
- Long-press action
- Independent target application
- Save and activate
- Restore original function
- Persistent configuration after reboot and vehicle wake

The same physical button cannot be assigned to both profiles.

### Available Actions

Each press type can be assigned to one of the following:

- Start Projection
- Stop Projection
- Restore Dashboard
- Open App
- Switch Camera View
- No Action

The Switch Camera View action cycles through:

```text
Dashcam
→ Rear Camera
→ Front Camera
→ Dual Mirror
→ Dashcam
```

---

## Vehicle Sleep and Wake Recovery

BYD KR Vision includes recovery handling for compatible vehicle and Android power events.

Supported recovery conditions include:

- Screen off and screen on
- Vehicle sleep and wake
- Android user unlock
- ACC changes
- Ignition changes
- Quick boot
- Cold boot
- Package update
- System process recreation

Recovery functions include:

- Projection restoration
- Camera task restoration
- Secondary-display recovery
- Steering-wheel button-service recovery
- Startup-pipeline recovery
- Existing task reuse

---

## OTA Updates

The app checks GitHub Releases for newer APK versions.

Recommended release format:

```text
Tag: v3.0.11
Asset: BYD-KR-Vision-v3.0.11-release.apk
```

## Installation

### Standard Installation

1. Download `BYD-KR-Vision-v3.0.11-release.apk`.
2. Copy the APK to the BYD head unit.
3. Open the APK using Android’s package installer.
4. Allow installation from the selected source when requested.
5. Install the application.
6. Open BYD KR Vision.
7. Grant the required permissions.
8. Complete camera and projection configuration while parked.

### Update an Existing Installation

Install the new APK directly over the existing application.

Do not:

- Uninstall the previous version
- Clear application data
- Change the package name
- Sign the new APK with a different key

### ADB Installation

```powershell
adb install -r "BYD-KR-Vision-v3.0.11-release.apk"
```

The `-r` option updates the application while preserving its existing data.

---

## Required Permissions

Available features may require some or all of the following:

- Camera access
- Accessibility Service
- Display-over-other-apps permission
- Notification permission
- Install unknown apps permission
- Storage access
- BYD vehicle permissions
- BYD camera permissions
- Local ADB access
- Privileged shell access for advanced projection functions

Permission availability varies by vehicle, firmware, region, and DiLink generation.

---

## Compatibility

Compatibility depends on:

- BYD vehicle model - Song plus - Seal 06 - Seal 07 - Leopard 3/5/7/8 - Qin L - Seal 05 (withdashcam)
- DiLink generation 5
- Local ADB availability

Not every feature is guaranteed to work on every BYD model but we can customize it and fix it.

---

## Recommended Initial Setup

1. Park the vehicle safely.
2. Open BYD KR Vision.
3. Grant the required permissions.
4. Select the correct DiLink compatibility mode.
5. Test Dashcam view.
6. Test Rear Camera.
7. Test Front Camera.
8. Calibrate crop and Move Y for each camera.
9. Test Dual Mirror.
10. Test the left blind-spot camera.
11. Test the right blind-spot camera.
12. Configure Custom Button 1.
13. Configure Custom Button 2.
14. Test single, double, and long presses.
15. Test vehicle sleep and wake recovery.

---

## Troubleshooting

### Custom button does not respond

- Confirm that the Accessibility Service is enabled.
- Detect the physical button again.
- Save and activate the profile.
- Confirm that the same button is not assigned to both profiles.
- Restart the button service or reboot the head unit.

### Camera opens on the wrong screen

- Verify the selected display destination.
- Confirm the correct DiLink compatibility mode.
- Use the projection recovery controls.
- Stop and restart the projection task.

### Crop adjustment is not visible

- Confirm that the correct camera profile is selected.
- Open the live camera preview.
- Use `−5` and `+5` for fine adjustment.
- Restart the projection if the firmware is caching the previous surface.

### Projection stops after vehicle sleep

- Enable vehicle wake recovery.
- Confirm the required background permissions.
- Open the app once after reboot.
- Test recovery while the vehicle is safely parked.

---

## Security

BYD KR Vision includes protection and validation features such as:

- Device-bound licensing
- Online license request

---

## Safety

> [!WARNING]
> Configure and test all camera, projection, blind-spot, and steering-wheel button functions only while the vehicle is safely parked.

Do not interact with the app while driving.

Camera views must not cover essential vehicle information or distract the driver. The user is responsible for following local traffic, vehicle, safety, and software regulations.

---

## Source and Distribution

This project is proprietary software.

The source code may not be copied, modified, republished, redistributed, sublicensed, or sold without written permission from the copyright owner.

The compiled APK may only be distributed through authorized BYD Kurdistan MODS channels.

---

## Disclaimer

BYD KR Vision is an independent third-party project.

BYD, DiLink, and related names and logos are trademarks of their respective owners. No affiliation, endorsement, partnership, or sponsorship is implied.

Use this software at your own risk. Camera systems, displays, firmware, and vehicle services may behave differently across vehicle models and software versions.

---

## Author

**Davo Amin**  
**BYD Kurdistan MODS**

---

## Copyright

Copyright © 2026 Davar Amin. All rights reserved.
