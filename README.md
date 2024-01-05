# Trinity Enabler Linux <sub>except i'm just building it because [twitter asked](https://twitter.com/1756_leroms/status/1742838568974704658)</sub>

Windows Usage: (credit [@luciascarlet](https://twitter.com/luciascarlet) and [@majorbean_](https://twitter.com/majorbean_))

0. ***Don't blindly follow instructions when playing with drivers like this. Report issues.***
1. Acquire Zadig (no install required - included in release[^1])
2. Go to options and enable list all devices
3. Select `"Speakers (Interface 2)"`[^1] in the devices list; if there's multiple, look for the one with the USB ID `"05AC 1101"`[^1]
4. Change the driver to be installed (to the right of the orange arrow) to `WinUSB`[^2]
5. Click replace/install driver
6. Run TrinityEnabler with the appropriate options from a command prompt[^3] (e.g. `.\trinityenabler_x86.exe --power-500`)
7. (Bonus) run `.\trinityenabler_x86.exe` with no options to see available parameters


[^1]: Zadig 2.8 provided and supports Windows 7 and newer
[^2]: Potential constants from instruction providers - I suspect that these values could be different (perhaps subtly) on your system. 
[^3]: If it doesn't work, try using an elevated terminal (run with administrative privileges) before creating an issue

------------------------------

# Original readme

libusb port of [Trinity Enabler](https://github.com/jeanthom/TrinityEnabler). Runs on Linux, and probably also on macOS and Windows.

## Compilation

You will need [libusb](https://libusb.info/).

```
make
```

Build artifacts are located in `src/`.

## Usage

```
trinityenabler --power-500
```
