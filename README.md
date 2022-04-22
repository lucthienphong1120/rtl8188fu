# rtl8188fu

Install wifi driver for Realtek RTL8188FTV (chipset rtl8188fu) for Kali/Parrot

Fixed for enable monitor mode

# Usage

```
sudo apt-get install build-essential git dkms linux-headers-$(uname -r)

git clone https://github.com/lucthienphong1120/rtl8188fu

sudo dkms add ./rtl8188fu

sudo dkms build rtl8188fu/1.0

sudo dkms install rtl8188fu/1.0

sudo cp ./rtl8188fu/firmware/rtl8188fufw.bin /lib/firmware/rtlwifi/

sudo reboot
```

## Change logs

if you want to enable monitor mode, use my repo

origin original belongs to @kelebek333

```
lines 40 and 61 need to change from y to n and n to y
CONFIG_POWER_SAVING = n
CONFIG_WIFI_MONITOR = y
```

