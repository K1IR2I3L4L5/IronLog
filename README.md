# IRON LOG // ANDROID GYM OS

![Platform](https://img.shields.io/badge/PLATFORM-ANDROID%208.0%2B-161616?style=flat-square&labelColor=1D2021&color=D5C4A1)
![Kotlin](https://img.shields.io/badge/KOTLIN-2.0-161616?style=flat-square&labelColor=1D2021&color=D5C4A1)
![UI](https://img.shields.io/badge/UI-JETPACK%20COMPOSE%20M3-161616?style=flat-square&labelColor=1D2021&color=D5C4A1)
![License](https://img.shields.io/badge/LICENSE-MIT-161616?style=flat-square&labelColor=1D2021&color=D5C4A1)

**IRON LOG** is a strict, ad-free, offline-first Android workout tracker designed for serious gym training. Built with a minimalist retro-terminal dark aesthetic (`#121212` / `#1A1C1E`), it features live background rest timers, lockscreen media controls, and voice guidance.

---

## Key Features

- **Weekly Program Planner (Mon–Sun)** — Customizable workout splits with exercise search, target weight/reps/sets configuration, and real-time weekly muscle volume tracking (hypertrophy range indicators).
- **Live Workout Mode** — Real-time tracking of each working set, auto-warmup set generator (`50% × 10`, `70% × 6`, `85% × 3`), RPE tracking, and one-click data loading from previous sessions.
- **Background Rest Timer & Media Shade** — Powered by a persistent `ForegroundService` and `WakeLock` to survive screen-off states. Includes a media-style notification controller (`MediaStyle` + `MediaSession`) directly on the lockscreen with quick actions (`-15s`, `+30s`, `Skip`, `✓ Complete Set`).
- **Tactical Alerts & Voice Callouts** — Audio-focus ducking (smoothly lowers your music instead of pausing it), custom synthetic alarm tones, and Russian Text-to-Speech (TTS) voice announcements announcing the next exercise, weight, and reps.
- **Gym Calculator Toolkit** — Symmetrical 2D barbell plate loading calculator (showing exact plates for each side of the bar), 1-Rep Max calculator (Epley & Brzycki formulas with percentage tables), and custom exercise creation.

---

## Tech Stack & Architecture

- **Language:** 100% Kotlin
- **UI:** Jetpack Compose (Material 3, Monospace typography, custom dark industrial design)
- **Architecture & System APIs:** `ForegroundService`, `MediaSession`, `AudioTrack`, `TextToSpeech`, `SharedPreferences` local persistence.

---

## Permissions Used

| Permission | Purpose |
|---|---|
| `FOREGROUND_SERVICE` / `SPECIAL_USE` | Keeping the rest timer and notification controller alive in the background. |
| `POST_NOTIFICATIONS` | Displaying the active workout media player in the notification shade. |
| `WAKE_LOCK` | Ensuring precise countdown accuracy even when the device screen is locked. |
| `VIBRATE` | Haptic feedback when rest time expires. |

---

## Download & Installation

### Option 1: Quick Install (Recommended)
1. Go to the **[Releases](../../releases)** page of this repository.
2. Download the latest `IronLog-vX.X.apk` file directly to your Android phone.
3. Install and run (offline, no ads or permissions required beyond system needs).

### Option 2: Build from Source
1. Clone the repository:
   ```bash
   git clone [https://github.com/K1IR2I3L4L5/IronLog.git](https://github.com/K1IR2I3L4L5/IronLog.git)
   Open the project in Android Studio.
   Build the APK via Build → Build Bundle(s) / APK(s) → Build APK(s) or run directly via Shift + F10.
