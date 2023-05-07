## Ansible project for Cisco Catalyst 9800 wirelesss controller.

Configures WLC from scratch.

Uses generic 'cisco.ios.ios_config' module as Ansible does not have WLC-specific resource modules. 

WLC needs initial base config and must be reachable via SSH, see example: `wlc_init_template.txt`

### Ansible hierarchy

```
/etc/ansible

├── ansible.cfg
├── group_vars
│   └── wlcs.yaml
├── playbooks
│   └── wlc_conf.yaml
├── wlc_hosts
└── wlc_init_template.txt
```
### Ansible Configuration

Changes to ansible.cfg
```
inventory = /etc/ansible/wlc_hosts
gathering = explicit
host_key_checking = False
record_host_keys=False
```
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

