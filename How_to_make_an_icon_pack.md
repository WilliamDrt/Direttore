#  Icon Packs

The Icon Pack window:

![Alt text](/Images/Icon_Pack.png?raw=true "Icon Pack")

### Change Icon Pack

[Ctrl] + [I] to bring up the Icon Packs window. Just click on one of the available packs (if any). Clicking on "System", resets to default. DrtFMngrPreview reads available packs (files with .drt-iconpack extension) from the following folder:

```
Desktop\YOUR-USERNAME\Documents\DrtFmngPreview\IconPacks
```

`Desktop\YOUR-USERNAME\Documents\DrtFmngPreview folder is hidden. [Ctrl] + [H] brings up Folder Options window. Go to View -> Advanced Settings -> "Show hidden files, folders, or drives". Click Ok.`

### Make New Icon Pack

Make a new folder and name it with your Icon Pack name. For this example "My First Icon Pack".

Inside this folder make a new folder and name it ".mp3". Inside ".mp3" folder, save an image named "Normal.png", size should be 256x256. We just made an icon pack with only one icon. (for .mp3 files)

It should look something like this:

```
My First Icon Pack(folder)
|-> .mp3(folder)
    |->Normal.png
```

[Ctrl] + [I] to bring up the Icon Packs window. Click the 3 dots (...) button and navigate to your Icon Pack folder, for this example "My First Icon Pack". Click on "Make Icon Pack". A message box will inform you on success or not. 

If everything is ok, a new file named "My First Icon Pack.drt-iconpack" should be inside your pack folder. Move this file to Desktop\YOUR-USERNAME\Documents\DrtFmngPreview\IconPacks as explained in Change Icon Pack above. Close Icon Packs window (if still open) and open it again. You should be able to see your new icon pack on the list. 

### Expanding our simple "My First Icon Pack"

Let's go back to "My First Icon Pack\\.mp3" folder. Save another image named "CutOff.png" size should be 64x64. Cutoff image is for small icons and is optional, however important, especially if your art has great detail. You can see example of cutoff icons in system's special folders like Downloads, where the full icon is a folder with an arrow pointing down, while the cutoff icon is just the arrow.

Let's make another change. Rename ".mp3" folder to ".mp3 .mp4&nbsp; Audio" . Now the image inside this folder will be used for mp3 & mp4. Use a single space to separate multiple extensions, and a double space for comments. Packager will ignore everything after a double space (in this example the word "Audio" has two spaces in front of it).

### Packager Rules

1. Extensions should start with a dot. eg: ".mp3"
2. If no extension are found, the folder will be skipped.
3. Multiple extensions are seperated with a single space. eg: ".jpg .jpeg"
4. Packager ignores everything after a double space. eg: ".jpg .jpeg &nbsp; ignored"
5. A file named "Normal.png" must be inside the folder, or the folder will be ignored. Size 256x256
6. An optional  file named "CutOff.png" will become the small icon, for that extension. Size 64x64
7. Everything else inside the folder is ignored.
8. If the packager skips one or more folders for whatever reason, it will generate a log file along with the icon pack

### Folders & Special Folders

For folders instead of extensions we use an icon index. For example the icon index for folders is 3. All the above rules still apply, so you should name the folder ".3".

Attention: If you include an icon for folders (`".3"`), folder thumbnails will not be shown.

`You cannot assign icons for programs like OneDrive etc. You can only assign icons to extensions and icon indexes from %systemroot%\system32\imageres.dll`

Side note: If MS ever change those Indexes we'll have to follow.

### Examples:

```
.3  Folder
.123  UserFolder
.109  This PC
.25  Network
.27  Control Panel
.53  Recycle Bin
.198  3D Objects
.183  Desktop
.112  Documents
.184  Downloads
.108  Music
.113  Pictures
.189  Videos
.181  Contacts
.115  Favorites
.185  Links
.186  Saved Games
.18  Searches
.1023  Libraries
.1001  Libraries-User Made
.1002  Libraries-Documents
.1003  Libraries-Camera Roll-Pictures-Saved Pictures
.1004  Libraries-Music
.1005  Libraries-Video

```

If you have any questions or/and ideas please start a new [issue](https://github.com/WilliamDrt/DrtFMngPreview/issues).

A simple Icon Pack structure example image:

![Alt text](/Images/Icon_Pack_Example.png?raw=true "Icon Pack Example")