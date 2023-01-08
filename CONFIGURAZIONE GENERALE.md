1)CONFIGURARE I3 (prima configurazione, poi approfondire)
nano .config/i3/config
#keyboard (tastiera)
exec setxkbmap it
#wallpaper
exec-always nitrogen --restore
#gaps
gaps_inner 7
gaps_outer 7
#picom
exec picom --no-fading -openclose
#monitor principale
exec xrandr --output eDP-1 --off --output DP-1 --primary --auto & (*verificare nomi monitor con xrandr | grep oppure con xrandr --output*)

2)configurare Xfce4
click dx su preferences
**cursor shape underline** e flag su **cursor blinks** 
**scrollbar is disabled**
**background: transparent (appareance)** -> non funziona se non configuri picom
**disable display menubar in new windows**

3)wallpaper (nitrogen)
preferences add -> filesystem - us- -share - backgrounds- archlinux
select -> ok
-> zoom filled

4)picom
cp /etc/xdg/picom.conf
nano .config/picom.con

5)demenu e desktop session
paru -S j4-dmenu-desktop
nano .config/i3/config
-> sostituire **dmenu_run** con **j4-dmenu-desktop** sotto #start dmenu (a program launcher)

6)customize look and feel
lxappearance
sudo pacman -S art-gtk-theme papirus-icon-theme

7)xfce4 terminal padding
cercare su firefox
copiare codice
-> in terminale: nano .config/gtk-3.0/gtk.css
copiare e salvare file + togliere titolo da preferenze