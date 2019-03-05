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

## 可以自行定制
可以定制以下文件【说明列表】:

| 文件                   | 说明                        |
| ---------------------- | --------------------------- |
| colors.txt             | 所有颜色可调             
| archive_icon.png       | 档案图标                 
| audio_icon.png         | 音频图标                 
| battery.png            | 电池边框图标             
| battery_bar_charge.png | 电池充电状态图标          
| battery_bar_green.png  | 电池绿色时的状态图标       
| battery_bar_red.png    | 电池红色时的状态图标           
| bg_audioplayer.png     | 音频播放器背景                
| bg_browser.png         | 文件浏览器背景                
| bg_hexeditor.png       | 十六进制编辑器的背景          
| bg_photoviewer.png     | 照片查看器的背景             
| bg_texteditor.png      | 文本编辑器的背景  
| context.png            | 上下文菜单图像（可以是任意大小。建议：如果您在图像中添加alpha频道，效果会很好）
| context_more.png       | 上下文菜单更多图像（可以是任意大小。建议：如果您在图像中添加alpha频道，效果会很好）
| cover.png              | 默认唱片集封面         
| dialog.png             | 对话框菜单图像（可以是任意大小。此图像文件将由vitalshell拉伸以适合对话框。建议不要使用，因为它看起来不好，比例不对）
| fastforward.png        | 快进图标            
| fastrewind.png         | 快退图标             
| file_icon.png          | 文件图标                   
| folder_icon.png        | 文件夹图标                 
| ftp.png                | FTP服务图标                    
| image_icon.png         | 图像图标                  
| pause.png              | 暂停图标                  
| play.png               | 开始图标                   
| settings.png           | 设置图标               
| sfo_icon.png           | SFO图标                    
| text_icon.png          | 文本图标                   
| wallpaper.png          | 墙纸                   

**主题设置:** vitashell将加载在“ux0:vitashell/theme/theme.txt”中设置的主题（theme\u name=“your\u theme\u name”`）

**通用信息:** 不需要在自定义主题中包含所有这些文件，如果其中一个丢失，则将加载默认图像文件。.

**对话框和上下文图像：**如果这些文件不可用，则将使用colors.txt文件中的“dialog-bg-color”和“context-menu-color”两种颜色.

## 多国语言
将需要的语言文件放在“ux0:vitalshell/language/x.txt”处，该文件必须是utf-8编码的，并且“x”是下面列出的语言之一:

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

vitalshell会自动加载与当前系统语言匹配的语言。
例如你的系统语言是法语，它将从'ux0:vitashell/language/french.txt加载`.

语言文件在此存储库的“l10n”文件夹中可用.

## 构建
安装[vitasdk]（https://github.com/vitasdk）并使用:

```
mkdir build && cd build && cmake .. && make
```

## Credits
* Team Molecule for HENkaku
* xerpi for ftpvitalib and vita2dlib
* wololo for the Revitalize contest
* sakya for Lightmp3
* Everybody who contributed on vitasdk
