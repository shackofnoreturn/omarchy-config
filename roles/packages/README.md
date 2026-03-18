# Role: Packages
    Installs and removes pacman/aur packages to be found on arch systems

## Prerequisites
Install the required ansible-galaxy collection:
```ansible-galaxy collection install kewlfft.aur```

## What
Use Pacman and AUR to install and remove packages set defined in the `default` variables.

## How
Include this role in your prefered playbook:

```yml
- name: Configure Omarchy System
  hosts: shack-book-001
  roles:
    - packages
```
