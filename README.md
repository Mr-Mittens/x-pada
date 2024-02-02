![img](wmb/ra-men.png) 
![img](wmb/ra-2.png) 
                                                  
An elegant hyprland config coming with less bloat, smooth workflow and aesthetic black theme 

- minimal setup with Archlinux
- I just usually forget things so if you are new to Window managers this space will save you !
- vimrc without bloated plugins.

</div>
<br>

___
<div align="">

Install Scripts & Wiki
===========
>[Arch install](https://github.com/Mr-Mittens/Scripts/tree/main/arch) &&
> [Hyprland Script](https://github.com/Mr-Mittens/Scripts/blob/main/hyprland/hyper)
 
**If you have arch already installed your (way) then only refer to hyprland script !** 
<br>

<div align="left">
  <details>
    <summary><strong>Arch Installation Script </strong></summary>
    <p>

```bash
bash <(curl -s https://raw.githubusercontent.com/Mr-Mittens/Scripts/main/arch/basebuild) && curl -sO https://raw.githubusercontent.com/Mr-Mittens/Scripts/main/arch/chrootbuild
```

<br>

make the bash executable and run.(make your own tweaks before running it !)

```
chmod +x basebuild && ./basebuild

```

> after the installation system will reboot and you can login. (you need to follow hyprland installation next)    

</div>



<div align="left">
  <details>
    <summary><strong>Hyprland Script </strong></summary>
    <p>

```bash
curl -sO https://raw.githubusercontent.com/Mr-Mittens/Scripts/main/hyprland/hyper

```

<br>

make the bash executable and run.(make your own tweaks before running it !)

```
chmod +x hyper && ./hyper

```

> just install only necessary items, these are my preferences you can tweak your likes & also im open for suggestions..   

</div>


<div align="left">
  <details>
    <summary><strong> Ref- packages </strong></summary>
    <p>

> Just install what you need manually you can opt for better packages.(Don't just install packages from a random script!) 
```
hyprland hyprpaper vim wayland-protocols waybar-hyprland brightnessctl make wlroots pipewire pipewire-alsa pipewire-pulse pipewire-jack wireplumber xdg-desktop-portal-wlr grim slurp sddm alacritty thunar pavucontrol bluez mpv mako neofetch btop swaybg swayidle swww lxappearance  

```
</div>

<br>



<br>


## Basic keybindings

> **Note** applications that are only necessary are included in the base-installer scripts.

#### Apps

| Keybind                                                  | Action                           |
| -------------------------------------------------------- | -------------------------------- |
| <kbd>⊞ Super</kbd> <kbd>X</kbd>                          | Terminal <sup>(alacritty)</sup>  |
| <kbd>⊞ Super</kbd> <kbd>Z</kbd>                          | App Launcher <sup>(Wofi)</sup>   |
| <kbd>⊞ Super</kbd> <kbd>F</kbd>                          | File manager <sup>(Thunar)</sup> |

#### Other

| Keybind                                                | Action                     |
| ------------------------------------------------------ | -------------------------- |
| <kbd>⊞ Super</kbd> <kbd>[0,9]</kbd>                    | Change workspace           |
| <kbd>⊞ Super</kbd> <kbd>⇧ Shift</kbd> <kbd>[0,9]</kbd> | Move window to a workspace |
| <kbd>⊞ Super</kbd> <kbd>Q</kbd>                        | Kill a window              |
| <kbd>⊞ Super</kbd> <kbd>right click</kbd>              | Move a window              |
| <kbd>⊞ Super</kbd> <kbd>right click</kbd>              | Resize a window            |


>additional-pkgs

     `wl-clipboard` ---> `wayland clipboard utility`
     `ttf-jetbrains-mono`
     `ttf-font-awesome`
     `gvfs-mtp` --> `for automount and all `
     `mtpfs`    --> `for media transfer protocol`



>switching from `pulseaudio` to `pipewire`  
>install necessary packages   
```
sudo pacman -S pipewire pipewire-alsa pipewire-pulse pipewire-jack
```
>stop the PulseAudio services and enable pipewire services:

>first method

```
systemctl --user stop pulseaudio.socket
systemctl --user stop pulseaudio.service
systemctl --user disable pulseaudio.socket
systemctl --user disable pulseaudio.service
```
>second method 
```
systemctl --user enable pipewire.socket
systemctl --user enable pipewire.service
systemctl --user start pipewire.socket
systemctl --user start pipewire.service
```
---

>sound card detecting issue (in your pavucontrol if sound card is showing dummy output)

`aplay -1` if audio device not listed then :
`sudo vim /etc/modprobe.d/alsa-base.conf` & 
```
systemctl --user enable pipewire.service
systemctl --user start pipewire.service
systemctl --user enable pipewire-pulse.service
systemctl --user start pipewire-pulse.service

```

>screen sharing issue `OBS` install this pkg

```
    sudo pacman -S xdg-desktop-portal-hyprland  
```
or `xdg-desktop-portal-wlr` reboot .. try [wiki](https://wiki.archlinux.org/title/XDG_Desktop_Portal) for better understanding!

**will be posting troubleshooting & other utilities if you really love nerding out !** 

## Support Me !
[![img](wmb/logo/odysee.png)](https://odysee.com/@pegasx:d/hyprlandfirstrice:b)




