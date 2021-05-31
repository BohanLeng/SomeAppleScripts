# SomeAppleScripts
Some Applescripts that meet Lamberhand's needs.



## *Contents*

1. [Script: Open Terminal then Change Directory](#dir)
2. [Script: Print to PDF with Safari](#print)
3. [Script: Play Album with NeteaseMusic](#album)
4. [Script: Play Song with NeteaseMusic](#song)
5. [Configuration Guide](#config)







## <span id="dir">Script: Open Terminal then Change Directory</span>

Git operation on Mac relies on command line tool. It frustates me when manually typing in `$ cd /.../.../...` after opening Terminal.

This scripts opens **Terminal** and automatically change directory to current folder and execute `$ ls`for you to check items in current folder. Now you are free to operate with Git or whatever you want in this directory.

If current application is other than **Finder**, this script will only open Terminal for you. 



## Script: Print to PDF with Safari

When I search for research papers, it is very possible that direct PDF download link is not provided by databases (eg. SpringerLink, ScienceDirect, etc.). Clicking "Download PDF" buttons will lead you to a webpage showing this PDF. To save it requires more additional steps:

- ~~Press **⌘+P** to open print settings~~
- ~~Change button "PDF" to "**Save as PDF**"~~
- ~~Go back and copy the title of article~~
- ~~Paste to the name~~
- ~~Click save~~

This script will help you tremendously shorten this procedure by nearly **5 seconds** when you find yourself trapped in this situation. It does all the job for you, including reading your clipboard and paste to text field when saving. Here is what you need to do now:

- Copy the title of article
- Run this script
- Confirm and save



## <span id="album">Script: Play Album with NeteaseMusic</span>

I listen to music with NeteaseMusic in most cases. When I listen to music, I listen by album in most cases. I have *The Dark Side of the Moon*, *Slowdive*, *Treasure*, *Unknown Pleasures*, etc. in my Favorites of albums in NeteaseMusic. Opening application and click and wait multiple times costs time, energy and mood. All I want is typing in *souvl* and *Souvlaki* is played subsequently.

This script opens NeteaseMusic and prompt dialog for input. Keyword accepted will be used to search in *我的收藏* page. If item exists, soon it will be played from the beginning. 

So make sure you have albums you want in your *我的收藏* folder. If not, this scripts will let you know. If there are multiple search results, this scripts will let you decide. If you don't type anything in, this scripts will open your *我的收藏* page and let you browse.

It generally takes approx. 5 to 20 seconds to start playing depending on network responsiveness. Since NeteaseMusic doesn't expose interfaces to AppleScript, it is potential that this script fails to bring you to your music. Just run it again if this is the case.



## <span id="song">Script: Play Song with NeteaseMusic</span>

As stated in [previous section](#album), this script, similarly, serves the purpose of searching a song, not album, in Favorites.

> Still in construction



## <span id="config">Configuration Guide</span>

### <span id ="configA">**A. Run by Keyboard Shortcut**</span>

1. Clone this repository or download .zip containing srcipts. 

2. **⌘+Space** to open Spotlight search. Input **Automator** to open **Automator**. Choose **Quick Action/服务**, creating new document.

3. Search **AppleScript** in search bar on the top left. Drag and drop **Run AppleScript/运行AppleScript** into workflow column on the right side.

4. Copy script and paste, overriding `(* Your script goes here *)` in **Run AppleScript/运行AppleScript** window. *i.e.* `on run {input, parameters}`, `return input` and `end run` should be reserved. 

   The whole script should be like this:

   ~~~objective-c
   on run {input, parameters}
   	
   	...(Thingy copied)
   	...(Thingy copied)
   	...(Thingy copied)
   	
   	return input
   end run
   ~~~

5. **⌘+S** to save this quick action/服务. Specify a proper name.

6. Click **** on the top left corner to open **System Preferences.../系统偏好设置** . Choose **Keyboard/键盘 &rArr; Shortcuts/快捷键设置&rArr; Services/服务**. Scroll to bottom and find your entitled service. Set a proper shotcuts as you like.

7. Good to go. Press the keyboard shotcut which you chose and enjoy. Initial launch in any new app will cause a window asking for access. Choose **OK** freely. 

> My personal shotcut assigning share:
>
> | Script                              | Shotcut |
> | ----------------------------------- | ------- |
> | Open Terminal then Change Directory | ⌥⌘+`    |
> | Play Album with NeteaseMusic        | ⌃⌥⌘+M   |
>
> ⌃ - control	⌥ - option / alt	⌘ - command	⇧ - shift



**B. Run by Spotlight Search**

1. Clone this repository or download .zip containing srcipts.
2. Click and open the script you want by **Script Editor/脚本编辑器** (by default). 
3. Click **File/文件 &rArr; Export/导出** on the menu bar. Choose **File Format** to **Application**. Specify a name and folder to export.
4. Good to go. **⌘+Space** to open Spotlight search and search the application which you entitled. Initial launch in any new app will cause a window asking for access. Choose **OK** freely. 



**C. Thirdparty Application - Keyboard Maestro**

Keyboard Maestro provides more convienent approach to binding keyboard chortcuts to script than automator does. Since it is a paid application and its configuration is similar to that of [**A**](#configA), we don't dive into Keyboard Maestro any longer for now.



 

***Developed by Lamberhand@SJTU***
