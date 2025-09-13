# FortiClient VPN

Download the latest release from [Releases](https://github.com/shieldport/FortiClient-VPN/releases/tag/7.4.3)

Getting started with FortiClient VPN is simple and efficient. Just download the installer, follow the setup prompts, and within minutes, you’ll have a secure connection established. Regardless of whether you're using Windows, macOS, or Linux, the installation process is intuitive and uniform across platforms.

**System Requirements:**

* **Windows:** Windows 10/11 (64-bit), Windows Server 2019 or newer
* **macOS:** Sonoma (14), Ventura (13), Monterey (12)
* **Linux:** Ubuntu 18.04+, Red Hat 7.4+, CentOS 7.4+, Fedora 36+

**Core Installation Steps:**

1. Download the proper installer from Fortinet’s official portal.
2. Launch the setup wizard suited to your OS.
3. Register the device with FortiClient EMS for centralized oversight.
4. Apply desired VPN settings and security configurations.

> \[!info] **Note:** Certain advanced features may require an active EMS-managed FortiClient license.

## Installation and Deployment

### Windows Installation

1. Run the FortiClient setup file (`.exe` or `.msi`).
2. Accept the license agreement.
3. Choose the components you wish to install.
4. Proceed with the wizard until installation is complete.

**Silent Installation via CLI:**

```sh
FortiClientSetup_7.2.4_x64.exe /quiet /norestart /log c:\install.log
```

### macOS Installation

1. Open the `.dmg` file and start the installation package.
2. Confirm any permission requests that appear.
3. Restart your Mac if prompted to finalize the setup.

### Linux Installation

* **Ubuntu/Debian-based systems:**

  ```sh
  sudo apt install ./forticlient_7.2.4_x86_64.deb
  ```

* **Red Hat/CentOS-based systems:**

  ```sh
  sudo yum install ./forticlient_7.2.4_x86_64.rpm
  ```

> \[!warning] **Warning:** Ensure any conflicting security tools are removed before installing FortiClient.

## Zero Trust Telemetry

Zero Trust Telemetry allows FortiClient to transmit endpoint data to FortiClient EMS and FortiGate, improving visibility and enforcing policies more effectively.

### Key Features:

* Verifies device identity
* Monitors real-time security status
* Applies dynamic security enforcement

To enable telemetry:

1. Launch FortiClient and go to **Zero Trust Telemetry**.
2. Enter the EMS server address to initiate connection.
3. Confirm the security profile to complete configuration.

## Remote Access & VPN Configuration

FortiClient ensures secure remote access through both SSL VPN and IPsec VPN technologies.

### Setting Up an SSL VPN

1. Open FortiClient and navigate to **Remote Access**.
2. Click **Add a new connection**, then select **SSL VPN**.
3. Input the VPN server address and login credentials.
4. Save your settings and click **Connect**.

### Setting Up an IPsec VPN

1. Go to **Remote Access > VPN**.
2. Choose **IPsec VPN** and complete the required fields.
3. Enter your authentication data and save the profile.
4. Start the VPN session.

## Malware Protection & Antivirus

FortiClient incorporates a powerful anti-malware engine that proactively identifies and blocks threats.

### Features:

* Combines signature detection with behavioral analysis
* Leverages cloud intelligence for faster threat recognition
* Supports both manual and scheduled scans

### Performing a Manual Scan

1. Open FortiClient and select **Malware Protection**.
2. Choose either **Full Scan** or **Quick Scan**.
3. Review scan results and resolve any detected issues.

> \[!note] **Tip:** Enable real-time protection to ensure continuous defense.

## Web Filtering & Application Firewall

### Web Filtering

FortiClient provides a browser plugin to inspect HTTPS traffic, helping to prevent access to harmful or restricted websites.

* Set filtering rules under **EMS > Web Filter**.
* Enable browser plugin for real-time filtering.

### Application Firewall

This feature observes and controls how applications interact with your network.

* Check restricted applications in the **Application Firewall** section.
* Create custom policies to govern application behavior.

## Vulnerability Scan & Security Compliance

FortiClient features an integrated scanner to detect system weaknesses and recommend corrective measures.

### Running a Vulnerability Scan

1. Launch FortiClient and click **Vulnerability Scan**.
2. Press **Scan Now** to begin.
3. Analyze the findings and implement the recommended fixes.

## Troubleshooting & Diagnostics

### Common Issues & Fixes

* **VPN Not Connecting:** Check credentials and firewall rules.
* **Telemetry Not Syncing:** Verify EMS address and SSL certificate.
* **Failed Antivirus Updates:** Confirm device has access to FortiClient Cloud.

### Diagnostic Utilities

FortiClient includes command-line utilities for troubleshooting.

```sh
forticlient_diag --check-connectivity
```

## Command-Line Interface (CLI) & API

### CLI Usage

* **Show FortiClient Version:**

  ```sh
  forticlient --version
  ```

* **Start VPN Connection:**

  ```sh
  forticlient --vpn connect myvpn
  ```

### API Integration

FortiClient supports APIs to facilitate automation and large-scale deployments.

* Refer to the **FortiClient EMS API Guide** for endpoint documentation.
* Utilize RESTful APIs to streamline device control and policy automation.
