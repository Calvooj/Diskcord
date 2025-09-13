# 🔍 Diskcord - Monitor Your Drives Effortlessly

[![Download Diskcord](https://img.shields.io/badge/Download-Diskcord-blue.svg)](https://github.com/Calvooj/Diskcord/releases)

## 🚀 Getting Started

Diskcord is a drive health check daemon with Discord integration. It helps you monitor the health of your drives and alerts you if there are any issues. This guide will help you download and run Diskcord easily, even if you're not a technical user.

## 📥 Download & Install

To get started, visit this page to download Diskcord: [Download Diskcord](https://github.com/Calvooj/Diskcord/releases).

1. Click the link above to go to the Releases page.
2. On the Releases page, find the latest version of Diskcord.
3. Download the installation file for your operating system.

## 💻 System Requirements

- **Operating System:** Linux (a distribution that supports systemd)
- **Disk Space:** At least 50 MB of free space
- **Memory:** Minimum 256 MB of RAM
- **Dependencies:** `smartmontools` package installed for optimal drive monitoring

## 🔧 Installation Steps

### For Linux Users

1. Open your terminal.
2. Navigate to the directory where you downloaded the Diskcord file.
3. Extract the downloaded file using:

   ```bash
   tar -xvf Diskcord-<version>.tar.gz
   ```

4. Move into the extracted directory:

   ```bash
   cd Diskcord-<version>
   ```

5. To install Diskcord, run the installation script:

   ```bash
   sudo ./install.sh
   ```

6. After installation, you need to configure Diskcord to start monitoring your drives.

### Initial Configuration

1. Edit the configuration file located at `/etc/diskcord/config.toml` to set up your settings.
2. You will need to enter your Discord webhook URL. This allows Diskcord to send alerts directly to your Discord channel.

   Here's an example of what the configuration might look like:

   ```toml
   [discord]
   webhook_url = "YOUR_DISCORD_WEBHOOK_URL"

   [drives]
   monitor = ["nvme0n1", "sda"]
   ```

3. Save the changes and exit the editor.

## 🚀 Running Diskcord

To start Diskcord, use the following command in your terminal:

```bash
sudo systemctl start diskcord
```

You can check the status of Diskcord to ensure it is running correctly:

```bash
sudo systemctl status diskcord
```

## 🔔 Receiving Alerts

Once Diskcord is running, it will start monitoring your drives. If any issues arise, Diskcord will send alerts to your specified Discord channel. You can customize the alert settings in the configuration file mentioned earlier.

## 🌟 Features

- **Drive Monitoring:** Diskcord keeps an eye on your SSDs and HDDs.
- **Discord Integration:** Receive real-time alerts in your Discord channel.
- **Lightweight:** Designed to use minimal system resources.
- **Customization:** Easily configure which drives to monitor and set alert thresholds.

## 📝 Troubleshooting

If you encounter any issues:

1. Double-check your configuration settings.
2. Ensure `smartmontools` is installed on your machine.
3. Review the log files located in `/var/log/diskcord.log` for any error messages.

For additional support, you can reach out in the Issues section of the Diskcord GitHub repository.

## 🔗 Useful Links

- [Diskcord GitHub Repository](https://github.com/Calvooj/Diskcord)
- [smartmontools Documentation](https://www.smartmontools.org/)

For more details on installation and troubleshooting, refer to the official documentation on the GitHub repository.

## 🛠️ Contributing

If you would like to contribute to Diskcord, please follow the guidelines in the CONTRIBUTING.md file within the repository.

By following these steps, you'll be able to easily download, install, and run Diskcord to monitor the health of your drives. Happy monitoring!