# VitaShell

Vitashell为PS Vita提供了一个文件管理器，这其中包含了安装程序、内置ftp等等功能。。

## Changelog
See [CHANGELOG.md](CHANGELOG.md)

## 如何将USB闪存驱动器当作PS TV上的存储卡使用？
- 将USB闪存驱动器格式化为exfat或fat32.
- 启动Vitashell并在主页部分按▲.
- 选择mount uma0:并连接USB闪存驱动器。然后把文件复制到U盘上.
- 一旦uma0:挂载到分区下，再次按▲并选择mount usb ux0:。这将会复制几个重要的应用程序，如vitalshell、molecularshell和其他文件.
- USB闪存驱动器现在已经被识别为内置存储卡.
- 要同步USB闪存驱动器上的所有应用程序，请按▲并选择刷新LiveArea。当然喽，这不会刷新PSP游戏.仅仅是PSV游戏生效
- 如果要恢复补丁，请按▲并选择umount usb ux0:.
- 请注意，修补程序只是临时的，并不能固化，每次启动PS TV时都需要重新执行此过程.

## Customization
You can customize those files:

| File                   | Note                        |
| ---------------------- | --------------------------- |
| colors.txt             | All colors adjustable       |
| archive_icon.png       | Archive icon                |
| audio_icon.png         | Audio icon                  |
| battery.png            | Battery border icon         |
| battery_bar_charge.png | Charging battery bar        |
| battery_bar_green.png  | Green battery bar           |
| battery_bar_red.png    | Red battery bar             |
| bg_audioplayer.png     | Background for audio player |
| bg_browser.png         | Background for file browser |
| bg_hexeditor.png       | Background for hex editor   |
| bg_photoviewer.png     | Background for photo viewer |
| bg_texteditor.png      | Background for text editor  |
| context.png            | Context menu image (Can be any size. Suggestion: It will look great if you add alpha channel to your image)  |
| context_more.png       | Context menu more image (Can be any size. Suggestion: It will look great if you add alpha channel to your image)  |
| cover.png              | Default album cover         |
| dialog.png             | Dialog menu image (Can be any size. This image file will be stretched by VitaShell to fit the dialog box. Suggestion: Don't use motives, as it will not look good with wrong proportion)  |
| fastforward.png        | Fastforward icon            |
| fastrewind.png         | Fastrewind icon             |
| file_icon.png          | File icon                   |
| folder_icon.png        | Folder icon                 |
| ftp.png                | FTP icon                    |
| image_icon.png         | Image icon                  |
| pause.png              | Pause icon                  |
| play.png               | Play icon                   |
| settings.png           | Settings icon               |
| sfo_icon.png           | SFO icon                    |
| text_icon.png          | Text icon                   |
| wallpaper.png          | Wallpaper                   |

**Theme setting:** VitaShell will load the theme that is set in `ux0:VitaShell/theme/theme.txt` (`THEME_NAME = "YOUR_THEME_NAME"`)

**General info:** You don't need to have all these files in your custom theme, if one of them is missing, the default image file will be loaded instead.

**Dialog and context image:** If these files are not available, the colors `DIALOG_BG_COLOR` and `CONTEXT_MENU_COLOR` from `colors.txt` will be used instead.

## Multi-language
Put your language file at `ux0:VitaShell/language/x.txt`, where the file must be UTF-8 encoded and `x` is one of the language listed below:

- japanese
- english_us
- french
- spanish
- german
- italian
- dutch
- portuguese
- russian
- korean
- chinese_t
- chinese_s
- finnish
- swedish
- danish
- norwegian
- polish
- portuguese_br
- turkish

VitaShell does automatically load the language that matches to the current system language.
If your system language is for example french, it will load from `ux0:VitaShell/language/french.txt`.

Languages files are available in the `l10n` folder of this repository.

## Building
Install [vitasdk](https://github.com/vitasdk) and build VitaShell using:

```
mkdir build && cd build && cmake .. && make
```

## Credits
* Team Molecule for HENkaku
* xerpi for ftpvitalib and vita2dlib
* wololo for the Revitalize contest
* sakya for Lightmp3
* Everybody who contributed on vitasdk
