# Check_RPI plugin

Plugin to report voltage/temp and use sudo where necessary. 

# Installation

Copy sudoer file and the plugin to their places

    sudo cp check_rpi /usr/lib/nagios/plugins
    sudo cp sudo.check_rpi /etc/sudoers.d/check_rpi
    
# Check installation

    sudo su nagios -s /bin/sh -c /usr/lib/nagios/plugins/check_rpi


## Copyright and license

Copyright 2019 Arne Schwabe, all code released under the [MIT license](LICENSE).
Copyright 2016 Achim Christ, all code released under the [MIT license](LICENSE).
