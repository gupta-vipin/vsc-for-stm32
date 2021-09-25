# Building a project from source files in VS Code

During development, it is very often necessary to build a project from source files. You can build it in different ways, the instructions describe the case when the project is built using _Makefile_, as the most popular option. As an example, an open project MPPT charge controller is used, but the assembly process is relevant for other projects as well.

## Step # 1
You need to get the source files from GitHub in two ways:

* __Download ZIP archive with the project__

>
![Installing VSC](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/9.PNG)

* __Clone the repository to your computer__

To do this, open any terminal and execute the command:
```
git clone https://github.com/RedCommissary/mppt-2420
```
>
![Installation VSC](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/10.PNG)
>
After that, all sources of the project will be downloaded. 

## Step #2

There are many options for organizing repositories, in this case, one repository contains both the "hardware" project and the firmware sources. To build, you only need the _firmware / source_ folder. We open it in the VS Code editor and see the following picture:
>
![Installation VSC](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/11.PNG)

The project has opened and we see its structure. The key settings of the development environment are located in the _.vscode_ folder, since the project build rules themselves are described in _Makefile_ and are not required to be edited, they remain unchanged. It is only necessary to register the paths to the used _ARM GCC Toolchain_. We register our paths in these 4 lines:
>
![Installation VSC](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/12.PNG)

## Step #3
This completes the settings and you can build the project by running the build script _Terminal -> Run Task -> Make Build_ and after the build is complete, we will get the following result:
>
![Installtion VSC](https://github.com/gupta-vipin/vsc-for-stm32/blob/master/docs/pic/13.PNG)

## Additionally
To train and consolidate your knowledge, you can collect several projects from the collection of templates for STM32, which [available on github](https://github.com/gupta-vipin/examples-cortex-mcu).
