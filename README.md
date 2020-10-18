# rtl8812au

## How To

### Edit File
```bash
/usr/src/rtl8812au-4.3.8.12175.20140902+dfsg/dkms.conf
```

### Change Line
```bash
MAKE="'make' all" 
```

### To:
```bash
MAKE="'make' all KVER=${kernelver}"
```

### Remove & Build & Install
```bash
dkms remove rtl8812au/4.3.8.12175.20140902+dfsg -k "$(uname -r)/$(uname -p)"  
dkms build rtl8812au/4.3.8.12175.20140902+dfsg -k "$(uname -r)/$(uname -p)"  
dkms install rtl8812au/4.3.8.12175.20140902+dfsg -k "$(uname -r)/$(uname -p)"
```

### Enable
```bash
sudo modprobe 8812au
```
