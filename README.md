# Le Capybara ZMK Config Repo:

Super experimental [Le Capybara](https://github.com/sporkus/le_capybara_keyboard/) keyboard support for ZMK.

## Calibration

After first loading the firmware, you need to run the calibration. Use a terminal, e.g. putty, tio, etc to connect to the virtual console device, e.g. `/dev/ttyACM0`:

You'll be presented with a prompt like `uart :~$`. At the prompt, type `ec matrix calibration start` and hit enter. As prompted, leave all the keys alone while the low baselines are set, and then when prompted press each key slowly in sequence.

After the calibration completes, type `ec matrix calibration save` to persist the calibration to flash. You can re-run this process later if needed if you've made changes and need to recalibrate things.

Once calibrated, the saved calibrations should be loaded the next time you plug in or reset the keyboard.
