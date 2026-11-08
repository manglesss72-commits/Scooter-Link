# ScooterLink VR

An installable iPhone-first VR-style dashboard preview for smart glasses and game streaming.

## Publish with GitHub Pages
1. Open **Settings → Pages**.
2. Choose **Deploy from a branch**, branch **main**, folder **/(root)**, then Save.
3. Wait for GitHub Pages to publish.
4. Open the HTTPS Pages URL in Safari on iPhone.
5. Tap **Share → Add to Home Screen**.

## Game library
- Roblox, Minecraft, Fortnite and VR media links are launch/information shortcuts only. They do not create VR modes or mirror the iPhone display.
- **Steam Link** is linked from the Steam tile. Install the official Steam Link iOS app, pair a compatible controller, and connect to a Windows, Mac, or Linux computer running Steam on the same local network. The gaming PC renders and runs the Steam game; the iPhone receives the video stream. The iPhone does not run the Windows Steam library natively.
- For best Steam Link performance, Valve recommends connecting the host PC to the router using Ethernet and connecting the iPhone to the router's 5 GHz Wi-Fi band. Keep the iPhone close to the router. Actual latency depends on the PC, network, game, and display path.

## What this version does
- Presents a responsive VR-inspired home screen.
- Provides a Steam Link App Store shortcut and game information links.
- Shows connection/display compatibility guidance.
- Offers interface-only display quality, motion, and audio preferences.
- Caches the app shell for offline reopening after the first successful load.

## What it does NOT do
- It does not mirror the iPhone screen to glasses.
- It does not stream Steam games itself; Steam Link is a separate official app and requires a computer running Steam.
- It does not convert Roblox, Minecraft, Fortnite, or Steam games into VR.
- It does not connect to the Temu glasses, read their battery, or route audio directly.
- It does not measure FPS, temperature, or display latency.

## Hardware and performance requirements
The previously shared Temu AI glasses listing did not establish that the glasses contain a video display or accept USB-C DisplayPort/HDMI input. Bluetooth alone cannot carry a smooth video feed. For a low-latency display path, the glasses must explicitly support a video input compatible with the exact iPhone model (for example, USB-C DisplayPort Alt Mode). iPhone model variants differ, so verify the exact model and glasses specifications before buying adapters.

A native iOS app or manufacturer-supported integration may be needed for hardware features. No compatibility or lag-free performance claim should be made until tested on the actual devices.

## Input and controller modes
The dashboard includes selectable UI modes for camera-based hand tracking, compatible VR controllers/gamepads, iPhone motion sensors, and touch controls. These are preference/interface selections, not implemented system-wide input drivers. Hand tracking requires compatible tracking hardware or a native app using camera/hand-pose APIs, plus an application that accepts the hand input. iPhone motion data requires permission and app-level integration. Bluetooth controllers work only where iOS, Steam Link, and the target game support them. This web app cannot inject hand/controller input into other iPhone apps.


## iPhone camera motion tracking (v5)
- Start the **iPhone camera motion tracker** from the dashboard in Safari over HTTPS and grant camera permission.
- The browser loads MediaPipe Pose Landmarker Lite and estimates a single person's 33 body landmarks. It draws a live skeleton overlay and displays simple arm-raise / arms-spread gesture labels.
- The camera feed is processed in the browser and is not uploaded or saved by this feature. Stop tracking or leave the page to stop the camera.
- Best results: use the rear or front camera in a bright, uncluttered space; place the iPhone so your full body is visible from roughly 6–10 feet away. Performance varies by iPhone, lighting, browser, and thermal state.
- This is **body-pose tracking**, not full Kinect hardware: it does not provide depth sensing, individual finger tracking, precise 6DoF tracking, or room-scale controller tracking. The gesture labels are visual feedback only and are not injected into other apps or games.
- The model and runtime are downloaded from public CDNs the first time the tracker is used, so an internet connection is required to initialize it. The camera itself requires HTTPS and explicit permission.
