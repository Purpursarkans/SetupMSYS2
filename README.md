# SetupMSYS2

## MSYS2
Download  
> https://www.msys2.org/
###### Install msys2 only on default directory

## Windows Terminal
Download
> https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701  
> https://github.com/microsoft/terminal  
> https://github.com/microsoft/terminal/releases  

## Setup MSYS2 into Windows Terminal
* New profile > New empty profile  
* Name - **MINGW64**
* Command line - **C:/msys64/msys2_shell.cmd -defterm -here -no-start -mingw64**
* Starting directory - **C:/msys64/home/%USERNAME%**
* Icon - **C:/msys64/mingw64.ico**  
![template](https://raw.githubusercontent.com/Purpursarkans/SetupMSYS2/main/wt.png)

## After Setup

* $ pacman -Syu 
* $ pacman -Syu mingw-w64-x86_64-toolchain cmake mingw-w64-x86_64-cmake  
if you see this error and are sure pacman is not open - **error: failed to synchronize all databases (failed to lock the database )**  
check pacman in task manager and kill him, then delete - **"C:\msys64\var\lib\pacman\db.lck"**   
**BUT**, dont delete this file if pacman is open
