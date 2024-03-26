<!-- https://developers.home-assistant.io/docs/add-ons/presentation#keeping-a-changelog -->

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
