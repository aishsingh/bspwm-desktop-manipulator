bspwm desktop manipulator
=========================

Some scripts I created while using bspwm, to help me manipulate the desktops on the fly. Took a while to function the way I wanted so I decided to share it.

What does it do?
---------------
Lets you Add, remove, rename and rearrange desktops with a press of a button

Requirments
-----------
* **dmenu2-underline** from archlinux aur- alternativly the default dmenu can be used by editing the scripts and removing the non-standard options
* Any panelling application such as **bar-aint-recursive** (see my dotfiles repo for my config)

Usage
------------
1. `git clone https://github.com/aishsingh/bspwm-desktop-manipulator.git` in to a directory
2. Edit sxhkdrc `vim ~/.config/sxhkd/sxhkdrc`

for example add the following keybindings *(replace `<path-to-scripts>` with your actual path)*
```
super + r
	<path-to-scripts>/renamedesk
super + backslash
	<path-to-scripts>/adddesk
super + shift + backslash
	<path-to-scripts>/adddesk tmp
super + shift + bracket{left,right}
    bspc desktop -s {prev,next}
```
Lastly, Restart sxhkd to use the new bindings by restarting X

NOTE: These scripts have been made for bspwm but could be modified for other window managers
