# Christmas Door Magic

Upload the contents to a GitHub Pages repository. Put five licensed MP3 files in `music/` named `a.mp3` through `e.mp3` (the folder is initially empty). The demo button plays the time-appropriate file, from 07:00 to 17:00. Cooldown: 20 seconds.

**Important:** GitHub Pages cannot directly access USB hardware or trigger autoplay without browser permission. For a real door sensor, run a local bridge on the Mac mini (e.g. a small local HTTP/WebSocket service reading an ESP32-S3 USB serial device or HID contact). The bridge must trigger `window.dispatchEvent(new Event('door-open'))` in a locally hosted or connected browser page. The exact bridge depends on the selected hardware and macOS permissions. The current download is the visual frontend/demo, not a completed hardware integration.

For reliable unattended playback, prefer a local macOS process to play audio (e.g. `afplay`) on door-open, rather than relying on GitHub Pages browser autoplay.
