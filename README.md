# RouterPi

Turn your Raspberry Pi into simple Wi-Fi hotspot

## How to use

### Install software

`sudo apt install dnsmasq hostapd iptables`

### Copy config files

`sudo cp -r etc/* /etc/`

Also it might be needed to add `denyinterfaces wlan0` to `/etc/dhcpcd.conf`

### Change Wi-Fi password

`sudo nano /etc/hostapd/hostapd.conf`

### Set iptables rules

You need to run this script after every reboot

`./forward.sh`

### Start services

`sudo systemctl start hostapd dnsmasq`

## License

MIT

