# AstolfOS

<img src="astolfos-logo.png" width="300" align="right">

Arch Linux, but with surprises!

## Installation

### Fresh install

1. Download the ISO [here](https://astolfo.laurinneff.ch/iso/) (please use the torrent)

2. Optionally verify the signature:

   ```bash
   gpg --recv-keys DED5EC74298A5DBAE86C6E13ACC6088154D0F6C7
   gpg --verify astolfos-yyyy.mm.dd-x86_64.iso.sig
   ```

3. Boot it and follow the [Arch Linux installation guide](https://wiki.archlinux.org/title/Installation_guide)

### Convert an existing Arch Linux install

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
