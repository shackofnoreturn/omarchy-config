# Omarchy Config
  An Ansible playbook with configurable roles and variables to set our dev machines in stone.


## What
Roles:
- Packages
- Configs
- Omarchy


## How
### Prerequisites
Install the required ansible-galaxy collection:
```ansible-galaxy collection install kewlfft.aur```

Add your current user to the sudoers file by running this command if you don't want to enter become password every run:
```
echo "yourUser ALL=(ALL) NOPASSWD: ALL" | sudo tee /etc/sudoers.d/shackadmin
sudo chmod 440 /etc/sudoers.d/shackadmin
```

### Terminal
```ansible-playbook -i inventory/hosts.yml playbook.yml```

### VSCode
  Ctrl + Shift + B
or
  Ctrl + Shift + P (Tasks: Run Task) --> Select "Run Ansible Playbook"


## Configuring
### Packages
Check your current packages with `pacman -Qqn` (official) and `pacman -Qqm` (unofficial)

Alter your package selection:
roles/packages/defaults/main.yml

(read the individual role's `README.md` files for more info into configuration)


## TODO
- [x] Set up basic framework
- [x] Install Ansible
- [x] Install Brave
- [x] Install VSCode
- [x] Remove Chromium
- [ ] Set up GitHub repository
- [ ] Go through all applications and make up list of removals
- [ ] Set system-wide default editor under Setup > Defaults

echo 255 | sudo tee /sys/class/leds/smc::kbd_backlight/brightness
