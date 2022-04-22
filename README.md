# rtl8188fu

Install wifi driver for Realtek RTL8188FTV (chipset rtl8188fu) for Kali/Parrot

Fixed for enable monitor mode

![image](https://user-images.githubusercontent.com/90561566/164728137-e0ecaf67-b1a0-411a-811c-3a6e655b5c0c.png)

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
CONFIG_POWER_SAVING = n # line 41
CONFIG_WIFI_MONITOR = y # line 60
```

