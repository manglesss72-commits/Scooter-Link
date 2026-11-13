# ScooterLink VR — Horizon OS

A redesigned, installable iPhone-first VR-style companion shell with an immersive home screen, app library, bottom dock, floating panels, quick controls, device center, media space, and locally saved preferences.

## Free iPhone installation
1. In GitHub, open **Settings → Pages**.
2. Choose **Deploy from a branch**, select **main** and **/(root)**, then Save.
3. Open the published HTTPS address in Safari on iPhone.
4. Tap **Share → Add to Home Screen**.
No paid Apple Developer membership is required for this web version.

## Included in this redesign
- Horizon OS-inspired spatial home screen and dock.
- App Library shortcuts for Roblox, Minecraft, Fortnite, Steam Link, media, and device center.
- Control Center, Device Center, Media Space, and Settings panels.
- Browser camera preview and iPhone motion permission request.
- Gamepad detection through the browser Gamepad API where supported.
- Local preferences for wallpaper, visual effects, and audio preference.
- Offline app shell after first successful load.

## Honest capability limits
This is a browser-based companion interface, not a replacement operating system or native VR runtime. It cannot mirror the iPhone screen to glasses, run PC Steam games locally, convert games into VR, inject input into other apps, provide full finger/depth/6DoF tracking, read glasses battery, force iOS audio routing, or guarantee low latency. Steam Link is a separate app and requires a gaming PC running Steam. Bluetooth alone cannot carry smooth video.

The previously shared Temu glasses listing did not confirm a display or compatible video input. Before implementing real mirroring, identify the exact glasses model and verify USB-C DisplayPort Alt Mode, HDMI input, or a supported wireless display receiver. Native iOS code or a manufacturer SDK may be required for deeper hardware integration.

Do not advertise screen mirroring, VR game support, or low-latency performance until tested on the actual iPhone and glasses.
