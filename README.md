# Fix some 42 computer "issues"
Fixing 42 skill issues (some apps).
- [Display Scale](##display-scale-100%-locked)
- [Dock bar](##dock-bar)
- [Installing Obsidian](##installing-obsidian)
- [VSCode with ZSH terminal](##visual-studio-code-with-zsh-terminal)

### <br>
## Display scale 100% locked
If you are in the cluster 2 and your Scale is locked in 100%, use:

```bash
gsettings set org.gnome.desktop.interface text-scaling-factor 0.85
```
You can change the 0.85 to any other scale.

### <br>
## Dock Bar
If you don't see a dockbar (taskbar) like in windows and you want it, you can search for EXTENTIONS app and enable the UBUNTU DOCK on it.
You can customize it on the settings > apperance in the DOCK session.
Feel free to explore the others extensions and customize your desktop environment.

If you want put the Show aplications button on the extreme left side of the dock, use this command on terminal:

 ```bash
gsettings set org.gnome.shell.extensions.dash-to-dock show-apps-at-top true
```

Your desktop can look like this:
![image](https://github.com/user-attachments/assets/961f0efb-6051-4c62-b9ca-41cddafc2c7b)

### <br>
## Installing Obsidian
If you want to use Obsidian on the 42 computers, you can use it by Appimage.
- Download the [Appimage](https://obsidian.md/download).
- Put it in some good directory (I suggest create the "app" folder on home and insert it there).
- Create a folder (Obsidian) and put the Appimage and the icon there.
- Open the terminal in this directory and execute:
```bash
chmod u+x Obsidian-<Version>.AppImage
```
Change the "&lt;Version&gt;" to your actual version (is like the file's name). Now you can run it.

- In the terminal use this command:
```bash
  nano ~/.local/share/applications/obsidian.desktop
```
- Put this on the nano file:
```
[Desktop Entry]
Name=Obsidian
Exec=/home/bportell/app/Obsidian/Obsidian-1.7.4.AppImage
Icon=/home/bportell/app/Obsidian/obsidian-icon.png
Type=Application
Categories=Utility;
Terminal=false
```
- Save the file (ctrl+o) and close it (ctrl+x)
- Execute this command in terminal:
```bash
chmod +x ~/.local/share/applications/obsidian.desktop
```
- Execute this command in terminal:
```bash
update-desktop-database ~/.local/share/applications
```
Now you can use Obsidian on 42 computer.

You can also do it for any other Appimage.

![image](https://github.com/user-attachments/assets/99bf60f2-d557-4433-977b-7da6c919329c)


### <br>
## Visual Studio Code with ZSH terminal
![image](https://github.com/user-attachments/assets/ec5ddb50-f492-42c3-802f-e494c16cf09a)

In the case you want to se a ZSH terminal on vscode, by default vscode on 42 computers, you won't be able to. But you can solve it following this steps:
- Download the version .tar.gz x64 on https://code.visualstudio.com/download
- Now you have to extract this files. I suggest to you create a folder on home directory, like "app" or something like that
- Put the VSCode-linux-x64 folder inside the app folder
- Download this [image](https://github.com/user-attachments/assets/ff30166c-2ae6-463b-ae28-1b04e7bf5160) and put inside the VSCode-linux-x64 folder

- Now on your terminal run this command:
```bash
  nano ~/.local/share/applications/vscode.desktop
```
- In the nano file, insert this:
```
[Desktop Entry]
Name=VSCode (bportell)
Comment=Code Editing. Redefined.
Exec=/home/USERNAME/app/VSCode-linux-x64/code
Icon=/home/USERNAME/app/VSCode-linux-x64/vscode.png
Type=Application
Terminal=false
Categories=Utility;TextEditor;Development;IDE;

```
OBS. change the Exec and Icon path to your actual path to /VSCode-linux-64/code
- Save your file (ctrl+o) and close it (ctrl+x)
- Now run this command on terminal:
```bash
  update-desktop-database ~/.local/share/applications/
```
