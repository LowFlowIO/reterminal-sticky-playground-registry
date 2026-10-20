# RxNudge

Household medication reminder firmware for the Seeed reTerminal Sticky.

> **Not a medical device.** RxNudge is a reminder aid. Always follow your doctor's and pharmacist's instructions.

## Overview

RxNudge turns the reTerminal Sticky into a tabletop/fridge magnet medication reminder for one or more people in a household. Each person has their own medicines, schedules, PIN, and history. When a dose is due the device beeps and the e-paper screen shows whose medicine is due. You confirm that you took it; the device keeps a record.

Source and full documentation: https://github.com/LowFlowIO/RxNudge

## Features

- Multi-person profiles with individual schedules, PIN lock, and privacy mode
- Flexible schedules: fixed times, weekdays, every N days/weeks, specific dates, on/off cycles, multi-phase tapers, and as-needed (PRN)
- Alarm ladder with snooze, grace period, quiet hours, and per-person/medicine tones
- No double-dosing: taken doses cannot be retaken
- Power-loss safe storage and deep sleep with catch-up
- Optional Wi-Fi (off by default): NTP, LAN web portal at `http://rx-nudge.local`, OTA, ntfy/webhook alerts
- CSV/JSON export and SD card backup/restore

## Controls

| Control | Action |
| --- | --- |
| Touch screen | Tap buttons |
| UP / DOWN | Move between buttons |
| OK / AI button | Confirm / wake |
| Hold OK 2 s (home) | Sleep |

## Setup

1. Flash the firmware from the Playground (or the factory image in the source release).
2. Follow the on-device setup wizard:
   - Welcome and language
   - Time zone (Europe/Berlin preselected)
   - Optional Wi-Fi
   - Set the clock (or sync from the internet)
   - Add the first person
   - Optional PIN
3. Add medicines under **Menu > Medications**.

Reminders start only after the clock is set.

## Hardware test record

| Item | Result |
| --- | --- |
| Hardware | reTerminal Sticky production hardware |
| Firmware version | `1.0.4` |
| Power-on and first boot | Passed |
| Setup wizard | Passed |
| Home screen and alarms | Passed |
| Touch and buttons | Passed |
| Sleep / wake | Passed |
| Optional Wi-Fi / portal | Passed |
| Flash method | Full image at offset 0, DIO, 40 MHz, 16 MB |

## Version history

- `1.0.4` — initial Playground release
