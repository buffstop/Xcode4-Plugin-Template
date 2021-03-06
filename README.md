# Xcode4 Plugin Template

Basic template for creating a plugin for Xcode4.


## Installation

- Clone or copy this project to `~/Library/Developer/Xcode/Templates/Project Templates/Application Plug-in/Xcode4 Plugin.xctemplate`. (Create the `Templates/Project Templates/Application Plug-in` subdirectories if they do not already exist.)
- Restart Xcode
- When creating a new Xcode plugin, create a new project and select **Xcode4 Plugin** from `OS X > Application Plug-in`.


## Usage

The default plugin file links against `AppKit` and `Foundation`, and, when built (and Xcode is restarted), creates a menu item labeled "Do Action" in the File menu. Pressing the menu item should open an alert. Customize at will!


## Notes

- Set `XCPluginHasUI` in `Info.plist` to `YES` to disable your plugin

### Plugin Debugging

- I would recommend keeping a console open with `tail -f /var/log/system.log` running, for that special moment when you crash Xcode, or want to see the output of your `NSLog()` statements.
- Plugins use ObjC GC, so remember to `retain` and `release` your things. :D
