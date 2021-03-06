# NVDA Unmute

* Author: Oleksandr Gryshchenko
* Version: 1.3
* Download [stable version][1]
* Download [development version][2]

This add-on checks the status of the Windows audio system when NVDA starts. And, if it turns out that the sound is muted - the add-on forcibly turns it on.
The add-on also checks the status of the speech synthesizer. If there are problems with its initialization, attempts are made to start the synthesizer, which is specified in the NVDA settings.
An additional feature is the ability to adjust the volume of the main audio device and separately for each running process using convenient keyboard shortcuts.

## Add-on settings dialog
The following options are available in the add-on settings dialog:

1. The first slider in the add-on settings dialog allows you to specify the volume level of Windows, which will be set when you start NVDA if the sound was previously muted or was too low.

2. The minimum Windows volume level at which the volume up procedure will be applied. This slider allows you to adjust the sensitivity level of the add-on.
If the volume level drops to less than the value specified here, the volume will be increased the next time you start NVDA.
Otherwise, if the volume level remains higher than the value specified here, then when you restart NVDA, its level will not change.
And, of course, if the sound was previously turned off, when restarts add-on will turn it on anyway.

3. The following check box allows to enable re-initialization of the voice synthesizer driver.
This procedure will only start if it is detected at NVDA startup that the voice synthesizer driver has not been initialized.

4. In this field you can specify the number of attempts to re-initialize the voice synthesizer driver. Attempts are performed cyclically with an interval of 1 second. A value of 0 means that attempts will be performed indefinitely until the procedure is successfully completed.

5. The next checkbox turns on or off playing the startup sound  when the operation is successful.

## Adjust the volume level
This add-on allows you to adjust the volume of the main audio device of Windows and separately for each currently running program.
To do this, use the keyboard shortcuts NVDA+Windows+ arrow keys.
The function works similarly to the NVDA settings circle. Use the left and right arrows to select a device or application. Then use the up and down arrows to adjust the volume level of the selected audio source.
If you reduce the volume to zero for a certain program and press the down arrow again, this sound source will be muted.

Note: The list of audio sources changes dynamically and depends on the currently running programs.

## Change log

### Version 1.3
* added the ability to control the volume of the main audio device and separately for each running program;
* updated translation into Vietnamese (thanks to Dang Manh Cuong);
* Turkish translation added (thanks to Cagri Dogan);
* updated Ukrainian translation;
* updated ReadMe.

### Version 1.2
* switched to using the **Core Audio Windows API** instead of **Windows Sound Manager**;
* added startup sound playback when audio is successfully turned on by add-on.

### Version 1.1
* added add-on settings dialog;
* updated Ukrainian translation.

### Version 1.0.1
* Performs repeated attempts to enabling the synth driver in case of its failed initialization;
* Vietnamese translation added by Dang Manh Cuong;
* Ukrainian translation added.

### Version 1.0. Features of implementation
The add-on uses a third-party module Windows Sound Manager.

## Altering NVDA Unmute
You may clone this repo to make alteration to NVDA Unmute.

### Third Party dependencies
These can be installed with pip:
- markdown
- scons
- python-gettext

### To package the add-on for distribution:
1. Open a command line, change to the root of this repo
2. Run the **scons** command. The created add-on, if there were no errors, is placed in the current directory.

[1]: https://github.com/grisov/Unmute/releases/download/v1.3/unmute-1.3.nvda-addon
[2]: https://github.com/grisov/Unmute/releases/download/v1.3/unmute-1.3.nvda-addon
