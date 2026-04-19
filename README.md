# Omarchy Config
  An Ansible playbook with configurable roles and variables to set our dev machines in stone.


## What
Roles:
- Packages
- Configs
- Omarchy


## How
### Prerequisites
Install the requirments:
```ansible-galaxy collection install -r requirements.yml```

### Terminal
```ansible-playbook -i inventory/hosts.yml playbook.yml```

### VSCode
  Ctrl + Shift + B
or
  Ctrl + Shift + P (Tasks: Run Task) --> Select "Run Ansible Playbook"


## Configuring
Read the individual role's `README.md` files for more info into configuration.


## TODO
- [x] Set up basic framework
- [x] Install Ansible
- [x] Install Brave
- [x] Install VSCode
- [x] Remove Chromium
- [x] Set up GitHub repository
- [x] List app removals
- [ ] Set system-wide default editor under Setup > Defaults
- [ ] Create snapshot with omarchy-snapshot create


## Stashed commands
echo 255 | sudo tee /sys/class/leds/smc::kbd_backlight/brightness
