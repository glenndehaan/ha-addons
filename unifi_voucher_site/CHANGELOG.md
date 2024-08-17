<!-- https://developers.home-assistant.io/docs/add-ons/presentation#keeping-a-changelog -->

## 2.7.2

- Hide email button when mail function is disabled

## 2.7.1

- Implemented HA config parameters for mail functionality

## 2.7.0

- Updated Dependencies
- Add axios override to patch CVE-2024-39338
- Implemented email functionality
- Updated README.md

## 2.6.4

- Updated Dependencies
- Updated GitHub actions

## 2.6.3

- Updated Dependencies
- Removed unused 'uuid' package
- Fixed text color within select dropdown on Chromium based browsers on Windows using Dark Mode

## 2.6.2

- Updated Dependencies
- Upgraded Alpine to 3.20

## 2.6.1

- Removed unused css
- Added a robots.txt
- Attempt to block iOS from adding invalid telephone link
- Added last sync to guest details
- Changed DateTimeFormat from en-US to en-GB

## 2.6.0

- Implemented guests cache
- Implemented guests function within unifi.js
- Updated app screenshots
- Updated manifest.json
- Added details.ejs component
- Implemented voucher detail slide-over
- Updated cache.js logic to fetch guests
- Updated README.md
- Implemented voucher detail component route

## 2.5.3

- Updated the README.md
- Updated the 'Share' copy to reflect 'Copy to Clipboard' function
- Updated the 'Copy to Clipboard' icon

## 2.5.2

- Implemented LOG_LEVEL environment variable
- Implemented log_level HA variable
- Implemented log level based on user preference
- Changed UniFi stack trace output from error to debug
- Removed duplicate cache error log
- Implemented internal build number
- Updated README.md
- Added account warning to README.md
- Output build version on application start

## 2.5.1

- Updated ejs dependency
- Fixed docker healthcheck IPv4 binding
- Reworked unifi.js settings/config sections
- Removed 1-hour session timeout from unifi.js
- Implemented retry params for all unifi.js functions
- Implemented re-authentication functions within catch blocks in unifi.js

## 2.5.0

- Added the jsonwebtoken package
- Implemented a web jwt verify flow
- Added missing JSON responses for api auth flows
- Added jwt module
- Moved bytes.js, logo.js, time.js and types.js to utils folder
- Updated README.md
- Implemented HA config check to allow API service configuration
- Implemented JWT initialization
- Replaced authorization cookie contents with JWT token
- Implemented /api/vouchers endpoint
- Updated /api endpoints list

## 2.4.1

- Fixed SERVICE_WEB variable not working correctly
- Implemented missing HA voucher_custom config setting
- Fixed VOUCHER_CUSTOM variable not working correctly
- Fixed an issue where HA voucher_types config was not used during validation causing an incorrect error
- Added bytes conversion

## 2.4.0

- Fixed missing logo link
- Implemented custom voucher type
- Implemented custom voucher fields
- Fixed divider visibility on dark mode
- Changed default VOUCHER_TYPES to single-use voucher type
- Implemented VOUCHER_CUSTOM environment variable

## 2.3.2

- Fixed padding issue for amount field

## 2.3.1

- Updated dependencies
- Removed unneeded dependency

## 2.3.0

- Updated screenshots
- Implemented color-scheme script to force browser color-scheme
- Implemented print functionality
- Updated README.md
- Implemented print route

## 2.2.0

- Implemented reusable UniFi sessions
- Fixed UniFi login rate-limit trigger
- Implemented bulk voucher generation
- Implemented revoke/delete voucher function
- Added grayscale logo
- Fixed issue where headers are send 2 times

## 2.1.0

- Refactored unifi.js to separate logic
- Updated application header
- Fixed incorrect screen-reader text
- Updated sync button text
- Implemented last sync date/time
- Implemented cache util
- Fixed missing vouchers check to prevent 'headers are already send' error
- Fixed missing cache sync on api voucher creation
- Implemented auto sync every 15 minutes

## 2.0.0

- Updated 404 and login branding/layout
- Moved tailwind dependencies to dev-dependencies
- Patched follow-redirects
- Implemented separate dependencies stage within Dockerfile to shrink image size
- Removed unneeded UniFi call to speed up communication
- Removed SID middleware
- Implemented cache module
- Updated screenshots
- Removed old background images
- Updated manifest.json
- Updated 404 and login background color
- Updated error alert styling
- Updated voucher branding/layout
- Updated README.md
- Cleanup server.js
- Removed GET /voucher route
- Updated redirects to GET /vouchers
- Implemented caching mechanism for UniFi vouchers overview
- Implemented force refresh option

## 1.1.0

- Implemented a logger.
- Fix UniFi error messages.
- Implemented additional UniFi logging
- Updated HA Panel Title
- Allow non-admins to access panel link

## 1.0.0

- Initial release
