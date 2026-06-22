# Privacy Policy for Živý Obraz

Effective date: June 22, 2026

This privacy policy explains how the Živý Obraz Android app handles user, account, device, and diagnostic data.

## Data We Collect or Process

The app is used to display and manage data from the Živý Obraz service. To provide its functionality, the app may process:

- Živý Obraz export keys and optional import keys entered by the user
- optional account aliases, device aliases, Group IDs, and device names entered by the user
- account information returned by the Živý Obraz export API, such as account ID, email address, verification state, prepaid device count, and subscription date if provided by the service
- e-paper identifiers, including MAC addresses, captions, notes, groups, model information, display metadata, board type, firmware, and reset reason
- sensor and status data such as temperature, humidity, pressure or CO2, battery level, battery voltage, Wi-Fi SSID, RSSI, last contact time, next expected contact time, picture download time, and display refresh time
- custom values returned by the Živý Obraz `my_values` export, including value names, values, timestamps, and notes
- local chart history generated from e-paper measurements and numeric custom values
- optional phone battery status and charging state if the user enables phone battery push
- local notification state used to avoid repeated e-paper alerts
- local diagnostic logs used for troubleshooting refresh, cache, widget, backup, notification, and phone battery push behavior
- backup settings, backup diagnostics, and encrypted backup files created by the user

The app does not collect location, contacts, calendar data, photos, videos, audio recordings, messages, browsing history, payment information, health data, advertising IDs, or installed app lists.

## Camera and QR Code Scanning

The app requests camera permission only when the user chooses to scan an export key or import key from a QR code.

Camera frames are processed locally on the device for QR code detection. The app does not store photos or videos and does not upload camera images or video frames to any server.

## Notifications

If enabled, the app can show local Android notifications for e-paper status changes, such as overdue devices, recovery, and low battery. Notification state is stored locally on the device.

The app does not use notifications for advertising or marketing.

## How We Use Data

The app uses data only to provide app functionality, including:

- loading and displaying e-paper devices
- loading and displaying custom values
- refreshing device and custom value status manually, on app foreground, through widgets, and in the background
- showing home screen widgets
- showing chart history for e-papers and numeric custom values
- showing local e-paper status notifications
- validating account settings and showing account subscription information when available
- optionally sending phone battery status to the Živý Obraz service
- creating and restoring user-controlled encrypted backups
- helping troubleshoot app behavior through diagnostic logs

## Data Sharing

The app does not sell user data.

The app communicates with the Živý Obraz service using HTTPS endpoints operated for app functionality:

- `https://out.zivyobraz.eu/` for loading account information, e-paper devices, and custom values
- `https://in.zivyobraz.eu/` for optional phone battery push

Data is not shared with advertising networks or analytics providers.

The app does not include advertising SDKs or third-party analytics SDKs. Third-party libraries used by the app provide local app functionality such as Android UI, background work, security storage, camera preview, and on-device barcode scanning.

Users may explicitly share diagnostic logs or backup files using Android system sharing or file picker features. In those cases, the destination is chosen by the user outside the app.

## Data Storage

The app stores configuration and cached app data locally on the user's device. This may include:

- account settings
- export and import keys
- device lists and custom values
- aliases
- hidden device settings and dashboard ordering
- widget selections
- refresh timestamps and diagnostics
- local notification state
- local chart history
- diagnostic logs
- backup configuration

Export keys, import keys, and the saved backup password are stored using Android encrypted storage.

Chart history is stored in a local SQLite database. The app may keep recent raw samples and longer-term rollups for chart display.

## Backups

If the user enables backups, the app creates encrypted backup files in a folder selected by the user through the Android file picker. Backup files may contain app settings, saved keys, custom cards, cached data, and optionally the local chart history database.

Backup files are encrypted with a password chosen by the user. The user is responsible for storing backup files and the backup password safely.

Automatic backups run only when the user has selected a backup folder, configured a backup password, and enabled automatic backups.

## Data Deletion

Users can remove stored account data from within the app by removing configured accounts.

Users can clear local chart history for specific devices or custom cards, and can clear diagnostic logs from the app.

Users can delete backup files from the selected backup folder using their file manager or storage provider.

Users can uninstall the app to remove locally stored app data from the device, subject to Android system backup behavior and any user-created backup files stored outside the app.

## Security

Data sent between the app and the Živý Obraz service is transmitted over HTTPS.

Sensitive local values such as export keys, import keys, and saved backup passwords are stored using Android encrypted storage.

User-created backup files are encrypted before being written to the selected backup folder.

## Children

The app is not intended for children under 13.

## Contact

If you have questions about this privacy policy or data handling, contact:

androidapp@coolajz.cz
