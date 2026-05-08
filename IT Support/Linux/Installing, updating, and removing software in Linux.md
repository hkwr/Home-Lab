# Installing, updating, and removing software in Linux

## Scenario
There are three learning objectives for this lab:
1. Update- The machine you'll be using comes preinstalled with an old version of the VLC Media Player. You'll update VLC to the newest version.
2. Install- You'll install the Mozilla Firefox web browser. There's currently no version of Firefox on the machine you'll be using, so it will be a fresh installation.
3. Uninstall - You'll uninstall the GIMP photo-editing tool from the machine, removing it entirely.

## Verifying installed software on Linux
Command to check software installation status
```terminal
dpkg -s unique_package_name
```
Check to make sure the software status before begin the lab.

### Checking Firefox
Command:
```terminal
dpkg -s firefox-esr
```
Output:

Explaination: This shows that Firefox isn`t currently install on the system

### Checking GIMP
Command:
```terminal
dpkg -s gimp
```
Output:

Explanation: GIMP is installed.

### Checking VLC
Command:
```terminal
dpkg -s vlc
```
Output:

Explanation: VLC is installed, current VLC version is

## Update VLC media player
1. Force an update of the package manager using the command:
```terminal
sudo apt-get install -f
```
2. Wait for package manager to update, if ask you'd like to continue, then enter y for "yes"
3. After the process is finished, use command below to verify the installation.
```terminal
dpkg -s vlc
```
Output:

Explanation: The latest VLC version is



