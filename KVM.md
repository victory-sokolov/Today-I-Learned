# QEMU/KVM setup to run Linux,macOS
---

## Align mouse with vm

```
-usb -device usb-kbd -device usb-tablet
```

## Access web-cam

```
-device usb-host,hostbus=1,hostaddr=5
```

`hostbus=1,hostaddr=5` is from 

```
lsusb
......
Bus 001 Device 005: ID 0408:2fb1 Quanta Computer, Inc.
```

---

### References:

https://dev.to/nicole/running-macos-on-windows-10-with-wsl2-kvm-and-qemu-21e1
https://boxofcables.dev/accelerated-kvm-guests-on-wsl-2/
https://homanhuang.medium.com/install-mac-on-wsl2-prepare-for-ios-editing-eb867a2b2b67
