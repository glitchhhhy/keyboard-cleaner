# KeyboardCleaner
KeyboardCleaner is macOS app for disabling your input devices temporarily &mdash; perfect for cleaning your keyboard without having to shut down!

## Usage
Once you start KeyboardCleaner, your screen will turn blank and display a message showing that the keyboard and mouse have been disabled. To re-enable them and close KeyboardCleaner, hold down right click for one second and release.

## Accessibility Access
If you are running KeyboardCleaner for the first time, you may need to grant it accessibility access. Usually macOS will show a system dialog with instructions to do so. If it does not, go to System Preferences > Security & Privacy > Privacy > Accessibility and grant KeyboardCleaner access.

## Malfunctions
If KeyboardCleaner were to malfunction and prevent you from deactivating, you must force shutdown your device. This can be done on most modern MacBook laptops by holding the power button down until the screen turns black.

## Event Taps
KeyboardCleaner creates an event tap to disable input. If you are running software that detects (and possibly terminates) programs doing this, you might need to whitelist KeyboardCleaner.

## AutoKill
While working on KeyboardCleaner, you should keep the AutoKill script running in the background. To do so, run:
```
python3 auto-kill.py [SECONDS]
```
The script will check for the KeyboardCleaner process every 2 seconds and send `SIGKILL` if its running time exceeds the `[SECONDS]` argument. This is useful to avoid needing to force restart your device if you make a change that prevents you from deactivating KeyboardCleaner normally.

## Note
This program does not automatically clean your keyboard. It only assists in the process of doing so.

## License
[MIT](https://choosealicense.com/licenses/mit/)
