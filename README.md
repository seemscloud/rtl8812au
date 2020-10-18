# rtl8812au

## AirCrack-NG 

### Clone Git Repository
```bash
https://github.com/aircrack-ng/rtl8812au
```

### Compile & Install
```bash
make 
make install 
```

### Enable Module
```
modprobe 88XXau
```

## From DKMS

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
modprobe -r 8812au
modprobe 8812au
```
