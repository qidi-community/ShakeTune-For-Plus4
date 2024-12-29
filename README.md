# Klipper Shake&Tune plugin for Qidi Plus 4

Shake&Tune is a Klipper plugin from the [Klippain](https://github.com/Frix-x/klippain) ecosystem, designed to create insightful visualizations to help you troubleshoot your mechanical problems and give you tools to better calibrate the input shaper filters on your 3D printer. It can be installed on any Klipper machine and is not limited to those using the full Klippain.

Check out the **[detailed documentation here](./docs/README.md)**.

![logo banner](./docs/banner.png)


## Attribution

This repository is a fork of https://github.com/Frix-x/klippain-shaketune version 4.1.0 and modified for deployment upon the Qidi Plus 4 3D Printer.
All thanks for Frix-x for their work on this project

## Installation

Follow these steps to install Shake&Tune on your printer:
  1. The Qidi Plus 4 already comes pre-installed with a working accelerometer and by default is configured with it enabled, and so there should be no additional work required for Klippain Shake & Tune to use it.

  1. Install Shake&Tune by running over SSH on your printer:
     ```bash
     cd /home/mks && wget -O - https://raw.githubusercontent.com/qidi-community/ShakeTune-For-Plus4/refs/heads/main/install.sh | bash
     ```

  1. Then, insert the following into your `printer.cfg` file BEFORE the `SAVE_CONFIG` section and restart Klipper:
     ```
     [shaketune]
     timeout: 1200
     #    The maximum time in seconds to let Shake&Tune process the CSV files and generate the graphs.
     # result_folder: ~/printer_data/config/ShakeTune_results
     #    The folder where the results will be stored. It will be created if it doesn't exist.
     # number_of_results_to_keep: 3
     #    The number of results to keep in the result_folder. The oldest results will
     #    be automatically deleted after each runs.
     # keep_raw_csv: False
     #    If True, the raw CSV files will be kept in the result_folder alongside the
     #    PNG graphs. If False, they will be deleted and only the graphs will be kept.
     # show_macros_in_webui: True
     #    Mainsail and Fluidd doesn't create buttons for "system" macros that are not in the
     #    printer.cfg file. If you want to see the macros in the webui, set this to True.

## Documentation

Don't forget to check out **[Shake&Tune documentation here](./docs/README.md)**.
