# aircrack-ng
## introduction
Aircrack-ng is a complete suite of tools to assess WiFi network security.

All tools are command line which allows for heavy scripting. A lot of GUIs have taken advantage of this feature. It works primarily on Linux but also Windows, macOS, FreeBSD, OpenBSD, NetBSD, as well as Solaris and even eComStation 2.

It focuses on different areas of WiFi security:
- Monitoring: Packet capture and export of data to text files for further processing by third party tools.
- Attacking: Replay attacks, deauthentication, fake access points and others via packet injection.
- Testing: Checking WiFi cards and driver capabilities (capture and injection).
- Cracking: WEP and WPA PSK (WPA 1 and 2).

We also maintain patches for:
- Packet injection for Linux drivers
- HostAPd and Freeradius, called WPE (Wireless Pawn Edition) patches, to attack WPA Enterprise.

## links
- [download page for program and driver patches](https://www.aircrack-ng.org/doku.php?id=Main#download)
- [injection test to make sure drivers are patched](https://www.aircrack-ng.org/doku.php?id=injection_test)
- [tutorial: how to crack WPA/WPA2](https://www.aircrack-ng.org/doku.php?id=cracking_wpa)

## install
update apt package source and install available upgrades
`sudo apt-get update && sudo apt-get upgrade`

install aircrack-ng tools
`sudo apt-get install -y aircrack-ng`

## getting started
check for connected wireless interfaces
`iwconfig`

start `wlan0` interface
`airmon-ng start wlan0`

this command may return error: `command failed: unknown error 524`
it can be ignored (?)

kill running processes
`airmon-ng check kill`

listen to nearby devices
`airodump-ng wlan0mon`
