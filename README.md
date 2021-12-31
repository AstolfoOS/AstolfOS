# AstolfOS

<img src="astolfos-logo.png" width="300" align="right">

AstolfOS is a Linux distribution themed around Astolfo, and it's based on Arch Linux

## Installation

For now, there are no ISOs available. You can however upgrade an existing Arch installation by adding the AstolfOS pacman repo and installing some new packages:

1. Add this to your /etc/pacman.conf (make sure it's above Arch's repo definitions, as we override some Arch packages):

   ```ini
   [astolfos]
   Server = https://astolfo.laurinneff.ch/repo/$arch
   SigLevel = PackageOptional
   ```

2. Install AstolfOS packages:
   ```shell
   pacman -Sy filesystem astolfos-backgrounds
   ```

Packages are currently unsigned, but I'll add it at some point in the future
