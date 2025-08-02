<!--
SPDX-FileCopyrightText: 2023-2025 Mirian Margiani
SPDX-License-Identifier: GFDL-1.3-or-later
-->

# Changelog

## upcoming

**Refactored signal/error handling:**

- Removed `MaintenanceOverlay`
- Added `MessageHandler` instead
- Added `DB.notify()` and `DB.notifyEnd()` functions

Fatal database errors will now automatically show a blocking overlay and stop
the user from continuing to use the app.

Custom events can be sent using the `DB.notify()` function. Custom events can be
handled in a custom handler for the `userSignalReceived` signal in
`MessageHandler`.

Custom events can show an overlay using the `MessageHandler::showOverlay()`
function.

Add `MessageHandler {}` to the main QML file to enable message handling.

## 0.1.0 (2025-07-31)

- first public release
