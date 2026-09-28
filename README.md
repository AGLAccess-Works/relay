# Relay

**Use an Xbox controller to move, click, scroll and type in Windows.**

Relay is a Windows desktop app from AGL Access Works. Its guided setup helps you choose the accessibility support you want, then creates a controller profile with the controls already assigned.

**Current release: [1.4.0-beta.6](https://github.com/AGLAccess-Works/relay/releases/tag/v1.4.0-beta.6).** This is a public beta. Feedback from disabled users, assistive-technology users and people helping someone set up a computer is welcome.

## Download and install

Download **Relay-1.4.0-beta.6-win-x64-Setup.exe** from the [beta release](https://github.com/AGLAccess-Works/relay/releases/tag/v1.4.0-beta.6). Run it on your Windows account; it adds a Start-menu shortcut and uninstall support. The installer includes the .NET runtime and does not require administrator rights.

The installer is currently **unsigned**, so Windows may show an unknown-publisher or SmartScreen notice. Check that you downloaded it from this repository's Releases page. A SHA-256 checksum is supplied with the release.

This repository currently distributes the installer and documentation. The application source code is not published here yet.

### Requirements

- A Windows x64 PC. Relay targets Windows 10 version 1809 or later and Windows 11. Clean-machine compatibility testing is still part of the beta.
- An Xbox or compatible XInput controller that already works in Windows, connected by USB, Bluetooth or Xbox Wireless.
- A microphone for Windows voice typing, if you want to use that feature.

Windows accessibility features vary by Windows version, language and connected hardware. Windows ARM64 emulation has not been tested.

## First launch

1. Open Relay and connect your controller.
2. Release the sticks, buttons and triggers briefly so Relay can start from neutral.
3. In the setup wizard, choose the help you want: larger text, zoom, reading aloud, steadier movement, on-screen typing, captions or voice typing.
4. Review your controls and optionally try the practice button.
5. Choose **Save and start**. Relay creates **My setup** and keeps any existing profiles.

Choose **Use one button at a time** if button combinations are difficult. You can run setup again from **Settings → Set up Relay for me**.

## Everyday controls

These are the basic pointer controls used by guided setup. Your active profile can change assignments; the Control page shows what each button currently does.

| Control | Action |
| --- | --- |
| Left stick | Move the mouse pointer |
| D-pad | Move the same pointer slowly for finer positioning |
| A | Left click; hold to drag |
| B | Right click |
| X | Middle click |
| Right stick | Scroll vertically or horizontally |
| View + Menu | Pause or resume controller output |
| Ctrl + Alt + P | Pause or resume using a keyboard |

If an older custom profile still sends arrow keys with the D-pad, choose **Mapping → Use D-pad to move the pointer**. Release the controls after changing settings, switching profiles or reconnecting. Closing Relay's window keeps it running in the notification area by default; use the tray menu to quit. Startup at sign-in is optional and off by default. Pause Relay before using your controller in a game.

### Accessibility tools

Guided setup assigns shortcuts for the features you select. The wizard shows the exact assignments before saving.

| Selected help | Guided setup assignment |
| --- | --- |
| On-screen keyboard | Press the left stick, or press A + B together |
| Magnifier | LT / RT zoom out / in; Y closes Magnifier; LB + RB changes its view |
| Read the screen aloud | Press the right stick to toggle Narrator |
| Captions | X + Y toggles Live captions on supported Windows versions |
| Speak instead of typing | Press both sticks together to open Windows voice typing (Windows + H) |

The **one button at a time** option uses individual tool buttons instead of combinations. Selecting a feature prepares its controls; it does not automatically turn that Windows feature on.

Relay includes a large, resizable on-screen keyboard. Click a text field first, open the Relay keyboard, then move the pointer over a key and press A. Voice typing is also available in **Accessibility → Quick tools** and in the mapping editor. Windows manages microphone permission, language support and the speech service.

You can adjust profiles, button mappings, pointer speed, dead zones, smoothing, scrolling, feedback and appearance in the app. Optional target assistance uses accessibility information exposed by other apps; you still make every click. Optional movement learning stores aggregate statistics and can be turned off or reset.

## Privacy and local data

Relay has no accounts, telemetry or application network calls. Settings, profiles, optional learned statistics and diagnostic logs are stored locally in `%LOCALAPPDATA%\XboxControllerMouse`.

Movement learning stores aggregate statistics, not raw movement history, screenshots, screen text or keystrokes. Windows features launched by Relay, including voice typing, follow their own Windows settings and privacy behaviour. Uninstalling preserves local preferences and removes Relay's startup entry.

## Beta limitations

- The app and installer are unsigned.
- Windows may block simulated input into administrator windows, protected Windows keyboards and secure desktops.
- The Xbox guide button is reserved by Windows. Elite paddles are not exposed as separate XInput controls.
- Stick-axis remapping and automatic app-specific profile switching are not included.
- Keyboard mappings send taps, not sustained key holds, text sequences or macros.
- One-button tool shortcuts do not provide scanning or dwell clicking; dragging still requires holding a mapped mouse button.
- Hands-on physical-controller, Narrator/NVDA, braille, switch-access, mixed-DPI and clean-install testing is still needed. The beta should not be treated as fully accessibility-validated.

## Send feedback

[Open an issue](https://github.com/AGLAccess-Works/relay/issues/new/choose) and include your Relay version, Windows version, controller model and connection type, what you tried, what happened, and steps to reproduce it. Tell us what would make any difficult part easier. You do not need to disclose a diagnosis or other personal medical information. Remove private information from screenshots, logs and exported profiles before sharing them.

Relay is an independent project and is not affiliated with Microsoft or Xbox.
