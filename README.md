 ![img](assets/wmb/ramen.gif)
                                                
  88bd88b d888b8b     88bd8b,d88b  d8888b  88bd88b 
  88P'  `d8P' ?88     88P'`?8P'?8bd8b_,dP  88P' ?8b
 d88     88b  ,88b    d88  d88  88P88b     d88   88P
d88'     `?88P'`88b   d88' d88'  88b`?888P'd88'   88b
                                                  
An elegant hyprland config coming with less bloat, smooth workflow and aesthetic black theme 

- minimal setup with Archlinux
- I just usually forget things so if you are new to Window managers this space will save you !
- vimrc without bloated plugins.


<br>

___
<div align="">

Install
===========

 
<br>
    

</div>

___


<br>

<br>

## Essential packages :

```
hyprland hyprpaper vim wayland-protocols waybar-hyprland brightnessctl make wlroots pipewire pipewire-alsa pipewire-pulse pipewire-jack wireplumber xdg-desktop-portal-wlr grim slurp sddm 

```
<br>

## Additional packages :
```
      alacritty thunar pavucontrol bluez lxappearance mpv mako neofetch btop swaybg swayidle swww 
```

<br>


## Basic keybindings

> **Note** This project may vary over-time.

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
```
systemctl --user stop pulseaudio.socket
systemctl --user stop pulseaudio.service
systemctl --user disable pulseaudio.socket
systemctl --user disable pulseaudio.service

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

>screen sharing issue `OBS`

```
    sudo pacman -S xdg-desktop-portal-hyprland 
     
```



