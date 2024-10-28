# Fix some 42 computer "issues"
Fixing 42 skill issues (some apps).
- [Display Scale](##Display-scale-100%-locked)
- [Dock bar](##Dock-bar)
- [VSCode with ZSH terminal](##Visual-Studio-Code-with-ZSH-terminal)

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

Your desktop can look like this:
![image](https://github.com/user-attachments/assets/961f0efb-6051-4c62-b9ca-41cddafc2c7b)

### <br>
## Visual Studio Code with ZSH terminal
![image](https://github.com/user-attachments/assets/ec5ddb50-f492-42c3-802f-e494c16cf09a)

In the case you want to se a ZSH terminal on vscode, by default vscode on 42 computers, you won't be able to. But you can solve it following this steps:
- Download the version .tar.gz x64 on https://code.visualstudio.com/download
- Now you have to extract this files. I suggest to you create a folder on home directory, like "app" or something like that
- Put the VSCode-linux-x64 folder inside the app folder
- Donwload this [image](https://github.com/user-attachments/assets/ff30166c-2ae6-463b-ae28-1b04e7bf5160) and put inside the VSCode-linux-x64 folder

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
