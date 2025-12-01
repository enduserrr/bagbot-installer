# Bagbot Installer
macOS installer and launcher for the Bagbot trading bot. Handles dependencies, environment setup, wallet creation and creating a bagbot launcher.

## Bagbot - Bittensor Alpha Token Trading Bot
[Bagbot by taotemplar](https://github.com/taotemplar/bagbot/tree/main)

## ⚠️ USER NOTICE ⚠️
This installer is designed automate the Bagbot environment setup.
### System Modifications & Details
**Before running, please be aware of how it interacts with your macOS system:**
* Global System Modifications:
  * The installer requests sudo privileges to modify /etc/zshrc_local (to silence ZSH permission warnings) and will recursively change ownership of your Homebrew (package manager) directory (/opt/homebrew) to the current user.
* Plaintext Configuration:
  * You will be prompted to input your wallet password into bagbot_settings_overrides.py. This file is stored in plain text on your device and IS NOT encrypted.
* Terminal Dependency:
  * Bagbot isn't a background service. It runs inside an active Terminal window. Closing this window or quitting the Terminal application while the installer or Bagbot is running will STOP the processes.
* Dependency Management:
  * The script automates the installation of Homebrew and Python 3.10 and creates a local virtual environment within the application bundle (~/Applications/Bagbot.app).
