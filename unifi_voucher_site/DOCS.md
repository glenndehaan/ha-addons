# Home Assistant Add-on: UniFi Voucher Site

This Home Assistant add-on allows you to easily set up a voucher-based authentication system for your UniFi network. By integrating with UniFi's API, it provides a web interface for generating and managing vouchers.

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]

![Screenshot](https://github.com/user-attachments/assets/6d1d9ec8-e60b-469d-9ad6-caf3fd346c55)

## Installation

1. Navigate to the Supervisor panel in your Home Assistant instance.
2. Select "Add-on Store."
3. Add the repository containing this add-on by clicking the three dots in the upper-right corner, then "Repositories," and enter the URL of this repository: https://github.com/glenndehaan/ha-addons.
4. Once the repository is added, the "UniFi Voucher Site" add-on will appear in the add-on store. Click on it.
5. Click "Install" and wait for the installation to complete.

## Configuration

The add-on requires configuration to connect to your UniFi controller. Here's an example configuration:

```yaml
unifi_ip: 192.168.1.1
unifi_port: 443
unifi_username: admin
unifi_password: ""
unifi_site_id: default
voucher_types: 480,0,,,;
voucher_custom: true
service_api: false
smtp_from: ''
smtp_host: ''
smtp_port: 25
smtp_secure: false
smtp_username: ''
smtp_password: ''
log_level: info
```

> Attention!: We recommend only using Local UniFi accounts due to short token lengths provided by UniFi Cloud Accounts. Also UniFi Cloud Accounts using 2FA won't work!

> Note: When creating a Local UniFi account ensure you give 'Full Management' access rights to the Network controller. The 'Hotspot Role' won't give access to the API and therefore the application will throw errors.

## Usage

1. Once the add-on is installed and configured, start it from the Supervisor panel.
2. After starting, access the UniFi Voucher Site web interface by clicking the 'Open Web UI' button

## Notes

* Make sure your UniFi controller is accessible from the network where your Home Assistant instance is running.
* For more information on how UniFi vouchers work and how to manage them, refer to the UniFi documentation.

By following these instructions, you can easily set up and manage UniFi vouchers directly from your Home Assistant instance, enhancing the authentication capabilities of your UniFi network.

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
