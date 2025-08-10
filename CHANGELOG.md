<!--
SPDX-FileCopyrightText: 2023-2025 Mirian Margiani
SPDX-License-Identifier: GFDL-1.3-or-later
-->

# Changelog

## 0.3.1 (2025-08-10)

- Added translations: Arabic, Belarusian, Dutch (Belgium), Lithuanian, Norwegian Nynorsk, Persian, Portuguese, Portuguese (Brazil)
- Updated translations: Ukrainian

## 0.3.0 (2025-08-08)

- Renamed `StorageHelper.js` to `LocalStorage.js`
- Added support for managing multiple databases by moving global functions and
  settings into a new `Database` class
- Added documentation for most properties and functions but it is still incomplete

## 0.2.0 (2025-08-02)

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
