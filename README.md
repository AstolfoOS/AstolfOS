# AstolfOS

<img src="astolfos-logo.png" width="300" align="right">

AstolfOS is a Linux distribution based on Arch Linux and themed around Astolfo

## Installation

For now, there are no ISOs available. You can however upgrade an existing Arch installation by adding the AstolfOS pacman repo and installing some new packages:

1. Add this to your /etc/pacman.conf (make sure it's above Arch's repo definitions, as we override some Arch packages):

   ```ini
   [astolfos]
   Server = https://astolfo.laurinneff.ch/repo/$arch
   SigLevel = PackageOptional
   ```

2. Install AstolfOS packages:
   ```bash
   pacman -Syu # To install packages which AstolfOS overrides
   pacman -Sy astolfos-backgrounds
   ```

Packages are currently unsigned, but I'll add signing at some point in the future
