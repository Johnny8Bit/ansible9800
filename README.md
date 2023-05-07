**ansible9800**

Ansible project for Cisco Catalyst 9800 wirelesss controller.

Configures WLC from scratch.

Uses 'cisco.ios.ios_config' module as Ansible does not have WLC-specific resource modules. 

WLC needs initial base config and must be reachable via SSH, e.g.: `wlc_init_template.txt`
