# Role: Packages
    Installs and removes pacman/aur packages to be found on arch systems

## Prerequisites
Install the required ansible-galaxy collection:
```ansible-galaxy collection install kewlfft.aur```

## What
Use Pacman and AUR to install and remove packages set defined in the `default` variables.

## How
List all packages to determine which you want to remove:

- `pacman -Qqn` (official)
- `pacman -Qqm` (unofficial)

To check for a specific package:
`pacman -Qqn | grep libre`

Include this role in your prefered playbook:

```yml
- name: Configure Omarchy System
  hosts: shack-book-001
  roles:
    - packages
```
