<div align="center">

# Awayra

### A calm, privacy-first break reminder for Windows

**Eye breaks. Movement reminders. Guided exercises. No account. No telemetry. No cloud dependency.**

[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows11&logoColor=white)](https://github.com/AWAYRA/AWAYRA-WPF/releases/latest)
[![.NET](https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![Version](https://img.shields.io/badge/version-1.3.2-4C8BF5)](https://github.com/AWAYRA/AWAYRA-WPF/releases/latest)
[![License](https://img.shields.io/badge/license-GPL--3.0--only-blue)](LICENSE)
[![Privacy](https://img.shields.io/badge/privacy-local--first-2ea44f)](#privacy)

### [Download Awayra for Windows](https://github.com/AWAYRA/AWAYRA-WPF/releases/latest/download/Awayra-Setup-x64.exe)

[Latest release](https://github.com/AWAYRA/AWAYRA-WPF/releases/latest) · [Changelog](CHANGELOG.md) · [Report an issue](https://github.com/AWAYRA/AWAYRA-WPF/issues)

</div>

---

## Overview

Awayra is a free and open-source Windows application for people who spend long periods working at a computer.

It runs quietly in the background and reminds you to:

- rest your eyes
- look away from the screen
- blink naturally
- stand up
- move and stretch
- avoid long uninterrupted periods of sitting

Awayra is deliberately local-first. It does not require an account, does not depend on a cloud service, and does not send usage telemetry.

The application provides two independent reminder systems:

| Reminder | Default interval | Default duration | Purpose |
|---|---:|---:|---|
| **Eye Reset** | 20 minutes | 20 seconds | Short visual reset with distance focus and counted blinking |
| **Move Break** | 45 minutes | 60 seconds | Stand, move, stretch and briefly leave the desk |

Both schedules can be customized independently.

---

# Product tour

The screenshots below show the current Awayra desktop experience.

## 1. System tray

<p align="center">
  <img src="docs/screenshots/awayra-system-tray.png" alt="Awayra system tray icon" />
</p>

Awayra is designed to remain available without occupying the taskbar during normal use.

The system tray integration provides persistent background access while keeping the main dashboard out of the way. Depending on your Windows configuration, Awayra can start minimized and continue running from the notification area until a reminder is due.

Key behavior:

- runs quietly in the Windows notification area
- keeps reminder timers active while the dashboard is closed
- supports launching with Windows
- supports starting minimized
- supports closing the dashboard back to the tray instead of exiting the application

---

## 2. Main dashboard

<p align="center">
  <img src="docs/screenshots/awayra-dashboard.png" alt="Awayra main dashboard" width="680" />
</p>

The dashboard gives a direct view of both reminder systems without requiring configuration screens.

Each reminder card shows its current state and countdown. Eye Reset and Move Break can be enabled, disabled or muted independently. You can also trigger either break immediately when you want to step away before the scheduled timer expires.

The dashboard also displays daily activity statistics, including completed eye resets, movement breaks, skipped reminders and snoozed reminders.

Main dashboard controls include:

- live countdown for Eye Reset
- live countdown for Move Break
- independent reminder on/off controls
- independent sound controls
- **Eye Reset Now** manual trigger
- **Move Break Now** manual trigger
- pause/resume control
- direct access to Settings
- daily reminder statistics

The goal is to keep the primary state of the application visible in one compact window.

---

## 3. Settings

<p align="center">
  <img src="docs/screenshots/awayra-settings.png" alt="Awayra settings window" width="1100" />
</p>

The Settings window groups the main behavior into four practical areas: sound and exercise, reminder timing, schedule behavior, and Windows/appearance options.

### Break sound and exercise

Awayra includes six locally generated reminder sounds:

| Sound | Character |
|---|---|
| Soft bell | Short, gentle alert |
| Gentle chime | Light notification tone |
| Calm drop | Minimal soft tone |
| Calm piano | Short piano phrase |
| Morning dew | Gentle rising melody |
| Still water | Slower, deeper calming melody |

You can configure:

- reminder sound
- volume
- repeat interval
- sound preview
- guided exercise animation

No sound asset needs to be downloaded at runtime.

### Reminder timers

Eye Reset and Move Break are configured independently.

For each reminder you can control:

- reminder enabled/disabled state
- sound enabled/disabled state
- interval
- break duration

This allows Awayra to support anything from frequent micro-breaks to longer movement intervals.

### Behavior and schedule

Awayra can be adapted to different work patterns with:

- optional Skip action
- optional Snooze action
- configurable snooze duration
- idle reset behavior
- configurable idle threshold
- optional work-hours restriction
- configurable start and end of the workday

When work hours are enabled, scheduled reminders can wait until the active work window resumes instead of appearing at inappropriate times.

### Appearance and Windows behavior

The break overlay can be adjusted from more solid to more transparent presentation.

Additional options include:

- overlay appearance
- Reduced Motion
- run at Windows startup
- start minimized
- close dashboard to tray

Reduced Motion keeps the break guidance available without relying on animated movement.

---

## 4. Move Break

<p align="center">
  <img src="docs/screenshots/awayra-move-break.png" alt="Awayra Move Break overlay" width="620" />
</p>

Move Break is intended to interrupt long periods of continuous sitting.

The overlay presents a short guided movement sequence with a large countdown and a simple instruction for the current stage. The break can encourage actions such as standing up, walking briefly, resetting posture, moving the shoulders and stretching away from the desk.

During a Move Break you can:

- keep reminder sound on or mute the current break
- skip the break when Skip is enabled
- snooze the break when Snooze is enabled
- mark the break complete

The interaction remains intentionally limited so the break screen does not become another task-management interface.

---

## 5. Eye Reset

<p align="center">
  <img src="docs/screenshots/awayra-eye-reset.png" alt="Awayra Eye Reset overlay" width="620" />
</p>

Eye Reset provides a short visual interruption to prolonged close-up screen focus.

The default experience is inspired by the commonly used 20-20-20 screen-break habit. Awayra's default configuration schedules a 20-second Eye Reset every 20 minutes.

The guided screen encourages you to look away, focus farther into the distance, relax your face and blink naturally. The default guided sequence counts ten blinks during the break.

The overlay provides:

- a large remaining-time indicator
- visual eye guidance
- blink counter
- simple distance-focus instructions
- current-break sound control
- optional Skip
- optional Snooze
- manual Complete action

Guided animation can be disabled entirely, and Reduced Motion is available for users who prefer static guidance.

---

# Core features

## Independent reminder engines

Eye Reset and Move Break maintain their own interval, duration, enabled state and sound preference.

You can use either reminder independently or run both together.

## Manual breaks

You do not need to wait for a timer. Both break types can be started directly from the dashboard.

## Daily statistics

Awayra records local daily counts for completed Eye Resets, completed Move Breaks, skipped reminders and snoozed reminders.

## Idle-aware scheduling

Awayra can reset reminder timing after the computer has been idle for a configured period. This prevents a reminder from appearing immediately after you return from a genuine break away from the computer.

## Work hours

Optional work hours let you restrict scheduled reminders to a defined time window.

## Multi-monitor and Windows lifecycle support

Awayra is designed for normal desktop conditions including:

- Windows 10 and Windows 11
- multiple displays
- per-monitor DPI
- display configuration changes
- monitor sleep and wake
- Windows lock and unlock
- suspend and resume
- Windows startup
- system tray operation

## Calm notification sounds

The included sounds are stored locally and are designed to function as gentle reminders rather than alarm-style interruptions.

---

# Privacy

Awayra is built to work locally.

It does **not** require:

- an account
- advertising
- telemetry
- analytics tracking
- a cloud profile
- browsing-history access
- application-usage tracking
- screenshot uploading

Settings, statistics and logs remain under:

```text
%LocalAppData%\Awayra\
```

## Break-overlay background capture

When a break overlay uses the blurred/frosted background effect, Awayra can temporarily capture the display underneath the overlay so it can be blurred locally.

That image:

- exists only in memory
- is not written to disk
- is not uploaded
- does not leave the computer
- is discarded when the break closes

If you do not want the display captured for this effect, set:

```text
Overlay appearance → Solid
```

---

# Download and installation

## Recommended download

| File | Purpose |
|---|---|
| [**Awayra-Setup-x64.exe**](https://github.com/AWAYRA/AWAYRA-WPF/releases/latest/download/Awayra-Setup-x64.exe) | Latest Windows x64 installer |
| [Awayra-Setup-x64.sha256.txt](https://github.com/AWAYRA/AWAYRA-WPF/releases/latest/download/Awayra-Setup-x64.sha256.txt) | SHA-256 checksum |
| [GitHub Releases](https://github.com/AWAYRA/AWAYRA-WPF/releases) | Release history and previous versions |

The installer includes the required .NET runtime.

Awayra installs per-user under:

```text
%LocalAppData%\Programs\Awayra
```

Administrator privileges are not required for normal installation.

Settings, schedules and statistics are preserved during normal upgrades unless data removal is explicitly requested.

### Silent clean installation

```powershell
Awayra-Setup-x64.exe /VERYSILENT /CLEANDATA=yes
```

### Silent uninstall with local-data removal

```powershell
unins000.exe /VERYSILENT /CLEANDATA=yes
```

> Official Awayra Windows binaries are distributed through this repository's GitHub Releases. Unsigned builds can trigger a Windows SmartScreen warning. Use the published SHA-256 checksum when you want to verify the installer.

---

# Development

## Requirements

- Windows 10 or Windows 11 x64
- .NET 10 SDK
- PowerShell
- Inno Setup 7 for installer builds

## Run locally

```powershell
powershell -ExecutionPolicy Bypass -File .\scripts\dev.ps1
```

## Build and test

```powershell
powershell -ExecutionPolicy Bypass -File .\scripts\verify-change.ps1
```

## Build installer

```powershell
powershell -ExecutionPolicy Bypass -File .\scripts\build-installer.ps1
```

CI builds the complete solution with warnings treated as errors and runs both core and application test suites on Windows.

---

# Repository structure

| Path | Responsibility |
|---|---|
| `src/Awayra.Core` | Scheduling, settings, validation, statistics and domain logic |
| `src/Awayra.App` | WPF UI, tray integration, overlays, persistence, sounds, diagnostics and Windows integration |
| `tests/Awayra.Core.Tests` | Platform-neutral domain tests |
| `tests/Awayra.App.Tests` | WPF application and service tests |
| `tests/Awayra.UiTests` | Windows UI automation tests |
| `installer` | Inno Setup installer configuration |
| `scripts` | Local development, verification and release helper scripts |
| `docs/screenshots` | README product screenshots |

---

# Contributing

Contributions are welcome.

Before opening a pull request, read [CONTRIBUTING.md](CONTRIBUTING.md).

For security issues, follow [SECURITY.md](SECURITY.md) rather than opening a public vulnerability report.

Additional project documents:

- [CHANGELOG.md](CHANGELOG.md) — release history
- [SECURITY.md](SECURITY.md) — security policy
- [CONTRIBUTING.md](CONTRIBUTING.md) — contribution guidelines
- [TRADEMARKS.md](TRADEMARKS.md) — use of the Awayra name and branding

---

# License

Awayra is licensed under **GPL-3.0-only**.

See [LICENSE](LICENSE) for the complete license text.

Copyright © 2026 Farzin Alavi.

---

## Medical notice

Awayra is a wellness and break-reminder application. It is not a medical device and is not a substitute for professional medical advice, diagnosis or treatment.

Persistent eye pain, severe headaches, double vision, numbness or ongoing musculoskeletal pain should be evaluated by a qualified healthcare professional.
