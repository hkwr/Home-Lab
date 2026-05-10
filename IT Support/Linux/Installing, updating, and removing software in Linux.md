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

<img alt="dpkg -s firefox-esr output 1" src="https://github.com/hkwr/Home-Lab/blob/dac2c0bd468ea7e6ccf436b3764d65fca7661dfd/IT%20Support/Linux/Images/dpkg%20-s%20firefox-esr%20output%201.png" align="left">
<br clear="left" />
<br>
Explaination: This shows that Firefox isn`t currently install on the system

### Checking GIMP
Command:
```terminal
dpkg -s gimp
```
Output:

<img alt="dpkg -s gimp output 1" src="https://github.com/hkwr/Home-Lab/blob/9d019f8d91dd020b5df625ba3c5636e659f04bf4/IT%20Support/Linux/Images/dpkg%20-s%20gimp%20output%201.png" align="left">
<br clear="left" />
<br>
Explanation: GIMP is installed.

### Checking VLC
Command:
```terminal
dpkg -s vlc
```
Output:

<img alt="dpkg -s vlc output 1" src="https://github.com/hkwr/Home-Lab/blob/9e87a9cb21b893bd8bdf2ba06e6bdee948885248/IT%20Support/Linux/Images/dpkg%20-s%20vlc%20output%201.png" align="left">
<br clear="left" />
<br>
Explanation: VLC is installed, current VLC version is 2.2.7

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
<br>
<img alt="dpkg -s vlc output 2" src="https://github.com/hkwr/Home-Lab/blob/8ee5521d392d362ccf958e074001798d959e076c/IT%20Support/Linux/Images/dpkg%20-s%20vlc%20output%202.png" align="left">
<br clear="left" />
<br>
Explanation: The latest VLC version is 3.0.23

## Installing Mozilla Firefox
1. Since Firefox are set up in repositories by default, need to make sure these repositories are up-to-date and all dependencies are fixed. To do so run the following command (you may have to enter the letter "Y" at some point during the process to confirm your action):
```terminal
sudo apt-get update
```

2. Run the below command to install Firefox:
```terminal
sudo apt-get install firefox-esr
```

3. You'll be prompted to confirm that you‘d like to continue with the installation. To continue, enter y (as in "yes") into the terminal, and hit enter:

Output:
<br>
<img alt="sudo apt-get install firefox-esr output 1" src="https://github.com/hkwr/Home-Lab/blob/f59d598f31ed9816caa5a54ec4be5721730b5597/IT%20Support/Linux/Images/sudo%20apt-get%20install%20firefox-esr%20output%201.png" align="left">
<br clear="left" />
<br>
4. Once this process is complete, Firefox will be installed on your instance. To verify that it's installed, enter command below into the terminal window again, and you'll see different output than before:

```terminal
dpkg -s firefox-esr
```

Output:
<br>
<img alt="dpkg -s firefox-esr output 2" src="https://github.com/hkwr/Home-Lab/blob/e0f39f2ec8a5c62693d973ae830cb887844c2857/IT%20Support/Linux/Images/dpkg%20-s%20firefox-esr%20output%202.png" align="left">
<br clear="left" />
<br>
Explanation: The status is listed as installed.

## Uninstall GIMP
1. To uninstall GIMP, use the command below:
```terminal
sudo apt-get remove gimp
```

2. It will prompt you to confirm the uninstallation. Enter y to confirm, and the process will begin:

Output:
<br>
<img alt="sudo apt-get remove gimp output 1" src="https://github.com/hkwr/Home-Lab/blob/ca5ab4e47de29d6cc8fdd6c626002b6d67087b86/IT%20Support/Linux/Images/sudo%20apt-get%20remove%20gimp%20output%201.png" align="left">
<br clear="left" />
<br>

3. To verify GIMP successfully unistall, used the command below:
```terminal
dpkg -s gimp
```

Output:
<br>
<img alt="dpkg -s gimp output 2" src="https://github.com/hkwr/Home-Lab/blob/56494383896a7f82792ef82ba0cf561dee4caadc/IT%20Support/Linux/Images/dpkg%20-s%20gimp%20output%202.png" align="left">
<br clear="left" />
<br>

Explanation: The status show that GIMP is not available on the system, thus uninstallation is successful.
