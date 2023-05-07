## Ansible project for Cisco Catalyst 9800 wirelesss controller.

Configures WLC from scratch.

Uses generic 'cisco.ios.ios_config' module as Ansible does not have WLC-specific resource modules. 

WLC needs initial base config and must be reachable via SSH, see example: `wlc_init_template.txt`

### Ansible hierarchy

/etc/ansible
    ansible.cfg
    wlc_hosts
    /group_vars
        wlcs.yaml
    /playbooks
        wlc_conf.yaml


### WLC Config
Simple but complete WLC configuration, including:
* VLAN
* AP Join Profile
* Site Tag
* RF Profiles
* RF Tag
* WLAN
* Policy Profile
* Policy Tag
* AP Filter
* Parameter Map
* Line VTY
* Line Con
* Global settings

This config results in a working PSK SSID, assuming APs join the WLC with hostnames starting with "AP".

Some of the configuration is redundant and serves only as an example.

