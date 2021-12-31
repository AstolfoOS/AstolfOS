# AstolfOS

<img src="astolfos-logo.png" width="300" align="right">

Arch Linux, but with surprises!

## Installation

For now, there are no ISOs available. You can however upgrade an existing Arch installation by adding the AstolfOS pacman repo and installing some new packages:

1. Import and sign my GPG key:

   ```bash
   pacman-key --recv-keys DED5EC74298A5DBAE86C6E13ACC6088154D0F6C7
   pacman-key --lsign-key DED5EC74298A5DBAE86C6E13ACC6088154D0F6C7
   ```

2. Add this to your /etc/pacman.conf (make sure it's above Arch's repo definitions, as we override some Arch packages):

   ```ini
   [astolfos]
   Server = https://astolfo.laurinneff.ch/repo/$arch
   ```

3. Install AstolfOS packages:
   ```bash
   pacman -Syu # To install packages which AstolfOS overrides
   pacman -Sy astolfos-backgrounds
   ```
