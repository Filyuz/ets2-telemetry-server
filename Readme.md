# ETS2 Telemetry Web Server

This is a modern ETS2 Telemetry Web Server written in C# and WebApi. The server exposes the following URLS:

### Telemetry REST API

For now there is only one method supported:
    
    GET http://localhost:25555/api/ets2/telemetry

It returns IEts2TelemetryData JSON object with the latest telemetry data read from the game. The state is updated upon every API call. You may use this REST API for your own Applications. 

You can minimize the application to tray by clicking "Minimize" button. Double-click on the tray icon will restore it back.

### Telemetry HTML5 Mobile Application
    http://localhost:25555/apps/ets2/index.htm

This application is designed for mobile browsers running in landscape mode. You should open the URL in your Mobile Safari (iPhone 8+) or Android 4+ Browsers (Default or Chrome).  

## Installation

1. Copy **ets2-telemetry.dll** to your **SteamApps\common\Euro Truck Simulator 2\bin\win_x86\plugins** directory. If **plugins** directory does not exist you must create it first. If you don't trust my compiled ets2-telemetry.dll you may compile it by yourself from [the official SDK](https://github.com/nlhans/ets2-sdk-plugin)
2. Make sure that **25555** (default) port in opened in your Firewall. You may change the port number inside Ets2Telemetry.exe.config. 

## Supported OS and Devices

- Windows Vista, Windows 7, Windows 8
- iPhone OS 8+ (using built-in Mobile Safari). It is recommended to create a shortcut for the application on the Home screen to automatically remove browser's navigation bar.
- Android 4+ devices (usingDefault or Chrome browser). **Warning:** since it is not possible to prevent Android device from going into sleep from a web page you must turn it off in the device's settings (or use third party apps that are capable of turning off sleep mode by application)

## Usage

1. Run Ets2Telemetry.exe (you have to run it *as Administrator* if you want to connect from other devices connected to your local network!). 
2. Run ETS2 game.
3. Open "ETS2 App URL" from your iPhone or Android device (Default or Chrome browser) and rotate device to landscape mode.
4. Enjoy!

## License

MIT.