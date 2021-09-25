# Configuring "VS Code + GCC + JLink" to work with STM32 for Windows 10
>
Visual Studio Code is a lightweight, feature-rich code and text editor that is extensible with plugins. In conjunction with the open source GCC and the Cortex-Debug plugin, the editor turns into a powerful firmware development tool for almost any microcontroller. The method described below allows you to work with any microcontrollers based on the ARM Cortex-M core and many others.

![Heading](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/1.PNG)

## Step #1
[You need to download and install the actual Visual Studio Code editor itself](https://code.visualstudio.com/)
>
![Installation VSC](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/2.PNG)

## Step #2
Now you need to install two plugins to extend the capabilities of VS Code:

* **C/C++**
*  **Cortex-Debug**

To install, go to the * Extensions * section or the combination * Ctrl + Shift + X *, then enter the names of the plugins in the search bar, some of the most popular and will be at the beginning of the list. Click on the plugin and install it. The sequence of the installation is not important. These 2 plugins are the minimum required set, you can also install other extensions for verification and this will not affect the performance in any way.
>
![Installing plugins](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/3.PNG)

## Step #3
[Install JLink Drivers and Utilities](https://www.segger.com/downloads/jlink/#J-LinkSoftwareAndDocumentationPack)

It is best to install Segger drivers in the root folder, the path to the files must be without Cyrillic characters, it is also desirable to use folder names without using spaces.

For work, the JLink v9.x debugger is used, however, it is allowed to work with other development tools, for example, with proprietary ST-Link and other solutions from manufacturers. It is recommended to use JLink because it supports a large number of microcontrollers, all solutions on ARM Cortex-M, and at the same time is not tied to the IDE and tools of specific developers.
>
![Installing JLink](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/4.PNG)

## Шаг №4
[Install toolchain GNU Arm Embedded GCC v10.x](https://github.com/xpack-dev-tools/arm-none-eabi-gcc-xpack/releases)

At the time of reading, the version of the toolchain may be more recent, then we install it. Installation is best done also in the root folder, the use of the Cyrillic alphabet in the path to the file is not allowed, and it is also advisable to avoid a space in the folder names.
>
![Installing the toolchain](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/5.PNG)

## Step #5
[Install Windows Build Tools](https://github.com/xpack-dev-tools/windows-build-tools-xpack/releases)

Install the latest version also in the root folder without Cyrillic names and ideally without spaces.
>
![Installation Windows Build Tools](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/6.PNG)

## Step #6
Checking! After going through all the previous steps, you should have the * VS Code * editor installed on your computer, as well as the development tools from steps 3-5. Approximate project structure:

* _Drive C_
    * _devs_ 
        * _jlink_
        * _toolchain_
        * _windows-build-tools_

Accordingly, the paths to these folders look like this:

* _C:\devs\jlink_
* _C:\devs\toolchain_
* _C:\devs\windows-build-tools_

>
![Installed files](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/7.PNG)

Your paths and folder structure may be different from mine! It is only important that the path to the files is not in Cyrillic and, ideally, there are no problems, as well as the paths themselves are short. If the paths are different, then when setting up you just use them and that's it.

## Step #7
After installing all the tools, you need to register the paths to the necessary folders in the environment variables. To do this, right-click on the icon * My computer * and select * Properties *. Next, click on * Additional system parameters * and the * System Properties * window will open, where there will be a menu * Environment Variables ... *, click and see the list of variables. Click on the * Path * variable and now you need to register the paths to the following folders:
>
![Folder paths](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/8.PNG)

The path for VS Code is registered automatically when installing the editor, but the paths for up to 3 folders must be written independently. Please note that here you must register your real paths, which may differ from mine.

**The configuration is complete, now it is advisable to reboot the system - you can start building the project!**
