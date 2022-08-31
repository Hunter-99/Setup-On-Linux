# Extensions

## Prerequirements
1. Install Extension Manager:
```shell
sudo apt intall gnome-shell-extension-manager
```
2. Install Gnome Tweaks:
```shell
sudo add-apt-repository universe
sudo apt install gnome-tweaks
```
## Extension list
1. `Clear Top Bar`
2. `Dash to Dock Animator`
3. `Impatience`
4. `OpenWeather`
5. `Vitals`

### Change dock bar opacity
 ```shell
gsettings set org.gnome.shell.extensions.dash-to-dock transparency-mode 'FIXED'
gsettings set org.gnome.shell.extensions.dash-to-dock background-opacity 0.2
```