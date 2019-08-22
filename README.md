# Check_RPI plugin

Plugin to report voltage/temp and flags and use sudo if necessary. 

# Installation

Copy sudoer file and the plugin to their places

    sudo cp check_rpi /usr/lib/nagios/plugins
    sudo cp sudo.check_rpi /etc/sudoers.d/check_rpi

If you are using Icinga you can also use the include
definition for checks:

    sudo cp check_rpi.conf /etc/icinga2/conf.d
    
# Check installation

    sudo su nagios -s /bin/sh -c /usr/lib/nagios/plugins/check_rpi
    
# Example output

Rpi zero W that is running normally:

    TEMP OK - Flags: Okay (0x0) - CPU temperature: 54.72°C - GPU temperature: 54.1°C - Core Voltage: 1.3500 - SDRAM P Voltage: 1.2250 | cputemp=54.72;60;70;0; gputemp=54.1;60;70;0; corevolt=1.3500; sdrampvolt=1.2250


Raspberry Pi 4 that is running too hot:

    TEMP WARNING - Flags:  undervoltage throtlling, historic state: undervoltage throttled frequency_capped (0x70005) - CPU temperature: 80.341°C - GPU temperature: 79.0°C - Core Voltage: 0.8982 - SDRAM P Voltage: 1.1000



## Copyright and license

Copyright 2019 Arne Schwabe, all code released under the [MIT license](LICENSE).
Copyright 2016 Achim Christ, all code released under the [MIT license](LICENSE).
