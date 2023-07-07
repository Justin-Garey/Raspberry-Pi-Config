# Overclocking a RPi
Adequate cooling and heatsinks are required

## For the RPi 4b

Update and upgrade the pis dependencies
```
sudo apt update && sudo apt upgrade -y
sudo apt dist-upgrade
sudo apt install rpi-update
```

Enter an editor for the boot config
```
sudo nano /boot/config.txt
```

There should be a section that reads
```
#uncomment to overclock the arm. 700 MHz is the default.
#arm_freq=800
```


Add this somewhere in the configuration:
```
over_voltage=6
arm_freq=2000
gpu_freq=750
```

To see the clock speeds or measure cpu temperatures
```
watch -n1 vcgencmd measure_clock arm
watch -n1 vcgencmd measure_temp
```