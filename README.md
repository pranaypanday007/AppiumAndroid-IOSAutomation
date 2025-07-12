
# 📱 Appium Android–iOS Automation

A robust framework for cross-platform (Android & iOS) mobile app test automation using Appium.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Reporting & Troubleshooting](#reporting--troubleshooting)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This project provides an easy-to-extend, platform-agnostic test automation solution for native mobile applications using [Appium](https://appium.io/) with Java and TestNG.  
Supports both Android and iOS, parallel execution, and integration with popular CI/CD tools.

---

## Features

- 🔄 Android & iOS automation support  
- 🚀 Java + TestNG-based test suites  
- 🖱️ Utility functions for gestures, waits, and screenshots  
- 🛠️ Easily parameterized for different devices & platforms  
- ⚡ CI/CD ready

---

## Prerequisites

- Java 17+ (recommended)
- Maven 3.x+
- Node.js & npm
- Appium CLI (`npm install -g appium`)
- Android SDK (for Android)
- Xcode & Xcode Command Line Tools (for iOS, macOS only)
- Real device or emulator/simulator setup
- Appium Inspector (optional, for element location)

---

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/pranaypanday007/AppiumAndroid-IOSAutomation.git
cd AppiumAndroid-IOSAutomation

**2. Install dependencies**
# Maven dependencies
mvn clean install

# Node dependencies (if using JS helpers)
npm install

**3. Configure your environment**
Update device names, platform versions, and app paths in the TestNG XML or config properties.

Make sure your Android emulator or iOS simulator/device is running.

**4. Start Appium server**
appium
# Or with specific host/port
appium -a 127.0.0.1 -p 4723

**5. Run your tests**
# Run all tests
mvn test

# Or specify TestNG suite
mvn test -DsuiteXmlFile=android-tests.xml
mvn test -DsuiteXmlFile=ios-tests.xml

**Project Structure**
AppiumAndroid-IOSAutomation/
│
├── src/
│   ├── main/java/com/yourcompany/
│   │     ├── DriverManager.java
│   │     ├── Utils.java
│   │     └── ...other utilities...
│   └── test/java/com/yourcompany/
│         ├── android/
│         └── ios/
│
├── pom.xml
├── testng.xml
└── README.md

**Usage**
Place your Android or iOS app under the specified path.
Update TestNG XML with your device/emulator details.
Run tests using Maven commands as shown above.
Check reports in the /target/surefire-reports/ directory.

**Reporting & Troubleshooting**
Test reports: Located in target/surefire-reports
Screenshots: Auto-captured on failure (see /screenshots or configured location)
Logs: View Appium server logs and test output for debugging
Device Connection:
Android: adb devices
iOS: xcrun simctl list
Common Issues:
Device not detected: Restart emulator/simulator and ensure drivers are installed
Port in use: Change Appium server port or kill process using the port

**Contributing**
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.
Fork this repo
Create your feature branch (git checkout -b feature/fooBar)
Commit your changes (git commit -am 'Add some fooBar')
Push to the branch (git push origin feature/fooBar)
Open a pull request

**License**
This project is licensed under the MIT License - see the LICENSE file for details.
