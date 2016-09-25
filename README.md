System Upgrader script
======================

This script was written to avoid typing same apt commands over and over again on my Ubuntu installation (update, upgrade, full-upgrade, auto-remove, auto-clean) so I wrote this bash script

This version is highly modified compared to the initial script I wrote for myself (I included it as well to compare the evolution).

This script is highly customizable, meaning that you can add your own `upgrader.conf` for your distro!

## What does it do?
As the name implies, this script takes the preferred package manager and performs several tasks like update, upgrade, and cleanup. These tasks are called options, but in `upgrader`, they're called cycles. Why? Because this program loops through a list of options which are called automatically.

## I want it! How do I proceed?
The installation is pretty simple and it's best done via CLI:
- Clone the project from this repo.
- Enter the directory: `cd upgrader`
- Create configuration directory: `sudo mkdir /etc/upgrader`
- Copy a configuration file, e.g.: `sudo cp etc/upgrader.ubuntu.conf /etc/upgrader/upgrader.conf`
  - If you don't find your distro, you can copy the template and edit it
- Symlink the binary: `sudo ln -s bin/upgrader /usr/local/bin/upgrader`
- Try it: `upgrader`
- Use it: `sudo upgrader cycle`

## Warning!
This script interacts with system maintenance tools, such as apt or zypper, so you must execute the script with as root (sudo should be enough and secure). In most cases, the updates executed by Upgrader works without any problems.

## License
This project is available under MIT license.
