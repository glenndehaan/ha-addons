<!-- https://developers.home-assistant.io/docs/add-ons/presentation#keeping-a-changelog -->

## 8.4.1

- Dependency updates
- Fixed incorrect logo path for ESC/POS printer function

## 8.4.0

- Updated dependencies
- Moved email assets from base64 to attachments to improve support in Gmail
- Implemented custom email branding support
- Implemented custom print branding support
- Moved image assets to email/kiosk directory
- Implemented kiosk dark mode logo support
- Updated README.md

## 8.3.2

- Fixed OIDC loop when using local authentication
- Removed default auth setting for mail.js
- Updated dependencies
- New translations email.json (German)
- New translations kiosk.json (German)
- New translations time.json (German)
- Added missing package-lock.json updates

## 8.3.1

- Moved fetchUserInfo call to authorization.js middleware
- Catch fetchUserInfo exceptions, causing invalided session to be stuck

## 8.3.0

- Implemented the `AUTH_OIDC_REDIRECT_LOGIN` environment variable
- Added an OIDC redirect function within authentication.js controller
- Updated README.md
- Updated dependencies

## 8.2.2

- Dependency updates

## 8.2.1

- Updated languages.js with new languages
- New translations time.json (Serbian (Cyrillic))
- New translations kiosk.json (Serbian (Cyrillic))
- New translations print.json (Serbian (Cyrillic))
- New translations email.json (Serbian (Cyrillic))

## 8.2.0

- Implemented `KIOSK_TIMEOUT` environment variable
- Introduced adjustable kiosk timeout timer
- Moved static animation from style.css to kiosk.ejs
- Fixed incorrect preload tag within kiosk.ejs
- Added missing bg.jpg preload tag within kiosk.ejs
- Updated docker-compose.yml
- Dependency updates
- Updated README.md

## 8.1.1

- Hide copy to clipboard button if browser API is not available

## 8.1.0

- Implemented `KIOSK_EMAIL` environment variable. Lowered log output from unifi.js
- Implemented kiosk email toggle
- Fixed missing kiosk printer check causing errors
- Updated README.md

## 8.0.0

> **Note**: [Please read the migration documentation before upgrading from 7.x to 8.x](https://github.com/glenndehaan/unifi-voucher-site#migration-from-7x-to-8x)

> **Warning!** This release is only compatible with:
> - UniFi OS v4.2.8+
> - UniFi Network v9.1.119+ (Cloud Gateways, Cloud Key, or UniFi OS software)

> **This release requires the setup of a UniFi OS Integration API Key**

> **Note**: This release breaks the Connected Guests feature due to a limitation within the UniFi Integration API. Please check and upvote this issue: https://community.ui.com/questions/Feature-Request-Network-API-Guest-Access-Voucher-ID/d3c470e2-433d-4386-8a13-211712311202

- Migrated languages.js from master
- Updated info.js guest warning
- Removed old dependencies
- Removed deprecated `UNIFI_USERNAME` and `UNIFI_PASSWORD` from variables.js
- Cleanup unifi.js to remove legacy implementation and switch to UniFi Integrations
- Implemented temporary guest features warning in info.js
- Removed old UniFi username check from info.js
- Refactor fetch.js to utilize global cache
- Lowered log intensity within server.js
- Dependency updates
- Added country flags to languages.js
- Updated the languages.js util with global filters
- Implemented cleanup.js for automatically cleaning-up expired and unused vouchers
- Added the created at field within details.ejs
- Updated language dropdown to hide themselves if the number of allowed languages is lower than 2
- Implemented the `TRANSLATION_HIDDEN_LANGUAGES`, `TASK_CLEANUP_EXPIRED` and `TASK_CLEANUP_UNUSED` environment variables in variables.js
- Added translation status to info.js
- Updated info.js to show deprecation messages when utilizing the options.json
- Updated README.md
- Updated docker-compose.yml
- Updated array.js with new deprecated variables
- Implemented Admin UI button within kiosk.ejs
- Implemented new / redirect structure base on `KIOSK_HOMEPAGE` variable
- Implemented `KIOSK_HOMEPAGE` environment variable
- Implemented `UNIFI_TOKEN` startup check within info.js
- Refactored server.js into separate controllers
- Temporary fixed guest mapping to voucher\_code instead of ids
- Fixed incorrect quote filter within server.js
- server.js refactored for compatibility with the UniFi integration API
- Added undici to the dependencies
- Check for undefined state in notes.js
- Added fetch.js util
- Added the `UNIFI_TOKEN` to variables.js
- Updated the unifi.js module to implement the UniFi Integration API
- Refactored print.js, bulk-print.ejs, details.ejs, email.ejs, print.ejs, voucher.ejs and size.js for object compatibility with the UniFi Integration API

## 7.2.2

- Updated the languages.js with new languages
- New translations email.json (Czech)
- New translations print.json (Czech)
- New translations kiosk.json (Czech)
- New translations time.json (Czech)

## 7.2.1

- Fixed notes.js util to catch null values

## 7.2.0

- Updated `PIN_OIDC_USER_TO_OWN_DOMAIN` to `AUTH_OIDC_RESTRICT_VISIBILITY`
- Fixed bulk-print.ejs notes view
- Updated details.ejs view with additional voucher metadata
- Updated voucher.ejs notes view
- Created notes.js utils for extracting voucher notes and metadata
- Updated docker-compose.yml
- Updated README.md
- Implemented voucher note check for seperator misuse
- Implemented new notes-metadata embed
- Implemented new voucher filter within existing chain
- Fixed notes sort to only filter on the notes not the metadata
- Removed unused `pinOidcUserToOwnDomain` variable forward to voucher.ejs
- Cleanup code prior to pull request (Contribution by: @bjoerrrrn)
- Merging PIN_OIDC_USER_TO_OWN_DOMAIN System to PR-Branch (Contribution by: @bjoerrrrn)
- New translations email.json (Italian)
- New translations print.json (Italian)
- New translations kiosk.json (Italian)
- New translations time.json (Italian)

## 7.1.1

- Updated dependencies
- Updated README.md

## 7.1.0

- Updated info.js to reflect auto kiosk print status
- Implemented `KIOSK_PRINTER` environment variable
- Updated docker-compose.yml
- Dependency updates
- Updated README.md
- Implemented voucher auto-print within kiosk in server.js

## 7.0.1

- Fixed missing time convert translation within kiosk.ejs

## 7.0.0

> **Note**: [Please read the migration documentation before upgrading from 6.x to 7.x](https://github.com/glenndehaan/unifi-voucher-site#migration-from-6x-to-7x)

- Updated kiosk.json with new translation strings
- Updated info.js to reflect the multiple kiosk voucher types
- Deprecated the `KIOSK_VOUCHER_TYPE` environment variable
- Implemented the `KIOSK_VOUCHER_TYPES` environment variable with support for multiple voucher types
- Moved the kiosk images (logo.png and bg.jpg) to a kiosk image sub-folder
- Redesign of the kiosk.ejs language selector to provide space for custom images
- Implemented voucher types within kiosk.ejs
- Utilize the bytes converter within voucher.ejs to reformat bytes labels
- Updated the docker-compose.yml
- Updated the README.md
- Implemented /kiosk custom assets overrides
- Implemented a type check for the voucher types from kiosk requests
- New translations kiosk.json (French)
- New translations kiosk.json (Spanish)
- New translations kiosk.json (Danish)
- New translations kiosk.json (German)
- New translations kiosk.json (Finnish)
- New translations kiosk.json (Dutch)
- New translations kiosk.json (Polish)
- New translations kiosk.json (Portuguese)
- New translations kiosk.json (Russian)
- New translations kiosk.json (Portuguese, Brazilian)

## 6.1.1

- Updated languages.js to include new languages from Crowdin
- Limit width of language selector in kiosk.ejs
- Updated dependencies
- New translations time.json (Portuguese, Brazilian)
- New translations kiosk.json (Portuguese, Brazilian)
- New translations print.json (Portuguese, Brazilian)
- New translations email.json (Portuguese, Brazilian)
- New translations email.json (Portuguese)
- New translations kiosk.json (Portuguese)
- New translations print.json (Portuguese)
- New translations email.json (Portuguese)

## 6.1.0

- Updated languages.js to include new languages from Crowdin
- Persist locale between kiosk voucher generation and email send page
- Also ensure locale is used as language when sending the email from the kiosk page
- Added guestName translation to kiosk.json
- Implemented time.json to time util translations
- Updated info.js to reflect kiosk name requirement
- Updated mail.js and print.js for localized time translations
- Implemented optional guest name (voucher note) within kiosk.ejs
- Implemented translations within time.js
- Updated docker-compose.yml
- Updated dependencies
- Updated README.md
- New translations email.json (Finnish)
- New translations print.json (Finnish)
- New translations kiosk.json (Finnish)
- New translations email.json (Portuguese)
- New translations print.json (Portuguese)
- New translations kiosk.json (Portuguese)
- New translations kiosk.json (French)
- New translations kiosk.json (Spanish)
- New translations kiosk.json (Danish)
- New translations kiosk.json (German)
- New translations kiosk.json (Finnish)
- New translations kiosk.json (Dutch)
- New translations kiosk.json (Polish)
- New translations kiosk.json (Portuguese)
- New translations kiosk.json (Russian)
- New translations time.json (French)
- New translations time.json (Spanish)
- New translations time.json (Danish)
- New translations time.json (German)
- New translations time.json (Finnish)
- New translations time.json (Dutch)
- New translations time.json (Polish)
- New translations time.json (Portuguese)

## 6.0.4

- Updated dependencies

## 6.0.3

- Updated dependencies

## 6.0.2

- Updated languages.js
- New translations kiosk.json (Russian)
- New translations print.json (Russian)
- New translations email.json (Russian)

## 6.0.1

- Updated README.md
- Hotfix HA printer fields

## 6.0.0

> **Note**: [Please read the migration documentation before upgrading from 5.x to 6.x](https://github.com/glenndehaan/unifi-voucher-site#migration-from-5x-to-6x)

- Updated info.js for new printers key
- Updated print.js to forward ESC/POS printer IPs
- Updated keys within variables.js
- Added 'UI_BACK_BUTTON', 'PRINTER_TYPE' and 'PRINTER_IP' to the deprecated strings array.js
- Updated status.js with new printing module
- Updated docker-compose.yml environment variables
- Updated dependencies
- Hotfix body type for express v5
- Updated README.md
- Removed back button from navigation.ejs
- Updated print.ejs and bulk-print.ejs with printer selection
- Updated print logic within server.js to allow printer selection by user

## 5.2.0

- Dependency updates
- Implemented en kiosk.json translations
- Updated locale middleware config
- Implemented translations within kiosk.ejs
- New translations kiosk.json (French)
- New translations kiosk.json (Spanish)
- New translations kiosk.json (Danish)
- New translations kiosk.json (German)
- New translations kiosk.json (Dutch)
- New translations kiosk.json (Polish)
- Implemented the missing email field translation

## 5.1.3

- Updated languages.js
- Removed unused language files
- New translations print.json (Danish)
- New translations email.json (Danish)
- New translations print.json (Spanish)
- New translations email.json (Spanish)
- New translations email.json (French)
- New translations print.json (French)

## 5.1.2

- Revert expressjs upgrade due to incompatibilities

## 5.1.1

- New translations email.json (Danish)
- New translations print.json (Danish)
- Dependency upgrades

## 5.1.0

- Added the kiosk_example.png
- Updated the README.md
- Implemented timer styles within style.css
- Added kiosk output within info.js
- Set default locale to 'en' for mail.js
- Implemented KIOSK_ENABLED and KIOSK_VOUCHER_TYPE environment variables within variables.js
- Added kiosk_bg.jpg
- Updated navigation.ejs with kiosk link
- Added kiosk.ejs template
- Updated status.ejs and status.js with kiosk module status
- Updated docker-compose.yml
- Added /kiosk routes to server.js
- Added kioskEnabled states to required routes in server.js

## 5.0.2

- Dependency updates

## 5.0.1

- Fixed crash within QR generation for larger SSIDs and Passwords

## 5.0.0

> **Note**: [Please read the migration documentation before upgrading from 4.x to 5.x](https://github.com/glenndehaan/unifi-voucher-site#migration-from-4x-to-5x)

- Updated NodeJS to 22.x LTS
- Updated Alpine to 3.21
- Pinned tough-cookie to clear deprecation message
- Dependency updates
- Removed nodemon
- Switched watcher to built-in version within NodeJS 22
- Updated README.md
- Removed version from docker-compose.yml since this is deprecated
- Implemented the /api/languages endpoint
- Refactored the /api endpoint to return methods for each endpoint
- Added the voucher id within /api/vouchers
- Refactored the /api/voucher endpoint from GET to POST method
- Implemented optional email sending within /api/voucher endpoint
- Implemented missing comments within api code
- Implemented missing HTTP status codes within api responses
- Enabled JSON responses within Express
- Updated the README.md with v5 migration documentation
- Upgrade/migrate tailwind v3 to v4
- Fixed small tailwind migration error

## 4.7.0

- Updated screenshots
- Fixed inconsistent 'unlimited' messaging
- Implemented direct usage without overrides within unifi.js
- Implemented voucher duration type dropdown during custom voucher creation
- Implemented Multi-use (Limited/Quota) option during custom voucher creation
- Updated README.md to reflect multi-use quota function within voucher type presets

## 4.6.1

- Added custom font for PDF exports for ensure special character sets are available

## 4.6.0

- Implemented expired states within templates
- Implemented expired filter
- Implemented notes within voucher creation
- Implemented Notes within voucher overview and detail pages
- Implemented notes sort option
- Fixed incorrect voucher type when custom quotas are in use
- Implemented quota display within templates
- Implemented bulk printing for both PDF and ESC/POS modules
- Updated README.md

## 4.5.2

- Fixed QR code generation for 'Open' networks
- Update README.md to reflect QR function
- Updated dependencies

## 4.5.1

- Dependency upgrades

## 4.5.0

- Implemented UI_BACK_BUTTON for kiosk users to navigate to the previous page
- Removed h1 to clean-up UI

## 4.4.1

- Rollback pdfkit update due to HA encoding error

## 4.4.0

- Dependency updates
- Implemented TRANSLATION_DEFAULT to override default selected translation

## 4.3.6

- New translations email.json (Polish)
- New translations print.json (Polish)
- Dependency updates
- Removed incomplete French translation
- Added Polish translation

## 4.3.5

- Updated dependencies
- New translations print.json (Catalan)
- New translations email.json (Catalan)
- New translations print.json (Spanish)
- New translations email.json (Spanish)

## 4.3.4

- Updated dependencies
- New translations print.json (Ukrainian)
- New translations email.json (Ukrainian)

## 4.3.3

- New translations email.json (German)
- New translations print.json (German)

## 4.3.2

- New translations email.json (Dutch)
- New translations print.json (Dutch)

## 4.3.1

- Update Crowdin configuration file
- New translations email.json (French)
- New translations email.json (German)
- New translations email.json (Dutch)
- New translations print.json (French)
- New translations print.json (German)
- New translations print.json (Dutch)
- Updated crowdin.yml pull request parameters
- Updated .dockerignore
- Added missing Crowdin locales

## 4.3.0

- Setup initial locales folder for translations
- Added English translations for email
- Added _locales.json for mapping
- Implemented the translation.js module
- Implemented the 'TRANSLATION_DEBUG' environment variable
- Updated the README.md to include the Translations chapter
- Moved en.json to en/email.json to better utilize Crowdin
- Implemented mail translations
- Updated debug output from translation.js
- Swapped mail function parameters
- Replaced throw errors for log warnings
- Implemented fallback language in translation.js
- Added express-locale for future web i18n use
- Removed _locales.json implementation
- Added language parameter to mail.js
- Implemented regex check to translation.js
- Added language dropdown to email component
- Added languages.js
- Implemented the print.json translation file
- Added a new print dialog
- Moved /print function to a post request
- Updated translation.js debug output
- Implemented translator within print.js
- Fixed typos
- Removed unused utils from email and print components render function
- Updated README.md

## 4.2.0

- Extended voucher.ejs with filters and sort fields
- Also implemented JS handlers for submit
- Implemented filter and sort selected functions
- Implemented revised filter and sort layout
- Implemented filters
- Adjust dropdown styling to conform with others in the app
- Implemented sort and updated sync button layout

## 4.1.5

- Dependency updates

## 4.1.4

- Fixed SMTP_SECURE type check within variables.js
- Removed smtpSecure checks from mail.js
- Disable TLS certificate checks within mail.js since this could cause issues with self-hosted solutions

## 4.1.3

- Moved static routes before OIDC to prevent errors due to silent login
- Removed unused transition-opacity
- Added event handler on details, email and create overlays when clicking outside the overlay

## 4.1.2

- Updated build output format
- Updated build log in info.js

## 4.1.1

- Moved build info to variables.js
- Simplified info.js build readout
- Added versions to user dropdown

## 4.1.0

- Implemented Git version tag into docker build and GitHub actions
- Implemented Release Notes button
- Updated Documentation button to directly navigate to the README.md

## 4.0.4

- Updated README.md. Revert type check within variables.js
- Implemented type check within config.js, fallback to 'null' when option is not defined

## 4.0.3

- Updated deprecation token list

## 4.0.2

- Fixed incorrect type check on 'VOUCHER_CUSTOM', 'SERVICE_WEB' and 'AUTH_INTERNAL_ENABLED'

## 4.0.1

- Revert "Setup non-root user within Dockerfile. Copy files as non-root user within Dockerfile. Launch app as non-root user within Dockerfile"

## 4.0.0

> **Note**: [Please read the migration documentation before upgrading from 3.x to 4.x](https://github.com/glenndehaan/unifi-voucher-site#migration-from-3x-to-4x)

- Setup non-root user within Dockerfile
- Copy files as non-root user within Dockerfile
- Launch app as non-root user within Dockerfile
- Replaced AUTH_PASSWORD with AUTH_INTERNAL_PASSWORD
- Removed 'public' flow from implementation documentation
- Removed 'public' OIDC flow from application
- Deprecated 'AUTH_OIDC_CLIENT_TYPE'
- Removed 'AUTH_OIDC_CLIENT_TYPE' from documentation
- Updated OIDC config checks
- Removed 'AUTH_OIDC_CLIENT_TYPE' and 'public' OIDC flow references from README.md
- Moved OIDC routes to /oidc/* paths
- Updated docker installation in README.md
- Added Release Noted chapter in README.md
- Added 3.x to 4.x migration documentation to README.md
- Updated OIDC integration documentation to mention new callback url
- Implement missing config getters within variables.js
- Implemented the 'AUTH_INTERNAL_ENABLED' and 'AUTH_OIDC_ENABLED' environment variables
- Removed complex if structures with 'AUTH_OIDC_ENABLED' checks
- Updated README.md
- Implemented new logout flow utilizing new /oidc/logout endpoints
- Added missing width and height for images
- Added 'AUTH_OIDC_ENABLED' to integration documentation
- Fixed incorrect config handling within variables.js
- Added Login with OIDC button to login page
- Made login.ejs dynamic based on enabled authentication services
- Made GitHub icon on login.ejs smaller
- Refactored authorization.js middleware to support running both internal and OIDC authentication within the same instance
- Added extra error to info.js when both authentication services are disabled but authentication itself is enabled
- Updated status.js to correctly display both authentication services running at the same time
- Enabled /login when OIDC is enabled
- Added missing middleware on /logout
- Fixed JWT not initializing when authInternalEnabled is true
- Enable attemptSilentLogin on OIDC for users that might be already signed in, this will skip the login page if users have authenticated with the idP before and still have a valid session
- Update project screenshots
- Updated OIDC documentation screenshots
- Renamed 'AUTH_TOKEN' to 'AUTH_INTERNAL_BEARER_TOKEN'

## 3.8.2

- Implemented GitHub issue forms
- Added GitHub issue template config.yml
- Fixed error on force re-sync when UniFi is unavailable
- Implemented check for deprecated environment variables
- Implemented check for valid UniFi usernames
- Implemented UniFi username check in unifi.js
- Added array.js utils

## 3.8.1

- Disabled userIcon for internal authentication

## 3.8.0

- Updated OIDC documentation
- Added Zitadel OIDC integration
- Dependency updates
- Fixed dark mode colors in details.ejs & email.ejs
- Moved navigation to dedicated navigation.ejs file
- Implemented user icon
- Implemented user menu
- Implemented /logout
- Implemented Gravatar icon
- Moved documentation and feature icons from menu to user menu

## 3.7.1

- Moved request logger to catch OIDC callback request for debugging

## 3.7.0

- Implemented UNIFI_SSID_PASSWORD environment variable
- Updated email template
- Updated PDF template
- Updated ESC/POS template
- Updated README.md
- Changed qr.js output based on open or password protected networks

## 3.6.0

- Updated dependencies
- Fixed missing email error response
- Refactored email layout
- Implemented voucher details in email layout
- Implemented UNIFI_SSID for templating
- Implemented email connect template
- Implemented qr.js for Scan to Connect
- Updated README.md
- Updated email_example.png screenshot
- Added extra logging to mail.js
- Implemented pdf connect template
- Updated pdf_example.png screenshot
- Implemented missing unifiSsid check for PDF exports
- Improved email margins
- Updated escpos_example.jpg screenshot
- Implemented qr.js buffer toggle
- Implemented ESC/POS Scan to Connect
- Optimized ESC/POS layout
- Implemented qr.js error logging

## 3.5.4

- Updated dependencies

## 3.5.3

- Added logo.svg
- Updated dependencies

## 3.5.2

- Created variables.js to replace duplicate code
- Moved more cache.js logs to debug level
- Fixed incorrect internal authentication state on status page
- Updated dependencies
- Fixed incorrect type check on /api/voucher/:type for HA users

## 3.5.1

- Fixed incorrect status url for Home Assistant users

## 3.5.0

- Updated README.md to improve authentication explanation
- Moved application startup logs to dedicated info.js module
- Lowered log output from unifi.js
- Created tag.ejs partial
- Implemented dedicated application status page
- Updated voucher.ejs to implement status link
- Lowered log output from cache.js
- General cleanup of server.js
- Implemented 501 Not Implemented responses when features are not enabled or configured properly

## 3.4.1

- Added UID Docs (Contribution by: @jlengelbrecht)
- Updated README.md
- Reformat some docs
- Implemented OIDC configuration verification on application start
- Updated auth type check

## 3.4.0

- Updated README.md
- Added Prerequisites section
- Implemented OIDC IdP Integration Guides
- Added Keycloak OIDC implementation guide
- Added Authentik OIDC implementation guide
- Updated .dockerignore
- Migrated README.md images to .docs folder
- Moved print logic to own module
- Implemented ESC/POS printer support
- Added logo_grayscale_dark.png
- Replaced PDF logo
- Implemented size.js util for dynamic PDF page length
- Updated auth output log with type
- Updated print output log with printer ip

## 3.3.1

- Implemented custom express error page

## 3.3.0

- Implemented OIDC confidential client type support
- Updated README.md
- Added missing environment variables to docker-compose.yml
- Ensure optional config parameters are actually optional

## 3.2.1

- Updated README.md
- Added missing en translation for printer_type

## 3.2.0

- Updated 'Voucher' log information
- Implemented missing custom voucher log output
- Implemented PRINTER_TYPE variable to prepare for future printers
- Disabled printer function by default
- Updated README.md

## 3.1.1

- Updated dependencies
- Fix micromatch CVE-2024-4067
- Updated README.md

## 3.1.0

- Switched docker build to path based to allow .dockerignore to work
- Implemented OIDC support
- Updated README.md

## 3.0.1

- Fixed missing x-ingress-path within authorization.js redirects
- Implemented local/development .options.json config

## 3.0.0

> **Note**: [Please read the migration documentation before upgrading from 2.x to 3.x](https://github.com/glenndehaan/unifi-voucher-site#migration-from-2x-to-3x)

- Updated .dockerignore to remove unneeded files from container build
- Updated docker-compose.yml with new environment variables
- Updated README.md
- Updated project description
- Replaced DISABLE_AUTH with AUTH_DISABLE
- Replaced SECURITY_CODE with AUTH_PASSWORD
- Implemented AUTH_TOKEN for api authentication
- Added migration guide

## 2.7.3

- Fixed create button copy
- Added email forum spinner

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

> **Note**: [Please read the migration documentation before upgrading from 1.x to 2.x](https://github.com/glenndehaan/unifi-voucher-site#migration-from-1x-to-2x)

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
