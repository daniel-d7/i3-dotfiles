# i3-dotfiles
This is just dotfiles for my personal laptop, which is collected and borrowed from many sources.
I won't hope that anyone will use these files, but I am very happy if it help you a little bit with somethings :D

## My laptop:
- Lenovo Legion 5 - 15ARH7H
- Ryzen 7 AMD 6800H
- NVIDIA RTX 3070ti

## Screenshot
![Screenshot1](/Screenshot/screenshot1.png "full")
![Screenshot2](/Screenshot/screenshot2.png "free")

## Re-deploy the dotfiles
Start with a minimal installation of Arch Linux.
Git, vim/nano (any text editor) is compulsory.

### Dependency
> #### Install yay-git with:
> git clone https://aur.archlinux.git/yay-git.git && cd yay-git && makepkg -si
> #### Packages I used, modified as your usage. Install with yay.
> - i3-wm sddm i3lock-color feh picom dunst polybar rofi thunar thunar-volman tumbler ffmpegthumbnailer file-roller thunar-archive-plugin gvfs gvfs-mtp bluez bluez-utils blueman network-manager-applet flameshot gtk-engine-murrine playerctl
> - font: noto-fonts-emoji otf-font-awesome ttf-droid ttf-fira-code ttf-jetbrains-mono ttf-jetbrains-mono-nerd ttf-cascadia-code-nerd ttf-cascadia-mono-nerd ttf-fira-mono ttf-fira-sans ttf-firacode-nerd ttf-nerd-fonts-symbols ttf-nerd-fonts-symbols-mono
ttf-meslo-nerd
> - Extract Flat-Remix-Blue-Dark.zip to ~/.icons
> - Extract Andromeda-dark.tar.gz to ~/.themes
> - <em>Optional cursor theme: Extract Bibata-Modern-Ice.tar.xz to /usr/share/icons and change the theme by <strong>Interits=Bibata-Modern-Ice</strong> in <strong>/usr/share/icons/default/index.theme</strong></em>
> - Make a udev rule at <em>/usr/lib/udev/rules.d/90-brightnessctl.rules</em> with the details in /assets/90-brightnessctl.rules (<em>credited to Hummer12007</em>) to ensure brightness scroll in polybar
>
> #### Optional
> - fcitx5 fcitx5-qt fcitx5-gtk fcitx5-configtool fcitx5-unikey (if you don't use fcitx5, please remove the <em>exec fcitx5</em> in config)
> - polkit-kde-agent (I use kde-polkit for authentication)
> - EFISTUB: efibootmgr --create --disk <strong>/dev/nvme0n1</strong> --part <strong>1</strong> --label "Arch Linux" --loader /vmlinuz-linux --unicode 'root=UUID=<strong>b90413d66-2e64-48c4-967b-831270e3d425</strong> rw loglevel=3 quiet nvidia-drm.modeset=1 nvidia_drm.fbdev=1 initrd=\initramfs-linux.img'
> replace the bold part with your details from <em>blkid, lsblk</em>
>
> #### After the installation of the dependencies and what you need.
> Just copy .wallpaper to your home directory and all folder in config_files to your ~/.config
>
> #### Some additional steps with polybar (at ~/.config/polybar/config.ini)
> - use <strong>ip link</strong> to get WLAN name and edit module/network
> - use <strong>ls -1 /sys/class/powls -1 /sys/class/power_supply/</strong> to get battery and adater name, after that edit the module/battery

### Reboot, and make changes to your system.
### Enjoy

# MY REGARDS TO
1. **parazeeknova** for his dotfile, which inspired me and most resource is borrowed from his repos at [link](https://github.com/parazeeknova/dotfiles/tree/main)
2. Thanks **JaKooLit** for his [install scripts](https://github.com/JaKooLit/Arch-Hyprland), which help me much from the start of Arch
3. Thanks **mylinuxforwork** for his [dotfiles](https://github.com/mylinuxforwork/dotfiles) and [hyprland-starter](https://github.com/mylinuxforwork/hyprland-starter)
4. Rofi-power-menu from **adi1090x** [rofi-power-menu](https://github.com/adi1090x/rofi/tree/master)
## And many other guys, I love you all for keeping your hard work.