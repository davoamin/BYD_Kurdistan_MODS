# BYD KR Vision

> [!IMPORTANT]
> BYD KR Vision is an independent third-party project and is not affiliated with BYD.

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
- Device-bound activation
- GitHub OTA update checking

---

## Release Information

| Item | Value |
| --- | --- |
| Version | `3.1.26` |
| Version code | `714` |
| Package name | `com.byd.kurdistan.dashcam` |
| GitHub release tag | `v3.1.26` |
| APK name | `BYD-KR-Vision-v3.1.26-release.apk` |

### What's Changed

- Fixed several bugs and stability issues
- Improved camera reliability
- Improved instrument-cluster projection
- Improved vehicle sleep and wake recovery
- Improved background service reliability
- Improved steering-wheel button handling
- Improved blind-spot camera reliability
- Improved camera preview and calibration behavior
- Improved compatibility across supported BYD vehicles
- Cleaned and polished the user interface
- General performance and reliability improvements

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
- Automatic camera recovery

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
- Multiple display-control methods
- Compatibility handling for different DiLink UI generations

### Projection Method

**Automatic (Recommended)** automatically selects the best available method for the detected vehicle system.

Manual compatibility methods are also available when required.

Compatibility depends on:

- Vehicle model
- Firmware version
- Android configuration
- Display layout
- Available system permissions

---

## Automatic Blind-Spot Camera

BYD KR Vision can automatically display the corresponding side camera when the left or right turn indicator is activated.

Features include:

- Independent left and right indicator detection
- Separate destination selection for each side
- Instrument-cluster display option
- Main-screen display option
- Automatic camera activation
- Automatic restoration when the indicator is cancelled
- Shared AVM camera session for faster switching
- Independent left and right calibration
- Preview Left and Preview Right controls

---

## Camera Calibration

Each supported camera view stores its own crop, size, and position configuration.

Available controls include:

- Width
- Height
- X position
- Y position
- Horizontal crop
- Vertical crop
- Move Y
- `−5` fine adjustment
- `+5` fine adjustment

Fine adjustment controls:

- Change the selected value by exactly five units
- Apply the result immediately
- Save the new value
- Update only the currently selected camera profile

Separate camera profiles are maintained for:

- Dashcam
- Rear Camera
- Front Camera
- Dual Mirror
- Blind-spot camera views

---

## Custom Steering-Wheel Buttons

BYD KR Vision provides two independent custom steering-wheel button profiles:

```text
Custom Button 1
Custom Button 2
```

Each profile supports:

- Independent physical-button detection
- Separate key-code and scan-code storage
- Single-press action
- Double-press action
- Long-press action
- Independent target application
- Save and activate
- Restore original function
- Persistent configuration after reboot
- Recovery after vehicle sleep and wake

The same physical button cannot be assigned to both profiles.

### Available Actions

Each supported press type can be assigned to one of the following:

- Start Projection
- Stop Projection
- Restore Dashboard
- Open App
- Switch Camera View
- No Action

The **Switch Camera View** action cycles through:

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
- Blind-spot service recovery
- Startup-pipeline recovery
- Existing task reuse

---

## Device Activation

BYD KR Vision uses device-bound activation.

The activation screen provides:

```text
Device ID
Copy Device ID
Send Request
Receive License
```

### Activation Steps

1. Open BYD KR Vision.
2. Make sure the vehicle head unit has internet access.
3. Copy the displayed Device ID if required.
4. Press **Send Request**.
5. Wait for the activation request to be approved.
6. Press **Receive License**.
7. Restart the app if requested.

---

## OTA Updates

BYD KR Vision can check GitHub Releases for newer application versions.

Recommended GitHub release format:

```text
Tag: v3.1.26
Asset: BYD-KR-Vision-v3.1.26-release.apk
```

Updates should always use the same package name and official release signing key.

---

## Installation

### Standard Installation

1. Download:

```text
BYD-KR-Vision-v3.1.26-release.apk
```

2. Copy the APK to the BYD head unit.
3. Open the APK using Android's package installer.
4. Allow installation from the selected source when requested.
5. Install BYD KR Vision.
6. Open the application.
7. Grant the required permissions.
8. Complete device activation.
9. Configure camera and projection options while the vehicle is safely parked.

---

### Update an Existing Installation

Install the new APK directly over the existing application.

Do not:

- Uninstall the previous version
- Clear application data
- Change the package name
- Sign the APK with a different key

The official package name is:

```text
com.byd.kurdistan.dashcam
```

---

### ADB Installation

```powershell
adb install -r "BYD-KR-Vision-v3.1.26-release.apk"
```

The `-r` option updates the application while preserving existing app data.

---

## Required Permissions

Available functions may require some or all of the following:

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

Permission availability varies by vehicle, firmware, region, and DiLink configuration.

---

## Compatibility

BYD KR Vision is designed primarily for compatible **BYD DiLink 5** vehicles.

Known or targeted vehicle families include:

- BYD Song Plus
- BYD Seal 06
- BYD Seal 07
- BYD Qin L
- BYD Seal 05 with compatible dashcam hardware
- Leopard 3
- Leopard 5
- Leopard 7
- Leopard 8

Compatibility requirements may include:

- DiLink 5
- Compatible BYD camera hardware
- Secondary instrument-cluster display
- Required BYD system permissions
- Local ADB availability
- Shell access for advanced functions

Not every feature is guaranteed to work on every BYD model or firmware version.

Different vehicles may use different:

- Camera IDs
- Display IDs
- Permissions
- System services
- Projection methods

Some models may require additional compatibility adjustments.

---

## Recommended Initial Setup

1. Park the vehicle safely.
2. Install BYD KR Vision.
3. Open the application.
4. Complete device activation.
5. Grant the required permissions.
6. Keep **Automatic (Recommended)** selected for Projection Method.
7. Preview the Dashcam view.
8. Preview the Rear Camera.
9. Preview the Front Camera.
10. Calibrate crop, size, and position where required.
11. Preview Dual Mirror.
12. Preview the left blind-spot camera.
13. Preview the right blind-spot camera.
14. Configure Custom Button 1 if required.
15. Configure Custom Button 2 if required.
16. Test single, double, and long-press actions.
17. Test projection recovery.
18. Test vehicle sleep and wake recovery.

---

## Troubleshooting

### Device Activation Does Not Complete

- Confirm the device has an internet connection.
- Confirm the displayed Device ID is correct.
- Send the activation request again.
- Wait for the request to be approved.
- Press **Receive License** after approval.
- Restart the app if necessary.

---

### Custom Button Does Not Respond

- Confirm that Accessibility Service is enabled.
- Detect the physical button again.
- Save and activate the profile.
- Confirm that the same physical button is not assigned to both profiles.
- Restart the button service if available.
- Reboot the head unit if necessary.

---

### Camera Opens on the Wrong Screen

- Verify the selected display destination.
- Keep the projection method on **Automatic (Recommended)**.
- Check **System Status** or **Projection Status**.
- Restore the dashboard and restart projection if required.

---

### Camera Preview Does Not Start

- Confirm the required camera permissions are available.
- Confirm the selected camera is supported by the vehicle.
- Stop any other active camera view.
- Try the camera preview again.
- Restart the application if required.

---

### Camera Calibration Is Not Visible

- Confirm that the correct camera profile is selected.
- Open the live camera preview.
- Adjust the required Width, Height, Crop, X, or Y value.
- Use `−5` and `+5` for fine adjustment.
- Restart the camera view if required.

---

### Blind-Spot Camera Does Not Open

- Confirm the blind-spot function is enabled.
- Preview the left and right cameras manually.
- Confirm the selected destination screen.
- Check the vehicle indicator operation.
- Restart the blind-spot function if necessary.

---

### Projection Does Not Start

- Keep the projection method on **Automatic (Recommended)**.
- Confirm that the secondary display is detected.
- Check **Projection Status**.
- Restore the original dashboard.
- Start projection again.
- Restart the application or head unit if necessary.

---

### Projection Stops After Vehicle Sleep

- Confirm vehicle wake recovery is enabled.
- Confirm the required background permissions are available.
- Open BYD KR Vision once after reboot.
- Start projection again if required.
- Test recovery while the vehicle is safely parked.

---

## Safety

> [!WARNING]
> Configure and test all camera, projection, blind-spot, and steering-wheel button functions only while the vehicle is safely parked.

Do not interact with the app while driving.

Camera views must not cover essential vehicle information or distract the driver.

The user is responsible for following applicable:

- Traffic regulations
- Vehicle regulations
- Safety requirements
- Software regulations

---

## Source and Distribution

BYD KR Vision is proprietary software.

The source code may not be:

- Copied
- Modified
- Republished
- Redistributed
- Sublicensed
- Sold

without written permission from the copyright owner.

The compiled APK may only be distributed through authorized **BYD Kurdistan MODS** channels.

Unauthorized modified or redistributed versions are not supported.

---

## Disclaimer

BYD KR Vision is an independent third-party project.

BYD, DiLink, Fang Cheng Bao, Leopard, and related names and logos are trademarks of their respective owners.

No affiliation, endorsement, partnership, or sponsorship by BYD is implied.

Use this software at your own risk.

Vehicle cameras, displays, firmware, Android services, permissions, and system behavior may vary across vehicle models and software versions.

---

## Author

**Davar Amin**  
**BYD Kurdistan MODS**

---

## Copyright

Copyright © 2026 Davar Amin. All rights reserved.
